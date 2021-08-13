---
description: La acción AllocateRegistrySpace garantiza que la cantidad de espacio libre del Registro especificado por la propiedad AVAILABLEFREEREG existe en el Registro.
ms.assetid: bb6ac685-5ad8-48e6-9c03-9ca42268d727
title: Acción AllocateRegistrySpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40e47a0a0ebc3edec4605cbfac45443e4d30ee25df82ad3eaeb9da9ec9d3a94b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118639583"
---
# <a name="allocateregistryspace-action"></a>Acción AllocateRegistrySpace

La acción AllocateRegistrySpace garantiza que la cantidad de espacio libre del Registro especificado por la propiedad [**AVAILABLEFREEREG**](availablefreereg.md) existe en el registro.

## <a name="sequence-restrictions"></a>Restricciones de secuencia

Se debe llamar a la acción AllocateRegistrySpace después [de InstallInitialize.](installinitialize-action.md) Es aconsejable programar AllocateRegistrySpace antes de todas las demás acciones para asegurarse de que hay suficiente espacio del Registro disponible para continuar.

## <a name="actiondata-messages"></a>Mensajes ActionData



| Campo | Descripción de los datos de acción     |
|-------|--------------------------------|
| \[1\] | Espacio del Registro necesario en KB. |



 

 

 



