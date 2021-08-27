---
description: Permite que el código de volcado obtenga la información del módulo descargado Ntdll.dll para el almacenamiento en el minivolfón.
ms.assetid: 017398da-e13e-4261-bda5-6f400a91dbe3
title: Función RtlGetUnloadEventTrace
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetUnloadEventTrace
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: d8575610ab34b62c9228f87fa64fbd6a40fa0201b7fe1a70ab95c7daae706854
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058595"
---
# <a name="rtlgetunloadeventtrace-function"></a>Función RtlGetUnloadEventTrace

\[Esta función se puede cambiar o quitar de Windows sin previo aviso.\]

Permite que el código de volcado obtenga la información del módulo descargado Ntdll.dll para el almacenamiento en el minivolfón.

## <a name="syntax"></a>Sintaxis


```C++
 PRTL_UNLOAD_EVENT_TRACE RtlGetUnloadEventTrace(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Esta función devuelve un puntero a una matriz. Para obtener más información, vea la sección Comentarios.

## <a name="remarks"></a>Comentarios

La matriz RtlpUnloadEventTrace se define de la siguiente manera:

``` syntax
#define RTL_UNLOAD_EVENT_TRACE_NUMBER 64

typedef struct _RTL_UNLOAD_EVENT_TRACE {
    PVOID BaseAddress;   // Base address of dll
    SIZE_T SizeOfImage;  // Size of image
    ULONG Sequence;      // Sequence number for this event
    ULONG TimeDateStamp; // Time and date of image
    ULONG CheckSum;      // Image checksum
    WCHAR ImageName[32]; // Image name
} RTL_UNLOAD_EVENT_TRACE, *PRTL_UNLOAD_EVENT_TRACE;

RTL_UNLOAD_EVENT_TRACE RtlpUnloadEventTrace[RTL_UNLOAD_EVENT_TRACE_NUMBER];
```

Esta función no tiene ningún archivo de encabezado asociado. La biblioteca de importación asociada, Ntdll.lib, está disponible en Windows Driver Kit (WDK). También puede llamar a esta función mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|--------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
