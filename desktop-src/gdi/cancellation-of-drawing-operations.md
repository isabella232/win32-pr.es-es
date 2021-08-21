---
description: Cuando las aplicaciones de dibujo complejas realizan operaciones de gráficos largas, consumen recursos valiosos del sistema.
ms.assetid: 3beef852-27fe-4ee2-b38b-3dc50e5d2fcf
title: Cancelación de operaciones de dibujo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ee2ddf90842ed7da612e046f8cc44bc8972b236232f3757bd31a295377eafab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119470041"
---
# <a name="cancellation-of-drawing-operations"></a>Cancelación de operaciones de dibujo

Cuando las aplicaciones de dibujo complejas realizan operaciones de gráficos largas, consumen recursos valiosos del sistema. Al aprovechar las características de multitarea del sistema, una aplicación puede usar subprocesos y la [**función CancelDC**](/windows/desktop/api/Wingdi/nf-wingdi-canceldc) para administrar estas operaciones. Por ejemplo, si la operación de gráficos realizada por el subproceso A consume los recursos necesarios, el subproceso B puede llamar a la función CancelDC para detener esa operación.

 

 



