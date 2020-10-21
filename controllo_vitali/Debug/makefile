################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32G0xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(S_DEPS)),)
-include $(S_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
controllo_vitali.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
controllo_vitali.list \

OBJCOPY_BIN += \
controllo_vitali.bin \


# All Target
all: controllo_vitali.elf secondary-outputs

# Tool invocations
controllo_vitali.elf: $(OBJS) $(USER_OBJS) C:\Users\39389\Desktop\Progetto_UART_repo\controllo_vitali\STM32G070RBTX_FLASH.ld
	arm-none-eabi-gcc -o "controllo_vitali.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m0plus -T"C:\Users\39389\Desktop\Progetto_UART_repo\controllo_vitali\STM32G070RBTX_FLASH.ld" --specs=nosys.specs -Wl,-Map="controllo_vitali.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

controllo_vitali.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "controllo_vitali.list"
	@echo 'Finished building: $@'
	@echo ' '

controllo_vitali.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "controllo_vitali.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
