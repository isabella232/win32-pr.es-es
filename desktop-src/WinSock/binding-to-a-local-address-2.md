---
description: Para poder usar un socket para configurar una conexión o recibir una solicitud de conexión, debe enlazarse a una dirección local.
ms.assetid: 8767a209-e293-47cd-b503-ff4cffbf6fb4
title: Enlace a una dirección local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dd4691e6581cbe1a3a2dee21d7dc4e0a0672812121028c515ad192b30279f61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132758"
---
# <a name="binding-to-a-local-address"></a>Enlace a una dirección local

Para poder usar un socket para configurar una conexión o recibir una solicitud de conexión, debe enlazarse a una dirección local. Esto se podría hacer explícitamente llamando a [**WSPBind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85))o implícitamente mediante [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) si el socket está desenlazado cuando se llama a esta función.

 

 
