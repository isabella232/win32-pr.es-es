---
description: Se realizan disposiciones para extender constantes y estructuras de forma independiente del dispositivo y en una forma específica del dispositivo (específica del proveedor).
ms.assetid: d30f80c3-3535-4d78-b0a1-c9a7389f8fd4
title: Extensibilidad de estructura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b00fcf80b1ecfb7cc4d31b9ff040b101707ae236
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688618"
---
# <a name="structure-extensibility"></a>Extensibilidad de estructura

Se realizan disposiciones para extender constantes y estructuras de forma independiente del dispositivo y en una forma específica del dispositivo (específica del proveedor).

En las constantes que son enumeraciones escalares, se reserva un intervalo de valores para futuras extensiones comunes. El resto de valores se identifica como específico del dispositivo. Un proveedor puede definir significados para estos valores de cualquier manera. La interpretación de estos valores se codifica en el *identificador de extensión* proporcionado a través de la estructura de datos [**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps) . En el caso de las constantes definidas como marcas de bits, se reserva un intervalo de bits de orden inferior, donde los bits de orden superior pueden ser específicos de la extensión. Se recomienda que los valores extendidos y las matrices de bits utilicen bits del valor más alto o del bit de orden superior. Esto deja la opción de desplazar el borde entre la parte común y la parte de la extensión si es necesario hacerlo en el futuro. A las estructuras de datos se les asigna un campo de tamaño de variable con el tamaño o el desplazamiento que forman parte de la parte fija. TSPI describe para cada estructura de datos qué extensiones específicas del dispositivo se permiten.

Además de reconocer un identificador de extensión específico, TAPI (que funciona en nombre de una aplicación) debe negociar el número de versión de la extensión en la que funciona la aplicación y el proveedor de servicios. Esto se realiza mediante las funciones [**TSPI \_ LineNegotiateExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiateextversion) y [**TSPI \_ phoneNegotiateExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiateextversion) .

Un identificador de extensión es un identificador único global. No hay ningún registro central para los identificadores de extensión. En su lugar, los genera localmente el fabricante una utilidad que está disponible con el kit de herramientas. El número se compone de elementos como una dirección LAN (única), una hora del día y un número aleatorio, para garantizar la exclusividad global. Los identificadores únicos globales están diseñados para distinguirlos de los identificadores únicos universales de HP/DEC y, por lo tanto, son totalmente compatibles con ellos.

 

 
