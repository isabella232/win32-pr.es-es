---
description: La función GetFrameTimeStamp devuelve la marca de tiempo de un fotograma determinado.
ms.assetid: 4ac50400-6674-40fa-9a69-9c0ccb55b92c
title: Función GetFrameTimeStamp (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameTimeStamp
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 37a75f946a5fc0ddb2b32d99334368a272fdf2e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667549"
---
# <a name="getframetimestamp-function"></a>GetFrameTimeStamp función)

La función **GetFrameTimeStamp** devuelve la marca de tiempo de un fotograma determinado.

## <a name="syntax"></a>Sintaxis


```C++
__int64 WINAPI GetFrameTimeStamp(
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

Si la función se realiza correctamente, el valor devuelto es la marca de tiempo del marco en microsegundos.

Si la función no se realiza correctamente, el valor devuelto es menos uno (-1).

## <a name="remarks"></a>Observaciones

La función **GetFrameTimeStamp** devuelve una marca de tiempo que muestra el tiempo transcurrido entre el inicio del proceso de captura y la grabación del marco.

Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **GetFrameTimeStamp** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




