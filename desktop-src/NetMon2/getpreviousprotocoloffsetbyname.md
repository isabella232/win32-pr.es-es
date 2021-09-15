---
description: La función GetPreviousProtocolOffsetByName devuelve la instancia anterior de un protocolo determinado.
ms.assetid: 94f80776-564f-4089-9e3a-fdf38d9dfe8a
title: Función GetPreviousProtocolOffsetByName (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPreviousProtocolOffsetByName
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2720d309224def5f368babf4f9ace85955907347
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476753"
---
# <a name="getpreviousprotocoloffsetbyname-function"></a>Función GetPreviousProtocolOffsetByName

La **función GetPreviousProtocolOffsetByName** devuelve la instancia anterior de un protocolo determinado.

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI GetPreviousProtocolOffsetByName(
  _In_  HFRAME hFrame,
  _In_  DWORD  dwStartOffset,
  _In_  LPSTR  szProtocolName,
  _Out_ DWORD  *pdwPreviousOffset
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hFrame* \[ En\]
</dt> <dd>

Identificador del marco.

</dd> <dt>

*dwStartOffset* \[ En\]
</dt> <dd>

Desplazamiento en el marco.

</dd> <dt>

*szProtocolName* \[ En\]
</dt> <dd>

Nombre del protocolo que desea buscar.

</dd> <dt>

*pdwPreviousOffset* \[ out\]
</dt> <dd>

Puntero a un **DWORD** que contiene el desplazamiento al protocolo anterior (si la función se realiza correctamente).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NMERR \_ SUCCESS.

Si la función no se realiza correctamente, el valor devuelto es NMERR \_ PROTOCOL \_ NOT \_ FOUND.

## <a name="remarks"></a>Observaciones

[*Los*](e.md) expertos [*y analizadores*](p.md) pueden llamar a **GetPreviousProtocolOffsetByName**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




