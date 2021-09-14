---
description: El tipo de texto arbitrario de tipo semántico es uno de los tipos de formato de texto.
ms.assetid: 503ad2db-0875-4d8b-90f7-3d04318a6b62
title: Tipo de texto arbitrario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9709a560398472fe79a2c77db827acdfa7994148
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159101"
---
# <a name="arbitrary-text-type"></a>Tipo de texto arbitrario

El tipo de texto arbitrario de [tipo semántico](semantic-types.md) es uno de los [tipos de formato de texto](text-format-types.md). Este tipo consta de una cadena de texto arbitraria de cualquier longitud proporcionada por el usuario. La herramienta de combinación sustituye esta cadena arbitraria en las plantillas especificadas en la columna Valor de la [tabla ModuleSubstitution](modulesubstitution-table.md).

Para especificar un elemento configurable de este tipo, los autores de módulos deben escribir el nombre de la cadena de texto en la columna Nombre, escribir "0" en la columna Formato y dejar en blanco las columnas Type y ContextData de la [tabla ModuleConfiguration](moduleconfiguration-table.md). La cadena de texto arbitraria puede estar en cualquier idioma compatible con la página de códigos de la base de datos. Para obtener más información, vea [Control de páginas de códigos (Windows instalador).](code-page-handling-windows-installer-.md) Null es un valor válido para la cadena de texto a menos que msmConfigItemNonNullable se haya incluido en el campo Atributos de la tabla ModuleConfiguration.

 

 



