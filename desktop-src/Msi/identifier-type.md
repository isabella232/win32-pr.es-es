---
description: El tipo de identificador de tipo semántico es uno de los tipos de formato de texto.
ms.assetid: 137c3ad8-e47c-4cc5-b5c5-ea130236551a
title: Tipo de identificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af6d4e63b473c9ba0705c093f1dec5bcdbc1e26f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156328"
---
# <a name="identifier-type"></a>Tipo de identificador

El tipo de identificador de [tipo semántico](semantic-types.md) es uno de los [tipos de formato de texto](text-format-types.md). Este tipo consta de una cadena de texto proporcionada por el usuario en el formato de un [identificador](identifier.md)de Windows Installer. La herramienta de combinación sustituye esta cadena en las plantillas especificadas en la columna valor de la [tabla ModuleSubstitution](modulesubstitution-table.md).

Para especificar un elemento configurable de este tipo, los autores de módulos deben escribir el nombre de la cadena de texto en la columna nombre, escribir "0" en la columna formato, escribir "identificador" en la columna tipo y dejar en blanco la columna ContextData de la [tabla ModuleConfiguration](moduleconfiguration-table.md). La cadena puede estar en cualquier lenguaje compatible con la página de códigos de la base de datos. Vea [control de páginas de códigos (Windows Installer)](code-page-handling-windows-installer-.md). NULL es un valor válido para la cadena de texto a menos que msmConfigItemNonNullable se haya incluido en el campo Attributes de la tabla ModuleConfiguration.

 

 



