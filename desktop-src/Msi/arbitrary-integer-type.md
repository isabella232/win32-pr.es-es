---
description: El tipo entero arbitrario de tipo semántico es uno de los tipos de formato entero.
ms.assetid: e35b27ca-be24-4aca-b12f-ca10ab153409
title: Tipo de entero arbitrario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f55f7b7cd1c66d75a6f3aeeef1741168fad6675
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156340"
---
# <a name="arbitrary-integer-type"></a>Tipo de entero arbitrario

El tipo entero arbitrario de [tipo semántico](semantic-types.md) es uno de los [tipos de formato entero](integer-format-types.md). Este tipo de elemento configurable es un entero proporcionado por el usuario. La herramienta de combinación sustituye este entero en las plantillas especificadas en la columna valor de la [tabla ModuleSubstitution](modulesubstitution-table.md).

Para especificar un elemento configurable de este tipo, los autores de módulos deben escribir el nombre de la cadena de texto en la columna nombre, escribir "2" en la columna formato y dejar en blanco las columnas Type y ContextData de la [tabla ModuleConfiguration](moduleconfiguration-table.md). Las columnas Type y ContextData están reservadas y deben ser null.

 

 



