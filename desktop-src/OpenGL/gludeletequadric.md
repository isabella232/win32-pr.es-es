---
title: función gluDeleteQuadric (GLU. h)
description: La función gluDeleteQuadric destruye un objeto quadric.
ms.assetid: 09efd887-0fe8-4a56-bc6f-2177a4930035
keywords:
- gluDeleteQuadric (función) OpenGL
topic_type:
- apiref
api_name:
- gluDeleteQuadric
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b5ee85e943cd958e394efb191932393d228d948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802822"
---
# <a name="gludeletequadric-function"></a>gluDeleteQuadric función)

La función **gluDeleteQuadric** destruye un objeto quadric.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI gluDeleteQuadric(
   GLUquadricObj *state
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*state* 
</dt> <dd>

El objeto quadric que se va a destruir (creado con [**gluNewQuadric**](glunewquadric.md)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La función **gluDeleteQuadric** destruye el objeto quadric y libera cualquier memoria que haya usado. Después de llamar a **gluDeleteQuadric**, no puede volver a usar el *Estado* .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Glu. h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**gluNewQuadric**](glunewquadric.md)
</dt> </dl>

 

 





