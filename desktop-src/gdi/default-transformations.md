---
description: Cada vez que una aplicación crea un controlador de dominio y comienza inmediatamente a llamar a funciones de dibujo o salida de GDI, aprovecha el espacio de página predeterminado para el espacio del dispositivo y el espacio del dispositivo para las transformaciones de área de cliente.
ms.assetid: 64465eb4-d23a-44e7-ad0d-060b195d37b3
title: Transformaciones predeterminadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ba34effd9d6d43ab3b0abc740250c58788a8ce2f1556e89c92b78af823e58c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119469685"
---
# <a name="default-transformations"></a>Transformaciones predeterminadas

Cada vez que una aplicación crea un controlador de dominio y comienza inmediatamente a llamar a funciones de dibujo o salida de GDI, aprovecha el espacio de página predeterminado para el espacio del dispositivo y el espacio del dispositivo para las transformaciones de área de cliente. No se puede producir una transformación de espacio de mundo a página hasta que la aplicación llama primero a la función [**SetGraphicsMode**](/windows/desktop/api/Wingdi/nf-wingdi-setgraphicsmode) para establecer el modo en GM ADVANCED y, a continuación, llama a la \_ [**función SetWorldTransform.**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform)

El uso de MM TEXT (la transformación de espacio de página predeterminada al espacio del dispositivo) da como resultado una asignación uno a uno; es decir, un punto determinado del espacio de página se asigna al mismo punto del espacio del \_ dispositivo. Como se mencionó anteriormente, esta transformación no se especifica mediante una matriz. En su lugar, se obtiene dividiendo el ancho de la ventanilla por el ancho de la ventana y el alto de la ventanilla por el alto de la ventana. En el caso predeterminado, las dimensiones de la ventanilla son de 1 píxel por 1 píxel y las dimensiones de ventana son de 1 página por unidad de 1 página.

La transformación de espacio de dispositivo a dispositivo físico (área de cliente, escritorio o papel de impresora) siempre da como resultado una asignación uno a uno. Es decir, una unidad en el espacio del dispositivo siempre es equivalente a una unidad en el área cliente, en el escritorio o en una página. El único propósito de esta transformación es la traducción; garantiza que la salida aparece correctamente en la ventana de una aplicación, independientemente de dónde se haya movido esa ventana en el escritorio.

El único aspecto de MM \_ TEXT es la orientación del eje Y en el espacio de página. En MM TEXT, el eje Y positivo se extiende hacia \_ abajo y el eje Y negativo se extiende hacia arriba.

 

 



