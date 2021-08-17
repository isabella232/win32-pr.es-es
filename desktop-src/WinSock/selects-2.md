---
description: En la interfaz de socket original de la distribución de software de Berkeley (BSD), la función select era el medio estándar (y solo) para obtener indicaciones de eventos de red.
ms.assetid: f7f42b03-1f89-4801-abf0-396ff8b61cae
title: Selecciona
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c075d2b8b18de79c25852eb0949cc727a8f3474e39392cf6e0a50fc60390d0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740927"
---
# <a name="selects"></a>Selecciona

En la interfaz de socket original de la distribución de software de Berkeley (BSD), la función [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) era el medio estándar (y solo) para obtener indicaciones de eventos de red. Para cada socket, se puede sondear o esperar información sobre el estado de lectura, escritura o error. Consulte [**WSPSelect para**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85)) obtener más información. Tenga en cuenta que este enfoque no puede obtener qos de FD de evento \_ de red.

 

 
