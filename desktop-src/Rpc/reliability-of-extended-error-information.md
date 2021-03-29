---
title: Confiabilidad de la información de error extendida
description: La información de error extendida no es confiable.
ms.assetid: d4735a7b-ede0-4230-b10a-bf9772aca6a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c20edfbaa68f2a9ce80893f4f47bba33ec5ce595
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772859"
---
# <a name="reliability-of-extended-error-information"></a>Confiabilidad de la información de error extendida

La información de error extendida no es confiable. No se puede usar la información de error extendida para compilar la lógica de código. Es adecuado comprobar la presencia de información de error extendida y, si la hay, para volcar, guardar o registrar esa información. Pero no se basan en la información o su contenido.

Las siguientes razones explican por qué la información de error extendida no es confiable:

-   La secuencia y el contenido de los registros de error extendidos dependen de la arquitectura interna del sistema, que está sujeta a cambios. Una determinada operación puede pasar por NPFS en los sistemas actuales, pero mañana podría pasar a través de TCP. Estos componentes diferentes generan códigos de error muy diferentes y, por tanto, las comprobaciones de código son intrínsecamente poco confiables y no se recomiendan.
-   La propagación de la información de error extendida se puede deshabilitar, como se explicó anteriormente. Si se incluye código de detección, es probable que la aplicación deje de funcionar en ciertos entornos.
-   La propagación de la información de error extendida se realiza de la mejor manera posible. Puede producirse un error en la propagación o la generación de información de error extendida si no hay suficiente memoria en el equipo para procesar o propagar la cadena. En estas circunstancias, se quitará la cadena. Algunos protocolos tienen longitudes limitadas para los paquetes de error, ya que normalmente no incluyen mucha información. Si la longitud de la cadena supera la longitud permitida del paquete, el tiempo de ejecución de RPC comienza a quitar información de la cadena en un intento de ajustar la cadena al paquete. En primer lugar, el tiempo de ejecución quita los registros, empezando por el penúltimo registro y retrocediendo hasta que solo quedan los registros primero y último. Si la cadena sigue sin caber en un paquete, el tiempo de ejecución quita los parámetros de cadena y los nombres de equipo. Si se quita un parámetro de cadena, el tipo del parámetro se establece en none. Si se quita un registro, la marca EEInfoNextRecordsMissing se establece en el Registro siguiente y EEInfoPreviousRecordsMissing se establece en el registro anterior.

 

 




