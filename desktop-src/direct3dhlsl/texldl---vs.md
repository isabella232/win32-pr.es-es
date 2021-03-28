---
title: texldl-vs
description: Muestra una textura con una muestra determinada. Se debe especificar el nivel de detalle de los mapas de bits concreto que se muestra como el cuarto componente de la coordenada de textura. | texldl-vs
ms.assetid: 774c058d-7b3e-46a9-adce-c9a44efefd78
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: be9240f5307bb1e70b1f10cc1e392b92e5833fd8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104083638"
---
# <a name="texldl---vs"></a>texldl-vs

Muestra una textura con una muestra determinada. Se debe especificar el nivel de detalle de los mapas de bits concreto que se muestra como el cuarto componente de la coordenada de textura.

## <a name="syntax"></a>Sintaxis



| texldl DST, src0, SRC1 |
|------------------------|



 

Donde:

-   DST es un registro de destino.
-   src0 es un registro de origen que proporciona las coordenadas de textura para el ejemplo de textura.
-   SRC1 identifica los registros de la muestra de origen \# , donde \# especifica el número de muestra de textura que se muestra. La muestra le ha asociado una textura y un estado de control definido por la enumeración [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype) (por ejemplo, D3DSAMP \_ MINFILTER).

## <a name="remarks"></a>Observaciones



| Versiones del sombreador de vértices | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| texldl                 |      |      |      |       | x    | x     |



 

texldl busca el conjunto de texturas en la fase de muestra a la que hace referencia SRC1. El nivel de detalle se selecciona de src0. w. Este valor puede ser negativo, en cuyo caso el nivel de detalle seleccionado es el "inicial uno" (el mapa más grande) con el MAGFILTER. Dado que src0. w es un valor de punto flotante, el valor fraccionario se usa para interpolar (si MIPFILTER es lineal) entre dos niveles de MIP. Se respetan los Estados de muestra MIPMAPLODBIAS y MAXMIPLEVEL. Para obtener más información sobre los Estados de muestra, vea [**D3DSAMPLERSTATETYPE**](/windows/desktop/direct3d9/d3dsamplerstatetype).

Si un programa de sombreador muestrea desde una muestra que no tiene un conjunto de texturas, se obtiene 0001 en el registro de destino.

Se trata de una aproximación al algoritmo de dispositivo de referencia.


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
   LOD = MAX( MAXMIPLEVEL, LOD);
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
-   DST debe ser un [registro temporal](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ).
-   DST puede aceptar una máscara de escritura. Vea [enmascaramiento del registro de destino](dx9-graphics-reference-asm-vs-registers-modifiers-masking.md).
-   Los valores predeterminados de los componentes que faltan son 0 o 1 y dependen del formato de textura.
-   SRC1 debe ser un [muestreador (Direct3D 9 ASM-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md) \# . SRC1 no puede usar un modificador Negate. SRC1 puede usar swizzle, que se aplica después del muestreo antes de que se respete la máscara de escritura. La muestra debe haberse declarado (mediante [DCL \_ samplerType (SM3-vs ASM)](dcl-samplertype---vs.md)) al principio del sombreador.
-   El número de coordenadas necesarias para realizar el ejemplo de textura depende de cómo se declaró la muestra. Si se declaró como un cubo, se necesita una coordenada de textura de tres componentes (. RGB). La validación exige que las coordenadas proporcionadas a texldl sean suficientes para la dimensión de textura declarada para la muestra. Sin embargo, no se garantiza que la aplicación establezca realmente una textura (a través de la API) con dimensiones iguales a la dimensión declarada para la muestra. En tal caso, el tiempo de ejecución intentará detectar discrepancias (posiblemente solo en depuración). Se permitirá el muestreo de una textura con menos dimensiones que las presentes en la coordenada de textura y se asumirá que omite los componentes de coordenadas de textura adicionales. Por el contrario, no se permite el muestreo de una textura con más dimensiones que las presentes en la coordenada de textura.
-   Si src0 (coordenada de textura) es un [registro temporal](dx9-graphics-reference-asm-vs-registers-temporary.md) (r \# ), los componentes necesarios para la búsqueda (descrito anteriormente) deben haberse escrito previamente.
-   El muestreo de texturas RGB sin signo dará como resultado valores Float entre 0,0 y 1,0.
-   Las texturas con signo de muestreo darán como resultado valores Float entre-1,0 y 1,0.
-   Al muestrear texturas de punto flotante, Float16 significa que los datos se van a rangos dentro de \_ FLOAT16 máx. Float32 significa que se usará el intervalo máximo de la canalización. El muestreo fuera de cualquier intervalo está sin definir.
-   No hay ningún límite de lectura dependiente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Instrucciones del sombreador de vértices](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
