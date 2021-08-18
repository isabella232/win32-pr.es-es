---
title: Interfaz IVMHostInfo (VPCCOMInterfaces.h)
description: Recupera información sobre el equipo host. Se devuelve un objeto IVMHostInfo de la propiedad IVMVirtualPC HostInfo.
ms.assetid: f30fa377-2067-4e03-bc6e-2ada62fc56b4
keywords:
- IVMHostInfo interface Virtual PC
- Interfaz IVMHostInfo del equipo virtual , descrito
topic_type:
- apiref
api_name:
- IVMHostInfo
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da45459379c468839b0bf48ae134db1885ea25acce5ac3befa289ae15ee6fe8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974265"
---
# <a name="ivmhostinfo-interface"></a>Interfaz IVMHostInfo

\[Windows El equipo virtual ya no está disponible para su uso a Windows 8. En su lugar, use [el proveedor WMI de Hyper-V (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Recupera información sobre el equipo host. Se devuelve un objeto **IVMHostInfo** de la [**propiedad IVMVirtualPC::HostInfo.**](ivmvirtualpc-hostinfo.md)

## <a name="members"></a>Miembros

La **interfaz IVMHostInfo** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMHostInfo también** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **interfaz IVMHostInfo** tiene estas propiedades.



| Propiedad                                                                                  | Tipo de acceso          | Descripción                                                                                        |
|:------------------------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------|
| [**DVDDrives**](ivmhostinfo-dvddrives.md)<br/>                                     | Solo lectura<br/> | Letras de unidad asociadas a los dispositivos de CD y DVD del host.<br/>                              |
| [**Disquetes**](ivmhostinfo-floppydrives.md)<br/>                               | Solo lectura<br/> | Letras de unidad asociadas a disquetes de host.<br/>                                   |
| [**LogicalProcessorCount**](ivmhostinfo-logicalprocessorcount.md)<br/>             | Solo lectura<br/> | Número de procesadores lógicos del equipo host.<br/>                                   |
| [**Memoria**](ivmhostinfo-memory.md)<br/>                                           | Solo lectura<br/> | Cantidad total de memoria física en el equipo host, en megabytes.<br/>                  |
| [**MemoryAvail**](ivmhostinfo-memoryavail.md)<br/>                                 | Solo lectura<br/> | Cantidad de memoria física disponible en el equipo host, en megabytes.<br/>              |
| [**MemoryAvailString**](ivmhostinfo-memoryavailstring.md)<br/>                     | Solo lectura<br/> | Cantidad de memoria física disponible en el equipo host, en megabytes, como una cadena.<br/> |
| [**MemoryTotalString**](ivmhostinfo-memorytotalstring.md)<br/>                     | Solo lectura<br/> | Cantidad total de memoria física en el equipo host, en megabytes, como una cadena.<br/>     |
| [**Mmx**](ivmhostinfo-mmx.md)<br/>                                                 | Solo lectura<br/> | Indica si el procesador admite el conjunto de instrucciones MMX.<br/>                       |
| [**NetworkAdapters**](ivmhostinfo-networkadapters.md)<br/>                         | Solo lectura<br/> | Colección enumerable de NIC en el equipo host.<br/>                                   |
| [**NetworkAddresses**](ivmhostinfo-networkaddresses.md)<br/>                       | Solo lectura<br/> | Colección enumerable de direcciones TCP/IP en el equipo host.<br/>                       |
| [**OperatingSystem**](ivmhostinfo-operatingsystem.md)<br/>                         | Solo lectura<br/> | Sistema operativo que se ejecuta en el equipo host.<br/>                                       |
| [**OSMajorVersion**](ivmhostinfo-osmajorversion.md)<br/>                           | Solo lectura<br/> | La versión principal del sistema operativo que se ejecuta en el equipo host.<br/>                  |
| [**OSMinorVersion**](ivmhostinfo-osminorversion.md)<br/>                           | Solo lectura<br/> | La versión secundaria del sistema operativo que se ejecuta en el equipo host.<br/>                  |
| [**OSServicePackString**](ivmhostinfo-osservicepackstring.md)<br/>                 | Solo lectura<br/> | Información del Service Pack del sistema operativo que se ejecuta en el equipo host.<br/>       |
| [**OSVersionString**](ivmhostinfo-osversionstring.md)<br/>                         | Solo lectura<br/> | Versión del sistema operativo que se ejecuta en el equipo host.<br/>                               |
| [**ParallelPort**](ivmhostinfo-parallelport.md)<br/>                               | Solo lectura<br/> | Puerto paralelo del host que se puede conectar al invitado.<br/>                               |
| [**PhysicalProcessorCount**](ivmhostinfo-physicalprocessorcount.md)<br/>           | Solo lectura<br/> | Número de procesadores físicos del equipo host.<br/>                                  |
| [**ProcessorFeaturesString**](ivmhostinfo-processorfeaturesstring.md)<br/>         | Solo lectura<br/> | Lista de características admitidas por el procesador host.<br/>                                   |
| [**ProcessorManufacturerString**](ivmhostinfo-processormanufacturerstring.md)<br/> | Solo lectura<br/> | Fabricante del procesador host.<br/>                                                 |
| [**ProcessorSpeed**](ivmhostinfo-processorspeed.md)<br/>                           | Solo lectura<br/> | Velocidad del procesador host, en megahercios (MHz) o gigahercios (GHz).<br/>                 |
| [**ProcessorSpeedString**](ivmhostinfo-processorspeedstring.md)<br/>               | Solo lectura<br/> | Velocidad del procesador host, en megahercios o gigahercios, como una cadena.<br/>                |
| [**ProcessorVersionString**](ivmhostinfo-processorversionstring.md)<br/>           | Solo lectura<br/> | Versión del procesador host.<br/>                                                      |
| [**SerialPorts**](ivmhostinfo-serialports.md)<br/>                                 | Solo lectura<br/> | Los nombres de puerto serie asociados a los puertos serie del host.<br/>                                |
| [**SSE**](ivmhostinfo-sse.md)<br/>                                                 | Solo lectura<br/> | Indica si el procesador admite el conjunto de instrucciones SSE.<br/>                       |
| [**SSE2**](ivmhostinfo-sse2.md)<br/>                                               | Solo lectura<br/> | Indica si el procesador admite el conjunto de instrucciones SSE2.<br/>                      |
| [**ThreeDNow**](ivmhostinfo-threednow.md)<br/>                                     | Solo lectura<br/> | Indica si el procesador admite el conjunto de instrucciones 3DNow.<br/>                     |
| [**HORA UTC**](ivmhostinfo-utctime.md)<br/>                                         | Solo lectura<br/> | Hora UTC en el equipo host.<br/>                                                       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID IVMHostInfo se define como \_ 5b5cf343-05ad-453b-be99-adf4e27b2ebc<br/>                |



 

