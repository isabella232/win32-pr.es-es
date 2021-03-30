---
description: '&\# 0034; Bit de bits&\# 0034; tipo sin solicitudes de contexto que el usuario proporciona un entero cuyo valor se utiliza para establecer uno o varios bits en un campo de bits. Este texto puede estar en cualquier lenguaje compatible con la página de códigos de la base de datos.'
ms.assetid: 28e1bdb9-a42d-46ce-ad24-71bc22e2d92a
title: Tipo de campo de bits arbitrario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6571b8585c94577927df8cfedaded802a67d125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156341"
---
# <a name="arbitrary-bitfield-type"></a>Tipo de campo de bits arbitrario

El tipo "campo de bits" sin solicitudes de contexto que el usuario proporciona un entero cuyo valor se usa para establecer uno o varios bits en un campo de bits. Este texto puede estar en cualquier lenguaje compatible con la página de códigos de la base de datos.

El tipo de campo de bits arbitrario de [tipo semántico](semantic-types.md) es uno de los tipos de campo de bits. Este tipo consta de un entero elegido por el usuario a partir de un conjunto de opciones. La herramienta de combinación sustituye el entero seleccionado en las plantillas especificadas en la columna valor de la [tabla ModuleSubstitution](modulesubstitution-table.md). Para especificar un elemento configurable de este tipo, los autores de módulos deben escribir el nombre del elemento en la columna nombre, escriba "3" en la columna formato, deje la columna tipo en blanco y escriba la lista de enteros posibles en la columna ContextData de la [tabla ModuleConfiguration](moduleconfiguration-table.md).

La columna de tipo está reservada y debe ser null. La entrada de la columna ContextData para todos los tipos de formato de campo de bits debe tener el formato " <mask> ;<Name>=<value>;<Name>=<value>.... ", donde <mask> es un valor entero que indica los bits de interés, <Name> es un nombre para mostrar localizable para la elección y <value> es un valor entero decimal. La columna de contexto está en uso en [formato especial CMsM](cmsm-special-format.md) y para todos los tipos de campo de bits. Se puede escribir un carácter literal "=" o ";" en el <Name> campo anteponiendo un carácter de barra diagonal inversa (" \\ ").

 

 



