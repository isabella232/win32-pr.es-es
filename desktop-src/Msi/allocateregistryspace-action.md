---
description: La acción AllocateRegistrySpace garantiza que la cantidad de espacio libre en el registro especificado por la propiedad AVAILABLEFREEREG existe en el registro.
ms.assetid: bb6ac685-5ad8-48e6-9c03-9ca42268d727
title: Acción AllocateRegistrySpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e6f986561595c73bf3bb1188d899af3d3d7d528
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667047"
---
# <a name="allocateregistryspace-action"></a>Acción AllocateRegistrySpace

La acción AllocateRegistrySpace garantiza que la cantidad de espacio libre en el registro especificado por la propiedad [**AVAILABLEFREEREG**](availablefreereg.md) existe en el registro.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

Se debe llamar a la acción AllocateRegistrySpace después de [InstallInitialize](installinitialize-action.md). Es aconsejable programar el AllocateRegistrySpace antes de todas las demás acciones para asegurarse de que hay suficiente espacio disponible en el registro para continuar.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción     |
|-------|--------------------------------|
| \[1\] | Espacio del registro necesario en KB. |



 

 

 



