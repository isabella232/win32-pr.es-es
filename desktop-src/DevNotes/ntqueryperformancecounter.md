---
description: Devuelve el valor actual de un contador de rendimiento y, opcionalmente, la frecuencia del contador de rendimiento.
ms.assetid: ab8973b7-a358-4e50-85e8-9dbff4e67010
title: NtQueryPerformanceCounter función)
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
ms.openlocfilehash: 5bf0aad74f6992212fb3b2238b3030c68cda2fc6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670625"
---
# <a name="ntqueryperformancecounter-function"></a>NtQueryPerformanceCounter función)

\[Esta función no se admite y no debe usarse. En su lugar, use las funciones **QueryPerformanceCounter** y **QueryPerformanceFrequency** .\]

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

*PerformanceCounter* \[ enuncia\]
</dt> <dd>

Dirección de una variable para recibir el valor del contador de rendimiento actual.

</dd> <dt>

*PerformanceFrequency* \[ out, opcional\]
</dt> <dd>

Dirección de una variable que va a recibir la frecuencia del contador de rendimiento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, devuelve el estado del código de **NTSTATUS** **\_ Success**; de lo contrario, devuelve un código de error como **\_ \_ infracción de acceso de estado**.

## <a name="remarks"></a>Observaciones

No hay ningún archivo de encabezado disponible para **NtQueryPerformanceCounter**. Debe utilizar las funciones alternativas mencionadas anteriormente, aunque también puede usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Ntdll.dll.

La frecuencia de rendimiento es la frecuencia del contador de rendimiento en hercios, en concreto en recuentos por segundo. Este valor depende de la implementación. Si la implementación no tiene hardware para admitir el tiempo de rendimiento, el valor devuelto es 0.

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

 

 
