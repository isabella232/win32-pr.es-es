---
description: El tipo con formato de tipo semántico es uno de los tipos de formato de texto.
ms.assetid: 44af5b5c-bbf9-4043-8076-0881680a36c1
title: Tipo con formato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09fc535a48f6d2e89cc46fb0d64ee998b8c062d6c2a406b9d5b8801ef1b62293
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044335"
---
# <a name="formatted-type"></a>Tipo con formato

El tipo con formato de [tipo semántico](semantic-types.md) es uno de los tipos [de formato de texto](text-format-types.md). Este tipo consta de una cadena de texto arbitraria de cualquier longitud proporcionada por el usuario y en el formato de texto con formato Windows instalador. Para obtener más información, vea [Formatted](formatted.md). La herramienta de combinación sustituye esta cadena por las plantillas especificadas en la columna Valor de la [tabla ModuleSubstitution](modulesubstitution-table.md).

Para especificar un elemento configurable de este tipo, los autores del módulo deben escribir el nombre de la cadena de texto en la columna Nombre, escribir "0" en la columna Formato, escribir "Formatted" en la columna Tipo y dejar en blanco la columna ContextData de la [tabla ModuleConfiguration](moduleconfiguration-table.md). La cadena puede estar en cualquier idioma compatible con la página de códigos de la base de datos. Para obtener más información, vea [Control de páginas de códigos (Windows instalador).](code-page-handling-windows-installer-.md) Null es un valor válido para la cadena de texto a menos que msmConfigItemNonNullable se haya incluido en el campo Atributos de la tabla ModuleConfiguration.

 

 



