################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Startup/subdir.mk
-include Src/subdir.mk
-include Middlewares/Protocol/GENE_I2C/subdir.mk
-include Middlewares/Protocol/DMX/subdir.mk
-include Drivers/System/subdir.mk
-include Drivers/STM32F1xx_HAL_Driver/Src/subdir.mk
-include Drivers/Devices/PWM/subdir.mk
-include Drivers/Devices/Display/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
DMX_Decoupe.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
DMX_Decoupe.list \

OBJCOPY_BIN += \
DMX_Decoupe.bin \


# All Target
all: DMX_Decoupe.elf secondary-outputs

# Tool invocations
DMX_Decoupe.elf: $(OBJS) $(USER_OBJS) Z:\TECHNIQUE\Projets\Decoupe_Theatre\Firmware\DMX_Decoupe\STM32F103C8TX_FLASH.ld
	arm-none-eabi-gcc -o "DMX_Decoupe.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"Z:\TECHNIQUE\Projets\Decoupe_Theatre\Firmware\DMX_Decoupe\STM32F103C8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="DMX_Decoupe.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

DMX_Decoupe.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "DMX_Decoupe.list"
	@echo 'Finished building: $@'
	@echo ' '

DMX_Decoupe.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "DMX_Decoupe.bin"
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
