---
description: La categoría de hardware sistema del equipo agrupa clases que representan objetos relacionados con el hardware. Entre los ejemplos se incluyen dispositivos de entrada, discos duros, tarjetas de expansión, dispositivos de vídeo, dispositivos de red y energía del sistema.
ms.assetid: 0b6cb410-166e-45cd-8dca-77a111b3cf62
ms.tgt_platform: multiple
title: Clases de hardware de sistema del equipo
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a3681f78d882a3e977b9721bd70f0b852114c257
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000612"
---
# <a name="computer-system-hardware-classes"></a>Clases de hardware de sistema del equipo

La categoría de hardware sistema del equipo agrupa clases que representan objetos relacionados con el hardware. Entre los ejemplos se incluyen dispositivos de entrada, discos duros, tarjetas de expansión, dispositivos de vídeo, dispositivos de red y energía del sistema.

-   [Clases de dispositivos de enfriamiento](#cooling-device-classes)
-   [Clases de dispositivos de entrada](#input-device-classes)
-   [Clases de almacenamiento masivo](#mass-storage-classes)
-   [Clases de placa base, controlador y Puerto](#motherboard-controller-and-port-classes)
-   [Clases de dispositivos de red](#networking-device-classes)
-   [Clases de energía](#power-classes)
-   [Clases de impresión](#printing-classes)
-   [Clases de telefonía](#telephony-classes)
-   [Clases de vídeo y de monitor](#video-and-monitor-classes)
-   [Temas relacionados](#related-topics)

## <a name="cooling-device-classes"></a>Clases de dispositivos de enfriamiento

La subcategoría dispositivos de refrigeración agrupa las clases que representan ventiladores instrumentales, sondas de temperatura y dispositivos de refrigeración.



| Clase                                                     | Descripción                                                                 |
|-----------------------------------------------------------|-----------------------------------------------------------------------------|
| [**Ventilador de Win32 \_**](win32-fan.md)                           | Representa las propiedades de un dispositivo de ventilador en el sistema del equipo.           |
| [**Win32 \_ HeatPipe**](win32-heatpipe.md)                 | Representa las propiedades de un dispositivo de refrigeración de canalización térmica.                    |
| [**\_Refrigeración Win32**](win32-refrigeration.md)       | Representa las propiedades de un dispositivo de refrigeración.                        |
| [**Win32 \_ TemperatureProbe**](win32-temperatureprobe.md) | Representa las propiedades de un sensor de temperatura (termómetro electrónico). |



 

## <a name="input-device-classes"></a>Clases de dispositivos de entrada

La subcategoría dispositivos de entrada agrupa las clases que representan teclados y dispositivos señaladores.



| Clase                                                 | Descripción                                                                                                         |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**\_Teclado Win32**](win32-keyboard.md)             | Representa un teclado instalado en un equipo con Windows.                                               |
| [**Win32 \_ PointingDevice**](win32-pointingdevice.md) | Representa un dispositivo de entrada que se usa para señalar y seleccionar regiones en la pantalla de un equipo que ejecuta Windows. |



 

## <a name="mass-storage-classes"></a>Clases de almacenamiento masivo

Las clases de la subcategoría almacenamiento masivo representan dispositivos de almacenamiento, como unidades de disco duro, unidades de CD-ROM y unidades de cinta.



| Clase                                                     | Descripción                                                                                  |
|-----------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**Win32 \_ AutochkSetting**](win32-autochksetting.md)     | Representa la configuración para la operación de comprobación de un disco.                               |
| [**Win32 \_ CDROMDrive**](win32-cdromdrive.md)             | Representa una unidad de CD-ROM en un equipo con Windows.                              |
| [**Win32 \_ DiskDrive**](win32-diskdrive.md)               | Representa una unidad de disco física tal como la muestra un equipo que ejecuta el sistema operativo Windows. |
| [**Win32 \_ FloppyDrive**](win32-floppydrive.md)           | Administra las capacidades de una unidad de disquete.                                             |
| [**Win32 \_ PhysicalMedia**](/previous-versions/windows/desktop/cimwin32a/win32-physicalmedia) | Representa cualquier tipo de documentación o medio de almacenamiento.                                      |
| [**Win32 \_ TapeDrive**](win32-tapedrive.md)               | Representa una unidad de cinta en un equipo con Windows.                                |



 

## <a name="motherboard-controller-and-port-classes"></a>Clases de placa base, controlador y Puerto

La subcategoría de la placa base, los controladores y los puertos agrupa las clases que representan dispositivos del sistema. Algunos ejemplos son la memoria del sistema, la memoria caché y los controladores.



| Clase                                                                       | Descripción                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ 1394Controller**](win32-1394controller.md)                       | Representa las capacidades y la administración de un controlador 1394.<br/>                                                                                                                                               |
| [**Win32 \_ 1394ControllerDevice**](win32-1394controllerdevice.md)           | Relaciona el controlador de bus serie de alta velocidad (IEEE 1394 FireWire) y la instancia de la instancia de [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) conectada a él.<br/>                                                            |
| [**Win32 \_ AllocatedResource**](win32-allocatedresource.md)                 | Relaciona un dispositivo lógico con un recurso del sistema.<br/>                                                                                                                                                                 |
| [**Win32 \_ AssociatedProcessorMemory**](win32-associatedprocessormemory.md) | Relaciona un procesador y su memoria caché.<br/>                                                                                                                                                                      |
| [**\_Placa base Win32**](win32-baseboard.md)                                 | Representa una placa base (también conocida como placa de sistema o placa base).<br/>                                                                                                                                          |
| [**\_BIOS Win32**](win32-bios.md)                                           | Representa los atributos de los servicios básicos de entrada y salida (BIOS) del sistema del equipo que están instalados en el equipo.<br/>                                                                                   |
| [**\_Bus Win32**](win32-bus.md)                                             | Representa un bus físico tal como lo muestra un sistema operativo Windows.<br/>                                                                                                                                               |
| [**Win32 \_ CacheMemory**](win32-cachememory.md)                             | Representa la memoria caché (interna y externa) de un equipo.<br/>                                                                                                                                          |
| [**Win32 \_ ControllerHasHub**](/previous-versions/windows/desktop/cimwin32a/win32-controllerhashub)             | Representa los concentradores de nivel inferior del controlador de bus serie universal (USB).<br/>                                                                                                                                 |
| [**Win32 \_ DeviceBus**](win32-devicebus.md)                                 | Relaciona un bus del sistema y un dispositivo lógico mediante el bus.<br/>                                                                                                                                                       |
| [**Win32 \_ DeviceMemoryAddress**](win32-devicememoryaddress.md)             | Representa una dirección de memoria de dispositivo en un sistema Windows.<br/>                                                                                                                                                        |
| [**Win32 \_ DeviceSettings**](win32-devicesettings.md)                       | Relaciona un dispositivo lógico y un valor de configuración que se puede aplicar a él.<br/>                                                                                                                                              |
| [**Win32 \_ DMAChannel**](win32-dmachannel.md)                               | Representa un canal de acceso directo a memoria (DMA) en un equipo que ejecuta Windows.<br/>                                                                                                                          |
| [**Win32 \_ FloppyController**](win32-floppycontroller.md)                   | Representa las capacidades y la capacidad de administración de un controlador de unidad de disquete.<br/>                                                                                                                         |
| [**Win32 \_ IDEController**](win32-idecontroller.md)                         | Representa las capacidades de un dispositivo de controlador de electrónica integrada de unidades (IDE).<br/>                                                                                                                        |
| [**Win32 \_ IDEControllerDevice**](win32-idecontrollerdevice.md)             | Clase de asociación que relaciona una controladora IDE y el dispositivo lógico.<br/>                                                                                                                                       |
| [**Win32 \_ InfraredDevice**](win32-infrareddevice.md)                       | Representa las capacidades y la administración de un dispositivo de infrarrojos.<br/>                                                                                                                                              |
| [**Win32 \_ IRQResource**](win32-irqresource.md)                             | Representa un número de línea de solicitud de interrupción (IRQ) en un equipo Windows.<br/>                                                                                                                                |
| [**Win32 \_ MemoryArray**](win32-memoryarray.md)                             | Representa las propiedades de la matriz de memoria del sistema del equipo y las direcciones asignadas.<br/>                                                                                                                            |
| [**Win32 \_ MemoryArrayLocation**](win32-memoryarraylocation.md)             | Relaciona una matriz de memoria lógica y la matriz de memoria física en la que existe.<br/>                                                                                                                             |
| [**Win32 \_ MemoryDevice**](win32-memorydevice.md)                           | Representa las propiedades del dispositivo de memoria de un equipo junto con sus direcciones asignadas asociadas.<br/>                                                                                                     |
| [**Win32 \_ MemoryDeviceArray**](win32-memorydevicearray.md)                 | Relaciona un dispositivo de memoria y la matriz de memoria en la que reside.<br/>                                                                                                                                              |
| [**Win32 \_ MemoryDeviceLocation**](win32-memorydevicelocation.md)           | Clase de asociación que relaciona un dispositivo de memoria y la memoria física en la que existe.<br/>                                                                                                                     |
| [**Win32 \_ MotherboardDevice**](win32-motherboarddevice.md)                 | Representa un dispositivo que contiene los componentes centrales del sistema de equipos que ejecutan Windows.<br/>                                                                                                               |
| [**Win32 \_ OnBoardDevice**](win32-onboarddevice.md)                         | Representa dispositivos de adaptador comunes integrados en la placa base (placa de sistema).<br/>                                                                                                                                   |
| [**Win32 \_ ParallelPort**](win32-parallelport.md)                           | Representa las propiedades de un puerto paralelo en un equipo con Windows.<br/>                                                                                                                             |
| [**Win32 \_ PCMCIAController**](win32-pcmciacontroller.md)                   | Administra las capacidades de un dispositivo de controlador de adaptador de interfaz de tarjeta de memoria de equipo personal (PCMCIA).<br/>                                                                                                      |
| [**Win32 \_ PhysicalMemory**](win32-physicalmemory.md)                       | Representa un dispositivo de memoria física ubicado en un equipo como disponible para el sistema operativo.<br/>                                                                                                                |
| [**Win32 \_ PhysicalMemoryArray**](win32-physicalmemoryarray.md)             | Representa los detalles sobre la memoria física del sistema del equipo.<br/>                                                                                                                                                |
| [**Win32 \_ PhysicalMemoryLocation**](win32-physicalmemorylocation.md)       | Relaciona una matriz de memoria física y su memoria física.<br/>                                                                                                                                                   |
| [**Win32 \_ PNPAllocatedResource**](win32-pnpallocatedresource.md)           | Representa una asociación entre dispositivos lógicos y recursos del sistema.<br/>                                                                                                                                        |
| [**Win32 \_ PNPDevice**](win32-pnpdevice.md)                                 | Relaciona un dispositivo (conocido como Configuration Manager como PNPEntity) y la función que realiza.<br/>                                                                                                                |
| [**Win32 \_ PNPEntity**](win32-pnpentity.md)                                 | Representa las propiedades de un dispositivo Plug and Play.<br/>                                                                                                                                                           |
| [**Win32 \_ PortConnector**](win32-portconnector.md)                         | Representa puertos de conexión físicos, como los machos DB-25 pin, Centronics y PS/2.<br/>                                                                                                                            |
| [**Win32 \_ PortResource**](win32-portresource.md)                           | Representa un puerto de e/s en un equipo con Windows.<br/>                                                                                                                                                   |
| [**\_Procesador Win32**](win32-processor.md)                                 | Representa un dispositivo capaz de interpretar una secuencia de instrucciones del equipo en un equipo que ejecuta Windows.<br/>                                                                                           |
| [**Win32 \_ SCSIController**](win32-scsicontroller.md)                       | Representa un controlador de interfaz del sistema de equipos pequeños (SCSI) en un equipo que ejecuta Windows.<br/>                                                                                                           |
| [**Win32 \_ SCSIControllerDevice**](win32-scsicontrollerdevice.md)           | Relaciona una controladora SCSI y el dispositivo lógico (unidad de disco) conectado a él.<br/>                                                                                                                                 |
| [**SerialPort de Win32 \_**](win32-serialport.md)                               | Representa un puerto serie de un equipo que ejecuta Windows.<br/>                                                                                                                                                 |
| [**Win32 \_ SerialPortConfiguration**](win32-serialportconfiguration.md)     | Representa la configuración para la transmisión de datos en un puerto serie de Windows.<br/>                                                                                                                                        |
| [**Win32 \_ SerialPortSetting**](win32-serialportsetting.md)                 | Relaciona un puerto serie y sus valores de configuración.<br/>                                                                                                                                                          |
| [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md)                           | Representa las capacidades y la administración de los dispositivos lógicos relacionados con la memoria.<br/>                                                                                                                                  |
| [**Win32 \_ SoundDevice**](win32-sounddevice.md)                             | Representa las propiedades de un dispositivo de sonido de un equipo que ejecuta Windows.<br/>                                                                                                                              |
| [**Win32 \_ SystemBIOS**](win32-systembios.md)                               | Relaciona un sistema informático (incluidos datos como propiedades de inicio, zonas horarias, configuraciones de arranque o contraseñas administrativas) y un BIOS del sistema (servicios, idiomas y propiedades de administración del sistema).<br/> |
| [**Win32 \_ SystemDriverPNPEntity**](win32-systemdriverpnpentity.md)         | Relaciona un dispositivo Plug and Play en el sistema del equipo Windows y el controlador que admite el dispositivo Plug and Play.<br/>                                                                                           |
| [**Win32 \_ SystemEnclosure**](win32-systemenclosure.md)                     | Representa las propiedades asociadas a un gabinete del sistema físico.<br/>                                                                                                                                         |
| [**Win32 \_ SystemMemoryResource**](win32-systemmemoryresource.md)           | Representa un recurso de memoria del sistema en un sistema Windows.<br/>                                                                                                                                                       |
| [**Win32 \_ SystemSlot**](win32-systemslot.md)                               | Representa los puntos de conexión físicos, incluidos los puertos, los periféricos y las ranuras de la placa base, y los puntos de conexión de propiedad.<br/>                                                                                  |
| [**Win32 \_ USBController**](win32-usbcontroller.md)                         | Administra las capacidades de un controlador de bus serie universal (USB).<br/>                                                                                                                                           |
| [**Win32 \_ USBControllerDevice**](win32-usbcontrollerdevice.md)             | Relaciona una controladora USB y las instancias [**de \_ LogicalDevice de CIM**](cim-logicaldevice.md) conectadas a ella.<br/>                                                                                                    |
| [**USBHub de Win32 \_**](/previous-versions/windows/desktop/cimwin32a/win32-usbhub)                                 | Representa las características de administración de un concentrador USB.<br/>                                                                                                                                                        |



 

## <a name="networking-device-classes"></a>Clases de dispositivos de red

La subcategoría dispositivos de red agrupa las clases que representan el controlador de la interfaz de red, sus configuraciones y su configuración.



| Clase                                                                           | Descripción                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Adaptador de Win32 \_**](win32-networkadapter.md)                           | Representa un adaptador de red en un equipo que ejecuta Windows.<br/>                                                                                                                                          |
| [**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) | Representa los atributos y los comportamientos de un adaptador de red. No se garantiza que la clase sea compatible después de la ratificación de la especificación de red CIM del equipo de administración distribuida (DMTF).<br/> |
| [**Win32 \_ NetworkAdapterSetting**](win32-networkadaptersetting.md)             | Relaciona un adaptador de red y sus valores de configuración.<br/>                                                                                                                                                   |



 

## <a name="power-classes"></a>Clases de energía

La subcategoría de energía agrupa las clases que representan fuentes de alimentación, baterías y eventos relacionados con estos dispositivos.



| Clase                                                             | Descripción                                                                                           |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**Batería de Win32 \_**](win32-battery.md)                           | Representa una batería conectada al sistema del equipo.<br/>                                     |
| [**Win32 \_ CurrentProbe**](win32-currentprobe.md)                 | Representa las propiedades de un sensor de supervisión actual (ammeter).<br/>                        |
| [**Win32 \_ PortableBattery**](win32-portablebattery.md)           | Representa las propiedades de una batería portátil, como una usada para un equipo portátil.<br/> |
| [**Win32 \_ PowerManagementEvent**](win32-powermanagementevent.md) | Representa los eventos de administración de energía resultantes de los cambios de estado de energía.<br/>                     |
| [**Win32 \_ VoltageProbe**](win32-voltageprobe.md)                 | Representa las propiedades de un detector de voltaje (el voltímetro electrónico).<br/>                      |



 

## <a name="printing-classes"></a>Clases de impresión

Las clases de grupos de subcategoría de impresión que representan impresoras, configuraciones de impresora y trabajos de impresión.



| Clase                                                             | Descripción                                                                                                                              |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ DriverForDevice**](win32-driverfordevice.md)           | Relaciona una impresora con un controlador de impresora.<br/>                                                                                        |
| [**\_Impresora Win32**](win32-printer.md)                           | Representa un dispositivo conectado a un equipo que ejecuta Windows y que es capaz de reproducir una imagen de objetos visuales en un medio.<br/> |
| [**Win32 \_ PrinterConfiguration**](win32-printerconfiguration.md) | Define la configuración de un dispositivo de impresora.<br/>                                                                               |
| [**Win32 \_ PrinterController**](win32-printercontroller.md)       | Relaciona una impresora y el dispositivo local al que está conectada la impresora.<br/>                                                     |
| [**Win32 \_ PrinterDriver**](win32-printerdriver.md)               | Representa los controladores para una instancia de [**\_ impresora de Win32**](win32-printer.md) .<br/>                                                |
| [**Win32 \_ PrinterDriverDll**](win32-printerdriverdll.md)         | Relaciona una impresora local y su archivo de controlador (no el propio controlador).<br/>                                                          |
| [**Win32 \_ PrinterSetting**](win32-printersetting.md)             | Relaciona una impresora y sus valores de configuración.<br/>                                                                             |
| [**PrintJob de Win32 \_**](win32-printjob.md)                         | Representa un trabajo de impresión generado por una aplicación basada en Windows.<br/>                                                              |
| [**Win32 \_ TCPIPPrinterPort**](win32-tcpipprinterport.md)         | Representa un punto de acceso al servicio TCP/IP.<br/>                                                                                     |



 

## <a name="telephony-classes"></a>Clases de telefonía

La subcategoría telefonía agrupa las clases que representan los dispositivos de módem "teléfono anterior sin formato" y sus conexiones serie asociadas.



| Clase                                                               | Descripción                                                                                                                                |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ POTSModem**](win32-potsmodem.md)                         | Representa los servicios y las características de un módem de servicio telefónico anterior (POTS) en un equipo que ejecuta Windows.<br/> |
| [**Win32 \_ POTSModemToSerialPort**](win32-potsmodemtoserialport.md) | Relaciona un módem y el puerto serie que usa el módem.<br/>                                                                             |



 

## <a name="video-and-monitor-classes"></a>Clases de vídeo y de monitor

El vídeo y los monitores agrupan las clases que representan monitores, tarjetas de vídeo y sus valores de configuración asociados.



| Clase                                                                                 | Descripción                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md)                                 | Representa el tipo de monitor o dispositivo de pantalla conectado al sistema del equipo.<br/>                                                                                                                                                                                                                                                                                       |
| [**Win32 \_ DisplayControllerConfiguration**](win32-displaycontrollerconfiguration.md) | Representa la información de configuración del adaptador de vídeo de un equipo que ejecuta Windows. Esta clase está obsoleta. En lugar de esta clase, use las propiedades de las [**clases \_ videocontroller**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md)y [CIM \_ VideoControllerResolution](cim-videocontrollerresolution.md) de Win32.<br/> |
| [**\_Videocontroladora Win32**](win32-videocontroller.md)                               | Representa las capacidades y la capacidad de administración del controlador de vídeo en un equipo que ejecuta Windows.<br/>                                                                                                                                                                                                                                                       |
| [**Videoconfiguración de Win32 \_**](win32-videosettings.md)                                   | Relaciona una configuración de vídeo y un controlador de vídeo que se puede aplicar a ella.<br/>                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Clases Win32](/previous-versions//aa394084(v=vs.85))
</dt> </dl>

 

