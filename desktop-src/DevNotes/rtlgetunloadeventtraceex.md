---
description: Recupera el tamaño y la ubicación de la lista de módulos descargados dinámicamente para el proceso actual.
ms.assetid: 53ac9a7f-aa4a-412d-a6f7-a3a73bede5c2
title: RtlGetUnloadEventTraceEx función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetUnloadEventTraceEx
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 05b9e076041d0cd2298799970670478e9d358d32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671361"
---
# <a name="rtlgetunloadeventtraceex-function"></a>RtlGetUnloadEventTraceEx función)

Recupera el tamaño y la ubicación de la lista de módulos descargados dinámicamente para el proceso actual.

## <a name="syntax"></a>Sintaxis


```C++
VOID WINAPI RtlGetUnloadEventTraceEx(
  _Out_ PULONG *ElementSize,
  _Out_ PULONG *ElementCount,
  _Out_ PVOID  *EventTrace
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Elementos de elemento* \[ enuncia\]
</dt> <dd>

Puntero a una variable que contiene el tamaño de un elemento de la lista.

</dd> <dt>

*ElementCount* \[ enuncia\]
</dt> <dd>

Puntero a una variable que contiene el número de elementos de la lista.

</dd> <dt>

*Eventtracer* \[ enuncia\]
</dt> <dd>

Puntero a una matriz de estructuras **de \_ \_ \_ seguimiento de eventos de la descarga RTL** . Para obtener más información, vea la sección Comentarios.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El cargador almacena la información de eventos descargados en ubicaciones que se pueden leer en los procesos aprovechando el hecho de que Ntdll.dll se carga en la misma dirección base en todos los procesos. Cuando un depurador necesita consultar información de módulo descargada, llama a esta función para determinar la dirección en la que residen las variables y, a continuación, consulta la memoria virtual en el proceso de destino en esas direcciones para leer los valores reales.

Cada elemento de la lista se define de la siguiente manera.

``` syntax
typedef struct _RTL_UNLOAD_EVENT_TRACE {
    PVOID BaseAddress;   // Base address of dll
    SIZE_T SizeOfImage;  // Size of image
    ULONG Sequence;      // Sequence number for this event
    ULONG TimeDateStamp; // Time and date of image
    ULONG CheckSum;      // Image checksum
    WCHAR ImageName[32]; // Image name
} RTL_UNLOAD_EVENT_TRACE, *PRTL_UNLOAD_EVENT_TRACE;
```

Esta función no tiene ningún archivo de encabezado asociado. La biblioteca de importación asociada, ntdll. lib, está disponible en el kit de controladores de Windows (WDK). También puede llamar a esta función mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|--------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
