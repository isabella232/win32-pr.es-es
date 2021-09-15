---
title: Confiabilidad de la información de error extendida
description: La información de error extendida no es confiable.
ms.assetid: d4735a7b-ede0-4230-b10a-bf9772aca6a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c20edfbaa68f2a9ce80893f4f47bba33ec5ce595
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473621"
---
# <a name="reliability-of-extended-error-information"></a>Confiabilidad de la información de error extendida

La información de error extendida no es confiable. La información de error extendida no se puede usar para compilar lógica de código. Es adecuado comprobar la presencia de información de error extendida y, si existe, volcar, guardar o registrar esa información. Pero no se base en la información ni en su contenido.

Las siguientes razones explican por qué la información de error extendida no es confiable:

-   La secuencia y el contenido de los registros de errores extendidos dependen de la arquitectura interna del sistema, que está sujeta a cambios. Una determinada operación puede pasar por NPFS en los sistemas actuales, pero mañana podría pasar por TCP. Estos componentes diferentes generan códigos de error muy diferentes y, por tanto, las comprobaciones de código son inherentemente poco confiables y no se recomiendan.
-   La propagación de la información de error extendida se puede deshabilitar, como se explicó anteriormente. Si se incluye código de detección, es probable que la aplicación deje de funcionar en determinados entornos.
-   La propagación de la información de error extendida se realiza de la mejor manera posible. La propagación o generación de información de error extendida puede producir un error si no hay suficiente memoria en el equipo para procesar o propagar la cadena. En tales circunstancias, se descartará la cadena. Algunos protocolos tienen longitudes limitadas para los paquetes de error, ya que normalmente no incluyen mucha información. Si la longitud de la cadena supera la longitud permitida del paquete, el tiempo de ejecución rpc comienza a quitar información de la cadena en un intento de ajustar la cadena al paquete. El tiempo de ejecución quita primero los registros, empezando por el penúltimo registro, retrocediendo hasta que solo permanecen el primero y el último. Si la cadena sigue sin caber en un paquete, el tiempo de ejecución quita los parámetros de cadena y los nombres de equipo. Si se descarta un parámetro de cadena, el tipo del parámetro se establece en none. Si se descarta un registro, la marca EEInfoNextRecordsMissing se establece en el registro siguiente y EEInfoPreviousRecordsMissing se establece en el registro anterior.

 

 




