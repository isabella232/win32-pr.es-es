---
description: El tipo de cuadro de diálogo de tipo semántico es uno de los tipos de formato de clave. Este tipo consta de una clave externa en la tabla de diálogo proporcionada por el usuario.
ms.assetid: 3656684a-de95-45e1-9c78-5c1cc8ca879a
title: Tipo de diálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39ed04dece5702d232f252caa7c0ee02e7576246
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667800"
---
# <a name="dialog-type"></a>Tipo de diálogo

El tipo de cuadro de diálogo de [tipo semántico](semantic-types.md) es uno de los [tipos de formato de clave](key-format-types.md). Este tipo consta de una clave externa en la [tabla de diálogo](dialog-table.md) proporcionada por el usuario.

La herramienta de combinación debe sustituir un [identificador](identifier.md) de Windows Installer válido para los elementos de este tipo. Mergemod.dll no aplica esta restricción y depende de la herramienta de combinación para asegurarse de que el usuario proporciona una clave válida en la tabla del cuadro de diálogo.

NULL es un valor válido para este tipo a menos que se haya incluido msmConfigItemNonNullable en el campo Attributes de la [tabla ModuleConfiguration](moduleconfiguration-table.md).

El tipo de cuadro de diálogo se puede usar con los siguientes tipos de ContextData.

**DialogNext ContextData**

Un módulo de combinación configurable puede usar este tipo para permitir que el usuario proporcione una clave externa en la tabla del cuadro de diálogo. Para especificar un elemento configurable de este tipo, los autores de módulos deben escribir el nombre del elemento configurable en la columna nombre, escriba "1" en la columna formato, escriba "cuadro de diálogo" en la columna tipo y escriba "DialogNext" en la columna ContextData de la [tabla ModuleConfiguration](moduleconfiguration-table.md).

**DialogPrev ContextData**

Un módulo de combinación configurable puede usar este tipo para permitir que el usuario proporcione una clave externa en la tabla del cuadro de diálogo. Para especificar un elemento configurable de este tipo, los autores de módulos deben escribir el nombre del elemento configurable en la columna nombre, escriba "1" en la columna formato, escriba "cuadro de diálogo" en la columna tipo y escriba "DialogPrev" en la columna ContextData de la tabla ModuleConfiguration.

 

 



