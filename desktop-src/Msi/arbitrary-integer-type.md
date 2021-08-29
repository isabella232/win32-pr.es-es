---
description: El tipo entero arbitrario de tipo semántico es uno de los tipos de formato entero.
ms.assetid: e35b27ca-be24-4aca-b12f-ca10ab153409
title: Tipo entero arbitrario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b965b623d2a0a213335086e9139a621fc093fc18bea2d1873faf68e4f24f2961
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821835"
---
# <a name="arbitrary-integer-type"></a>Tipo entero arbitrario

El tipo entero arbitrario de tipo [semántico](semantic-types.md) es uno de los [tipos de formato entero](integer-format-types.md). Este tipo de elemento configurable es un entero proporcionado por el usuario. La herramienta de combinación sustituye este entero por las plantillas especificadas en la columna Valor de la [tabla ModuleSubstitution](modulesubstitution-table.md).

Para especificar un elemento configurable de este tipo, los autores de módulos deben escribir el nombre de la cadena de texto en la columna Nombre, escribir "2" en la columna Formato y dejar en blanco las columnas Type y ContextData de la [tabla ModuleConfiguration](moduleconfiguration-table.md). Las columnas Type y ContextData están reservadas y deben ser NULL.

 

 



