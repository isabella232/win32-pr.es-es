---
description: El shell utiliza una subclave del registro de identificador de programación (ProgID) para asociar un tipo de archivo a una aplicación y controlar el comportamiento de la asociación.
ms.assetid: f2b666d6-bf22-47b5-87e1-8de5ff51c152
title: Identificadores de programación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67720fed1ad4b8401d11f6532cdc79836911e7cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997221"
---
# <a name="programmatic-identifiers"></a>Identificadores de programación

El shell utiliza una subclave del registro de identificador de programación (ProgID) para asociar un tipo de archivo a una aplicación y controlar el comportamiento de la asociación. Las entradas ProgID utilizadas para las asociaciones de archivo se encuentran en **HKEY \_ classes \_ root** en el registro.

Este tema se organiza de la siguiente manera:

-   [Elementos de identificador de programación usados por las asociaciones de archivo](#programmatic-identifier-elements-used-by-file-associations)
-   [Usar identificadores de programación con versión](#using-versioned-programmatic-identifiers)
-   [Temas relacionados](#related-topics)

Para obtener más información, consulte [registro de un tipo de archivo para una nueva aplicación](how-to-register-a-file-type-for-a-new-application.md) .

## <a name="programmatic-identifier-elements-used-by-file-associations"></a>Elementos de identificador de programación usados por las asociaciones de archivo

El formato correcto de un nombre de clave ProgID es \[ *Vendor o Application* \] . \[ *Componente* \] . \[ *Versión* \] , separados por puntos y sin espacios, como en Word.Document. 6. La parte de la *versión* es opcional, pero se recomienda encarecidamente. Para obtener más información, vea [usar identificadores de programación con versiones](#using-versioned-programmatic-identifiers).

Una subclave ProgID debe incluir los elementos siguientes. Tenga en cuenta que algunos datos de cadena de esta clave requieren un formato específico.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Predeterminada</strong></td>
<td>Establezca la entrada predeterminada de la subclave ProgID en un nombre descriptivo para ese ProgID, que se pueda mostrar al usuario. El uso de esta entrada para contener el nombre descriptivo está en desuso en la entrada FriendlyTypeName en sistemas que ejecutan Windows 2000 o posterior. Sin embargo, debe establecer este valor para mantener la compatibilidad con versiones anteriores.<br/></td>
</tr>
<tr class="even">
<td><strong>AllowSilentDefaultTakeOver</strong> (introducido en Windows 8)</td>
<td>Establezca esta entrada opcional para indicar que Windows debe omitir este ProgID al determinar un controlador predeterminado para un tipo de archivo público. Independientemente de si se establece este valor, el ProgID seguirá apareciendo en el cuadro de diálogo y el menú contextual de OpenWith. Se trata de un valor de REG_NONE.</td>
</tr>
<tr class="odd">
<td><strong>AppUserModelID</strong> (introducido en Windows 7)</td>
<td>Establezca esta entrada opcional en el identificador de modelo de usuario de la aplicación explícito de la aplicación (AppUserModelID) si la aplicación usa un AppUserModelID explícito y usa las listas de acceso <strong>frecuente</strong> o <strong>recientes</strong> generadas automáticamente del sistema, o proporciona una Jump List personalizada. Si una aplicación utiliza un AppUserModelID explícito y no establece este valor, los elementos no aparecerán en las Jump Lists de esa aplicación. Se trata de una cadena de REG_SZ. Para obtener más información, vea <a href="appids.md">identificadores de modelo de usuario de la aplicación (AppUserModelIDs)</a>.<br/></td>
</tr>
<tr class="even">
<td><strong>EditFlags</strong></td>
<td>Establezca esta entrada opcional mediante marcas de la enumeración <a href="/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags"><strong>FILETYPEATTRIBUTEFLAGS</strong></a> . La entrada marcas controla algunos aspectos de la administración del shell de los tipos de archivo vinculados a este ProgID. También puede usar la entrada marcas para limitar la cantidad de tiempo que el usuario puede modificar determinados aspectos de estos tipos de archivo mediante la hoja de propiedades de un archivo. Los valores de <strong>FILETYPEATTRIBUTEFLAGS</strong> usados para marcas son valores binarios diseñados para que pueda combinar varios atributos en un solo valor en una operación OR bit a bit. Se trata de un valor REG_DWORD o REG_BINARY.<br/></td>
</tr>
<tr class="odd">
<td><strong>FriendlyTypeName</strong></td>
<td>Establezca esta entrada en un nombre descriptivo para el ProgID, que se pueda mostrar al usuario. Por coherencia, esta cadena debe contener los mismos datos que la entrada predeterminada para esta clave ProgID. Esta entrada puede ser una cadena REG_SZ o REG_EXPAND_SZ, pero debe tener el formato de una cadena indirecta (un nombre de archivo completo y un valor de recurso precedidos del símbolo @), por ejemplo, <em>@% systemroot% \shell32.dll,-154</em>.<br/></td>
</tr>
<tr class="even">
<td><strong>InfoTip</strong></td>
<td>Establezca esta entrada en un breve mensaje de ayuda que el shell muestre para este ProgID. La entrada de recuadro informativo se muestra en un cuadro de diálogo de pasar el mouse. Este valor puede ser una cadena REG_SZ o REG_EXPAND_SZ pero, como FriendlyTypeName, debe tener el formato de una cadena indirecta.<br/></td>
</tr>
<tr class="odd">
<td><strong>CurVer</strong></td>
<td>Establezca la entrada (predeterminada) de esta subclave en la versión más reciente de este ProgID.<br/>
<blockquote>
[!Note]<br />
A menos que tenga versiones de aplicaciones en paralelo, es decir, varias versiones instaladas en el mismo sistema, debe evitar el uso de <strong>curver</strong>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>DefaultIcon</strong>.</td>
<td>Establezca la entrada (predeterminada) de esta subclave en el icono predeterminado que desea mostrar para los tipos de archivo asociados a este ProgID. Este valor puede ser un REG_SZ o REG_EXPAND_SZ cadena, pero se debe proporcionar como un nombre de archivo completo con su valor de recurso de operador, por ejemplo, <em>% systemroot% \shell32.dll,-154</em>.<br/></td>
</tr>
</tbody>
</table>



 

El siguiente ejemplo de clave del registro ilustra un nodo de clave ProgID de Asociación de archivo:

```
HKEY_CLASSES_ROOT
   Vendor.App.1
      (Default) = My Friendly Name
      AllowSilentDefaultTakeOver
      AppUserModelID = Vendor.Application
      EditFlags = 0x00000001
      FriendlyTypeName = @%SystemRoot%\shell32.dll,-154
      InfoTip = @%SystemRoot%\shell32.dll,-54
      CurVer
         (Default) = Vendor.App.1
      DefaultIcon
         (Default) = %SystemRoot%\shell32.dll,-1
```

## <a name="using-versioned-programmatic-identifiers"></a>Usar identificadores de programación con versión

Un ProgID con versión es aquél cuya versión se indica en su nombre. Para ello, normalmente se agrega un punto y el número de versión al nombre. Por ejemplo:

-   Word.Document. 6
-   Word.Document. 8

Se trata de ProgID con versión, con las versiones 6 y 8, respectivamente. Si tiene una aplicación en paralelo, es decir, una que admita varias versiones de la aplicación instaladas al mismo tiempo, use los ProgID independientes de curva y de versión. De lo contrario, deben evitarse los ProgID independientes de la versión y del curvador, ya que provocarán ineficiencias.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo registrar un tipo de archivo para una nueva aplicación](how-to-register-a-file-type-for-a-new-application.md)
</dt> <dt>

[Registro de aplicaciones](app-registration.md)
</dt> <dt>

[Tipos de archivo](fa-file-types.md)
</dt> <dt>

[Cómo funcionan las asociaciones de archivos](fa-how-work.md)
</dt> <dt>

[Vista de contenido por tipo de archivo o tipo](prophand-content-view.md)
</dt> <dt>

[Comprobador de tipo de archivo](file-type-verifier.md)
</dt> <dt>

[Controladores de tipo de archivo](fa-file-extensions.md)
</dt> <dt>

[Tipos percibidos](fa-perceivedtypes.md)
</dt> <dt>

[Matrices de asociación](fa-associationarray.md)
</dt> </dl>

 

 




