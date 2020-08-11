################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Middlewares/Third_Party/FreeRTOS/Source/portable/MemMang/subdir.mk
-include Middlewares/Third_Party/FreeRTOS/Source/portable/GCC/ARM_CM4F/subdir.mk
-include Middlewares/Third_Party/FreeRTOS/Source/CMSIS_RTOS_V2/subdir.mk
-include Middlewares/Third_Party/FreeRTOS/Source/subdir.mk
-include Drivers/STM32F4xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
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
wireless_cnt_Bot.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
wireless_cnt_Bot.list \

OBJCOPY_BIN += \
wireless_cnt_Bot.bin \


# All Target
all: wireless_cnt_Bot.elf secondary-outputs

# Tool invocations
wireless_cnt_Bot.elf: $(OBJS) $(USER_OBJS) /home/rishap/STM32CubeIDE/MCU_Programming/wireless_cnt_Bot/STM32F407VGTX_FLASH.ld
	arm-none-eabi-gcc -o "wireless_cnt_Bot.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m4 -T"/home/rishap/STM32CubeIDE/MCU_Programming/wireless_cnt_Bot/STM32F407VGTX_FLASH.ld" --specs=nosys.specs -Wl,-Map="wireless_cnt_Bot.map" -Wl,--gc-sections -static --specs=nano.specs -mfpu=fpv4-sp-d16 -mfloat-abi=hard -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

wireless_cnt_Bot.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "wireless_cnt_Bot.list"
	@echo 'Finished building: $@'
	@echo ' '

wireless_cnt_Bot.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "wireless_cnt_Bot.bin"
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
