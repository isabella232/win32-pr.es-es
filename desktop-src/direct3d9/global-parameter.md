---
description: Cada efecto compatible con DXSAS debe definir, como mínimo, un parámetro de efecto global único con la semántica global.
ms.assetid: 2112db8d-6a11-451d-a9d2-ac1b3cb2da95
title: Parámetro global
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 647ef789e37cd7c8d6cd2fe554f1f8becbfd5e92
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714733"
---
# <a name="global-parameter"></a>Parámetro global

Cada efecto compatible con DXSAS debe definir, como mínimo, un parámetro de efecto global único con la semántica global. El parámetro global también puede usar una o varias anotaciones opcionales. La sintaxis es la siguiente:


```
int VariableName : SasGlobal
<
    SasVersion 
    [OptionalAnnotations]
>;
```



donde:

-   VariableName es un nombre de variable de cadena de texto ASCII especificado por el usuario.
-   SasGlobal es la palabra clave semántica que identifica este parámetro como el parámetro DXSAS global.
-   SasVersion es la única anotación requerida.
-   OptionalAnnotations puede incluir lo siguiente:
    -   [SasEffectAuthor](#saseffectauthor)
    -   [SasEffectAuthoringSoftware](#saseffectauthoringsoftware)
    -   [SasEffectCategory](#saseffectcategory)
    -   [SasEffectCompany](#saseffectcompany)
    -   [SasEffectDescription](#saseffectdescription)
    -   [SasEffectHelp](#saseffecthelp)
    -   [SasEffectRevision](#saseffectrevision)

## <a name="sasversion"></a>SasVersion

La única anotación necesaria es SasVersion. Se declara de la siguiente manera:


```
int3 SasVersion = { major, minor, revision };
```



donde:

-   Major indica la versión principal de DXSAS. Las versiones principales de DXSAS pueden contener cambios de barrido en el conjunto de semánticas y anotaciones definidas. La semántica y las anotaciones se pueden agregar y quitar y, en general, no se garantiza la compatibilidad con versiones anteriores.
-   Minor indica la versión secundaria de SAS. Las versiones secundarias de DXSAS pueden incluir la adición de nuevas semánticas o anotaciones. Además, la semántica y las anotaciones se pueden marcar como desusadas en el estándar DXSAS. Las aplicaciones host todavía deben admitir la semántica y las anotaciones desusadas, pero pueden emitir un diagnóstico de advertencia cuando se use una semántica o una anotación de este tipo. Las versiones secundarias son compatibles con versiones anteriores.
-   revisión indica la revisión de DXSAS. Las revisiones de DXSAS solo existen como un medio para corregir errores, quitar ambigüedad y perfeccionar el estándar. Las revisiones del estándar son compatibles con versiones anteriores.

La versión actual es 1.0.0. No hay ningún valor predeterminado para esta anotación.

## <a name="saseffectauthor"></a>SasEffectAuthor

Esto declara a la persona que creó el efecto. Se declara de la siguiente manera:


```
string SasEffectAuthor = "value";
```



donde value es una cadena que identifica el autor del efecto. El valor predeterminado es una cadena vacía.

## <a name="saseffectauthoringsoftware"></a>SasEffectAuthoringSoftware

Esto declara el software en el que se creó el efecto. Se declara de la siguiente manera:


```
string SasEffectAuthoringSoftware = "value";
```



donde value es una cadena que identifica el software de creación de efectos. El valor predeterminado es una cadena vacía.

## <a name="saseffectcategory"></a>SasEffectCategory

Esto declara la categoría del efecto. Se declara de la siguiente manera:


```
string SasEffectCategory = "value";
```



donde valor es una cadena que identifica la categoría del efecto. El valor predeterminado es una cadena vacía. La categoría se expresa mediante un valor similar a la ruta de acceso mediante la barra diagonal como delimitador. Los efectos solo pueden pertenecer a una categoría, ya que no hay ninguna sintaxis para expresar la inclusión en varias rutas de acceso dentro de un valor de SasEffectCategory único. La aplicación host no trata el valor de esta anotación como lo distingue entre mayúsculas y minúsculas.

## <a name="saseffectcompany"></a>SasEffectCompany

Esto declara la compañía que creó el efecto. Se declara de la siguiente manera:


```
string SasEffectCompany = "value";
```



donde value es una cadena que identifica el nombre de la compañía a la que pertenece el efecto. El valor predeterminado es una cadena vacía.

## <a name="saseffectdescription"></a>SasEffectDescription

Esto describe el efecto. Se declara de la siguiente manera:


```
string SasEffectDescription = "value";
```



donde value es una cadena que describe el efecto. El valor predeterminado es una cadena vacía.

## <a name="saseffecthelp"></a>SasEffectHelp

Se trata de una cadena de ayuda que se puede mostrar al usuario cada vez que se solicita ayuda sobre el efecto asociado. Se declara de la siguiente manera:


```
string SasEffectHelp = "value";
```



donde value es una cadena que se puede mostrar si el usuario solicita ayuda. El valor predeterminado es una cadena vacía.

## <a name="saseffectrevision"></a>SasEffectRevision

Esta anotación permite a las herramientas y los usuarios registrar el número de revisión del archivo de efectos asociado. Por ejemplo, los usuarios podrían insertar las palabras clave adecuadas en el valor de esta anotación para invocar la sustitución de palabras clave en su software de control de revisiones favorito. Se declara de la siguiente manera:


```
string SasEffectRevision = "value";
```



donde value es una cadena que identifica la revisión del efecto. El valor predeterminado es una cadena vacía.

## <a name="examples"></a>Ejemplos

A continuación se muestra un ejemplo en el que solo se usa la anotación única requerida:


```
int gp : SasGlobal
<
  int3 SasVersion = {1,0,0};
>;
```



Este es un ejemplo que utiliza la anotación requerida y varias anotaciones opcionales:


```
int gp : SasGlobal
<
  int3 SasVersion = {1,0,0};
  string SasEffectAuthor = "Mike's Shader";
  string SasEffectAuthoringSoftware = "fxe 2.5.4";
  string SasEffectCategory = "/surface/procedural/wood";
  string SasEffectCompany = "Microsoft Corporation";
  string SasEffectDescription = "Renders an irridescent surface.";
  string SasEffectHelp = "For more information, see https://somelocation/skin.htm";    
  string SasEffectRevision = "$Revision$";  
>;
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de las anotaciones y semánticas estándar de DirectX](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



