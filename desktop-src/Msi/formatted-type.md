---
description: El tipo con formato de tipo semántico es uno de los tipos de formato de texto.
ms.assetid: 44af5b5c-bbf9-4043-8076-0881680a36c1
title: Tipo con formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b97e0c0c1763352f75424bf54d01f6871604f51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082336"
---
# <a name="formatted-type"></a>Tipo con formato

El tipo con formato de [tipo semántico](semantic-types.md) es uno de los [tipos de formato de texto](text-format-types.md). Este tipo consta de una cadena de texto arbitraria de cualquier longitud proporcionada por el usuario y en el formato de texto con formato de Windows Installer. Para obtener más información, vea [con formato](formatted.md). La herramienta de combinación sustituye esta cadena en las plantillas especificadas en la columna valor de la [tabla ModuleSubstitution](modulesubstitution-table.md).

Para especificar un elemento configurable de este tipo, los autores de módulos deben escribir el nombre de la cadena de texto en la columna nombre, escribir "0" en la columna formato, escribir "con formato" en la columna tipo y dejar en blanco la columna ContextData de la [tabla ModuleConfiguration](moduleconfiguration-table.md). La cadena puede estar en cualquier lenguaje compatible con la página de códigos de la base de datos. Para obtener más información, vea [control de páginas de códigos (Windows Installer)](code-page-handling-windows-installer-.md). NULL es un valor válido para la cadena de texto a menos que msmConfigItemNonNullable se haya incluido en el campo Attributes de la tabla ModuleConfiguration.

 

 



