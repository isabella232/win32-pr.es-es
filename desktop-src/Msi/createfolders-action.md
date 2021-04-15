---
description: La acción CreateFolders crea carpetas vacías para los componentes que están configurados para instalarse.
ms.assetid: 3982eac8-8272-4fb4-870c-390a0b6bd9a1
title: Acción CreateFolders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 349388bf07fe867fc2cd88df6b5c7a76d28a1bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669927"
---
# <a name="createfolders-action"></a>Acción CreateFolders

La acción CreateFolders crea carpetas vacías para los componentes que están configurados para instalarse. El instalador crea carpetas para los componentes que se ejecutan localmente y se ejecutan desde el origen. Las carpetas recién creadas se registran con el identificador de componente adecuado.

La acción CreateFolders consulta la [tabla CreateFolder](createfolder-table.md) y la [tabla de componentes](component-table.md).

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción CreateFolders se debe ejecutar antes de la acción [InstallFiles](installfiles-action.md) o antes de cualquier acción que agregue archivos a carpetas.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de la descripción de los datos de la acción |
|-------|----------------------------------------|
| \[1\] | Identificador de directorio de la carpeta.        |



 

## <a name="remarks"></a>Observaciones

El instalador no quita automáticamente las carpetas creadas por la acción CreateFolders durante la desinstalación de la aplicación. El instalador solo quita las carpetas si la [acción RemoveFolders](removefolders-action.md) se incluye en la secuencia de acción.

 

 



