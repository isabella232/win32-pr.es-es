---
description: El tipo RTF de tipo semántico es uno de los tipos de formato de texto.
ms.assetid: 91fc47c1-520a-4002-9dbe-4ee2b56f84b3
title: Tipo RTF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 269b378644fbf41e906993097cea8bb4fb27f969cbda046aab59700896513774
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039695"
---
# <a name="rtf-type"></a>Tipo RTF

El tipo RTF de [tipo semántico](semantic-types.md) es uno de los tipos [de formato de texto](text-format-types.md). Este tipo consta de una cadena de texto arbitraria en formato de texto enriquecido (RTF) de cualquier longitud proporcionada por el usuario. La herramienta de combinación sustituye esta cadena en las plantillas especificadas en la columna Valor de la [tabla ModuleSubstitution](modulesubstitution-table.md).

Para especificar un elemento configurable de este tipo, los autores de módulos deben escribir el nombre de la cadena de texto en la columna Nombre, escribir "0" en la columna Formato, escribir "RTF" en la columna Tipo y dejar en blanco la columna ContextData de la tabla [ModuleConfiguration](moduleconfiguration-table.md). La cadena puede estar en cualquier idioma compatible con la página de códigos de la base de datos. Vea [Control de páginas de códigos (Windows instalador).](code-page-handling-windows-installer-.md) Null es un valor válido para la cadena de texto a menos que msmConfigItemNonNullable se haya incluido en el campo Atributos de la tabla ModuleConfiguration.

 

 



