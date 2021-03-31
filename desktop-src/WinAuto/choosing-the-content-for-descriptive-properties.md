---
title: Elección del contenido para propiedades descriptivas
description: Aunque el contenido de algunas propiedades es específico, el contenido de otras propiedades se compone del texto descriptivo que se deja que proporcione el desarrollador del servidor.
ms.assetid: 3f399451-e9c5-4901-9b6e-198aa0c2deab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b77860eaefeb4e371c69fdf6acd205c77d763c3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793623"
---
# <a name="choosing-the-content-for-descriptive-properties"></a>Elección del contenido para propiedades descriptivas

Aunque el contenido de algunas propiedades es específico, el contenido de otras propiedades se compone del texto descriptivo que se deja que proporcione el desarrollador del servidor. Además, el tipo de información de cada propiedad varía en función del objeto. En la tabla siguiente se proporcionan sugerencias para elegir el contenido de estas propiedades descriptivas.



| Propiedad                                        | Sugerencia de contenido                                                                                                                                                                                                                                                    |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Name**](name-property.md)                   | Una etiqueta que describe brevemente e identifica el objeto dentro de su contenedor, como el texto de un botón de control, el nombre de un elemento de menú o una etiqueta que se muestra junto a un control de edición.                                                                              |
| [**DefaultAction**](defaultaction-property.md) | Interacción predeterminada con el objeto. La cadena devuelta por esta propiedad es un verbo único, como "presionar" para un botón de la barra de herramientas, o una frase corta que comienza con un verbo.                                                                               |
| [**Value**](value-property.md)                 | Información contenida en el objeto, como el texto de un control de edición o el nombre de un vínculo HTML. El contenido de la propiedad [**Value**](value-property.md) puede cambiar, mientras que el contenido de la propiedad [**Name**](name-property.md) no cambia. |
| [**Descripción**](description-property.md)     | Describe la apariencia del objeto.                                                                                                                                                                                                                                    |
| [**Ayuda**](help-property.md)                   | Información sobre herramientas o información de estilo de globo utilizada para describir lo que hace el objeto o cómo usarlo.                                                                                                                                                                   |
| [**HelpTopic**](helptopic-property.md)         | Identificador de contexto de un tema de [WinHelp](/windows/win32/api/winuser/nf-winuser-winhelpa) que documenta el objeto.                                                                                                                                                 |



 

Use uno de los valores de [rol de objeto](object-roles.md) predefinidos para el [**rol**](role-property.md) y la combinación adecuada de [constantes de estado de objeto](object-state-constants.md) para el [**Estado**](state-property.md).

El contenido de las propiedades de los controles personalizados debe coincidir con el contenido de las propiedades de los controles proporcionados por el sistema que los controles personalizados emulan. Para obtener información sobre las propiedades admitidas por los controles proporcionados por el sistema, consulte [Apéndice A: referencia de elementos de la interfaz de usuario compatibles](appendix-a--supported-user-interface-elements-reference.md).

 

 