---
description: Obtenga información sobre la extensibilidad. Las provisiones se realizan para extender constantes y estructuras tanto de forma independiente del dispositivo como de forma específica del dispositivo.
ms.assetid: bc0a18f3-1f58-4a24-8afb-c31f3b561375
title: Extensibilidad (API de telefonía)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f29ad34b5156bdd652ab6b6f8901be7a2341bdc
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406568"
---
# <a name="extensibility"></a>Extensibilidad

Las provisiones se realizan para extender constantes y estructuras tanto de forma independiente del dispositivo como de forma específica del dispositivo (específica del proveedor). En las constantes que son enumeraciones escalares, se reserva un intervalo de valores para futuras extensiones comunes. El resto de valores se identifican como específicos del dispositivo. Un proveedor puede definir los significados de estos valores de la manera deseada. Su interpretación está clave en el identificador *de extensión* proporcionado en la estructura de datos [**LINEDEVCAPS.**](/windows/win32/api/tapi/ns-tapi-linedevcaps) En el caso de las constantes que se definen como marcas de bits, se reserva un intervalo de bits de orden bajo, donde los bits de orden superior pueden ser específicos de la extensión. Se recomienda que los valores extendidos y las matrices de bits usen bits del valor más alto o bit de orden superior hacia abajo. Esto deja la opción de mover el borde entre la parte común y la parte de extensión si es necesario hacerlo en el futuro. A las extensiones de las estructuras de datos se les asigna un campo de tamaño variable con tamaño o desplazamiento como parte de la parte fija. TAPI describe para cada estructura de datos qué extensiones específicas del dispositivo se permiten.

Además de reconocer un identificador de extensión específico, la aplicación debe negociar el número de versión de la extensión en el que funcionan la aplicación y el proveedor de servicios. Esto se hace en la segunda fase de negociación de versiones de la [**función lineGetDevCaps.**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps)

Un identificador de extensión es un identificador único global. No hay ningún registro central para los identificadores de extensión. En su lugar, el fabricante los genera localmente mediante una utilidad que está disponible con el kit de herramientas. El número se forma de partes, como una dirección LAN única, la hora del día y un número aleatorio, para garantizar la unidad global. Los identificadores únicos globales están diseñados para distinguirse de los identificadores únicos universales de HP/DEC y, por tanto, son totalmente compatibles con ellos.

 

 
