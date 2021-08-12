---
description: Devuelve el valor actual de un contador de rendimiento y, opcionalmente, la frecuencia del contador de rendimiento.
ms.assetid: ab8973b7-a358-4e50-85e8-9dbff4e67010
title: Función NtQueryPerformanceCounter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NtQueryPerformanceCounter
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 9c92863adbc0865700dad272bbc299e1f1a667b2fd4afbcd75d548e3330890b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667232"
---
# <a name="ntqueryperformancecounter-function"></a>Función NtQueryPerformanceCounter

\[Esta función no se admite y no se debe usar. Use las **funciones QueryPerformanceCounter y** **QueryPerformanceFrequency en** su lugar.\]

Devuelve el valor actual de un contador de rendimiento y, opcionalmente, la frecuencia del contador de rendimiento.

## <a name="syntax"></a>Sintaxis


```C++
NTSTATUS NtQueryPerformanceCounter(
  _Out_     PLARGE_INTEGER PerformanceCounter,
  _Out_opt_ PLARGE_INTEGER PerformanceFrequency
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PerformanceCounter* \[ out\]
</dt> <dd>

Dirección de una variable para recibir el valor del contador de rendimiento actual.

</dd> <dt>

*RendimientoFrequency* \[ out, opcional\]
</dt> <dd>

Dirección de una variable para recibir la frecuencia del contador de rendimiento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, devuelve el código **NTSTATUS STATUS** **\_ SUCCESS;** de lo contrario, devuelve un código de error como **STATUS ACCESS \_ \_ VIOLATION**.

## <a name="remarks"></a>Observaciones

No hay ningún archivo de encabezado disponible **para NtQueryPerformanceCounter**. Debe usar las funciones alternativas mencionadas anteriormente, aunque también puede usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Ntdll.dll.

Frecuencia de rendimiento es la frecuencia del contador de rendimiento en hercios, específicamente en recuentos por segundo. Este valor depende de la implementación. Si la implementación no tiene hardware para admitir el tiempo de rendimiento, el valor devuelto es 0.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|--------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter)
</dt> <dt>

[**QueryPerformanceFrequency**](/windows/win32/api/profileapi/nf-profileapi-queryperformancefrequency)
</dt> </dl>

 

 
