---
description: El tipo entero arbitrario de tipo semántico es uno de los tipos de formato entero.
ms.assetid: e35b27ca-be24-4aca-b12f-ca10ab153409
title: Tipo entero arbitrario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f55f7b7cd1c66d75a6f3aeeef1741168fad6675
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159105"
---
# <a name="arbitrary-integer-type"></a>Tipo entero arbitrario

El tipo entero arbitrario de tipo [semántico](semantic-types.md) es uno de los [tipos de formato entero](integer-format-types.md). Este tipo de elemento configurable es un entero proporcionado por el usuario. La herramienta de combinación sustituye este entero por las plantillas especificadas en la columna Valor de la [tabla ModuleSubstitution](modulesubstitution-table.md).

Para especificar un elemento configurable de este tipo, los autores de módulos deben escribir el nombre de la cadena de texto en la columna Nombre, escribir "2" en la columna Formato y dejar en blanco las columnas Type y ContextData de la [tabla ModuleConfiguration](moduleconfiguration-table.md). Las columnas Type y ContextData están reservadas y deben ser null.

 

 



