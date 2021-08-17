---
description: Obtenga información sobre la extensibilidad. Las provisiones se realizan para extender constantes y estructuras tanto de forma independiente del dispositivo como de una manera específica del dispositivo.
ms.assetid: bc0a18f3-1f58-4a24-8afb-c31f3b561375
title: Extensibilidad (API de telefonía)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89b9b130c27ffb01131181ad0b765d6a41b3eae0bbfc84cc2ab325c3a13230a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140678"
---
# <a name="extensibility"></a>Extensibilidad

Las provisiones se realizan para extender constantes y estructuras tanto de forma independiente del dispositivo como de forma específica del dispositivo (específica del proveedor). En las constantes que son enumeraciones escalares, se reserva un intervalo de valores para futuras extensiones comunes. El resto de valores se identifican como específicos del dispositivo. Un proveedor puede definir los significados de estos valores de la manera deseada. Su interpretación está clave en el identificador *de extensión* proporcionado en la estructura de [**datos LINEDEVCAPS.**](/windows/win32/api/tapi/ns-tapi-linedevcaps) Para las constantes que se definen como marcas de bits, se reserva un intervalo de bits de orden bajo, donde los bits de orden superior pueden ser específicos de la extensión. Se recomienda que los valores extendidos y las matrices de bits usen bits del valor más alto o bit de orden superior hacia abajo. Esto deja la opción de mover el borde entre la parte común y la parte de extensión si es necesario hacerlo en el futuro. A las extensiones de las estructuras de datos se les asigna un campo de tamaño variable con tamaño o desplazamiento como parte de la parte fija. TAPI describe para cada estructura de datos qué extensiones específicas del dispositivo se permiten.

Además de reconocer un identificador de extensión específico, la aplicación debe negociar el número de versión de la extensión en el que funcionan la aplicación y el proveedor de servicios. Esto se hace en la segunda fase de negociación de versiones de la [**función lineGetDevCaps.**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps)

Un identificador de extensión es un identificador único global. No hay ningún registro central para los identificadores de extensión. En su lugar, el fabricante los genera localmente mediante una utilidad que está disponible con el kit de herramientas. El número se forma de partes, como una dirección LAN única, la hora del día y un número aleatorio, para garantizar la unidad global. Los identificadores únicos globales están diseñados para distinguirse de los identificadores únicos universales de HP/DEC y, por tanto, son totalmente compatibles con ellos.

 

 
