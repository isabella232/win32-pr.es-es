---
description: Un proceso puede llamar a WSPCloseSocket en un socket duplicado y el descriptor se desasignará. Sin embargo, el socket subyacente permanecerá abierto hasta que se llame a WSPCloseSocket en el último descriptor restante.
ms.assetid: dff1e932-5e87-4ec5-995d-686d20ba6236
title: Recuento de referencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72d9ef7b3e5e31cc7941d30c47f107fc068489ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696808"
---
# <a name="reference-counting"></a>Recuento de referencias

Un proceso puede llamar a [**WSPCloseSocket**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) en un socket duplicado y el descriptor se desasignará. Sin embargo, el socket subyacente permanecerá abierto hasta que se llame a **WSPCloseSocket** en el último descriptor restante.

 

 
