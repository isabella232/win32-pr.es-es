---
description: La categoría Hardware del sistema de equipo agrupa las clases que representan objetos relacionados con el hardware. Algunos ejemplos son los dispositivos de entrada, los discos duros, las tarjetas de expansión, los dispositivos de vídeo, los dispositivos de red y la alimentación del sistema.
ms.assetid: 0b6cb410-166e-45cd-8dca-77a111b3cf62
ms.tgt_platform: multiple
title: Clases de hardware del sistema de equipo
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d541071698c08510452faaf6bef0cd706dab66e5eaa77b5db121e522785c5c4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118420100"
---
# <a name="computer-system-hardware-classes"></a>Clases de hardware del sistema de equipo

La categoría Hardware del sistema de equipo agrupa las clases que representan objetos relacionados con el hardware. Algunos ejemplos son los dispositivos de entrada, los discos duros, las tarjetas de expansión, los dispositivos de vídeo, los dispositivos de red y la alimentación del sistema.

-   [Clases de dispositivos de refrigeración](#cooling-device-classes)
-   [Clases de dispositivo de entrada](#input-device-classes)
-   [Clases de Storage masivas](#mass-storage-classes)
-   [Clases de placa base, controlador y puerto](#motherboard-controller-and-port-classes)
-   [Clases de dispositivos de red](#networking-device-classes)
-   [Clases de energía](#power-classes)
-   [Clases de impresión](#printing-classes)
-   [Clases de telefonía](#telephony-classes)
-   [Clases de vídeo y supervisión](#video-and-monitor-classes)
-   [Temas relacionados](#related-topics)

## <a name="cooling-device-classes"></a>Clases de dispositivos de refrigeración

La subcategoría Dispositivos de refrigeración agrupa clases que representan ventiladores instrumentables, sondeos de temperatura y dispositivos de refrigeración.



| Clase                                                     | Descripción                                                                 |
|-----------------------------------------------------------|-----------------------------------------------------------------------------|
| [**Win32 \_ Fan**](win32-fan.md)                           | Representa las propiedades de un dispositivo de ventilador en el sistema informático.           |
| [**Win32 \_ HeatPipe**](win32-heatpipe.md)                 | Representa las propiedades de un dispositivo de refrigeración de canalización de calor.                    |
| [**Refrigeración win32 \_**](win32-refrigeration.md)       | Representa las propiedades de un dispositivo de refrigeración.                        |
| [**Win32 \_ TemperatureProbe**](win32-temperatureprobe.md) | Representa las propiedades de un sensor de temperatura (termómetro electrónico). |



 

## <a name="input-device-classes"></a>Clases de dispositivo de entrada

La subcategoría Dispositivos de entrada agrupa clases que representan teclados y dispositivos que apuntan.



| Clase                                                 | Descripción                                                                                                         |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**Teclado \_ Win32**](win32-keyboard.md)             | Representa un teclado instalado en un sistema informático que ejecuta Windows.                                               |
| [**Win32 \_ PointingDevice**](win32-pointingdevice.md) | Representa un dispositivo de entrada que se usa para señalar y seleccionar regiones en la pantalla de un sistema informático que ejecuta Windows. |



 

## <a name="mass-storage-classes"></a>Clases de Storage masivas

Las clases de la subcategoría Storage representan dispositivos de almacenamiento, como unidades de disco duro, unidades de CD-ROM y unidades de cinta.



| Clase                                                     | Descripción                                                                                  |
|-----------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**AutochkSetting de Win32 \_**](win32-autochksetting.md)     | Representa la configuración de la operación de comprobación automática de un disco.                               |
| [**Win32 \_ CDROMDrive**](win32-cdromdrive.md)             | Representa una unidad de CD-ROM en un sistema informático que ejecuta Windows.                              |
| [**Win32 \_ DiskDrive**](win32-diskdrive.md)               | Representa una unidad de disco físico tal como la ve un equipo que ejecuta Windows sistema operativo. |
| [**Win32 \_ FloppyDrive**](win32-floppydrive.md)           | Administra las funcionalidades de una unidad de disquete.                                             |
| [**Win32 \_ PhysicalMedia**](/previous-versions/windows/desktop/cimwin32a/win32-physicalmedia) | Representa cualquier tipo de documentación o medio de almacenamiento.                                      |
| [**Win32 \_ TapeDrive**](win32-tapedrive.md)               | Representa una unidad de cinta en un sistema informático que ejecuta Windows.                                |



 

## <a name="motherboard-controller-and-port-classes"></a>Clases de placa base, controlador y puerto

La subcategoría Placa base, Controladores y Puertos agrupa las clases que representan dispositivos del sistema. Algunos ejemplos son la memoria del sistema, la memoria caché y los controladores.



| Clase                                                                       | Descripción                                                                                                                                                                                                               |
|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ 1394Controller**](win32-1394controller.md)                       | Representa las funcionalidades y la administración de un controlador 1394.<br/>                                                                                                                                               |
| [**Win32 \_ 1394ControllerDevice**](win32-1394controllerdevice.md)           | Relaciona el controlador de bus serie de alta velocidad (IEEE 1394 Firewire) y la instancia [**\_ de LogicalDevice**](cim-logicaldevice.md) de CIM conectada a él.<br/>                                                            |
| [**Win32 \_ AllocatedResource**](win32-allocatedresource.md)                 | Relaciona un dispositivo lógico con un recurso del sistema.<br/>                                                                                                                                                                 |
| [**Win32 \_ AssociatedProcessorMemory**](win32-associatedprocessormemory.md) | Relaciona un procesador y su memoria caché.<br/>                                                                                                                                                                      |
| [**Win32 \_ BaseBoard**](win32-baseboard.md)                                 | Representa un placa base (también conocido como placa base o placa del sistema).<br/>                                                                                                                                          |
| [**BIOS de Win32 \_**](win32-bios.md)                                           | Representa los atributos de los servicios básicos de entrada o salida (BIOS) del sistema informático que están instalados en el equipo.<br/>                                                                                   |
| [**Win32 \_ Bus**](win32-bus.md)                                             | Representa un bus físico tal como lo ve un Windows operativo.<br/>                                                                                                                                               |
| [**Win32 \_ CacheMemory**](win32-cachememory.md)                             | Representa la memoria caché (interna y externa) en un sistema informático.<br/>                                                                                                                                          |
| [**Win32 \_ ControllerHasHub**](/previous-versions/windows/desktop/cimwin32a/win32-controllerhashub)             | Representa los concentradores de bajada desde el controlador de bus serie universal (USB).<br/>                                                                                                                                 |
| [**Win32 \_ DeviceBus**](win32-devicebus.md)                                 | Relaciona un bus del sistema y un dispositivo lógico mediante el bus.<br/>                                                                                                                                                       |
| [**Win32 \_ DeviceMemoryAddress**](win32-devicememoryaddress.md)             | Representa una dirección de memoria del dispositivo en Windows sistema.<br/>                                                                                                                                                        |
| [**Dispositivo \_ Win32Settings**](win32-devicesettings.md)                       | Relaciona un dispositivo lógico y una configuración que se puede aplicar a él.<br/>                                                                                                                                              |
| [**Win32 \_ DMAChannel**](win32-dmachannel.md)                               | Representa un canal de acceso directo a memoria (DMA) en un sistema informático que ejecuta Windows.<br/>                                                                                                                          |
| [**Win32 \_ FloppyController**](win32-floppycontroller.md)                   | Representa las funcionalidades y la capacidad de administración de un controlador de unidad de disquete.<br/>                                                                                                                         |
| [**IdeController de Win32 \_**](win32-idecontroller.md)                         | Representa las funciones de un dispositivo de controlador de Integrated Drive Electronics (IDE).<br/>                                                                                                                        |
| [**Win32 \_ IDEControllerDevice**](win32-idecontrollerdevice.md)             | Clase de asociación que relaciona un controlador IDE y el dispositivo lógico.<br/>                                                                                                                                       |
| [**Win32 \_ DesarrobaDispositivo**](win32-infrareddevice.md)                       | Representa las funcionalidades y la administración de un dispositivo de carga.<br/>                                                                                                                                              |
| [**Win32 \_ IRQResource**](win32-irqresource.md)                             | Representa un número de línea de solicitud de interrupción (IRQ) en un Windows equipo.<br/>                                                                                                                                |
| [**MemoryArray de Win32 \_**](win32-memoryarray.md)                             | Representa las propiedades de la matriz de memoria del sistema del equipo y las direcciones asignadas.<br/>                                                                                                                            |
| [**MemoryArrayLocation de Win32 \_**](win32-memoryarraylocation.md)             | Relaciona una matriz de memoria lógica y la matriz de memoria física en la que existe.<br/>                                                                                                                             |
| [**MemoryDevice de Win32 \_**](win32-memorydevice.md)                           | Representa las propiedades del dispositivo de memoria de un sistema informático junto con sus direcciones asignadas asociadas.<br/>                                                                                                     |
| [**MemoryDeviceArray de Win32 \_**](win32-memorydevicearray.md)                 | Relaciona un dispositivo de memoria y la matriz de memoria en la que reside.<br/>                                                                                                                                              |
| [**MemoryDeviceLocation de Win32 \_**](win32-memorydevicelocation.md)           | Clase de asociación que relaciona un dispositivo de memoria y la memoria física en la que existe.<br/>                                                                                                                     |
| [**Placa base \_ Win32Dispositivo**](win32-motherboarddevice.md)                 | Representa un dispositivo que contiene los componentes centrales del sistema informático que ejecuta Windows.<br/>                                                                                                               |
| [**Win32 \_ OnBoardDevice**](win32-onboarddevice.md)                         | Representa los dispositivos adaptadores comunes integrados en la placa base (placa del sistema).<br/>                                                                                                                                   |
| [**Win32 \_ ParallelPort**](win32-parallelport.md)                           | Representa las propiedades de un puerto paralelo en un sistema de equipo que ejecuta Windows.<br/>                                                                                                                             |
| [**Win32 \_ PCMCIAController**](win32-pcmciacontroller.md)                   | Administra las funcionalidades de un dispositivo de controlador de adaptador de interfaz de tarjeta de memoria (PCMCIA) del equipo personal.<br/>                                                                                                      |
| [**Win32 \_ PhysicalMemory**](win32-physicalmemory.md)                       | Representa un dispositivo de memoria física ubicado en un equipo como disponible para el sistema operativo.<br/>                                                                                                                |
| [**Win32 \_ PhysicalMemoryArray**](win32-physicalmemoryarray.md)             | Representa detalles sobre la memoria física del sistema del equipo.<br/>                                                                                                                                                |
| [**Win32 \_ PhysicalMemoryLocation**](win32-physicalmemorylocation.md)       | Relaciona una matriz de memoria física y su memoria física.<br/>                                                                                                                                                   |
| [**Win32 \_ PNPAllocatedResource**](win32-pnpallocatedresource.md)           | Representa una asociación entre dispositivos lógicos y recursos del sistema.<br/>                                                                                                                                        |
| [**Win32 \_ PNPDevice**](win32-pnpdevice.md)                                 | Relaciona un dispositivo (conocido por Administrador de configuración como PNPEntity) y la función que realiza.<br/>                                                                                                                |
| [**Win32 \_ PNPEntity**](win32-pnpentity.md)                                 | Representa las propiedades de un Plug and Play dispositivo.<br/>                                                                                                                                                           |
| [**Win32 \_ PortConnector**](win32-portconnector.md)                         | Representa puertos de conexión físicos, como DB-25 pin male, Centronics y PS/2.<br/>                                                                                                                            |
| [**Win32 \_ PortResource**](win32-portresource.md)                           | Representa un puerto de E/S en un sistema de equipo que ejecuta Windows.<br/>                                                                                                                                                   |
| [**Procesador \_ Win32**](win32-processor.md)                                 | Representa un dispositivo capaz de interpretar una secuencia de instrucciones de máquina en un sistema informático que ejecuta Windows.<br/>                                                                                           |
| [**Win32 \_ SCSIController**](win32-scsicontroller.md)                       | Representa un controlador de interfaz de sistema de equipo pequeño (SCSI) en un sistema informático que ejecuta Windows.<br/>                                                                                                           |
| [**Win32 \_ SCSIControllerDevice**](win32-scsicontrollerdevice.md)           | Relaciona una controladora SCSI y el dispositivo lógico (unidad de disco) conectado a él.<br/>                                                                                                                                 |
| [**Win32 \_ SerialPort**](win32-serialport.md)                               | Representa un puerto serie en un sistema informático que ejecuta Windows.<br/>                                                                                                                                                 |
| [**SerialPortConfiguration de Win32 \_**](win32-serialportconfiguration.md)     | Representa la configuración de la transmisión de datos en un Windows serie.<br/>                                                                                                                                        |
| [**SerialPortSetting de Win32 \_**](win32-serialportsetting.md)                 | Relaciona un puerto serie y sus opciones de configuración.<br/>                                                                                                                                                          |
| [**Win32 \_ SMBIOSMemory**](win32-smbiosmemory.md)                           | Representa las funcionalidades y la administración de dispositivos lógicos relacionados con la memoria.<br/>                                                                                                                                  |
| [**Win32 \_ SoundDevice**](win32-sounddevice.md)                             | Representa las propiedades de un dispositivo de sonido en un sistema informático que ejecuta Windows.<br/>                                                                                                                              |
| [**Win32 \_ SystemBIOS**](win32-systembios.md)                               | Relaciona un sistema informático (incluidos datos como propiedades de inicio, zonas horarias, configuraciones de arranque o contraseñas administrativas) y un BIOS del sistema (servicios, idiomas y propiedades de administración del sistema).<br/> |
| [**Win32 \_ SystemDriverPNPEntity**](win32-systemdriverpnpentity.md)         | Relaciona un dispositivo Plug and Play en el Windows del equipo y el controlador que admite el Plug and Play dispositivo.<br/>                                                                                           |
| [**Sistema \_ Win32Enclosure**](win32-systemenclosure.md)                     | Representa las propiedades asociadas a un gabinete del sistema físico.<br/>                                                                                                                                         |
| [**Win32 \_ SystemMemoryResource**](win32-systemmemoryresource.md)           | Representa un recurso de memoria del sistema en un Windows sistema.<br/>                                                                                                                                                       |
| [**Win32 \_ SystemSlot**](win32-systemslot.md)                               | Representa puntos de conexión físicos, incluidos puertos, ranuras de placa base y periféricos, y puntos de conexión propietarios.<br/>                                                                                  |
| [**Win32 \_ USBController**](win32-usbcontroller.md)                         | Administra las funcionalidades de un controlador de bus serie universal (USB).<br/>                                                                                                                                           |
| [**Win32 \_ USBControllerDevice**](win32-usbcontrollerdevice.md)             | Relaciona un controlador USB y las instancias [**\_ de Cim LogicalDevice**](cim-logicaldevice.md) conectadas a él.<br/>                                                                                                    |
| [**Win32 \_ USBHub**](/previous-versions/windows/desktop/cimwin32a/win32-usbhub)                                 | Representa las características de administración de un concentrador USB.<br/>                                                                                                                                                        |



 

## <a name="networking-device-classes"></a>Clases de dispositivos de red

La subcategoría Dispositivos de red agrupa clases que representan el controlador de interfaz de red, sus configuraciones y su configuración.



| Clase                                                                           | Descripción                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NetworkAdapter de Win32 \_**](win32-networkadapter.md)                           | Representa un adaptador de red en un sistema informático que ejecuta Windows.<br/>                                                                                                                                          |
| [**NetworkAdapterConfiguration de Win32 \_**](win32-networkadapterconfiguration.md) | Representa los atributos y comportamientos de un adaptador de red. No se garantiza que se admite la clase después de la vigencia de la especificación de red CIM del Grupo de tareas de administración distribuida (DMTF).<br/> |
| [**Win32 \_ NetworkAdapterSetting**](win32-networkadaptersetting.md)             | Relaciona un adaptador de red y sus opciones de configuración.<br/>                                                                                                                                                   |



 

## <a name="power-classes"></a>Clases de energía

La subcategoría Power agrupa clases que representan fuentes de alimentación, baterías y eventos relacionados con estos dispositivos.



| Clase                                                             | Descripción                                                                                           |
|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**Batería \_ Win32**](win32-battery.md)                           | Representa una batería conectada al sistema informático.<br/>                                     |
| [**CurrentProbe de Win32 \_**](win32-currentprobe.md)                 | Representa las propiedades de un sensor de supervisión actual (ammeter).<br/>                        |
| [**Win32 \_ PortableBattery**](win32-portablebattery.md)           | Representa las propiedades de una batería portátil, como la que se usa para un equipo notebook.<br/> |
| [**Win32 \_ PowerManagementEvent**](win32-powermanagementevent.md) | Representa los eventos de administración de energía resultantes de los cambios de estado de energía.<br/>                     |
| [**Win32 \_ VoltageProbe**](win32-voltageprobe.md)                 | Representa las propiedades de un sensor de voltaje (voltómetro electrónico).<br/>                      |



 

## <a name="printing-classes"></a>Clases de impresión

La subcategoría Printing agrupa clases que representan impresoras, configuraciones de impresora y trabajos de impresión.



| Clase                                                             | Descripción                                                                                                                              |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ DriverForDevice**](win32-driverfordevice.md)           | Relaciona una impresora con un controlador de impresora.<br/>                                                                                        |
| [**Impresora \_ Win32**](win32-printer.md)                           | Representa un dispositivo conectado a un sistema informático Windows que es capaz de reproducir una imagen visual en un medio.<br/> |
| [**PrinterConfiguration de Win32 \_**](win32-printerconfiguration.md) | Define la configuración de un dispositivo de impresora.<br/>                                                                               |
| [**Win32 \_ PrinterController**](win32-printercontroller.md)       | Relaciona una impresora y el dispositivo local al que está conectada la impresora.<br/>                                                     |
| [**Win32 \_ PrinterDriver**](win32-printerdriver.md)               | Representa los controladores de una [**instancia de \_ Impresora Win32.**](win32-printer.md)<br/>                                                |
| [**Win32 \_ PrinterDriverDll**](win32-printerdriverdll.md)         | Relaciona una impresora local y su archivo de controlador (no el propio controlador).<br/>                                                          |
| [**PrinterSetting de Win32 \_**](win32-printersetting.md)             | Relaciona una impresora y sus opciones de configuración.<br/>                                                                             |
| [**PrintJob de Win32 \_**](win32-printjob.md)                         | Representa un trabajo de impresión generado por una Windows basada en aplicaciones.<br/>                                                              |
| [**Win32 \_ TCPIPPrinterPort**](win32-tcpipprinterport.md)         | Representa un punto de acceso del servicio TCP/IP.<br/>                                                                                     |



 

## <a name="telephony-classes"></a>Clases de telefonía

La subcategoría De telefonía agrupa las clases que representan dispositivos de módem "teléfono antiguo sin formato" y sus conexiones serie asociadas.



| Clase                                                               | Descripción                                                                                                                                |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ POTSModem**](win32-potsmodem.md)                         | Representa los servicios y las características de un módem del Servicio de teléfono antiguo sin formato (POTS) en un sistema informático que ejecuta Windows.<br/> |
| [**Win32 \_ POTSModemToSerialPort**](win32-potsmodemtoserialport.md) | Relaciona un módem y el puerto serie que usa el módem.<br/>                                                                             |



 

## <a name="video-and-monitor-classes"></a>Clases de vídeo y supervisión

La subcategoría Video y Monitores agrupa las clases que representan monitores, tarjetas de vídeo y su configuración asociada.



| Clase                                                                                 | Descripción                                                                                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md)                                 | Representa el tipo de monitor o dispositivo de visualización conectado al sistema informático.<br/>                                                                                                                                                                                                                                                                                       |
| [**DisplayControllerConfiguration de Win32 \_**](win32-displaycontrollerconfiguration.md) | Representa la información de configuración del adaptador de vídeo de un sistema informático que ejecuta Windows. Esta clase está obsoleta. En lugar de esta clase, use las propiedades de las clases [**Win32 \_ VideoController**](win32-videocontroller.md), [**Win32 \_ DesktopMonitor**](win32-desktopmonitor.md)y [CIM \_ VideoControllerResolution.](cim-videocontrollerresolution.md)<br/> |
| [**Win32 \_ VideoController**](win32-videocontroller.md)                               | Representa las capacidades y la capacidad de administración del controlador de vídeo en un sistema informático que ejecuta Windows.<br/>                                                                                                                                                                                                                                                       |
| [**Win32 \_ VideoSettings**](win32-videosettings.md)                                   | Relaciona un controlador de vídeo y la configuración de vídeo que se puede aplicar a él.<br/>                                                                                                                                                                                                                                                                                                |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Clases win32](/previous-versions//aa394084(v=vs.85))
</dt> </dl>

 

