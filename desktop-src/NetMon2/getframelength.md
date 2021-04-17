---
description: La función GetFrameLength devuelve la longitud del marco.
ms.assetid: 30be1f5c-9b13-42ad-944a-92b1aee8a6bc
title: Función GetFrameLength (Netmon. h)
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
ms.openlocfilehash: 29a2a08ac105414a914e14a9ce8e69976725700c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666281"
---
# <a name="getframelength-function"></a>GetFrameLength función)

La función **GetFrameLength** devuelve la longitud del marco.

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI GetFrameLength(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hFrame* \[ de\]
</dt> <dd>

Identificador de un marco.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es la longitud del marco en bytes.

Si la función no se realiza correctamente, el valor devuelto es cero.

## <a name="remarks"></a>Observaciones

Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **GetFrameLength** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




