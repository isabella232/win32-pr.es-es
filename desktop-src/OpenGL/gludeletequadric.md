---
title: Función gluDeleteQuadric (Glu.h)
description: La función gluDeleteQuadric destruye un objeto cuádigo.
ms.assetid: 09efd887-0fe8-4a56-bc6f-2177a4930035
keywords:
- Función gluDeleteQuadric OpenGL
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
ms.openlocfilehash: ad0c12bd77d3d8b7f7de641671916bb8a901d29d812dfa4e9af6ef116984a128
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519625"
---
# <a name="gludeletequadric-function"></a>función gluDeleteQuadric

La **función gluDeleteQuadric** destruye un objeto cuádigo.

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

Objeto cuádigo que se va a destruir (creado [**con gluNewQuadric).**](glunewquadric.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

La **función gluDeleteQuadric** destruye el objeto cuádigo y libera la memoria que usó. Después de llamar a **gluDeleteQuadric,** no puede volver a usar *el* estado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Glu32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**gluNewQuadric**](glunewquadric.md)
</dt> </dl>

 

 





