---
description: El tipo de enumeración de tipo semántico es uno de los tipos de formato de texto.
ms.assetid: fff01044-5749-42a5-b026-5b22671870bd
title: Enum (tipo)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc582a7f96d8fc91aad66387f579f05f9255346f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001607"
---
# <a name="enum-type"></a>Enum (tipo)

El tipo de enumeración de [tipo semántico](semantic-types.md) es uno de los [tipos de formato de texto](text-format-types.md). Este tipo consta de una cadena de texto elegida por el usuario a partir de un conjunto de opciones. La herramienta de combinación sustituye la cadena seleccionada seleccionada en las plantillas especificadas en la columna valor de la [tabla ModuleSubstitution](modulesubstitution-table.md).

Para especificar un elemento configurable de este tipo, los autores de módulos deben escribir el nombre de la cadena de texto en la columna nombre, escriba "0" en la columna formato, escriba "enum" en la columna tipo y escriba la lista de posibles cadenas en la columna ContextData de la [tabla ModuleConfiguration](moduleconfiguration-table.md). La lista de cadenas posibles se debe proporcionar como una lista de cadenas deliminated por punto y coma. Cada opción debe tener el formato "nombre = valor". Se puede Agregar un punto y coma literal al valor prefijando el punto y coma con un carácter de barra diagonal inversa. NULL es un valor válido a menos que se haya incluido msmConfigItemNonNullable en el campo Attributes de la tabla ModuleConfiguration.

 

 



