---
description: La función GetFrameNumber devuelve el número de un marco.
ms.assetid: 97d343a3-2a1e-47d7-bfc2-b63f8d84b29d
title: Función GetFrameNumber (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameNumber
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: de04fa513fab98b1a82d036f6f40a6c67cdda3ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000930"
---
# <a name="getframenumber-function"></a>GetFrameNumber función)

La función **GetFrameNumber** devuelve el número de un marco.

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPI GetFrameNumber(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hFrame* \[ de\]
</dt> <dd>

Identificador del marco.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es un número de marco basado en cero.

Si la función no es correcta, el valor devuelto es menos uno (-1).

## <a name="remarks"></a>Observaciones

Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **GetFrameNumber** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




