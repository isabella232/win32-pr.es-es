---
description: El tipo enum de tipo semántico es uno de los tipos de formato de texto.
ms.assetid: fff01044-5749-42a5-b026-5b22671870bd
title: Tipo de enumeración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56c5df6b0f76cc789c148e841827a75e7184aca2892d7d6e2233843e26aac80f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869325"
---
# <a name="enum-type"></a>Tipo de enumeración

El tipo enum de [tipo semántico](semantic-types.md) es uno de los [tipos de formato de texto](text-format-types.md). Este tipo consta de una cadena de texto elegida por el usuario entre un conjunto de opciones. La herramienta de combinación sustituye la cadena seleccionada en las plantillas especificadas en la columna Valor de la [tabla ModuleSubstitution](modulesubstitution-table.md).

Para especificar un elemento configurable de este tipo, los autores de módulos deben escribir el nombre de la cadena de texto en la columna Nombre, escribir "0" en la columna Formato, escribir "Enumeración" en la columna Tipo y escribir la lista de cadenas posibles en la columna ContextData de la [tabla ModuleConfiguration](moduleconfiguration-table.md). La lista de cadenas posibles debe proporcionarse como una lista de cadenas deliminated por punto y coma. Cada opción debe tener el formato "Nombre=Valor". Se puede agregar un punto y coma literal al valor mediante el prefijo del punto y coma con un carácter de barra diagonal inversa. Null es un valor válido a menos que msmConfigItemNonNullable se haya incluido en el campo Atributos de la tabla ModuleConfiguration.

 

 



