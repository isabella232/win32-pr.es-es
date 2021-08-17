---
description: La función GetFrameLength devuelve la longitud del marco.
ms.assetid: 30be1f5c-9b13-42ad-944a-92b1aee8a6bc
title: Función GetFrameLength (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameLength
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 2344f2401995af3bac2e8245f48824dfb992076113eb8c27dcb9eff0a54eae04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117795707"
---
# <a name="getframelength-function"></a>Función GetFrameLength

La **función GetFrameLength** devuelve la longitud del marco.

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI GetFrameLength(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hFrame* \[ En\]
</dt> <dd>

Identificador de un marco.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función es correcta, el valor devuelto es la longitud del marco en bytes.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Comentarios

[*Los*](e.md) expertos [*y analizadores*](p.md) pueden llamar a **la función GetFrameLength.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




