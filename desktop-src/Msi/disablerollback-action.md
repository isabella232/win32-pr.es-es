---
description: La acción DisableRollback deshabilita la reversión durante el resto de la instalación.
ms.assetid: 5510b393-1f2e-44ba-97f5-663674d55b20
title: Acción DisableRollback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cbe500e3b810e5b06802e3a0face1da9b76441099a407882da08d5911a37d60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745375"
---
# <a name="disablerollback-action"></a>Acción DisableRollback

La acción DisableRollback deshabilita [la reversión](rollback-installation.md) durante el resto de la instalación. La reversión solo está deshabilitada para las acciones que se secuencian después de la acción DisableRollback en las tablas de secuencia. La reversión está deshabilitada para toda la instalación si la acción DisableRollback se secuencia antes de [la acción InstallInitialize](installinitialize-action.md).

## <a name="sequence-restrictions"></a>Restricciones de secuencia

No hay restricciones de secuencia.

## <a name="actiondata-message"></a>ActionData Message

No hay ningún mensaje ActionData.

 

 



