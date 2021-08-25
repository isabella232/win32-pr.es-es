---
title: importlib (atributo)
description: La directiva \ importlib\ hace que los tipos que ya se han compilado en otra biblioteca de tipos estén disponibles para la biblioteca de tipos que se va a crear.
ms.assetid: d5f15a77-c6b1-4918-be86-07d2995ca2d4
keywords:
- atributo importlib MIDL
topic_type:
- apiref
api_name:
- importlib
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c83d5c4b19800f92e3080d3fb435ddd20d62e4b6fe76986869a0f4da86deabcb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895075"
---
# <a name="importlib-attribute"></a>importlib (atributo)

La **\[ directiva \] importlib** hace que los tipos que ya se han compilado en otra biblioteca de tipos estén disponibles para la biblioteca de tipos que se va a crear.

``` syntax
[
    library-attributes
]
library (library-name)
{
    importlib(file-to-import); 
    ... 
}
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

*library-attributes* 
</dt> <dd>

Cero o más atributos que se aplicarán a la biblioteca.

</dd> <dt>

*library-name* 
</dt> <dd>

Identificador que los componentes de software usarán para denotar esta [**biblioteca.**](library.md)

</dd> <dt>

*archivo para importar* 
</dt> <dd>

Nombre y ubicación del archivo importado en tiempo de compilación MIDL.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Todas **\[ las \] directivas importlib** deben preceder a las demás descripciones de tipos de la biblioteca. Tenga en cuenta que la biblioteca importada, así como la biblioteca generada, se deben distribuir con la aplicación para que esté disponible en tiempo de ejecución.

En la mayoría de los casos, debe usar la directiva de importación MIDL **\[** [](import.md) **\]** para hacer referencia a definiciones de otro . Archivo IDL en . Archivo IDL. Este método proporciona a la biblioteca de tipos toda la información del archivo original, mientras que **\[ importlib \]** solo incluye el contenido de la biblioteca de tipos.

> [!Note]  
> La **\[ directiva \] importlib** hace que cualquier tipo definido en la biblioteca importada sea accesible desde la biblioteca que se compila. Para evitar ambigüedades cuando hay referencias duplicadas, se recomienda calificar cada una de estas referencias con el nombre de biblioteca adecuado, como se muestra a continuación:

 

``` syntax
library_name.type
```

En ausencia de esta calificación, MIDL resuelve la ambigüedad de referencia duplicada como se muestra a continuación:

-   A partir de la versión 3.1, MIDL usa la primera referencia que encuentra.
-   La versión 3.0 de MIDL, la primera versión de MIDL que podría generar bibliotecas de tipos, usa la última referencia que encontró.

## <a name="examples"></a>Ejemplos

``` syntax
library BrowseHelper 
{ 
    importlib("stdole32.tlb"); 
    importlib("mydisp.tlb"); 
    //Remainder of library definition 
};
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Biblioteca**](library.md)
</dt> <dt>

[**Importación**](import.md)
</dt> <dt>

[Importación de archivos de encabezado del sistema](importing-system-header-files.md)
</dt> <dt>

[Importar archivos y bibliotecas de tipos](importing-files-and-type-libraries.md)
</dt> <dt>

[Sintaxis de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 