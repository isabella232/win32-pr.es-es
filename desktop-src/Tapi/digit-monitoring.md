---
description: La supervisión de dígitos supervisa la llamada de dígitos.
ms.assetid: 6ba28fdf-87d5-4d39-9e12-8201585a86ee
title: Supervisión de dígitos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2454f6886bba4e859348df929c1a35f10c3d481
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686634"
---
# <a name="digit-monitoring"></a>Supervisión de dígitos

La supervisión de dígitos supervisa la llamada de dígitos. TAPI permite que los dígitos se señalen de acuerdo con dos métodos (modos de dígito):

-   Los dígitos de pulsos se señalan como secuencias giratorias o con impulsos. Para la detección, estos impulsos se manifiestan como nada más que las secuencias de clics auditivos. Los dígitos de pulso válidos son de "0" a "9".
-   Los dígitos DTMF se señalan como tonos DTMF (frecuencia múltiple de tono dual). Los dígitos DTMF válidos son de ' 0 ' a ' 9 ', ' A '. ' B ', ' C ', ' d ', ' \* ' y ' \# '. Se pueden supervisar tanto el extremo inicial como el borde inferior de los dígitos DTMF.

Una aplicación puede habilitar o deshabilitar la supervisión de dígitos en una llamada especificada con [**lineMonitorDigits**](/windows/desktop/api/Tapi/nf-tapi-linemonitordigits). Cuando está habilitada la supervisión de dígitos, los dígitos detectados hacen que la aplicación reciba una notificación con el mensaje de [**línea \_ MONITORDIGITS**](line-monitordigits.md) . Este mensaje proporciona el identificador de llamada en el que se ha detectado el dígito, así como el valor de dígito y el modo de dígito. El ámbito de la supervisión de dígitos está limitado por la duración de la llamada. La supervisión de dígitos en una llamada finaliza en cuanto la llamada se *desconecta* o se queda *inactiva*.

 

 



