---
title: Tipo de estructura
description: Tipo de estructura
ms.assetid: 896030b0-07cd-41bd-8c94-e173eabc81dd
keywords:
- Tipo de estructura HLSL
topic_type:
- apiref
api_name:
- Struct Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b050a60911212a550433c5cc961a12ea52209b268330739c2f73158bf8fe1063
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068145"
---
# <a name="struct-type"></a>Tipo de estructura

Use la sintaxis siguiente para declarar una estructura mediante HLSL.

struct *Name*{ \[ *InterpolationModifier* \] *Type* \[ *R* x *C* \] *MemberName*;     ... };



 

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nombre*
</dt> <dd>

Cadena ASCII que identifica de forma única el nombre de la estructura.

</dd> <dt>

<span id="_InterpolationModifier_"></span><span id="_interpolationmodifier_"></span><span id="_INTERPOLATIONMODIFIER_"></span>\[*InterpolationModifier*\]
</dt> <dd>

Modificador opcional que especifica un tipo de interpolación. Consulte [Comentarios](#remarks) para obtener más detalles.

</dd> <dt>

<span id="Type_RxC_"></span><span id="type_rxc_"></span><span id="TYPE_RXC_"></span>*Tipo* \[ *R* x *C*\]
</dt> <dd>

Tipo de miembro con un tamaño de matriz de fila opcional *(R*) x columna (*C).* Una estructura contiene al menos un elemento; si contiene más de un elemento, los elementos son del mismo tipo. El número de filas y columnas son enteros sin signo entre 1 y 4 inclusivos.

</dd> <dt>

<span id="MemberName"></span><span id="membername"></span><span id="MEMBERNAME"></span>*MemberName*
</dt> <dd>

Cadena ASCII que identifica de forma única el nombre del miembro.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Se puede especificar un modificador de interpolación en cualquier miembro de estructura o en un argumento para una función de sombreador de píxeles. Si aparece un modificador en ambos lugares, el modificador externo (el modificador de argumento del sombreador de píxeles) anula el modificador inside (el modificador de estructura).

Al compilar un sombreador o un efecto, el compilador del sombreador empaqueta miembros de estructura según las reglas de [empaquetado hlsl](dx-graphics-hlsl-packing-rules.md).

### <a name="interpolation-modifiers-introduced-in-shader-model-4"></a>Modificadores de interpolación introducidos en el modelo de sombreador 4

Las salidas del sombreador de vértices que se usan para las entradas del sombreador de píxeles se interpolan linealmente para obtener valores por píxel durante la rasterización. Para establecer el método de interpolación, use cualquiera de los valores siguientes, que se admiten en el modelo [de sombreador 4](dx-graphics-hlsl-sm4.md) o posterior. El modificador se omite en cualquier salida del sombreador de vértices que no se utilice como entrada del sombreador de píxeles.



| Modificador de interpolación | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Lineal**             | Interpolar entre entradas del sombreador; **linear** es el valor predeterminado si no se especifica ningún modificador de interpolación.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Centroide**           | Interpolar entre muestras que están en algún lugar dentro del área cubierta del píxel (esto puede requerir la extrapolación de puntos finales desde un centro de píxeles). El muestreo de centroide puede mejorar el suavizado de contorno si un píxel está parcialmente cubierto (incluso si el centro de píxeles no está cubierto). El **modificador centroide** debe combinarse con el **modificador lineal** o **noperspectivo.**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **nointerpolation**    | No interpolar .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **noperspective**      | No realice la corrección de perspectiva durante la interpolación. El **modificador noperspective** se puede combinar con el **modificador centroide.**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Muestra**             | **Disponible en el modelo de sombreador 4.1 y versiones posteriores** Interpolar en la ubicación de la muestra en lugar de en el centro de píxeles. Esto hace que el sombreador de píxeles se ejecute por ejemplo en lugar de por píxel. Otra manera de provocar la ejecución por ejemplo es tener una entrada con [SV \_ SampleIndex](dx-graphics-hlsl-semantics.md)semántico, que indica el ejemplo actual. Solo las entradas  con la muestra especificada (o la entrada SV SampleIndex) difieren entre las invocaciones del sombreador en el píxel, mientras que otras entradas que no especifican modificadores (por ejemplo, si se mezclan modificadores en distintas entradas) todavía se interpolan en el centro de \_ píxeles. Tanto la invocación del sombreador de píxeles como las pruebas de profundidad o galería de símbolos se producen para cada muestra cubierta del píxel. Esto se conoce a veces como *supermuestreo.* Por el contrario, en ausencia de invocación de frecuencia de muestra, conocida como *multimuestreo,* el sombreador de píxeles se invoca una vez por píxel, independientemente del número de muestras que se cubren, mientras que las pruebas de profundidad o galería de símbolos se producen con la frecuencia de la muestra. Ambos modos proporcionan suavizado de contorno de borde equivalente. Sin embargo, el supermuestreo proporciona una mejor calidad de sombreado mediante la invocación del sombreador de píxeles con más frecuencia.<br/> |



 

<dl> 1. Cuando se usa un tipo int/uint, la única opción válida es **nointerpolation**.  
</dl>

Los modificadores de interpolación se pueden aplicar a miembros de estructura o [argumentos de función,](dx-graphics-hlsl-function-parameters.md)o ambos.

## <a name="examples"></a>Ejemplos

Estas son algunas declaraciones de estructura de ejemplo.


```
struct struct1
{
  int    a;
}
```



Esta declaración incluye una matriz.


```
struct struct2
{
  int    a;
  float  b;
  int4x4 iMatrix;
}
```



Esta declaración incluye un modificador de interpolación.


```
struct In
{
  centroid float2 Texcoord;
};
```



## <a name="see-also"></a>Vea también

<dl> <dt>

[Tipos de datos (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

 





