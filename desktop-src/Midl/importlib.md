---
title: importlib (atributo)
description: La Directiva \ importlib \ hace que los tipos que ya se han compilado en otra biblioteca de tipos estén disponibles para la biblioteca de tipos que se va a crear.
ms.assetid: d5f15a77-c6b1-4918-be86-07d2995ca2d4
keywords:
- importlib (atributo) MIDL
topic_type:
- apiref
api_name:
- importlib
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b9c233103330e9f8ae7318a613cbc5103315a74
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487546"
---
# <a name="importlib-attribute"></a>importlib (atributo)

La directiva **\[ importlib \]** hace que los tipos que ya se han compilado en otra biblioteca de tipos estén disponibles para la biblioteca de tipos que se va a crear.

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

*Biblioteca: atributos* 
</dt> <dd>

Cero o más atributos que se aplicarán a la biblioteca.

</dd> <dt>

*nombre de biblioteca* 
</dt> <dd>

El identificador que los componentes de software usarán para denotar esta [**biblioteca**](library.md).

</dd> <dt>

*archivo a importar* 
</dt> <dd>

Nombre y ubicación del archivo importado en tiempo de compilación de MIDL.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Todas las directivas **\[ importlib \]** deben preceder a las demás descripciones de tipos de la biblioteca. Tenga en cuenta que la biblioteca importada, así como la biblioteca generada, deben distribuirse con la aplicación para que esté disponible en tiempo de ejecución.

En la mayoría de los casos, debe usar la Directiva de **\[** [**importación**](import.md) **\]** de MIDL para hacer referencia a definiciones de otro. Archivo IDL en su. Archivo IDL. Este método proporciona a la biblioteca de tipos toda la información del archivo original, mientras que **\[ importlib \]** solo aporta el contenido de la biblioteca de tipos.

> [!Note]  
> La directiva **\[ importlib \]** hace que cualquier tipo definido en la biblioteca importada sea accesible desde dentro de la biblioteca que se está compilando. Para evitar la ambigüedad cuando hay referencias duplicadas, se recomienda calificar cada una de ellas con el nombre de biblioteca adecuado, como se indica a continuación:

 

``` syntax
library_name.type
```

En ausencia de tal calificación, MIDL resuelve la ambigüedad de la referencia duplicada como se indica a continuación:

-   A partir de la versión 3,1, MIDL usa la primera referencia que encuentra.
-   La versión 3,0 de MIDL, la primera versión de MIDL que podría generar bibliotecas de tipos, utiliza la última referencia encontrada.

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

[**biblioteca**](library.md)
</dt> <dt>

[**importar**](import.md)
</dt> <dt>

[Importación de archivos de encabezado del sistema](importing-system-header-files.md)
</dt> <dt>

[Importar archivos y bibliotecas de tipos](importing-files-and-type-libraries.md)
</dt> <dt>

[Sintaxis del archivo ODL](/previous-versions/windows/desktop/automat/odl-file-syntax)
</dt> <dt>

[Ejemplo de archivo ODL](/previous-versions/windows/desktop/automat/odl-file-example)
</dt> <dt>

[Generar una biblioteca de tipos con MIDL](generating-a-type-library-with-midl-2.md)
</dt> </dl>

 

 