---
description: En la tabla siguiente se enumeran los GUID de propiedad de paquetes usados por la estructura PACKET \_ PROPERTY.
ms.assetid: d3e94b57-3078-4a84-b58a-faa31bdff79e
title: GUID de PacketProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c897e19aea30db6e5dfa026fbdcfec77de5afa4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481651"
---
# <a name="packetproperty-guids"></a>GUID de PacketProperty

En la tabla siguiente se enumeran los GUID de propiedad de paquetes usados por la [**estructura PACKET \_ PROPERTY.**](/windows/desktop/api/tpcshrd/ns-tpcshrd-packet_property)




| GUID | Descripción | 
|------|-------------|
| GUID_ALTITUDE_ORIENTATION<br /> | Ángulo entre el eje del lápiz y la superficie de la tableta. El valor es 0 cuando el lápiz es paralelo a la superficie y 90 cuando el lápiz está en paralelo a la superficie. Los valores son negativos cuando se invierte el lápiz.<br /> | 
| GUID_AZIMUTH_ORIENTATION<br /> | Rotación en el sentido de las agujas del reloj del cursor alrededor del eje Z a través de un intervalo circular completo.<br /> | 
| GUID_BOXNUMBER<br /> | GUID que se usa para recuperar el número de cuadro de un reconocimiento de entrada de lápiz alternativo cuando el reconocedor funciona en modo de cuadro.<br /> | 
| GUID_BUTTON_PRESSURE<br /> | Presión en un botón sensible a la presión.<br /> | 
| GUID_NORMAL_PRESSURE<br /> | GUID del objeto PacketProperty que representa la presión de la punta del lápiz a la superficie de la tableta. Mayor es la presión que se coloca en la punta del lápiz, más lápiz se dibuja.<br /> | 
| GUID_PACKET_STATUS<br /> | Contiene uno o varios de los siguientes valores de marca:<br /><ul><li>El cursor está tocándose la superficie de dibujo (Valor = 1).</li><li>El cursor se invierte. Por ejemplo, el extremo del borrador del lápiz apunta hacia la superficie (Valor = 2).</li><li>No se usa (valor = 4).</li><li>Se presiona el botón de botones (Valor = 8).</li></ul> | 
| GUID_PACKETPROPERTY_GUID_DEVICE_CONTACT_ID<br /> | Identificador de contacto del dispositivo para un paquete.<br /> | 
| GUID_SERIAL_NUMBER<br /> | Identifica el paquete. Este es el mismo valor que se usa para recuperar el paquete de la cola de paquetes.<br /> | 
| GUID_TANGENT_PRESSURE<br /> | GUID del objeto PacketProperty que representa la presión de la punta del lápiz a lo largo del plano de la superficie de la tableta.<br /> | 
| GUID_TIMER_TICK<br /> | Hora en que se generó el paquete.<br /> | 
| GUID_TWIST_ORIENTATION<br /> | Rotación en el sentido de las agujas del reloj del cursor alrededor de su propio eje.<br /> | 
| GUID_X<br /> | Coordenada X en el espacio de coordenadas de la tableta. Cada paquete contiene esta propiedad de forma predeterminada. El origen (0,0) de la tableta es la esquina superior izquierda.<br /> | 
| GUID_X_TILT_ORIENTATION<br /> | Para un cursor de lápiz, la orientación de inclinación X es el ángulo entre el plano y, z y el plano del lápiz y del eje Y. El valor es 0 cuando el lápiz está situado en la superficie de dibujo y es positivo cuando el lápiz está a la derecha de la ventana.<br /> | 
| GUID_Y<br /> | Coordenada Y en el espacio de coordenadas de la tableta. Cada paquete contiene esta propiedad de forma predeterminada. El origen (0,0) de la tableta es la esquina superior izquierda.<br /> | 
| GUID_Y_TILT_ORIENTATION<br /> | Para un cursor de lápiz, la orientación de inclinación y es el ángulo entre el plano x, z y el lápiz y el plano del eje X. El valor es 0 cuando el lápiz está cerca de la superficie de dibujo y es positivo cuando el lápiz está hacia arriba o lejos del usuario.<br /> | 
| GUID_Z<br /> | Coordenada z o distancia de la punta del lápiz desde la superficie de la tableta. El <a href="/windows/desktop/api/tpcshrd/ne-tpcshrd-property_units"><strong>PROPERTY_UNITS</strong></a> de enumeración determina la unidad de medida de esta propiedad. <br /> | 




 

> [!Note]  
> El campo TangentPressure representa la presión a lo largo del plano de la superficie de la tableta; El campo NormalPressure representa la presión en el plano de la superficie de la tableta.

 

 

 




