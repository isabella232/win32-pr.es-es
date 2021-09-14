---
description: Los identificadores proporcionan un medio eficaz para hacer referencia a las técnicas, los pases, las anotaciones y los parámetros con ID3DXEffectCompiler o ID3DXEffect.
ms.assetid: 2494ecf9-88a7-43dc-a75b-ed743b11993a
title: Identificadores (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9e0dbbcbbc38685cae7c89b334bfb5458bc8386
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127060640"
---
# <a name="handles-direct3d-9"></a>Identificadores (Direct3D 9)

Los identificadores proporcionan un medio eficaz para hacer referencia a las técnicas, los pases, las anotaciones y los parámetros [**con ID3DXEffectCompiler**](id3dxeffectcompiler.md) [**o ID3DXEffect**](id3dxeffect.md). Se generan dinámicamente al llamar a funciones con el formato Get \[ Parameter Annotation Function Technique Pass \| \| \| \| \] \[ ByName \| BySemantic \| Element \] .

Al ejecutar un programa, la generación de un identificador para el mismo objeto varias veces devolverá el mismo identificador cada vez. Pero no confíe en que el identificador se mantiene constante al ejecutar el programa varias veces. Tenga en cuenta también que los identificadores generados por diferentes instancias de [**ID3DXEffect**](id3dxeffect.md) e [**ID3DXEffectCompiler**](id3dxeffectcompiler.md) serán diferentes.

Si ve los archivos de encabezado, observará que los identificadores (D3DXHANDLEs) son técnicamente punteros de cadena.

Los identificadores que se pasan a funciones como GetParameter \[ ByName \| Element \| BySemantic o \] GetAnnotation \[ ByName pueden tener tres \] formas:

1.  Identificadores devueltos por funciones como GetParameter \[ ByName \| Element \| BySemantic. \]
2.  Cadenas como MyVariableName, MyTechniqueName o MyArray \[ \] 0.
3.  Identificador = **NULL.** Hay cuatro casos.
    -   Si es un valor devuelto de método, el método no pudo encontrar el identificador.
    -   Si se **pasa un** identificador NULL como primer parámetro del elemento \[ \| \| BySemantic GetParameter ByName , la función \] devuelve un parámetro de nivel superior. Por el contrario, si el identificador no es **NULL,** la función devuelve un miembro o elemento de estructura identificado por el identificador.
    -   Si se **pasa un** identificador NULL como el primer argumento de ValidateTechnique o el segundo argumento de IsParameterUsed, se valida la técnica actual.
    -   Si se **pasa un** identificador NULL como primer argumento de FindNextValidTechnique, la búsqueda de una técnica válida se inicia en la primera técnica del efecto.

Sugerencia de rendimiento Al principio de la aplicación, realice un paso de inicialización para generar identificadores a partir de las cadenas. A partir de ese momento, use solo identificadores. Pasar cadenas en lugar de identificadores generados es más lento.

## <a name="examples"></a>Ejemplos

Estos son algunos ejemplos que usan las funciones Get \[ Parameter Annotation Function Technique Pass \| \| \| \| \] \[ ByName \| BySemantic \| Element para generar \] identificadores.


```
// Gets handle of second top-level parameter handle in the effect file
h1 = GetParameter(NULL, 1);    

// Gets handle of the third struct member of MyStruct
h2 = GetParameter("MyStruct", 2); 

// Gets handle of the third array element handle of MyArray
h3 = GetParameterElement("MyArray", 2); 

// Gets handle of first member of h1 (that is, the second top-level param)
h4 = GetParameter(h1, 0);    

// Gets handle of MyStruct.Data
h5 = GetParameterByName("MyStruct", "Data");    
// or 
h6 = GetParameterByName(NULL, "MyStruct.Data");    

// Gets handle of MyStruct.Data.SubData
h7 = GetParameterByName("MyStruct.Data", "SubData"); 
// or 
h8 = GetParameterByName(NULL, "MyStruct.Data.SubData");

// Gets handle of fifth annotation of h1 (that is, second top-level param)
h9 = GetAnnotation(h1, 4);    

// Gets handle of MyStruct's annotation, called Author
h10 = GetAnnotationByName("MyStruct", "Author");  
// or
h11 = GetParameterByName(NULL, "MyStruct@Author"); 
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Formato de efecto](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



