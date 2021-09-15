---
title: Elegir el contenido para propiedades descriptivas
description: Aunque el contenido de algunas propiedades es específico, el contenido de otras propiedades consta de texto descriptivo que se deja al desarrollador del servidor para proporcionar.
ms.assetid: 3f399451-e9c5-4901-9b6e-198aa0c2deab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b77860eaefeb4e371c69fdf6acd205c77d763c3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127466129"
---
# <a name="choosing-the-content-for-descriptive-properties"></a>Elegir el contenido para propiedades descriptivas

Aunque el contenido de algunas propiedades es específico, el contenido de otras propiedades consta de texto descriptivo que se deja al desarrollador del servidor para proporcionar. Además, el tipo de información de cada propiedad varía en función del objeto . En la tabla siguiente se proporcionan sugerencias para elegir el contenido de estas propiedades descriptivas.



| Propiedad                                        | Sugerencia de contenido                                                                                                                                                                                                                                                    |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Nombre**](name-property.md)                   | Etiqueta que describe e identifica brevemente el objeto dentro de su contenedor, como el texto de un botón de inserción, el nombre de un elemento de menú o una etiqueta que se muestra junto a un control de edición.                                                                              |
| [**DefaultAction**](defaultaction-property.md) | Interacción predeterminada con el objeto . La cadena devuelta por esta propiedad es un solo verbo, como "Presionar" para un botón de la barra de herramientas, o una frase corta que comienza con un verbo.                                                                               |
| [**Value**](value-property.md)                 | Información contenida en el objeto , como el texto de un control de edición o el nombre de archivo de un vínculo HTML. El contenido de la [**propiedad Value**](value-property.md) puede cambiar, mientras que el contenido de la [**propiedad Name**](name-property.md) no cambia. |
| [**Descripción**](description-property.md)     | Describe la apariencia del objeto.                                                                                                                                                                                                                                    |
| [**Ayuda**](help-property.md)                   | Información sobre herramientas o de estilo globo que se usa para describir lo que hace el objeto o cómo usarlo.                                                                                                                                                                   |
| [**HelpTopic**](helptopic-property.md)         | Identificador de contexto de un [tema de WinHelp](/windows/win32/api/winuser/nf-winuser-winhelpa) que documenta el objeto.                                                                                                                                                 |



 

Use uno de los valores de [rol de objeto predefinidos](object-roles.md) para [**El rol**](role-property.md) y la combinación adecuada de constantes de estado [de objeto](object-state-constants.md) para el [**estado**](state-property.md).

El contenido de las propiedades de los controles personalizados debe coincidir con el contenido de las propiedades de los controles proporcionados por el sistema que emulan los controles personalizados. Para obtener información sobre las propiedades compatibles con los controles proporcionados por el sistema, vea [Apéndice A: Referencia Interfaz de usuario elementos admitidos](appendix-a--supported-user-interface-elements-reference.md).

 

 