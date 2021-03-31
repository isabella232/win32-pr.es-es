---
title: función gluTessProperty (GLU. h)
description: La función gluTessProperty establece la propiedad de un objeto de teselación.
ms.assetid: 1306b9ef-4f1e-4684-99ea-464bae1d0a61
keywords:
- gluTessProperty (función) OpenGL
topic_type:
- apiref
api_name:
- gluTessProperty
api_location:
- glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe21f2961cd4cb1df31a1fdb3f407a71d6e6d68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151025"
---
# <a name="glutessproperty-function"></a>gluTessProperty función)

La función **gluTessProperty** establece la propiedad de un objeto de teselación.

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI gluTessProperty(
   GLUtesselator *tess,
   GLenum        which,
   GLdouble      value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*tess* 
</dt> <dd>

Objeto de teselación (creado con [**gluNewTess**](glunewtess.md)).

</dd> <dt>

*cuales* 
</dt> <dd>

Valor de la propiedad que se establecerá. Los valores siguientes son válidos: \_ Glu \_ Tess \_ , Glu \_ Tess \_ BOUNDARY \_ y Glu \_ Tess \_ Tolerance.



| Value                                                                                                                                                                                      | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_TESS_WINDING_RULE"></span><span id="glu_tess_winding_rule"></span><dl> <dt>**GLU \_ \_ regla de bobinado de Tess \_**</dt> </dl>    | Determina qué partes del polígono se encuentran en el interior. El parámetro de valor se puede establecer en uno de los siguientes: GLU \_ Tess \_ bobinado \_ impar, Glu \_ Tess \_ bobinado \_ unzero, Glu \_ Tess \_ devanado \_ Positive, Glu \_ Tess \_ bobinado \_ negative o Glu \_ Tess \_ bobinado \_ ABS \_ GEQ \_ Two. <br/> Para entender cómo funciona la regla de bobinado, considere primero que los contornos de entrada particionan el plano en regiones. La regla de bobinado determina cuál de estas regiones se encuentra dentro del polígono.<br/> En el caso de un solo contorno C, el número de bobinado de un punto x es simplemente el número de revoluciones con signo que hacemos alrededor de x a medida que nos desplazamos una vez alrededor de C (donde el sentido contrario a las agujas del reloj es positivo). Cuando hay varios contornos, se suman los números de bobinado individuales. Este procedimiento asocia un valor entero con signo a cada punto x del plano. Tenga en cuenta que el número de bobinado es el mismo para todos los puntos de una sola región.<br/> La regla de bobinado clasifica una región como "dentro" Si su número de bobinado pertenece a la categoría elegida (impar, distinto de cero, positivo, negativo o valor absoluto de al menos dos). La GLU anterior del teselador (anterior a GLU 1,2) usaba la regla "impar". La regla "NonZero" (GLU \_ Tess \_ sinuoso \_ noncero) es otra forma habitual de definir el interior. Las otras tres reglas (GLU \_ Tess \_ devanado \_ positivo, Glu \_ Tess \_ bobinado \_ negativo, Glu \_ Tess \_ bobinado \_ ABS \_ GEQ \_ dos) son útiles para las operaciones de Polygon CSG.<br/> |
| <span id="GLU_TESS_BOUNDARY_ONLY"></span><span id="glu_tess_boundary_only"></span><dl> <dt>**\_ \_ solo límites de Tess de Glu \_**</dt> </dl> | Especifica un valor booleano (establecer valor en GL \_ true o GL \_ false). Al establecer Value en GL \_ true, se devuelve un conjunto de contornos cerrados que separan el interior y el exterior del polígono en lugar de una teselación. Los contornos exteriores se orientan en sentido contrario a las agujas del reloj con respecto al normal; los contornos interiores están orientados a la derecha. Las \_ \_ \_ devoluciones de llamada de datos Begin y GLU Tess de Glu Tess \_ \_ usan el tipo \_ \_ de bucle de línea de libro de contabilidad para cada perfil.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="GLU_TESS_TOLERANCE"></span><span id="glu_tess_tolerance"></span><dl> <dt>**\_tolerancia Tess \_ Glu**</dt> </dl>              | Especifica una tolerancia para la combinación de características para reducir el tamaño de la salida. Por ejemplo, dos vértices que son muy cercanos entre sí se pueden reemplazar por un solo vértice. La tolerancia se multiplica por la magnitud de la coordenada más grande de cualquier vértice de entrada; Especifica la distancia máxima que cualquier característica puede moverse como resultado de una sola operación de combinación. Si una sola característica participa en varias operaciones de combinación, la distancia total movida puede ser mayor. <br/> La combinación de características es totalmente opcional; la tolerancia es solo una sugerencia. La implementación es gratuita para la fusión mediante combinación en algunos casos, no en otras o para no combinar nunca características. La tolerancia predeterminada es cero.<br/> La implementación actual combina los vértices solo si son exactamente coincidentes, independientemente de la tolerancia actual. Un vértice se une a un borde solo si la implementación no puede distinguir en qué lado del borde reside el vértice. Dos bordes se combinan solo cuando ambos extremos son idénticos.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

*value* 
</dt> <dd>

Valor de la propiedad indicada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La función **gluTessProperty** controla las propiedades almacenadas en un objeto de teselación. Estas propiedades afectan a la manera en que se interpretan y representan los polígonos.

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

[**gluGetTessProperty**](glugettessproperty.md)
</dt> <dt>

[**gluNewTess**](glunewtess.md)
</dt> </dl>

 

 





