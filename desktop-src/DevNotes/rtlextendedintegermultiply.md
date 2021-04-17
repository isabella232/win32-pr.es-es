---
description: Multiplica los enteros extendidos.
ms.assetid: 6a59d211-4baf-4c7c-af2a-ffb0c5773445
title: RtlExtendedIntegerMultiply función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlExtendedIntegerMultiply
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 8b824080c28da3265be6dc0333f236b8c9a4cbaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670699"
---
# <a name="rtlextendedintegermultiply-function"></a>RtlExtendedIntegerMultiply función)

\[La función **RtlExtendedIntegerMultiply** se exporta para admitir los archivos binarios del controlador existentes y está obsoleto. Para mejorar el rendimiento, use la compatibilidad del compilador con las operaciones de enteros de 64 bits.\]

Multiplica los enteros extendidos.

## <a name="syntax"></a>Sintaxis


```C++
LARGE_INTEGER RtlExtendedIntegerMultiply(
  _In_ LARGE_INTEGER Multiplicand,
  _In_ LONG          Multiplier
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Multiplicando* \[ de\]
</dt> <dd>

Multiplicando.

</dd> <dt>

*Multiplicador* \[ de\]
</dt> <dd>

Multiplicador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el resultado de multiplicación.

## <a name="remarks"></a>Observaciones

Esta función no tiene asociado ningún archivo de encabezado o biblioteca de importación. debe llamarlo mediante las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------|--------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
