---
description: Se realizan disposiciones para extender constantes y estructuras de forma independiente del dispositivo y en una forma específica del dispositivo (específica del proveedor).
ms.assetid: 78430503-3e1f-49ab-be9c-d48bd21a840e
title: Extensibilidad constante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a470ccb52af1bdc92596ac42bbafb74d4821db1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687018"
---
# <a name="constant-extensibility"></a>Extensibilidad constante

Se realizan disposiciones para extender constantes y estructuras de forma independiente del dispositivo y en una forma específica del dispositivo (específica del proveedor).

En las constantes que son enumeraciones escalares, se reserva un intervalo de valores para futuras extensiones comunes. El resto de valores se identifica como específico del dispositivo. Un proveedor puede definir significados para estos valores de la forma que desee. La interpretación de estos valores se codifica en el identificador de extensión proporcionado a través de la estructura de datos [**LINEDEVCAPS**](/windows/win32/api/tapi/ns-tapi-linedevcaps) . En el caso de las constantes definidas como marcas de bits, se reserva un intervalo de bits de orden inferior, donde los bits de orden superior pueden ser específicos de la extensión. Se recomienda que los valores extendidos y las matrices de bits utilicen bits del valor más alto o del bit de orden superior. Esto deja la opción de desplazar el borde entre la parte común y la parte de la extensión si es necesario para hacerlo en el futuro. A las estructuras de datos se les asigna un campo de tamaño de variable con el tamaño o el desplazamiento que forman parte de la parte fija. TSPI describe las extensiones específicas del dispositivo que se permiten para cada estructura de datos. Para obtener más información, vea el tema [asignación de memoria](./memory-allocation.md) .

Además de reconocer un identificador de extensión específico, TAPI (que funciona en nombre de una aplicación) debe negociar el número de versión de la extensión en el que funcionarán la aplicación y el proveedor de servicios. Esto se realiza mediante las funciones [**TSPI \_ LineNegotiateExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiateextversion) y [**TSPI \_ phoneNegotiateExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiateextversion) .

Un identificador de extensión es un identificador único global. No hay ningún registro central para los identificadores de extensión. En su lugar, los genera localmente el fabricante una utilidad que está disponible con el kit de herramientas. Para garantizar la exclusividad global, el número se compone de elementos como una dirección LAN (única), una hora del día y un número aleatorio. Los identificadores únicos globales están diseñados para distinguirlos de los identificadores únicos universales de HP/DEC y, por lo tanto, son totalmente compatibles con ellos.

 

 
