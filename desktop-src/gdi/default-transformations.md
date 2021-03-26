---
description: Cada vez que una aplicación crea un controlador de dominio y comienza inmediatamente a llamar a funciones de dibujo o de salida de GDI, aprovecha el espacio de página predeterminado para el espacio de dispositivo y el espacio de dispositivo a las transformaciones del área de cliente.
ms.assetid: 64465eb4-d23a-44e7-ad0d-060b195d37b3
title: Transformaciones predeterminadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab5f13c764a92c005fad36c9f2599b99a654284f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985003"
---
# <a name="default-transformations"></a>Transformaciones predeterminadas

Cada vez que una aplicación crea un controlador de dominio y comienza inmediatamente a llamar a funciones de dibujo o de salida de GDI, aprovecha el espacio de página predeterminado para el espacio de dispositivo y el espacio de dispositivo a las transformaciones del área de cliente. No se puede realizar una transformación de espacio de página universal hasta que la aplicación llama primero a la función [**SetGraphicsMode**](/windows/desktop/api/Wingdi/nf-wingdi-setgraphicsmode) para establecer el modo en GM \_ Advanced y, a continuación, llama a la función [**SetWorldTransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) .

El uso de \_ texto mm (el espacio de página predeterminado para la transformación del espacio de dispositivo) da como resultado una asignación de uno a uno, es decir, un punto determinado en el espacio de la página se asigna al mismo punto en el espacio del dispositivo. Como se mencionó anteriormente, esta transformación no se especifica mediante una matriz. En su lugar, se obtiene dividiendo el ancho de la ventanilla por el ancho de la ventana y el alto de la ventanilla por el alto de la ventana. En el caso predeterminado, las dimensiones de la ventanilla son de 1 píxel por 1 píxel y las dimensiones de la ventana son una unidad de 1 página por unidad de página.

La transformación espacio de dispositivo en dispositivo físico (área de cliente, escritorio o impresora) siempre da como resultado una asignación uno a uno; es decir, una unidad en el espacio del dispositivo siempre es equivalente a una unidad en el área cliente, en el escritorio o en una página. El único propósito de esta transformación es la traducción; garantiza que la salida aparece correctamente en la ventana de una aplicación, independientemente de dónde se mueva esa ventana en el escritorio.

El aspecto único del texto MM \_ es la orientación del eje y en el espacio de la página. En \_ el texto mm, el eje y positivo se extiende hacia abajo y el eje y negativo se extiende hacia arriba.

 

 



