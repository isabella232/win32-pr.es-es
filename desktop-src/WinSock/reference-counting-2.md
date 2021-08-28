---
description: Un proceso puede llamar a WSPCloseSocket en un socket duplicado y el descriptor se desasignará. Sin embargo, el socket subyacente permanecerá abierto hasta que se llame a WSPCloseSocket en el último descriptor restante.
ms.assetid: dff1e932-5e87-4ec5-995d-686d20ba6236
title: Recuento de referencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c8cd281363636cc2022725b4921d3b2d2b300e7262173e157a2be1610f6af0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996665"
---
# <a name="reference-counting"></a>Recuento de referencias

Un proceso puede llamar a [**WSPCloseSocket en**](/previous-versions/windows/hardware/network/ff566273(v=vs.85)) un socket duplicado y el descriptor se desasignará. Sin embargo, el socket subyacente permanecerá abierto hasta que se llame a **WSPCloseSocket** en el último descriptor restante.

 

 
