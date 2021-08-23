---
description: La función GetFrameMacHeaderLength devuelve la longitud, en bytes, del encabezado MAC del marco.
ms.assetid: 4a0f6a8c-04e0-47cb-abd1-b4011cd2d062
title: Función GetFrameMacHeaderLength (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameMacHeaderLength
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 0e6c4abe859cd4c307d8ade586b9371b69b5c171681006cf4aa1634ef815d794
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743905"
---
# <a name="getframemacheaderlength-function"></a>Función GetFrameMacHeaderLength

La **función GetFrameMacHeaderLength** devuelve la longitud, en bytes, del encabezado MAC del marco.

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI GetFrameMacHeaderLength(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hFrame* \[ En\]
</dt> <dd>

Identificador del marco.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es la longitud en bytes del encabezado MAC.

Si la función no se realiza correctamente o se encuentra un tipo MAC desconocido, el valor devuelto es cero.

## <a name="remarks"></a>Comentarios

[*Los*](e.md) expertos [*y analizadores pueden*](p.md) llamar a **la función GetFrameMacHeaderLength.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




