---
description: Obtenga información sobre la extensibilidad constante. Las provisiones se realizan para extender las constantes y estructuras tanto de forma independiente del dispositivo como de una manera específica del dispositivo.
ms.assetid: 78430503-3e1f-49ab-be9c-d48bd21a840e
title: Extensibilidad constante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 975d2901dcc3f7e574ffdacdabbcf457821ef932
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409978"
---
# <a name="constant-extensibility"></a>Extensibilidad constante

Las provisiones se realizan para extender las constantes y estructuras tanto de forma independiente del dispositivo como de forma específica del dispositivo (específica del proveedor).

En las constantes que son enumeraciones escalares, se reserva un intervalo de valores para futuras extensiones comunes. El resto de valores se identifica como específico del dispositivo. Un proveedor puede definir los significados de estos valores de la manera deseada. La interpretación de estos valores se clave en el identificador de extensión proporcionado a través de la estructura de datos [**LINEDEVCAPS.**](/windows/win32/api/tapi/ns-tapi-linedevcaps) Para las constantes que se definen como marcas de bits, se reserva un intervalo de bits de orden bajo, donde los bits de orden superior pueden ser específicos de la extensión. Se recomienda que los valores extendidos y las matrices de bits usen bits del valor más alto o del bit de orden superior hacia abajo. Esto deja la opción de mover el borde entre la parte común y la parte de extensión si es necesario hacerlo en el futuro. A las extensiones de las estructuras de datos se les asigna un campo de tamaño variable con tamaño o desplazamiento como parte de la parte fija. TSPI describe qué extensiones específicas del dispositivo se permiten para cada estructura de datos. Para obtener más información, vea el tema [asignación de](./memory-allocation.md) memoria.

Además de reconocer un identificador de extensión específico, TAPI (que funciona en nombre de una aplicación) debe negociar el número de versión de extensión con el que funcionarán la aplicación y el proveedor de servicios. Esto se hace mediante las [**funciones \_ TSPI lineNegotiateExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiateextversion) y [**TSPI \_ phoneNegotiateExtVersion.**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiateextversion)

Un identificador de extensión es un identificador único global. No hay ningún registro central para los identificadores de extensión. En su lugar, el fabricante los genera localmente mediante una utilidad que está disponible con el kit de herramientas. Para garantizar la unidad global, el número se compone de partes como una dirección LAN (única), la hora del día y un número aleatorio. Los identificadores únicos globales están diseñados para distinguirse de los identificadores únicos universales de HP/DEC y, por tanto, son totalmente compatibles con ellos.

 

 
