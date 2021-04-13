---
title: función gluNextContour (GLU. h)
description: La función gluNextContour marca el principio de otro contorno.
ms.assetid: 622cd631-3426-4206-9e23-af2a74343da5
keywords:
- gluNextContour (función) OpenGL
topic_type:
- apiref
api_name:
- gluNextContour
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c7b798eba50205053c019e3e8d1708c9ed834e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422109"
---
# <a name="glunextcontour-function"></a>gluNextContour función)

\[La función **gluNextContour** está obsoleta y solo se proporciona por razones de compatibilidad con versiones anteriores. La función **gluNextContour** se asigna a [**GluTessEndContour**](glutessendcontour.md) seguido de [**gluTessBeginContour**](glutessbegincontour.md).\]

La función **gluNextContour** marca el principio de otro contorno.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI gluNextContour(
   GLUtesselator *tess,
   GLenum        type
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*tess* 
</dt> <dd>

Objeto de teselación (creado con [**gluNewTess**](glunewtess.md)).

</dd> <dt>

*type* 
</dt> <dd>

Tipo del contorno que se va a definir. Los valores siguientes son válidos.



| Value                                                                                                                                                                | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_EXTERIOR"></span><span id="glu_exterior"></span><dl> <dt>**GLU \_ exterior**</dt> </dl>           | Un contorno exterior define un límite exterior del polígono.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="GLU_INTERIOR"></span><span id="glu_interior"></span><dl> <dt>**\_interior Glu**</dt> </dl>           | Un contorno interior define un límite interior del polígono (por ejemplo, un hueco).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GLU_UNKNOWN"></span><span id="glu_unknown"></span><dl> <dt>**GLU \_ desconocido**</dt> </dl>              | La biblioteca analiza un perfil desconocido para determinar si es interior o exterior.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="GLU_CCW__GLU_CW"></span><span id="glu_ccw__glu_cw"></span><dl> <dt>**GLU \_ CCW, Glu \_ CW**</dt> </dl> | Se considera que el primer \_ contorno Glu CCW o Glu \_ CW definido es exterior. El resto de los contornos se consideran exteriores si están orientados en la misma dirección (en el sentido de las agujas del reloj o en el sentido contrario a las agujas del reloj) como el primer perfil y interior si no lo están.<br/> Si un contorno es de tipo GLU \_ CCW o Glu CW, todos los contornos \_ deben ser del mismo tipo (si no lo son, todos los contornos de Glu \_ CCW y Glu \_ CW se cambiarán a Glu \_ Unknown). Tenga en cuenta que no hay ninguna diferencia real entre los \_ tipos de contorno Glu CCW y Glu \_ CW.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Use la función **gluNextContour** para describir polígonos con varios contornos. Después de describir el primer contorno a través de una serie de llamadas de [**gluTessVertex**](glutessvertex.md) , una llamada a **gluNextContour** indica que el contorno anterior está completo y que el siguiente perfil está a punto de comenzar. Realice otra serie de llamadas de **gluTessVertex** para describir el nuevo contorno. Repita este proceso hasta que se hayan descrito todos los contornos.

El parámetro de *tipo* define el tipo de perfil que sigue.

Para definir el tipo del primer perfil, puede llamar a **gluNextContour** antes de describir el primer contorno. Si no llama a **gluNextContour** antes del primer perfil, el primer contorno está marcado como Glu \_ exterior.

## <a name="examples"></a>Ejemplos

Puede describir un cuadrangular con un orificio triangular en él de la manera siguiente:

``` syntax
gluBeginPolygon(tess); 
    gluTessVertex(tess, v1, v1); 
    gluTessVertex(tess, v2, v2); 
    gluTessVertex(tess, v3, v3); 
    gluTessVertex(tess, v4, v4);  
gluNextContour(tess, GLU_INTERIOR); 
    gluTessVertex(tess, v5, v5); 
    gluTessVertex(tess, v6, v6); 
    gluTessVertex(tess, v7, v7);  
gluEndPolygon(tess);
```

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

[**gluNewTess**](glunewtess.md)
</dt> <dt>

[**gluTessBeginContour**](glutessbegincontour.md)
</dt> <dt>

[**gluTessBeginPolygon**](glubeginpolygon.md)
</dt> <dt>

[*gluTessCallback*](glutess.md)
</dt> <dt>

[**gluTessEndContour**](glutessendcontour.md)
</dt> <dt>

[**gluTessVertex**](glutessvertex.md)
</dt> </dl>

 

 





