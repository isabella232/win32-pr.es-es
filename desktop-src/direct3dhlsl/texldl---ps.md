---
title: 'texldl: ps'
description: 'Muestrear una textura con un muestreador determinado. El nivel de detalle de mapa mip concreto que se muestrea debe especificarse como el cuarto componente de la coordenada de textura. | texldl: ps'
ms.assetid: f0ca8a1d-ac98-49ef-850a-c534e986c7ac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a6ab8a6f55ce5e069a01edb5d281bfe506c5fee6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966424"
---
# <a name="texldl---ps"></a>texldl: ps

Muestrear una textura con un muestreador determinado. El nivel de detalle de mapa mip concreto que se muestrea debe especificarse como el cuarto componente de la coordenada de textura.

## <a name="syntax"></a>Sintaxis



| texldl dst, src0, src1 |
|------------------------|



 

Donde:

-   dst es un registro de destino.
-   src0 es un registro de origen que proporciona las coordenadas de textura para la muestra de textura. Consulte [Registro de coordenadas de textura.](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md)
-   src1 identifica el registro (s) del muestreador de origen, donde especifica qué número de muestreador de textura se va \# \# a muestrear. El muestreador le ha asociado una textura y un estado de control definidos por la enumeración [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) (por ejemplo, D3DSAMP \_ MINFILTER).

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de píxeles | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texldl                |      |      |      |      |      |      |       | x    | x     |



 

texldl busca el conjunto de texturas en la fase sampler a la que hace referencia src1. El nivel de detalle se selecciona en src0.w. Este valor puede ser negativo, en cuyo caso el nivel de detalle seleccionado es el cero (mapa más grande) con MAGFILTER. Puesto que src0.w es un valor de punto flotante, el valor fraccionado se usa para interpolar (si MIPFILTER es LINEAR) entre dos niveles mip. Se respetan los estados de muestreo MIPMAPLODBIAS y MAXMIPLEVEL. Para obtener más información sobre los estados del sampler, [**vea D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).

Si un programa de sombreador toma muestras de un muestreador que no tiene un conjunto de texturas, se obtiene 0001 en el registro de destino.

A continuación se muestra un algoritmo aproximado que sigue el dispositivo de referencia:


```
LOD = src0.w + LODBIAS;
if (LOD <= 0 )
{
   LOD = 0;
   Filter = MagFilter;
   tex = Lookup( MAX(MAXMIPLEVEL, LOD), Filter );
}
else
{
   Filter = MinFilter;
   LOD = MAX( MAXMIPLEVEL, LOD );
   tex = Lookup( Floor(LOD), Filter );
   if( MipFilter == LINEAR )
   {
      tex1 = Lookup( Ceil(LOD), Filter );                        
      tex = (1 - frac(src0.w))*tex + frac(src0.w)*tex1;
   }
}
```



Restricciones:

-   Las coordenadas de textura no se deben escalar por tamaño de textura.
-   dst debe ser un [registro temporal](dx9-graphics-reference-asm-ps-registers-temporary.md) (r \# ).
-   dst puede aceptar una máscara de escritura. Vea Destination Register Write Mask ( [Máscara de escritura de registro de destino).](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)
-   Los valores predeterminados de los componentes que faltan son 0 o 1 y dependen del formato de textura.
-   src1 debe ser [sampler (Direct3D 9 asm-ps)](dx9-graphics-reference-asm-ps-registers-sampler.md) (s \# ). src1 no puede usar un modificador negate (vea [Máscara de escritura del registro de destino).](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md) src1 puede usar swzzle (consulte [Source Register Swlingling),](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md)que se aplica después del muestreo, pero antes de que se respeta la máscara de escritura (consulte Máscara de escritura del registro de destino). El sampler se debe haber declarado (mediante [dcl \_ samplerType (sm2, sm3 - ps asm)](dcl-samplertype---ps.md)al principio del sombreador.
-   El número de coordenadas necesarias para realizar la muestra de textura depende de cómo se declaró el muestreador. Si se declaró como un cubo, se requiere una coordenada de textura de tres componentes (.rgb). La validación exige que las coordenadas proporcionadas a la clase sean suficientes para \_ la dimensión de textura declarada para el muestreador. Sin embargo, no se garantiza que la aplicación realmente establece una textura (a través de la API) con dimensiones iguales a la dimensión declarada para el muestreador. En tal caso, el tiempo de ejecución intentará detectar errores de coincidencia (posiblemente solo en depuración). Se permitirá el muestreo de una textura con menos dimensiones que las presentes en la coordenada de textura y se supone que omite los componentes de coordenadas de textura adicionales. Por el contrario, el muestreo de una textura con más dimensiones de las que están presentes en la coordenada de textura no es posible.
-   Si src0 (coordenada de textura) es [Registro](dx9-graphics-reference-asm-ps-registers-temporary.md)temporal , los componentes necesarios para la búsqueda (descrito anteriormente) se deben haber escrito previamente.
-   El muestreo de texturas RGB sin signo dará como resultado valores flotantes entre 0,0 y 1,0.
-   El muestreo de texturas firmadas dará como resultado valores float entre -1.0 y 1.0.
-   Al muestrear texturas de punto flotante, Float16 significa que los datos oscilarán dentro de MAX \_ FLOAT16. Float32 significa que se usará el intervalo máximo de la canalización. El muestreo fuera de cualquiera de los intervalos no está definido.
-   No hay ningún límite de lectura dependiente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de píxeles](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 
