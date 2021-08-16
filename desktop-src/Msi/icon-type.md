---
description: El tipo de icono de tipo semántico es uno de los tipos de formato de clave. Este tipo consta de una clave en la tabla Icono proporcionada por el usuario.
ms.assetid: 8e155846-cc29-43f4-b1f7-9880320edbec
title: Tipo de icono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28510eff674d1f25e632b1181943af70da73d9fc97a6a64ec5abd0807fe15cf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118634958"
---
# <a name="icon-type"></a>Tipo de icono

El tipo de icono [de tipo semántico](semantic-types.md) es uno de los [tipos de formato de clave](key-format-types.md). Este tipo consta de una clave en la tabla [Icono proporcionada](icon-table.md) por el usuario.

La herramienta de combinación debe sustituir un identificador Windows [instalador válido](identifier.md) para los elementos de este tipo. Mergemod.dll no aplica esta restricción y es la herramienta de combinación la que debe asegurarse de que el usuario proporciona una clave válida en la tabla Icono.

Null es un valor válido para este tipo a menos que msmConfigItemNonNullable se haya incluido en el campo Atributos de la [tabla ModuleConfiguration](moduleconfiguration-table.md).

El tipo Binary se puede usar con los siguientes tipos de ContextData.

**ShortcutIcon ContextData**

Un módulo de combinación configurable puede usar este tipo para permitir [](icon-table.md) al usuario proporcionar una clave externa a una fila de la tabla de iconos que contiene una imagen adecuada para su uso como icono de acceso directo. Para especificar un elemento configurable de este tipo, los autores del módulo deben escribir el nombre del elemento configurable en la columna Nombre, escribir "1" en la columna Formato, escribir "Icono" en la columna Tipo y escribir "ShorcutIcon" en la columna ContextData de la tabla ModuleConfiguration. Este tipo no es adecuado para su uso en una tabla de interfaz de usuario. Para modificar una clave de la tabla Icon de estas tablas, vea Icon ContextData en [Tipo binario.](binary-type.md)

 

 



