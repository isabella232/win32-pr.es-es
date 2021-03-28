---
description: La función GetDC se usa para llevar a cabo el dibujo que debe producirse de forma instantánea en lugar de cuando \_ se procesa un mensaje de pintura de WM.
ms.assetid: 75525e26-72f5-4a58-a663-0bbdc2034759
title: Usar la función GetDC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98c018228eccbce7b487444341481165e24214b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985347"
---
# <a name="using-the-getdc-function"></a>Usar la función GetDC

La función [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) se usa para llevar a cabo el dibujo que debe producirse de forma instantánea en lugar de cuando se procesa un mensaje de [**\_ pintura de WM**](wm-paint.md) . Este dibujo suele ser en respuesta a una acción por parte del usuario, como hacer una selección o dibujar con el mouse. En tales casos, el usuario debe recibir comentarios instantáneos y no debe verse obligado a detener la selección o el dibujo para que la aplicación muestre el resultado. En las secciones siguientes se muestra cómo usar GetDC para dibujar en una ventana:

-   [Dibujar con el mouse](drawing-with-the-mouse.md)
-   [Dibujar a intervalos de tiempo](drawing-at-timed-intervals.md)

 

 



