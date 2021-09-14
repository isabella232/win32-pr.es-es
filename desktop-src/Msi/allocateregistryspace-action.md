---
description: La acción AllocateRegistrySpace garantiza que la cantidad de espacio libre del Registro especificado por la propiedad AVAILABLEFREEREG existe en el Registro.
ms.assetid: bb6ac685-5ad8-48e6-9c03-9ca42268d727
title: Acción AllocateRegistrySpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e6f986561595c73bf3bb1188d899af3d3d7d528
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159152"
---
# <a name="allocateregistryspace-action"></a>Acción AllocateRegistrySpace

La acción AllocateRegistrySpace garantiza que la cantidad de espacio libre del Registro especificado por la [**propiedad AVAILABLEFREEREG**](availablefreereg.md) existe en el Registro.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

Se debe llamar a la acción AllocateRegistrySpace después [de InstallInitialize.](installinitialize-action.md) Es aconsejable programar AllocateRegistrySpace antes de todas las demás acciones para asegurarse de que hay suficiente espacio del Registro disponible para continuar.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción     |
|-------|--------------------------------|
| \[1\] | Espacio del Registro necesario en KB. |



 

 

 



