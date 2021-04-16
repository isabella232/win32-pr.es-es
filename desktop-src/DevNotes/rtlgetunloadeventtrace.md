---
description: Permite al código de volcado obtener la información de módulo descargada de Ntdll.dll para el almacenamiento en el minivolcado.
ms.assetid: 017398da-e13e-4261-bda5-6f400a91dbe3
title: RtlGetUnloadEventTrace función)
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
ms.openlocfilehash: 9297ba0019c89c5e93961d4b36e0fe16da04d6bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649999"
---
# <a name="rtlgetunloadeventtrace-function"></a>RtlGetUnloadEventTrace función)

\[Esta función se puede cambiar o quitar de Windows sin previo aviso.\]

Permite al código de volcado obtener la información de módulo descargada de Ntdll.dll para el almacenamiento en el minivolcado.

## <a name="syntax"></a>Sintaxis


```C++
 PRTL_UNLOAD_EVENT_TRACE RtlGetUnloadEventTrace(void);
```



## <a name="parameters"></a>Parámetros

Esta función no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Esta función devuelve un puntero a una matriz. Para obtener más información, vea la sección Comentarios.

## <a name="remarks"></a>Observaciones

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

Esta función no tiene ningún archivo de encabezado asociado. La biblioteca de importación asociada, ntdll. lib, está disponible en el kit de controladores de Windows (WDK). También puede llamar a esta función mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|--------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
