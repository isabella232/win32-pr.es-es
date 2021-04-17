---
description: La función GetPreviousProtocolOffsetByName devuelve la instancia anterior de un protocolo determinado.
ms.assetid: 94f80776-564f-4089-9e3a-fdf38d9dfe8a
title: Función GetPreviousProtocolOffsetByName (Netmon. h)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677277"
---
# <a name="getpreviousprotocoloffsetbyname-function"></a>GetPreviousProtocolOffsetByName función)

La función **GetPreviousProtocolOffsetByName** devuelve la instancia anterior de un protocolo determinado.

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

*hFrame* \[ de\]
</dt> <dd>

Identificador del marco.

</dd> <dt>

*dwStartOffset* \[ de\]
</dt> <dd>

Desplazamiento en el marco.

</dd> <dt>

*szProtocolName* \[ de\]
</dt> <dd>

Nombre del protocolo que desea buscar.

</dd> <dt>

*pdwPreviousOffset* \[ enuncia\]
</dt> <dd>

Puntero a un **valor DWORD** que contiene el desplazamiento al protocolo anterior (si la función se ejecuta correctamente).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.

Si la función no se realiza correctamente, el valor devuelto es el \_ Protocolo NMERR \_ no \_ encontrado.

## <a name="remarks"></a>Observaciones

Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a **GetPreviousProtocolOffsetByName**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




