---
description: La acción RemoveFolders quita todas las carpetas vinculadas a los componentes establecidos para quitarse o ejecutarse desde el origen. Estas carpetas solo se quitan si están vacías. Si se quita una carpeta, se anula el registro con el identificador de componente adecuado.
ms.assetid: 0f68458e-ae9a-4ca5-bc60-06d4de91e2e9
title: Acción RemoveFolders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b476de044ef48b50120575a8d6991d27bf063dec37a026a2f5d2ea0e604abee0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120082545"
---
# <a name="removefolders-action"></a>Acción RemoveFolders

La acción RemoveFolders quita todas las carpetas vinculadas a los componentes establecidos para quitarse o ejecutarse desde el origen. Estas carpetas solo se quitan si están vacías. Si se quita una carpeta, se anula el registro con el identificador de componente adecuado.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción RemoveFolders debe ir después de la [acción RemoveFiles](removefiles-action.md) o cualquier acción que pueda quitar archivos de las carpetas.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción    |
|-------|-------------------------------|
| \[1\] | Identificador de la carpeta quitada. |



 

## <a name="remarks"></a>Comentarios

El instalador no quita automáticamente las carpetas creadas por la [acción CreateFolders](createfolders-action.md) durante una desinstalación de la aplicación. Se debe indicar al instalador que quite estas carpetas mediante la creación de la acción RemoveFolders en la secuencia de acciones.

Para especificar el nombre y la ubicación de la carpeta, use la columna Directory \_ de la [tabla CreateFolder](createfolder-table.md). Se supone que cada nombre de carpeta de la tabla CreateFolder es una propiedad que define la ubicación de la carpeta.

Para especificar el componente que posee la carpeta, use la columna ComponentId de la [tabla Component](component-table.md).

 

 



