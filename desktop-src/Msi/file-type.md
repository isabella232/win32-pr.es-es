---
description: El tipo de archivo de tipo semántico es uno de los tipos de formato de clave. Este tipo consta de una clave externa en la tabla de archivos proporcionada por el usuario.
ms.assetid: cbcaa016-879e-48c2-93c6-b0e91e1eb9ed
title: Tipo de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36b47e76f4a910b336c749a4f0d5001c8568cead
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668073"
---
# <a name="file-type"></a>Tipo de archivo

El tipo de archivo de [tipo semántico](semantic-types.md) es uno de los [tipos de formato de clave](key-format-types.md). Este tipo consta de una clave externa en la [tabla de archivos](file-table.md) proporcionada por el usuario.

El tipo de archivo se puede usar con los siguientes tipos de ContextData.

**AssemblyContext ContextData**

Este tipo se puede usar para permitir que los usuarios configuren claves externas para los ensamblados de Common Language Runtime o Win32. La herramienta de fusión mediante combinación debe sustituir un [identificador](identifier.md) de Windows Installer para los elementos de este tipo en la plantilla de la columna valor de la [tabla ModuleSubstitution](modulesubstitution-table.md). Mergemod.dll no lo exige y depende de la herramienta de fusión mediante combinación para asegurarse de que el usuario proporciona una clave válida en la tabla de archivos.

NULL es un valor válido para este tipo a menos que se haya incluido msmConfigItemNonNullable en el campo Attributes de la [tabla ModuleConfiguration](moduleconfiguration-table.md).

 

 



