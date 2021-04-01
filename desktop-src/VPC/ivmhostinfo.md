---
title: Interfaz IVMHostInfo (VPCCOMInterfaces. h)
description: Recupera información sobre el equipo host. Se devuelve un objeto IVMHostInfo de la propiedad IVMVirtualPC HostInfo.
ms.assetid: f30fa377-2067-4e03-bc6e-2ada62fc56b4
keywords:
- Interfaz IVMHostInfo Virtual PC
- Interfaz IVMHostInfo Virtual PC, descripción
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
ms.openlocfilehash: d4ca5f296dd4a7437ea136dbaee0d04c68a93efc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150250"
---
# <a name="ivmhostinfo-interface"></a>Interfaz IVMHostInfo

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera información sobre el equipo host. Se devuelve un objeto **IVMHostInfo** de la propiedad [**IVMVirtualPC:: HostInfo**](ivmvirtualpc-hostinfo.md) .

## <a name="members"></a>Miembros

La interfaz **IVMHostInfo** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **IVMHostInfo** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La interfaz **IVMHostInfo** tiene estas propiedades.



| Propiedad                                                                                  | Tipo de acceso          | Descripción                                                                                        |
|:------------------------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------|
| [**DVDDrives**](ivmhostinfo-dvddrives.md)<br/>                                     | Solo lectura<br/> | Las letras de unidad asociadas a los dispositivos de CD y DVD del host.<br/>                              |
| [**FloppyDrives**](ivmhostinfo-floppydrives.md)<br/>                               | Solo lectura<br/> | Las letras de unidad asociadas a las unidades de disquete del host.<br/>                                   |
| [**LogicalProcessorCount**](ivmhostinfo-logicalprocessorcount.md)<br/>             | Solo lectura<br/> | El número de procesadores lógicos en el equipo host.<br/>                                   |
| [**Memory**](ivmhostinfo-memory.md)<br/>                                           | Solo lectura<br/> | La cantidad total de memoria física en el equipo host, en megabytes.<br/>                  |
| [**MemoryAvail**](ivmhostinfo-memoryavail.md)<br/>                                 | Solo lectura<br/> | La cantidad de memoria física disponible en el equipo host, en megabytes.<br/>              |
| [**MemoryAvailString**](ivmhostinfo-memoryavailstring.md)<br/>                     | Solo lectura<br/> | La cantidad de memoria física disponible en el equipo host, en megabytes, como una cadena.<br/> |
| [**MemoryTotalString**](ivmhostinfo-memorytotalstring.md)<br/>                     | Solo lectura<br/> | La cantidad total de memoria física en el equipo host, en megabytes, como una cadena.<br/>     |
| [**MMX**](ivmhostinfo-mmx.md)<br/>                                                 | Solo lectura<br/> | Indica si el procesador admite el conjunto de instrucciones MMX.<br/>                       |
| [**Adaptadores**](ivmhostinfo-networkadapters.md)<br/>                         | Solo lectura<br/> | Colección enumerable de NIC en el equipo host.<br/>                                   |
| [**NetworkAddresses**](ivmhostinfo-networkaddresses.md)<br/>                       | Solo lectura<br/> | Colección enumerable de direcciones TCP/IP en el equipo host.<br/>                       |
| [**Identifica**](ivmhostinfo-operatingsystem.md)<br/>                         | Solo lectura<br/> | El sistema operativo que se ejecuta en el equipo host.<br/>                                       |
| [**OSMajorVersion**](ivmhostinfo-osmajorversion.md)<br/>                           | Solo lectura<br/> | La versión principal del sistema operativo que se ejecuta en el equipo host.<br/>                  |
| [**OSMinorVersion**](ivmhostinfo-osminorversion.md)<br/>                           | Solo lectura<br/> | Versión secundaria del sistema operativo que se ejecuta en el equipo host.<br/>                  |
| [**OSServicePackString**](ivmhostinfo-osservicepackstring.md)<br/>                 | Solo lectura<br/> | La información Service Pack del sistema operativo que se ejecuta en el equipo host.<br/>       |
| [**OSVersionString**](ivmhostinfo-osversionstring.md)<br/>                         | Solo lectura<br/> | La versión del sistema operativo que se ejecuta en el equipo host.<br/>                               |
| [**ParallelPort**](ivmhostinfo-parallelport.md)<br/>                               | Solo lectura<br/> | El puerto paralelo del host que se puede adjuntar al invitado.<br/>                               |
| [**PhysicalProcessorCount**](ivmhostinfo-physicalprocessorcount.md)<br/>           | Solo lectura<br/> | El número de procesadores físicos en el equipo host.<br/>                                  |
| [**ProcessorFeaturesString**](ivmhostinfo-processorfeaturesstring.md)<br/>         | Solo lectura<br/> | Lista de características admitidas por el procesador del host.<br/>                                   |
| [**ProcessorManufacturerString**](ivmhostinfo-processormanufacturerstring.md)<br/> | Solo lectura<br/> | Fabricante del procesador del host.<br/>                                                 |
| [**Velocidaddeprocesador**](ivmhostinfo-processorspeed.md)<br/>                           | Solo lectura<br/> | La velocidad del procesador del host, en megahercios (MHz) o gigahercios (GHz).<br/>                 |
| [**ProcessorSpeedString**](ivmhostinfo-processorspeedstring.md)<br/>               | Solo lectura<br/> | La velocidad del procesador del host, en megahercios o gigahercios, como una cadena.<br/>                |
| [**ProcessorVersionString**](ivmhostinfo-processorversionstring.md)<br/>           | Solo lectura<br/> | Versión del procesador del host.<br/>                                                      |
| [**SerialPorts**](ivmhostinfo-serialports.md)<br/>                                 | Solo lectura<br/> | Los nombres de puerto serie asociados a los puertos serie del host.<br/>                                |
| [**SSE**](ivmhostinfo-sse.md)<br/>                                                 | Solo lectura<br/> | Indica si el procesador admite el conjunto de instrucciones SSE.<br/>                       |
| [**SSE2**](ivmhostinfo-sse2.md)<br/>                                               | Solo lectura<br/> | Indica si el procesador admite el conjunto de instrucciones SSE2.<br/>                      |
| [**ThreeDNow**](ivmhostinfo-threednow.md)<br/>                                     | Solo lectura<br/> | Indica si el procesador admite el conjunto de instrucciones 3DNow.<br/>                     |
| [**UTCTime**](ivmhostinfo-utctime.md)<br/>                                         | Solo lectura<br/> | La hora UTC en el equipo host.<br/>                                                       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHostInfo se define como 5b5cf343-05ad-453b-be99-adf4e27b2ebc<br/>                |



 

