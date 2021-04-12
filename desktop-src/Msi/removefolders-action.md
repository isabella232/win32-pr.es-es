---
description: La acción RemoveFolders quita todas las carpetas vinculadas a los componentes que se van a quitar o ejecutar desde el origen. Estas carpetas se quitan solo si están vacías. Si se quita una carpeta, se anula el registro con el identificador de componente adecuado.
ms.assetid: 0f68458e-ae9a-4ca5-bc60-06d4de91e2e9
title: Acción RemoveFolders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69648fbae333f0e7b989f2e989f0982d49736317
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277741"
---
# <a name="removefolders-action"></a>Acción RemoveFolders

La acción RemoveFolders quita todas las carpetas vinculadas a los componentes que se van a quitar o ejecutar desde el origen. Estas carpetas se quitan solo si están vacías. Si se quita una carpeta, se anula el registro con el identificador de componente adecuado.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción RemoveFolders debe aparecer después de la acción [RemoveFiles](removefiles-action.md) o cualquier acción que pueda quitar archivos de las carpetas.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción    |
|-------|-------------------------------|
| \[1\] | Identificador de la carpeta quitada. |



 

## <a name="remarks"></a>Observaciones

El instalador no quita automáticamente las carpetas creadas por la [acción CreateFolders](createfolders-action.md) durante la desinstalación de la aplicación. Se debe indicar al instalador que quite estas carpetas mediante la creación de la acción RemoveFolders en la secuencia de acción.

Para especificar el nombre y la ubicación de la carpeta, utilice la \_ columna directorio de la [tabla CreateFolder](createfolder-table.md). Se supone que cada nombre de carpeta de la tabla CreateFolder es una propiedad que define la ubicación de la carpeta.

Para especificar el componente propietario de la carpeta, utilice la columna ComponentId de la [tabla de componentes](component-table.md).

 

 



