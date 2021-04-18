---
description: Divide los enteros extendidos.
ms.assetid: d46f65f0-6c41-4cb2-9882-5b11f7aae3ca
title: RtlExtendedLargeIntegerDivide función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlExtendedLargeIntegerDivide
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: b17c89a744748214d74dc24abdaa8a12ac71e960
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671272"
---
# <a name="rtlextendedlargeintegerdivide-function"></a>RtlExtendedLargeIntegerDivide función)

\[La función **RtlExtendedLargeIntegerDivide** se exporta para admitir los archivos binarios del controlador existentes y está obsoleto. Para mejorar el rendimiento, use la compatibilidad del compilador con las operaciones de enteros de 64 bits.\]

Divide los enteros extendidos.

## <a name="syntax"></a>Sintaxis


```C++
LARGE_INTEGER RtlExtendedLargeIntegerDivide(
  _In_    LARGE_INTEGER Dividend,
  _In_    ULONG         Divisor,
  _Inout_ PULONG        Remainder
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Dividendo* \[ de\]
</dt> <dd>

Divi.

</dd> <dt>

*Divisor* \[ de\]
</dt> <dd>

Divisor.

</dd> <dt>

*Resto* \[ in, out\]
</dt> <dd>

Puntero al resto de la división.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el resultado de la operación de división.

## <a name="remarks"></a>Observaciones

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|--------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
