---
title: Función gluTessProperty (Glu.h)
description: La función gluTessProperty establece la propiedad de un objeto de teselación.
ms.assetid: 1306b9ef-4f1e-4684-99ea-464bae1d0a61
keywords:
- Función gluTessProperty OpenGL
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071456"
---
# <a name="glutessproperty-function"></a>función gluTessProperty

La **función gluTessProperty** establece la propiedad de un objeto de teselación.

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

*Tess* 
</dt> <dd>

Objeto de teselación (creado [**con gluNewTess**](glunewtess.md)).

</dd> <dt>

*Que* 
</dt> <dd>

Valor de la propiedad que se establecerá. Los valores siguientes son válidos: GLU \_ TESS \_ WINDING \_ RULE, GLU \_ TESS \_ BOUNDARY ONLY y GLU \_ \_ TESS \_ TOLERANCE.



| Value                                                                                                                                                                                      | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_TESS_WINDING_RULE"></span><span id="glu_tess_winding_rule"></span><dl> <dt>**REGLA DE ENROLLADO DE GLU \_ TESS \_ \_**</dt> </dl>    | Determina qué partes del polígono están en el interior. El parámetro value se puede establecer en uno de los siguientes: GLU \_ TESS \_ WINDING \_ ODD, GLU \_ TESS \_ \_ WINDING NONZERO, GLU \_ TESS \_ WINDING \_ POSITIVE, GLU \_ TESS WINDING NEGATIVE o \_ GLU \_ \_ TESS \_ WINDING \_ ABS \_ GEQ \_ TWO. <br/> Para entender cómo funciona la regla de desenlazamiento, primero tenga en cuenta que los contornos de entrada particionan el plano en regiones. La regla de sinuoso determina cuál de estas regiones está dentro del polígono.<br/> Para una C de contorno único, el número sinuoso de un punto x es simplemente el número con signo de revoluciones que hacemos alrededor de x cuando viajamos una vez alrededor de C (donde en sentido contrario a las agujas del reloj es positivo). Cuando hay varios contornos, se suman los números de sinuoso individuales. Este procedimiento asocia un valor entero con signo a cada punto x del plano. Tenga en cuenta que el número de sinuoso es el mismo para todos los puntos de una sola región.<br/> La regla sinuoso clasifica una región como "dentro" si su número de sinuoso pertenece a la categoría elegida (impar, distinto de cero, positivo, negativo o valor absoluto de al menos dos). El teselador GLU anterior (antes de GLU 1.2) usaba la regla "impar". La regla "distinto de cero" (GLU \_ TESS \_ WINDING \_ NONZERO) es otra manera común de definir el interior. Las otras tres reglas (GLU \_ TESS \_ WINDING \_ POSITIVE, GLU \_ TESS \_ WINDING \_ NEGATIVE y GLU \_ TESS \_ WINDING ABS GEQ TWO) \_ \_ \_ son útiles para las operaciones de CSG de polígono.<br/> |
| <span id="GLU_TESS_BOUNDARY_ONLY"></span><span id="glu_tess_boundary_only"></span><dl> <dt>**SOLO LÍMITE \_ DE GLU TESS \_ \_**</dt> </dl> | Especifica un valor booleano (establezca el valor en GL \_ TRUE o GL \_ FALSE). Cuando se establece value en GL TRUE, se devuelve un conjunto de contornos cerrados que separan el interior y exterior del polígono en lugar de \_ una teselación. Los contornos exteriores están orientados en sentido contrario a las agujas del reloj con respecto a lo normal; Los contornos interiores están orientados en el sentido de las agujas del reloj. Las devoluciones de llamada BEGIN y GLU TESS BEGIN DATA de GLU TESS usan el tipo \_ GL LINE LOOP para cada \_ \_ \_ \_ \_ \_ contorno.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="GLU_TESS_TOLERANCE"></span><span id="glu_tess_tolerance"></span><dl> <dt>**TOLERANCIA \_ A GLU TESS \_**</dt> </dl>              | Especifica una tolerancia para combinar características para reducir el tamaño de la salida. Por ejemplo, dos vértices muy cercanos entre sí podrían reemplazarse por un solo vértice. La tolerancia se multiplica por la magnitud de coordenada más grande de cualquier vértice de entrada; especifica la distancia máxima que cualquier característica puede moverse como resultado de una única operación de combinación. Si una sola característica participa en varias operaciones de combinación, la distancia total movida puede ser mayor. <br/> La combinación de características es completamente opcional; la tolerancia es solo una sugerencia. La implementación es libre de combinar en algunos casos y no en otros, o nunca combinar características. La tolerancia predeterminada es cero.<br/> La implementación actual combina vértices solo si son exactamente coincidentes, independientemente de la tolerancia actual. Un vértice se convierte en un borde solo si la implementación no puede distinguir en qué lado del borde se encuentra el vértice. Solo se combinan dos bordes cuando ambos extremos son idénticos.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

*value* 
</dt> <dd>

Valor de la propiedad indicada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La **función gluTessProperty** controla las propiedades almacenadas en un objeto de teselación. Estas propiedades afectan a la forma en que se interpretan y representan los polígonos.

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

[**gluGetTessProperty**](glugettessproperty.md)
</dt> <dt>

[**gluNewTess**](glunewtess.md)
</dt> </dl>

 

 





