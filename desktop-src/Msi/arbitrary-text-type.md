---
description: El tipo de texto arbitrario de tipo semántico es uno de los tipos de formato de texto.
ms.assetid: 503ad2db-0875-4d8b-90f7-3d04318a6b62
title: Tipo de texto arbitrario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bcf22ea2a7c4be001a5c036d3e2ee2e8c441ba061f3a7ba5bda32abde3806c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066265"
---
# <a name="arbitrary-text-type"></a>Tipo de texto arbitrario

El tipo de texto arbitrario de [tipo semántico](semantic-types.md) es uno de los [tipos de formato de texto](text-format-types.md). Este tipo consta de una cadena de texto arbitraria de cualquier longitud proporcionada por el usuario. La herramienta de combinación sustituye esta cadena arbitraria en las plantillas especificadas en la columna Valor de la [tabla ModuleSubstitution](modulesubstitution-table.md).

Para especificar un elemento configurable de este tipo, los autores de módulos deben escribir el nombre de la cadena de texto en la columna Nombre, escribir "0" en la columna Formato y dejar en blanco las columnas Type y ContextData de la [tabla ModuleConfiguration](moduleconfiguration-table.md). La cadena de texto arbitraria puede estar en cualquier idioma compatible con la página de códigos de la base de datos. Para obtener más información, vea [Control de páginas de códigos (Windows instalador).](code-page-handling-windows-installer-.md) Null es un valor válido para la cadena de texto a menos que msmConfigItemNonNullable se haya incluido en el campo Atributos de la tabla ModuleConfiguration.

 

 



