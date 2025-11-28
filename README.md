# ATmega128 Embedded System Practice

## Overview
- 과목: 마이크로프로세서 실험 1 
- 목표: ATmega128의 GPIO, Interrupt, Timer, ADC 등 주변 장치(Peripheral) 제어 기초 습득
- 환경: Microchip Studio (C Language)
- 하드웨어:학교 실습용 ATmega128 개발 보드 (PCB Type)
- 구성: 7-Segment, 4x4 Keypad, VR, LED Array

## Curriculum
임베디드 시스템의 기초가 되는 입출력 제어부터 인터럽트 처리까지 단계적으로 기능을 구현

### GPIO & 디스플레이 기초
- LED 제어: 포트(PORT) 입출력 설정을 통한 비트 제어 (Bit masking)
- 7-Segment: 0~9 숫자 폰트 배열 구현 및 다이내믹 구동 방식 이해

### Keypad
- 매트릭스 스캔: 4x4 키패드의 행(Row)/열(Col) 스캔 원리 구현
- 입력 처리: 폴링(Polling) 방식으로 키 입력 감지 및 7-Segment 디스플레이 연동

### ADC & 센서 기초 
- 가변저항 값 측정: ADC 레지스터 설정 (Prescaler, Reference Voltage)
- 데이터 변환: 0~1023의 아날로그 값을 0~99 범위로 매핑하여 디스플레이 표시

### Timer/Counter
- 정밀 시간 제어: _delay_ms() 방식의 한계를 극복하기 위해 Timer/Counter 사용
- ISR: 오버플로우 인터럽트를 활용한 비동기 LED 토글 및 시계 구현

### 종합 설계 
- 기능:키패드로 동작 모드를 선택하고, 가변저항 값에 따라 LED 점멸 속도와 7-Segment 패턴이 실시간으로 변하는 통합 시스템 구현
- 의의: 폴링 방식과 인터럽트 방식을 혼용하여 멀티태스킹 구조의 기초를 다짐

## Relation to Micromouse
이 프로젝트는 이후 진행한 [자율 주행 마이크로마우스 프로젝트]의 선수 과정입니다.

