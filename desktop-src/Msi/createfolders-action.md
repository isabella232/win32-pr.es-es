---
description: La acción CreateFolders crea carpetas vacías para los componentes que están configurados para instalarse.
ms.assetid: 3982eac8-8272-4fb4-870c-390a0b6bd9a1
title: Acción CreateFolders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 349388bf07fe867fc2cd88df6b5c7a76d28a1bf2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158742"
---
# <a name="createfolders-action"></a>Acción CreateFolders

La acción CreateFolders crea carpetas vacías para los componentes que están configurados para instalarse. El instalador crea carpetas para los componentes que se ejecutan localmente y se ejecutan desde el origen. Las carpetas recién creadas se registran con el identificador de componente adecuado.

La acción CreateFolders consulta la [tabla CreateFolder y](createfolder-table.md) la [tabla Component](component-table.md).

## <a name="sequence-restrictions"></a>Restricciones de secuencia

La acción CreateFolders debe ejecutarse antes de la acción [InstallFiles](installfiles-action.md) o antes de cualquier acción que agrega archivos a carpetas.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de la descripción de los datos de acción |
|-------|----------------------------------------|
| \[1\] | Identificador de directorio de la carpeta.        |



 

## <a name="remarks"></a>Observaciones

El instalador no quita automáticamente las carpetas creadas por la acción CreateFolders durante una desinstalación de la aplicación. El instalador solo quita carpetas si la [acción RemoveFolders](removefolders-action.md) se incluye en la secuencia de acciones.

 

 



