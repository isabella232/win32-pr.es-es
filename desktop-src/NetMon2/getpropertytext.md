---
description: La función GetPropertyText devuelve un puntero al texto de la propiedad.
ms.assetid: 1bcbdbb8-4ec5-4cea-a1c6-4a1f37476f50
title: Función GetPropertyText (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPropertyText
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 10dbabf32840d2ae5f965687a6261b8bec27a1a1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171449"
---
# <a name="getpropertytext-function"></a>Función GetPropertyText

La **función GetPropertyText** devuelve un puntero al texto de la propiedad.

## <a name="syntax"></a>Sintaxis


```C++
LPSTR WINAPI GetPropertyText(
  _In_ HFRAME         hFrame,
  _In_ LPPROPERTYINST lpPI,
  _In_ LPSTR          szBuffer,
  _In_ DWORD          BufferSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hFrame* \[ En\]
</dt> <dd>

Identificador del marco.

</dd> <dt>

*lpPI* \[ En\]
</dt> <dd>

Puntero a una instancia de propiedad.

</dd> <dt>

*szBuffer* \[ En\]
</dt> <dd>

Puntero a la cadena de texto de propiedad.

</dd> <dt>

*BufferSize* \[ En\]
</dt> <dd>

Tamaño del búfer de cadena de texto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un puntero al texto de la propiedad.

Si la función no se realiza correctamente, el valor devuelto es **NULL.**

## <a name="remarks"></a>Observaciones

[*Los*](e.md) expertos [*y analizadores pueden*](p.md) llamar a **la función GetPropertyText.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




