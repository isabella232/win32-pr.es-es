---
description: El tipo de archivo de tipo semántico es uno de los tipos de formato de clave. Este tipo consta de una clave externa en la tabla File proporcionada por el usuario.
ms.assetid: cbcaa016-879e-48c2-93c6-b0e91e1eb9ed
title: Tipo de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36b47e76f4a910b336c749a4f0d5001c8568cead
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074794"
---
# <a name="file-type"></a>Tipo de archivo

El tipo de archivo de [tipo semántico](semantic-types.md) es uno de los [tipos de formato de clave](key-format-types.md). Este tipo consta de una clave externa en la [tabla File proporcionada](file-table.md) por el usuario.

El tipo de archivo se puede usar con los siguientes tipos de ContextData.

**AssemblyContext ContextData**

Este tipo se puede usar para permitir a los usuarios configurar claves externas en ensamblados de Win32 o Common Language Runtime. La herramienta de combinación debe sustituir un identificador Windows [instalador](identifier.md) por elementos de este tipo en la plantilla de la columna Valor de la [tabla ModuleSubstitution](modulesubstitution-table.md). Mergemod.dll no aplica esto y es la herramienta de combinación la que debe asegurarse de que el usuario proporciona una clave válida en la tabla File.

Null es un valor válido para este tipo a menos que msmConfigItemNonNullable se haya incluido en el campo Atributos de la [tabla ModuleConfiguration](moduleconfiguration-table.md).

 

 



