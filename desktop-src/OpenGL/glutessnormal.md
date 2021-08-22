---
title: Función gluTessNormal (Glu.h)
description: La función gluTessNormal especifica un valor normal para un polígono.
ms.assetid: 8c3a90d3-760d-4a0a-9808-a797383fcc42
keywords:
- Función GluTessNormal OpenGL
topic_type:
- apiref
api_name:
- gluTessNormal
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2db848c6971fe2893f2bc2cd4ca33e96811dda0d44e81e8a852cd441a6478d79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119488475"
---
# <a name="glutessnormal-function"></a>función gluTessNormal

La **función gluTessNormal** especifica un valor normal para un polígono.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI gluTessNormal(
   GLUtesselator *tess,
   GLdouble      x,
   GLdouble      y,
   GLdouble      z
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Tess* 
</dt> <dd>

Objeto de teselación (creado [**con gluNewTess).**](glunewtess.md)

</dd> <dt>

*x* 
</dt> <dd>

Componente de coordenada X de un normal.

</dd> <dt>

*y* 
</dt> <dd>

Componente de coordenada Y de un normal.

</dd> <dt>

*Z* 
</dt> <dd>

Componente de coordenada z de un normal.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

La **función gluTessNormal** describe un normal para un polígono que defina. Todos los datos de entrada se proyectan en un plano a uno de los tres ejes de coordenadas antes de la teselación, y todos los triángulos de salida se orientan en sentido contrario a las agujas del reloj con respecto a lo normal. (Para obtener la orientación en el sentido de las agujas del reloj, invierta el signo de la normal proporcionada). Por ejemplo, si sabe que todos los polígonos se encuentran en el plano x-y, llame a **gluTessNormal**(tess, 0.0, 0.0, 1.0) antes de representar cualquier polígono.

Si el valor normal proporcionado es (0,0, 0,0, 0,0) (el valor predeterminado), el valor normal se determina de la siguiente manera:

1.  La dirección de lo normal, hasta su signo, se encuentra al ajustar un plano a los vértices, sin tener en cuenta cómo se conectan los vértices. Se espera que los datos de entrada se encuentran aproximadamente en el plano; De lo contrario, la proyección a uno de los tres ejes de coordenadas puede cambiar considerablemente la geometría.
2.  Se elige el signo de normal para que la suma de las áreas firmadas de todos los contornos de entrada sea no negativo (donde un contorno contrario a las agujas del reloj tiene un área positiva).

La normal proporcionada se conserva hasta que otra llamada a **gluTessNormal** la cambia.

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

[**gluTessBeginPolygon**](glutessbeginpolygon.md)
</dt> <dt>

[**gluTessEndPolygon**](glutessendpolygon.md)
</dt> </dl>

 

 





