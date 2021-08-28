---
description: El Shell usa una subclave del Registro de identificador de programación (ProgID) para asociar un tipo de archivo a una aplicación y para controlar el comportamiento de la asociación.
ms.assetid: f2b666d6-bf22-47b5-87e1-8de5ff51c152
title: Identificadores mediante programación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf982f865fa8b856bc29c00a9b2371b88b34615b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467292"
---
# <a name="programmatic-identifiers"></a>Identificadores mediante programación

El Shell usa una subclave del Registro de identificador de programación (ProgID) para asociar un tipo de archivo a una aplicación y para controlar el comportamiento de la asociación. Las entradas progID usadas para las asociaciones de archivo se encuentran en **HKEY \_ CLASSES \_ ROOT** en el Registro.

Este tema se organiza de la siguiente manera:

-   [Elementos de identificador mediante programación usados por asociaciones de archivo](#programmatic-identifier-elements-used-by-file-associations)
-   [Usar identificadores de programación con versiones](#using-versioned-programmatic-identifiers)
-   [Temas relacionados](#related-topics)

Para obtener más información, [lea Cómo registrar un tipo de archivo para una nueva aplicación.](how-to-register-a-file-type-for-a-new-application.md)

## <a name="programmatic-identifier-elements-used-by-file-associations"></a>Elementos de identificador mediante programación usados por asociaciones de archivo

El formato adecuado de un nombre de clave de ProgID \[ *es Proveedor o Aplicación.* \] \[ *Componente* \] . \[ *Versión*, separada por puntos y sin espacios, como en \] Word.Document.6. La *parte* Versión es opcional, pero se recomienda encarecidamente. Para obtener más información, [vea Usar identificadores de programación con versiones](#using-versioned-programmatic-identifiers).

Una subclave ProgID debe incluir los siguientes elementos. Tenga en cuenta que algunos datos de cadena de esta clave requieren un formato específico.




| Elemento | Descripción | 
|---------|-------------|
| <strong>(Valor predeterminado)</strong> | Establezca la entrada predeterminada de la subclave ProgID en un nombre descriptivo para ese ProgID, adecuado para mostrar al usuario. El uso de esta entrada para contener el nombre descriptivo está en desuso por la entrada FriendlyTypeName en sistemas que ejecutan Windows 2000 o posterior. Sin embargo, debe establecer este valor por compatibilidad con versiones anteriores.<br /> | 
| <strong>AllowSilentDefaultTakeOver</strong> (introducido en Windows 8) | Establezca esta entrada opcional para indicar que Windows debe omitir este ProgID al determinar un controlador predeterminado para un tipo de archivo público. Independientemente de si se establece este valor, progID sigue apareciendo en el menú contextual y el cuadro de diálogo AbrirCon. Se trata de REG_NONE valor. | 
| <strong>AppUserModelID</strong> (introducido en Windows 7) | Establezca esta entrada opcional en el identificador de modelo de usuario de aplicación (AppUserModelID) explícito de la aplicación <strong></strong> si <strong></strong> la aplicación usa un AppUserModelID explícito y usa listas de acceso rápido frecuentes o recientes generadas automáticamente por el sistema o proporciona una Lista de accesos directos. Si una aplicación usa un AppUserModelID explícito y no establece este valor, los elementos no aparecerán en las listas de accesos rápidos de esa aplicación. Se trata de una REG_SZ cadena. Para obtener más información, <a href="appids.md">vea Application User Model IDs (AppUserModelIDs) ( Id. de modelo de usuario de aplicación [AppUserModelID]).</a><br /> | 
| <strong>EditFlags</strong> | Establezca esta entrada opcional mediante marcas de la <a href="/windows/desktop/api/Shlwapi/ne-shlwapi-filetypeattributeflags"><strong>enumeración FILETYPEATTRIBUTEFLAGS.</strong></a> La entrada EditFlags controla algunos aspectos del control del shell de los tipos de archivo vinculados a este ProgID. También puede usar la entrada EditFlags para limitar cuánto puede modificar el usuario determinados aspectos de estos tipos de archivo mediante la hoja de propiedades de un archivo. Los <strong>valores FILETYPEATTRIBUTEFLAGS usados</strong> para EditFlags son valores binarios diseñados para que pueda combinar varios atributos en un único valor en una operación OR bit a bit. Se trata de REG_DWORD o REG_BINARY valor.<br /> | 
| <strong>FriendlyTypeName</strong> | Establezca esta entrada en un nombre descriptivo para progID, adecuado para mostrarlo al usuario. Por coherencia, esta cadena debe contener los mismos datos que la entrada Default para esta clave ProgID. Esta entrada puede ser una cadena REG_SZ o REG_EXPAND_SZ, pero se debe dar formato como una cadena indirecta (un nombre de archivo completo y un valor de recurso precedido por el símbolo @), por ejemplo <em>@%SystemRoot%\shell32.dll,-154</em>.<br /> | 
| <strong>InfoTip</strong> | Establezca esta entrada en un breve mensaje de ayuda que el shell muestra para este ProgID. La entrada Información sobre se muestra en un cuadro de diálogo de mouse sobre . Este valor puede ser una cadena REG_SZ o REG_EXPAND_SZ pero, al igual que FriendlyTypeName, debe tener formato de cadena indirecta.<br /> | 
| <strong>Curver</strong> | Establezca la entrada (Valor predeterminado) de esta subclave en la versión más reciente de este ProgID.<br /><blockquote>[!Note]<br />A menos que tenga versiones de aplicación en paralelo, es decir, varias versiones instaladas en el mismo sistema, debe evitar el uso de <strong>CurVer</strong>.</blockquote><br /> | 
| <strong>DefaultIcon</strong>. | Establezca la entrada (Valor predeterminado) de esta subclave en el icono predeterminado que desea mostrar para los tipos de archivo asociados a este ProgID. Este valor puede ser una cadena REG_SZ o REG_EXPAND_SZ, pero debe proporcionarse como un nombre de archivo completo con su valor de recurso de asistencia, por ejemplo <em>%SystemRoot%\shell32.dll,-154</em>.<br /> | 




 

En el siguiente ejemplo de clave del Registro se muestra un nodo de clave ProgID de asociación de archivos:

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

## <a name="using-versioned-programmatic-identifiers"></a>Usar identificadores de programación con versiones

Un ProgID con versión es aquella cuya versión se indica en su nombre. Normalmente, esto se hace agregando un punto y el número de versión al nombre. Por ejemplo:

-   Word.Document.6
-   Word.Document.8

Se trata de progID con versiones, con las versiones 6 y 8, respectivamente. Si tiene una aplicación en paralelo, es decir, una que admite varias versiones de la aplicación instaladas al mismo tiempo, use CurVer y ProgID independientes de versión. De lo contrario, se deben evitar los ProgID de CurVer y Version Independent, ya que darán lugar a ineficacias.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo registrar un tipo de archivo para una nueva aplicación](how-to-register-a-file-type-for-a-new-application.md)
</dt> <dt>

[Registro de aplicaciones](app-registration.md)
</dt> <dt>

[Tipos de archivo](fa-file-types.md)
</dt> <dt>

[Cómo funcionan las asociaciones de archivo](fa-how-work.md)
</dt> <dt>

[Vista de contenido por tipo o tipo de archivo](prophand-content-view.md)
</dt> <dt>

[Comprobador de tipos de archivo](file-type-verifier.md)
</dt> <dt>

[Controladores de tipos de archivo](fa-file-extensions.md)
</dt> <dt>

[Tipos percibidos](fa-perceivedtypes.md)
</dt> <dt>

[Matrices de asociaciones](fa-associationarray.md)
</dt> </dl>

 

 




