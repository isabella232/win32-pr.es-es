---
description: La acción DisableRollback deshabilita la reversión durante el resto de la instalación.
ms.assetid: 5510b393-1f2e-44ba-97f5-663674d55b20
title: Acción DisableRollback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 740e838a6dca2d97db616703faf24c590ab69bc4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158538"
---
# <a name="disablerollback-action"></a>Acción DisableRollback

La acción DisableRollback deshabilita [la reversión](rollback-installation.md) durante el resto de la instalación. La reversión solo está deshabilitada para las acciones que se secuencian después de la acción DisableRollback en las tablas de secuencia. La reversión está deshabilitada para toda la instalación si la acción DisableRollback se secuencia antes de [la acción InstallInitialize](installinitialize-action.md).

## <a name="sequence-restrictions"></a>Restricciones de secuencia

No hay restricciones de secuencia.

## <a name="actiondata-message"></a>Mensaje ActionData

No hay ningún mensaje ActionData.

 

 



