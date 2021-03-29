---
description: El tipo RTF de tipo semántico es uno de los tipos de formato de texto.
ms.assetid: 91fc47c1-520a-4002-9dbe-4ee2b56f84b3
title: Tipo RTF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a81c708183596d794f20e38bf89c073472e3affb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652738"
---
# <a name="rtf-type"></a>Tipo RTF

El tipo RTF de [tipo semántico](semantic-types.md) es uno de los [tipos de formato de texto](text-format-types.md). Este tipo consta de una cadena de texto arbitraria en formato de texto enriquecido (RTF) de cualquier longitud proporcionada por el usuario. La herramienta de combinación sustituye esta cadena en las plantillas especificadas en la columna valor de la [tabla ModuleSubstitution](modulesubstitution-table.md).

Para especificar un elemento configurable de este tipo, los autores de módulos deben escribir el nombre de la cadena de texto en la columna nombre, escribir "0" en la columna formato, escribir "RTF" en la columna tipo y dejar en blanco la columna ContextData de la [tabla ModuleConfiguration](moduleconfiguration-table.md). La cadena puede estar en cualquier lenguaje compatible con la página de códigos de la base de datos. Vea [control de páginas de códigos (Windows Installer)](code-page-handling-windows-installer-.md). NULL es un valor válido para la cadena de texto a menos que msmConfigItemNonNullable se haya incluido en el campo Attributes de la tabla ModuleConfiguration.

 

 



