---
description: Multiplica los enteros extendidos.
ms.assetid: 6a59d211-4baf-4c7c-af2a-ffb0c5773445
title: Función RtlExtendedIntegerMultiply
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
ms.openlocfilehash: 0048da80026029274a89d089f5c232311a481a6010c0aad32d8b1a6ae6cc6786
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571475"
---
# <a name="rtlextendedintegermultiply-function"></a>Función RtlExtendedIntegerMultiply

\[La **función RtlExtendedIntegerMultiply** se exporta para admitir archivos binarios de controlador existentes y está obsoleta. Para mejorar el rendimiento, use la compatibilidad del compilador con operaciones de enteros de 64 bits.\]

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

*Multiplicando* \[ En\]
</dt> <dd>

Multiplicando.

</dd> <dt>

*Multiplicador* \[ En\]
</dt> <dd>

Multiplicador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el resultado de multiplicación.

## <a name="remarks"></a>Comentarios

Esta función no tiene asociada la biblioteca de importación ni el archivo de encabezado; Debe llamarlo mediante las [**funciones LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**y GetProcAddress.**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|--------------------------------------------------------------------------------------|
| Archivo DLL<br/> | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
