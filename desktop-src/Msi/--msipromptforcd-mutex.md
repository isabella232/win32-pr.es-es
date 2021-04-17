---
description: La \_ \_ exclusión mutua MsiPromptForCD existe cuando el instalador solicita al usuario que inserte un CD-ROM.
ms.assetid: f6319cda-48ac-4351-8eb5-f326490e3aff
title: __MsiPromptForCD exclusión mutua
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e646b23a003d10cce29807297e56abaebf3d935
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667085"
---
# <a name="__msipromptforcd-mutex"></a>\_\_Exclusión mutua MsiPromptForCD

La \_ \_ exclusión mutua MsiPromptForCD existe cuando el instalador solicita al usuario que inserte un CD-ROM. Los programas de reproducción automática deben comprobar que la \_ \_ exclusión mutua MsiPromptForCD no está establecida actualmente antes de iniciarse. Tenga en cuenta que es posible que se produzca un aviso de CD-ROM antes de que exista la clave de progreso o la \_ exclusión mutua de MSIExecute.

 

 



