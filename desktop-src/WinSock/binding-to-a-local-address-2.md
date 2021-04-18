---
description: Antes de que se pueda usar un socket para configurar una conexión o recibir una solicitud de conexión, debe enlazarse a una dirección local.
ms.assetid: 8767a209-e293-47cd-b503-ff4cffbf6fb4
title: Enlazar a una dirección local
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39aa022d17a8862e6092c52b18edd1539f2d95ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715138"
---
# <a name="binding-to-a-local-address"></a>Enlazar a una dirección local

Antes de que se pueda usar un socket para configurar una conexión o recibir una solicitud de conexión, debe enlazarse a una dirección local. Esto puede realizarse explícitamente mediante una llamada a [**WSPBind**](/previous-versions/windows/hardware/network/ff566268(v=vs.85))o implícitamente por [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) si el socket está sin enlazar cuando se llama a esta función.

 

 
