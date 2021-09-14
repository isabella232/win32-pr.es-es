---
title: Función gluNextContour (Glu.h)
description: La función gluNextContour marca el principio de otro contorno.
ms.assetid: 622cd631-3426-4206-9e23-af2a74343da5
keywords:
- gluNextContour, función OpenGL
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244971"
---
# <a name="glunextcontour-function"></a>función gluNextContour

\[La **función gluNextContour** está obsoleta y solo se proporciona por compatibilidad con versiones anteriores. La **función gluNextContour** se asigna [**a gluTessEndContour**](glutessendcontour.md) seguido de [**gluTessBeginContour.**](glutessbegincontour.md)\]

La **función gluNextContour** marca el principio de otro contorno.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI gluNextContour(
   GLUtesselator *tess,
   GLenum        type
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Tess* 
</dt> <dd>

Objeto de teselación (creado [**con gluNewTess**](glunewtess.md)).

</dd> <dt>

*type* 
</dt> <dd>

Tipo del contorno que se va a definir. Los valores siguientes son válidos.



| Value                                                                                                                                                                | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_EXTERIOR"></span><span id="glu_exterior"></span><dl> <dt>**GLU \_ EXTERIOR**</dt> </dl>           | Un contorno exterior define un límite exterior del polígono.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="GLU_INTERIOR"></span><span id="glu_interior"></span><dl> <dt>**GLU \_ INTERIOR**</dt> </dl>           | Un contorno interior define un límite interior del polígono (como un hueco).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GLU_UNKNOWN"></span><span id="glu_unknown"></span><dl> <dt>**GLU \_ UNKNOWN**</dt> </dl>              | La biblioteca analiza un contorno desconocido para determinar si es interior o exterior.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="GLU_CCW__GLU_CW"></span><span id="glu_ccw__glu_cw"></span><dl> <dt>**GLU \_ CCW, GLU \_ CW**</dt> </dl> | El primer contorno DE GLU \_ CCW o GLU \_ CW definido se considera exterior. Todos los demás contornos se consideran exteriores si están orientados en la misma dirección (en el sentido de las agujas del reloj o en sentido contrario a las agujas del reloj) que el primer contorno y en el interior si no lo están.<br/> Si un contorno es de tipo GLU CCW o GLU CW, todos los contornos deben ser del mismo tipo (si no lo están, todos los contornos DE GLU CCW y GLU CW se cambiarán a \_ \_ GLU \_ \_ \_ UNKNOWN). Tenga en cuenta que no hay ninguna diferencia real entre los tipos de contorno GLU \_ CCW y GLU \_ CW.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Use la **función gluNextContour para** describir polígonos con varios contornos. Después de describir el primer contorno a través de una serie de llamadas [**gluTessVertex,**](glutessvertex.md) una llamada **a gluNextContour** indica que el contorno anterior está completo y que el contorno siguiente está a punto de comenzar. Realice otra serie de **llamadas a gluTessVertex** para describir el nuevo contorno. Repita este proceso hasta que se hayan descrito todos los contornos.

El *parámetro type* define el tipo de contorno que sigue.

Para definir el tipo del primer contorno, puede llamar a **gluNextContour** antes de describir el primer contorno. Si no llama a **gluNextContour antes** del primer contorno, el primer contorno se marca como GLU \_ EXTERIOR.

## <a name="examples"></a>Ejemplos

Puede describir un cuadrángulo con un hueco triangular como se muestra a continuación:

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
| Encabezado<br/>                   | <dl> <dt>Glu.h</dt> </dl>     |
| Biblioteca<br/>                  | <dl> <dt>Glu32.lib</dt> </dl> |
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

 

 





