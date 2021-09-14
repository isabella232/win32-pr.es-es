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
ms.openlocfilehash: 9b5ee85e943cd958e394efb191932393d228d948
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071489"
---
# <a name="gludeletequadric-function"></a>Función gluDeleteQuadric

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

## <a name="remarks"></a>Observaciones

La **función gluDeleteQuadric** destruye el objeto cuádigo y libera la memoria que usó. Después de llamar a **gluDeleteQuadric,** no puede volver a usar *el* estado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

 





