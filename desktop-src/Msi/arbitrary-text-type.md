---
description: El tipo de texto arbitrario de tipo semántico es uno de los tipos de formato de texto.
ms.assetid: 503ad2db-0875-4d8b-90f7-3d04318a6b62
title: Tipo de texto arbitrario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9709a560398472fe79a2c77db827acdfa7994148
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667043"
---
# <a name="arbitrary-text-type"></a>Tipo de texto arbitrario

El tipo de texto arbitrario de [tipo semántico](semantic-types.md) es uno de los [tipos de formato de texto](text-format-types.md). Este tipo consta de una cadena de texto arbitraria de cualquier longitud proporcionada por el usuario. La herramienta de combinación sustituye esta cadena arbitraria a las plantillas especificadas en la columna valor de la [tabla ModuleSubstitution](modulesubstitution-table.md).

Para especificar un elemento configurable de este tipo, los autores de módulos deben escribir el nombre de la cadena de texto en la columna nombre, escribir "0" en la columna formato y dejar en blanco las columnas Type y ContextData de la [tabla ModuleConfiguration](moduleconfiguration-table.md). La cadena de texto arbitraria puede estar en cualquier lenguaje compatible con la página de códigos de la base de datos. Para obtener más información, vea [control de páginas de códigos (Windows Installer)](code-page-handling-windows-installer-.md). NULL es un valor válido para la cadena de texto a menos que msmConfigItemNonNullable se haya incluido en el campo Attributes de la tabla ModuleConfiguration.

 

 



