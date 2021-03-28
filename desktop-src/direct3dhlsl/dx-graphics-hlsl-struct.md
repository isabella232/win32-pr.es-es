---
title: Tipo de estructura
description: Tipo de estructura
ms.assetid: 896030b0-07cd-41bd-8c94-e173eabc81dd
keywords:
- Tipo de struct HLSL
topic_type:
- apiref
api_name:
- Struct Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 416c14c18fa1d0b76f4d13b609b895b0c64c2594
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104996820"
---
# <a name="struct-type"></a>Tipo de estructura

Use la siguiente sintaxis para declarar una estructura mediante HLSL.



|                                                                                           |
|-------------------------------------------------------------------------------------------|
| *nombre* de struct { \[ *InterpolationModifier* \] *Type* \[ *R* x *C* \] *memberName*;     ... }; |



 

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*
</dt> <dd>

Cadena ASCII que identifica de forma única el nombre de la estructura.

</dd> <dt>

<span id="_InterpolationModifier_"></span><span id="_interpolationmodifier_"></span><span id="_INTERPOLATIONMODIFIER_"></span>\[*InterpolationModifier*\]
</dt> <dd>

Modificador opcional que especifica un tipo de interpolación. Consulte [Comentarios](#remarks) para obtener más detalles.

</dd> <dt>

<span id="Type_RxC_"></span><span id="type_rxc_"></span><span id="TYPE_RXC_"></span>*Tipo* \[ de *R* x *C*\]
</dt> <dd>

El tipo de miembro con un tamaño de matriz de columna (*C*) x de fila opcional (*R*). Una estructura contiene al menos un elemento; Si contiene más de un elemento, los elementos son del mismo tipo. El número de filas y columnas son enteros sin signo entre 1 y 4, ambos incluidos.

</dd> <dt>

<span id="MemberName"></span><span id="membername"></span><span id="MEMBERNAME"></span>*NombreDeMiembro*
</dt> <dd>

Cadena ASCII que identifica de forma única el nombre del miembro.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Se puede especificar un modificador de interpolación en cualquier miembro de estructura o en un argumento para una función de sombreador de píxeles. Si un modificador aparece en ambos lugares, el modificador exterior (el modificador de argumento del sombreador de píxeles) sobreasignará el modificador in (el modificador de estructura).

Al compilar un sombreador o un efecto, el compilador del sombreador empaqueta los miembros de la estructura de acuerdo con [las reglas de empaquetado de HLSL](dx-graphics-hlsl-packing-rules.md).

### <a name="interpolation-modifiers-introduced-in-shader-model-4"></a>Modificadores de interpolación introducidos en el modelo de sombreador 4

Las salidas del sombreador de vértices que se usan para las entradas del sombreador de píxeles se interpolan linealmente para obtener valores por píxel durante la rasterización. Para establecer el método de interpolación, use cualquiera de los siguientes valores, que se admiten en el [modelo de sombreador 4](dx-graphics-hlsl-sm4.md) o posterior. El modificador se omite en cualquier salida del sombreador de vértices que no se use como entrada de sombreador de píxeles.



| Modificador de interpolación | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **lineal**             | Interpolar entre las entradas del sombreador; **lineal** es el valor predeterminado si no se especifica ningún modificador de interpolación.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **centroide**           | Interpolar entre las muestras que se encuentran en algún lugar dentro del área tratada del píxel (esto puede requerir la extrapolación de los puntos finales de un centro de píxeles). El muestreo de centroide puede mejorar el suavizado de contorno si un píxel está parcialmente incluido (aunque no esté incluido el centro de píxeles). El modificador **centroide** debe combinarse con el modificador **linear** o **noperspective** .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **nointerpolación**    | No se interpolan.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| **noperspective**      | No realice correcciones de perspectiva durante la interpolación. El modificador **noperspective** se puede combinar con el modificador **centroide** .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **AdventureWorks**             | **Disponible en el modelo de sombreador 4,1 y versiones posteriores** Interpolación en la ubicación de ejemplo en lugar de en el centro de píxeles. Esto hace que el sombreador de píxeles se ejecute por ejemplo en lugar de por píxel. Otra manera de producir la ejecución por muestra es tener una entrada con la [ \_ SampleIndex semántica](dx-graphics-hlsl-semantics.md), que indica el ejemplo actual. Solo las entradas con el **ejemplo** especificado (o la entrada \_ SampleIndex de SV) difieren entre las invocaciones del sombreador en el píxel, mientras que otras entradas que no especifican modificadores (por ejemplo, si se mezclan modificadores en entradas diferentes) todavía se interpolan en el centro de píxeles. Tanto la invocación del sombreador de píxeles como la prueba de profundidad y estarcido se producen para cada muestra incluida en el píxel. A veces, esto se conoce como *supermuestreo*. Por el contrario, en ausencia de una invocación de frecuencia de muestreo, conocida como *multimuestreo*, el sombreador de píxeles se invoca una vez por píxel, independientemente del número de muestras que se cubran, mientras que las pruebas de profundidad y estarcido se producen con frecuencia de ejemplo. Ambos modos proporcionan suavizado de contorno de borde equivalente. Sin embargo, el supermuestreo proporciona una mejor calidad de sombreado mediante la invocación del sombreador de píxeles con más frecuencia.<br/> |



 

<dl> 1. Cuando se usa un tipo int/uint, la única opción válida es **nointerpolation**.  
</dl>

Los modificadores de interpolación se pueden aplicar a los miembros de la estructura o a los argumentos de la [función](dx-graphics-hlsl-function-parameters.md), o a ambos.

## <a name="examples"></a>Ejemplos

A continuación se muestran algunas declaraciones de estructura de ejemplo.


```
struct struct1
{
  int    a;
}
```



Esta Declaración incluye una matriz.


```
struct struct2
{
  int    a;
  float  b;
  int4x4 iMatrix;
}
```



Esta Declaración incluye un modificador de interpolación.


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

 

 





