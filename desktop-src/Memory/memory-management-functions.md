---
description: 'En este tema se describen las funciones de administración de memoria:'
ms.assetid: 5a2a7a62-0bda-4a0d-93d2-25b4898871fd
title: Funciones de administración de memoria
ms.topic: article
ms.date: 11/06/2018
ms.openlocfilehash: a203583016a127a550f609068df8e86da384fa34
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159845"
---
# <a name="memory-management-functions"></a>Funciones de administración de memoria

- [Funciones de memoria generales](#general-memory-functions)
- [Funciones de prevención de ejecución de datos](#data-execution-prevention-functions)
- [Funciones de asignación de archivos](#file-mapping-functions)
- [Funciones de AWE](#awe-functions)
- [Funciones de montón](#heap-functions)
- [Funciones de memoria virtual](#virtual-memory-functions)
- [Funciones globales y locales](#global-and-local-functions)
- [Funciones de memoria no necesarias](#bad-memory-functions)
- [Funciones de enclave](#enclave-functions)
- [Funciones thunk atl](#atl-thunk-functions)
- [Funciones obsoletas](#obsolete-functions)

## <a name="general-memory-functions"></a>Funciones de memoria generales

| Función | Descripción |
|-|-|
| [**AddSecureMemoryCacheCallback**](/windows/desktop/api/WinBase/nf-winbase-addsecurememorycachecallback) | Registra una función de devolución de llamada a la que se va a llamar cuando se libera un intervalo de memoria protegido o se cambian sus protecciones. |
| [**CopyMemory**](/previous-versions/windows/desktop/legacy/aa366535(v=vs.85)) | Copia un bloque de memoria de una ubicación a otra. |
| [**CreateMemoryResourceNotification**](/windows/win32/api/memoryapi/nf-memoryapi-creatememoryresourcenotification) | Crea un objeto de notificación de recursos de memoria. |
| [**FillMemory**](/previous-versions/windows/desktop/legacy/aa366561(v=vs.85)) | Rellena un bloque de memoria con un valor especificado. |
| [**GetLargePageMinimum**](/windows/win32/api/memoryapi/nf-memoryapi-getlargepageminimum) | Recupera el tamaño mínimo de una página grande. |
| [**GetPhysicallyInstalledSystemMemory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getphysicallyinstalledsystemmemory) | Recupera la cantidad de RAM que está instalada físicamente en el equipo. |
| [**GetSystemFileCacheSize**](/windows/win32/api/memoryapi/nf-memoryapi-getsystemfilecachesize) | Recupera los límites de tamaño actuales para el conjunto de trabajo de la caché del sistema. |
| [**GetWriteWatch**](/windows/win32/api/memoryapi/nf-memoryapi-getwritewatch) | Recupera las direcciones de las páginas que se han escrito en en una región de memoria virtual. |
| [**GlobalMemoryStatusEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex) | Obtiene información sobre el uso actual del sistema de la memoria física y virtual. |
| [**MoveMemory**](/previous-versions/windows/desktop/legacy/aa366788(v=vs.85)) | Mueve un bloque de memoria de una ubicación a otra. |
| [**QueryMemoryResourceNotification**](/windows/win32/api/memoryapi/nf-memoryapi-querymemoryresourcenotification) | Recupera el estado del objeto de recurso de memoria especificado. |
| [**RemoveSecureMemoryCacheCallback**](/windows/desktop/api/WinBase/nf-winbase-removesecurememorycachecallback) | Anula el registro de una función de devolución de llamada que se registró anteriormente con [**la función AddSecureMemoryCacheCallback.**](/windows/desktop/api/WinBase/nf-winbase-addsecurememorycachecallback) |
| [**ResetWriteWatch**](/windows/win32/api/memoryapi/nf-memoryapi-resetwritewatch) | Restablece el estado de seguimiento de escritura para una región de memoria virtual. |
| [**SecureMemoryCacheCallback**](/windows/desktop/api/WinNT/nc-winnt-psecure_memory_cache_callback) | Función definida por la aplicación a la que se llama cuando se libera un intervalo de memoria protegido o se cambian sus protecciones. |
| [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) | Rellena un bloque de memoria con ceros. |
| [**SetSystemFileCacheSize**](/windows/win32/api/memoryapi/nf-memoryapi-setsystemfilecachesize) | Limita el tamaño del conjunto de trabajo para la caché del sistema de archivos. |
| [**ZeroMemory**](/previous-versions/windows/desktop/legacy/aa366920(v=vs.85)) | Rellena un bloque de memoria con ceros. |

## <a name="data-execution-prevention-functions"></a>Funciones de prevención de ejecución de datos

Estas funciones se usan con [prevención de ejecución de datos](data-execution-prevention.md) (DEP).

| Función | Descripción |
|-|-|
| [**GetProcessDEPPolicy**](/windows/desktop/api/WinBase/nf-winbase-getprocessdeppolicy) | Recupera la configuración de DEP de un proceso. |
| [**GetSystemDEPPolicy**](/windows/desktop/api/WinBase/nf-winbase-getsystemdeppolicy) | Recupera la configuración de DEP del sistema. |
| [**SetProcessDEPPolicy**](/windows/desktop/api/WinBase/nf-winbase-setprocessdeppolicy) | Cambia la configuración de DEP de un proceso. |

## <a name="file-mapping-functions"></a>Funciones de asignación de archivos

Estas funciones se usan en la [asignación de archivos](file-mapping.md).

| Función | Descripción |
|-|-|
| [**CreateFileMappingA**](/windows/win32/api/winbase/nf-winbase-createfilemappinga) | Crea o abre un objeto de asignación de archivos con nombre o sin nombre para un archivo especificado. |
| [**CreateFileMappingW**](/windows/win32/api/memoryapi/nf-memoryapi-createfilemappingw) | Crea o abre un objeto de asignación de archivos con nombre o sin nombre para un archivo especificado. |
| [**CreateFileMapping2**](/windows/win32/api/memoryapi/nf-memoryapi-createfilemapping2) | Crea o abre un objeto de asignación de archivos con nombre o sin nombre para un archivo especificado. Puede especificar un nodo NUMA preferido para la memoria física como parámetro extendido; vea el *parámetro ExtendedParameters.* |
| [**CreateFileMappingFromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-createfilemappingfromapp) | Crea o abre un objeto de asignación de archivos con nombre o sin nombre para un archivo especificado desde una Windows Store. |
| [**CreateFileMappingNuma**](/windows/desktop/api/WinBase/nf-winbase-createfilemappingnumaa) | Crea o abre un objeto de asignación de archivos con nombre o sin nombre para un archivo especificado y especifica el nodo NUMA para la memoria física. |
| [**FlushViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-flushviewoffile) | Escribe en el disco un intervalo de bytes dentro de una vista asignada de un archivo. |
| [**GetMappedFileName**](/windows/win32/api/psapi/nf-psapi-getmappedfilenamea) | Comprueba si la dirección especificada está dentro de un archivo asignado a memoria en el espacio de direcciones del proceso especificado. Si es así, la función devuelve el nombre del archivo asignado a la memoria. |
| [**MapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile) | Mapas una vista de una asignación de archivos en el espacio de direcciones de un proceso de llamada. |
| [**MapViewOfFile2**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffile2) | Mapas una vista de un archivo o una sección con copia de seguridad de archivos de paginación en el espacio de direcciones del proceso especificado. |
| [**MapViewOfFile3**](/windows/desktop/api/MemoryApi/nf-memoryapi-mapviewoffile3) | Mapas una vista de un archivo o una sección con copia de seguridad de archivos de paginación en el espacio de direcciones del proceso especificado. |
| [**MapViewOfFile3FromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-mapviewoffile3fromapp) | Mapas una vista de una asignación de archivos en el espacio de direcciones de un proceso de llamada desde una Windows Store. |
| [**MapViewOfFileEx**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffileex) | Mapas una vista de una asignación de archivos en el espacio de direcciones de un proceso de llamada. Opcionalmente, un llamador puede especificar una dirección de memoria sugerida para la vista. |
| [**MapViewOfFileExNuma**](/windows/desktop/api/WinBase/nf-winbase-mapviewoffileexnuma) | Mapas una vista de una asignación de archivos en el espacio de direcciones de un proceso de llamada y especifica el nodo NUMA para la memoria física. |
| [**MapViewOfFileFromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-mapviewoffilefromapp) | Mapas una vista de una asignación de archivos en el espacio de direcciones de un proceso de llamada desde una Windows Store. |
| [**MapViewOfFileNuma2**](/windows/win32/api/memoryapi/nf-memoryapi-mapviewoffilenuma2) | Mapas una vista de un archivo o una sección con copia de seguridad de archivos de paginación en el espacio de direcciones del proceso especificado. |
| [**OpenFileMapping**](/windows/win32/api/winbase/nf-winbase-openfilemappinga) | Abre un objeto de asignación de archivos con nombre. |
| [**OpenFileMappingFromApp**](/windows/win32/api/winbase/nf-winbase-openfilemappingafromapp) | Abre un objeto de asignación de archivos con nombre. |
| [**UnmapViewOfFile**](/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile) | Desasigna una vista asignada de un archivo del espacio de direcciones del proceso de llamada. |
| [**UnmapViewOfFile2**](/windows/win32/api/memoryapi/nf-memoryapi-unmapviewoffile2) | Desasigna una vista previamente asignada de un archivo o una sección con copia de seguridad de archivos de página. |
| [**UnmapViewOfFileEx**](/windows/desktop/api/MemoryApi/nf-memoryapi-unmapviewoffileex) | Desasigna una vista previamente asignada de un archivo o una sección con copia de seguridad de archivos de página. |

## <a name="awe-functions"></a>Funciones de AWE

Estas son las [funciones de AWE.](address-windowing-extensions.md)

| Función | Descripción |
|-|-|
| [**AllocateUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages) | Asigna páginas de memoria física que se asignarán y desasignarán dentro de cualquier región de AWE del proceso. |
| [**AllocateUserPhysicalPagesNuma**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpagesnuma) | Asigna páginas de memoria física que se asignarán y desasignarán dentro de cualquier región AWE del proceso y especifica el nodo NUMA para la memoria física. |
| [**FreeUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-freeuserphysicalpages) | Libera las páginas de memoria física previamente asignadas [**con AllocateUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpages). |
| [**MapUserPhysicalPages**](/windows/win32/api/memoryapi/nf-memoryapi-mapuserphysicalpages) | Mapas páginas de memoria física previamente asignadas en la dirección especificada dentro de una región de AWE. |
| [**MapUserPhysicalPagesScatter**](/windows/desktop/api/WinBase/nf-winbase-mapuserphysicalpagesscatter) | Mapas páginas de memoria física previamente asignadas en la dirección especificada dentro de una región de AWE. |

## <a name="heap-functions"></a>Funciones de montón

Estas son las [funciones del montón](heap-functions.md).

| Función | Descripción |
|-|-|
| [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap) | Obtiene un identificador para el montón del proceso de llamada. |
| [**GetProcessHeaps**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheaps) | Obtiene identificadores para todos los montones que son válidos para el proceso de llamada. |
| [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) | Asigna un bloque de memoria desde un montón. |
| [**HeapCompact**](/windows/desktop/api/HeapApi/nf-heapapi-heapcompact) | Une bloques libres adyacentes de memoria en un montón. |
| [**HeapCreate**](/windows/desktop/api/HeapApi/nf-heapapi-heapcreate) | Crea un objeto de montón. |
| [**HeapDestroy**](/windows/desktop/api/HeapApi/nf-heapapi-heapdestroy) | Destruye el objeto de montón especificado. |
| [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) | Libera un bloque de memoria asignado de un montón. |
| [**HeapLock**](/windows/desktop/api/HeapApi/nf-heapapi-heaplock) | Intenta adquirir el bloqueo asociado a un montón especificado. |
| [**HeapQueryInformation**](/windows/desktop/api/HeapApi/nf-heapapi-heapqueryinformation) | Recupera información sobre el montón especificado. |
| [**HeapReAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heaprealloc) | Asigna un bloque de memoria de un montón. |
| [**HeapSetInformation**](/windows/desktop/api/HeapApi/nf-heapapi-heapsetinformation) | Establece la información del montón para el montón especificado. |
| [**HeapSize**](/windows/desktop/api/HeapApi/nf-heapapi-heapsize) | Recupera el tamaño de un bloque de memoria asignado desde un montón. |
| [**HeapUnlock**](/windows/desktop/api/HeapApi/nf-heapapi-heapunlock) | Libera la propiedad del bloqueo asociado a un montón especificado. |
| [**HeapValidate**](/windows/desktop/api/HeapApi/nf-heapapi-heapvalidate) | Intenta validar un montón especificado. |
| [**HeapWalk**](/windows/desktop/api/HeapApi/nf-heapapi-heapwalk) | Enumera los bloques de memoria de un montón especificado. |

## <a name="virtual-memory-functions"></a>Funciones de memoria virtual

Estas son las [funciones de memoria virtual](virtual-memory-functions.md).

| Función | Descripción |
|-|-|
| [**DiscardVirtualMemory**](/windows/win32/api/memoryapi/nf-memoryapi-discardvirtualmemory) | Descarta el contenido de memoria de un intervalo de páginas de memoria, sin desacomprimir la memoria. El contenido de la memoria descartada no está definido y la aplicación debe volver a escribirlo. |
| [**OfferVirtualMemory**](/windows/win32/api/memoryapi/nf-memoryapi-offervirtualmemory) | Indica que la aplicación ya no necesita los datos contenidos en un intervalo de páginas de memoria y que el sistema puede descartarlos si es necesario. |
| [**Captura previaVirtualMemory**](/windows/win32/api/memoryapi/nf-memoryapi-prefetchvirtualmemory) | Captura previamente los intervalos de direcciones virtuales en la memoria física. |
| [**QueryVirtualMemoryInformation**](/windows/desktop/api/MemoryApi/nf-memoryapi-queryvirtualmemoryinformation) | Devuelve información sobre una página o un conjunto de páginas dentro del espacio de direcciones virtuales del proceso especificado. |
| [**ReclaimVirtualMemory**](/windows/win32/api/memoryapi/nf-memoryapi-reclaimvirtualmemory) | Reclama un intervalo de páginas de memoria que se ofrecían al sistema [**con OfferVirtualMemory**](/windows/win32/api/memoryapi/nf-memoryapi-offervirtualmemory). |
| [**SetProcessValidCallTargets**](/windows/desktop/api/MemoryApi/nf-memoryapi-setprocessvalidcalltargets) | Proporciona CFG con una lista de destinos de llamadas indirectas válidos y especifica si deben marcarse como válidos o no. |
| [**VirtualAlloc**](/windows/desktop/api/MemoryApi/nf-memoryapi-virtualalloc) | Reserva o confirma una región de páginas en el espacio de direcciones virtuales del proceso de llamada. |
| [**VirtualAlloc2**](/windows/desktop/api/MemoryApi/nf-memoryapi-virtualalloc2) | Reserva, confirma o cambia el estado de una región de memoria dentro del espacio de direcciones virtuales de un proceso especificado. La función inicializa la memoria que asigna a cero. |
| [**VirtualAlloc2FromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-virtualallocfromapp) | Reserva, confirma o cambia el estado de una región de páginas en el espacio de direcciones virtuales del proceso de llamada. La memoria asignada por esta función se inicializa automáticamente en cero. |
| [**VirtualAllocEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocex) | Reserva o confirma una región de páginas en el espacio de direcciones virtuales del proceso especificado. |
| [**VirtualAllocExNuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma) | Reserva o confirma una región de memoria dentro del espacio de direcciones virtuales del proceso especificado y especifica el nodo NUMA para la memoria física. |
| [**VirtualAllocFromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-virtualallocfromapp) | Reserva, confirma o cambia el estado de una región de páginas en el espacio de direcciones virtuales del proceso de llamada. La memoria asignada por esta función se inicializa automáticamente en cero. |
| [**VirtualFree**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) | Libera o desacomprime una región de páginas dentro del espacio de direcciones virtuales del proceso de llamada. |
| [**VirtualFreeEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfreeex) | Libera o desacomprime una región de memoria dentro del espacio de direcciones virtuales de un proceso especificado. |
| [**VirtualLock**](/windows/win32/api/memoryapi/nf-memoryapi-virtuallock) | Bloquea la región especificada del espacio de direcciones virtuales del proceso en la memoria física. |
| [**VirtualProtect**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotect) | Cambia la protección de acceso en una región de páginas confirmadas en el espacio de direcciones virtuales del proceso de llamada. |
| [**VirtualProtectEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualprotectex) | Cambia la protección de acceso en una región de páginas confirmadas en el espacio de direcciones virtuales del proceso de llamada. |
| [**VirtualProtectFromApp**](/windows/desktop/api/MemoryApi/nf-memoryapi-virtualprotectfromapp) | Cambia la protección en una región de páginas confirmadas en el espacio de direcciones virtuales del proceso de llamada. |
| [**VirtualQuery**](/windows/win32/api/memoryapi/nf-memoryapi-virtualquery) | Proporciona información sobre un intervalo de páginas en el espacio de direcciones virtuales del proceso de llamada. |
| [**VirtualQueryEx**](/windows/win32/api/memoryapi/nf-memoryapi-virtualqueryex) | Proporciona información sobre un intervalo de páginas en el espacio de direcciones virtuales del proceso de llamada. |
| [**VirtualUnlock**](/windows/win32/api/memoryapi/nf-memoryapi-virtualunlock) | Desbloquea un intervalo especificado de páginas en el espacio de direcciones virtuales de un proceso. |

## <a name="global-and-local-functions"></a>Funciones globales y locales

Consulte también funciones [globales y locales.](global-and-local-functions.md) Estas funciones se proporcionan por compatibilidad con objetos de Windows de 16 bits y se usan con datos dinámicos Exchange (DDE), las funciones del Portapapeles y los objetos de datos OLE. A menos que la documentación indique específicamente que se debe [](heap-functions.md) usar una función global o local, las nuevas aplicaciones deben usar la función de montón correspondiente con el identificador devuelto por [**GetProcessHeap**](/windows/desktop/api/HeapApi/nf-heapapi-getprocessheap). Para obtener una funcionalidad equivalente a la función global o local, establezca el parámetro *dwFlags* de la función del montón en 0.

| Función | Descripción | Función de montón correspondiente |
|-|-|-|
| [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc), [ **LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) | Asigna el número especificado de bytes del montón. | [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) |
| [**GlobalDiscard,**](/windows/desktop/api/WinBase/nf-winbase-globaldiscard) [ **LocalDiscard**](/windows/win32/api/minwinbase/nf-minwinbase-localdiscard) | Descarta el bloque de memoria global especificado. | No aplicable. |
| [**GlobalFlags**](/windows/desktop/api/WinBase/nf-winbase-globalflags), [ **LocalFlags**](/windows/desktop/api/WinBase/nf-winbase-localflags) | Devuelve información sobre el objeto de memoria global especificado. | No aplicable. Use [**HeapValidate para**](/windows/desktop/api/HeapApi/nf-heapapi-heapvalidate) validar el montón. |
| [**GlobalFree**](/windows/desktop/api/WinBase/nf-winbase-globalfree), [ **LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree) | Libera el objeto de memoria global especificado. | [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) |
| [**GlobalHandle**](/windows/desktop/api/WinBase/nf-winbase-globalhandle), [ **LocalHandle**](/windows/desktop/api/WinBase/nf-winbase-localhandle) | Recupera el identificador asociado al puntero especificado a un bloque de memoria global. Esta función solo debe usarse con funciones OLE y del Portapapeles que la requieran. | No aplicable. |
| [**GlobalLock**](/windows/desktop/api/WinBase/nf-winbase-globallock), [ **LocalLock**](/windows/desktop/api/WinBase/nf-winbase-locallock) | Bloquea un objeto de memoria global y devuelve un puntero al primer byte del bloque de memoria del objeto. | No aplicable. |
| [**GlobalReAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalrealloc), [ **LocalReAlloc**](/windows/desktop/api/WinBase/nf-winbase-localrealloc) | Cambia el tamaño o los atributos de un objeto de memoria global especificado. | [**HeapReAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heaprealloc) |
| [**GlobalSize**](/windows/desktop/api/WinBase/nf-winbase-globalsize), [ **LocalSize**](/windows/desktop/api/WinBase/nf-winbase-localsize) | Recupera el tamaño actual del objeto de memoria global especificado. | [**HeapSize**](/windows/desktop/api/HeapApi/nf-heapapi-heapsize) |
| [**GlobalUnlock**](/windows/desktop/api/WinBase/nf-winbase-globalunlock), [ **LocalUnlock**](/windows/desktop/api/WinBase/nf-winbase-localunlock) | Disminuye el número de bloqueos asociado a un objeto de memoria. Esta función solo debe usarse con funciones OLE y del Portapapeles que la requieran. | No aplicable. |

## <a name="bad-memory-functions"></a>Funciones de memoria no necesarias

| Función | Descripción |
|-|-|
| [**BadMemoryCallbackRoutine**](/previous-versions/windows/desktop/legacy/hh691011(v=vs.85)) | Función definida por la aplicación registrada con la función [**RegisterBadMemoryNotification**](/windows/win32/api/memoryapi/nf-memoryapi-registerbadmemorynotification) a la que se llama cuando se detecta una o varias páginas de memoria no correctas. |
| [**GetMemoryErrorHandlingCapabilities**](/windows/win32/api/memoryapi/nf-memoryapi-getmemoryerrorhandlingcapabilities) | Obtiene las funcionalidades de control de errores de memoria del sistema. |
| [**RegisterBadMemoryNotification**](/windows/win32/api/memoryapi/nf-memoryapi-registerbadmemorynotification) | Registra una notificación de memoria no detectada a la que se llama cuando se detectan una o varias páginas de memoria no buena. |
| [**UnregisterBadMemoryNotification**](/windows/win32/api/memoryapi/nf-memoryapi-unregisterbadmemorynotification) | Cierra el identificador de notificación de memoria no disponible especificado. |

## <a name="enclave-functions"></a>Funciones de enclave

| Función | Descripción |
|-|-|
| [**CreateEnclave**](/windows/desktop/api/enclaveapi/nf-enclaveapi-createenclave) | Crea un nuevo enclave sin inicializar. Un enclave es una región aislada de código y datos dentro del espacio de direcciones de una aplicación. Solo el código que se ejecuta dentro del enclave puede acceder a los datos dentro del mismo enclave. |
| [**InitializeEnclave**](/windows/desktop/api/enclaveapi/nf-enclaveapi-initializeenclave) | Inicializa un enclave que creó y cargó con datos. |
| [**IsEnclaveTypeSupported**](/windows/desktop/api/enclaveapi/nf-enclaveapi-isenclavetypesupported) | Recupera si se admite el tipo de enclave especificado. |
| [**LoadEnclaveData**](/windows/desktop/api/enclaveapi/nf-enclaveapi-loadenclavedata) | Carga los datos en un enclave sin inicializar que creó mediante una llamada [**a CreateEnclave.**](/windows/desktop/api/enclaveapi/nf-enclaveapi-createenclave) |

## <a name="atl-thunk-functions"></a>Funciones thunk atl

| Función | Descripción |
|-|-|
| [**AtlThunk_AllocateData**](/windows/desktop/api/atlthunk/nf-atlthunk-atlthunk_allocatedata) | Asigna espacio en memoria para un thunk ATL. |
| [**AtlThunk_DataToCode**](/windows/desktop/api/atlthunk/nf-atlthunk-atlthunk_datatocode) | Devuelve una función ejecutable correspondiente al parámetro AtlThunkData_t. |
| [**AtlThunk_FreeData**](/windows/desktop/api/atlthunk/nf-atlthunk-atlthunk_freedata) | Libera la memoria asociada a un código thunk ATL. |
| [**AtlThunk_InitData**](/windows/desktop/api/atlthunk/nf-atlthunk-atlthunk_initdata) | Inicializa un código thunk atl. |

## <a name="obsolete-functions"></a>Funciones obsoletas

Estas funciones solo se proporcionan para la compatibilidad con versiones de 16 bits de Windows:

- [**IsBadCodePtr**](/windows/desktop/api/WinBase/nf-winbase-isbadcodeptr)
- [**IsBadReadPtr**](/windows/desktop/api/WinBase/nf-winbase-isbadreadptr)
- [**IsBadStringPtr**](/windows/desktop/api/WinBase/nf-winbase-isbadstringptra)
- [**IsBadWritePtr**](/windows/desktop/api/WinBase/nf-winbase-isbadwriteptr)

La función siguiente puede devolver información incorrecta y no debe usarse. En su lugar, [**use la función GlobalMemoryStatusEx.**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-globalmemorystatusex)

- [**GlobalMemoryStatus**](/windows/desktop/api/WinBase/nf-winbase-globalmemorystatus)