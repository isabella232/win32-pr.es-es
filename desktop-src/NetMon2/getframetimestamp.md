---
description: La función GetFrameTimeStamp devuelve la marca de tiempo de un fotograma determinado.
ms.assetid: 4ac50400-6674-40fa-9a69-9c0ccb55b92c
title: Función GetFrameTimeStamp (Netmon.h)
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
ms.openlocfilehash: 29be85c3181e9ae3ffeab9c6bf9ea3a8c2795b47b8a3e2c1f9afc8732ec7840c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910735"
---
# <a name="getframetimestamp-function"></a>Función GetFrameTimeStamp

La **función GetFrameTimeStamp** devuelve la marca de tiempo de un fotograma determinado.

## <a name="syntax"></a>Sintaxis


```C++
__int64 WINAPI GetFrameTimeStamp(
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

Si la función se realiza correctamente, el valor devuelto es la marca de tiempo del fotograma en microsegundos.

Si la función no se realiza correctamente, el valor devuelto es menos uno (-1).

## <a name="remarks"></a>Comentarios

La **función GetFrameTimeStamp** devuelve una marca de tiempo que muestra el tiempo transcurrido entre el inicio del proceso de captura y la grabación del fotograma.

[*Los*](e.md) expertos [*y analizadores*](p.md) pueden llamar a **la función GetFrameTimeStamp.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




