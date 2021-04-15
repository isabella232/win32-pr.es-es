---
description: TAPI divide los servicios de comunicaciones en Basic, Supplemental y Extended. Consulte niveles de servicio de TAPI para obtener información adicional.
ms.assetid: e2e6b113-b6b0-43a1-ac95-6e8e188a6120
title: Niveles de servicio de TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d829199bdcfce350d82f3c56cbbf9414fc46b35b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104545638"
---
# <a name="tspi-levels-of-service"></a>Niveles de servicio de TSPI

TAPI divide los servicios de comunicaciones en Basic, Supplemental y Extended. Consulte [niveles de servicio de TAPI](./tapi-levels-of-service.md) para obtener información adicional.

Se requiere un TSP para implementar todas las funciones básicas de telefonía. [Las funciones de telefonía básicas de TSPI](tspi-basic-telephony-functions.md) contienen un resumen de estas funciones.

La telefonía complementaria incluye características que se encuentran en las PBX modernas, como la retención, la transferencia, la Conferencia, el parque, etc. Un proveedor de servicios debe proporcionar un servicio de telefonía suplementario solo si puede implementar el significado exacto tal y como se define en TAPI. Si no es así, la característica debe proporcionarse como un servicio de telefonía extendido. Todas las características complementarias son opcionales. Un proveedor de servicios especifica qué servicios admite a través de las respuestas a funciones como [**TSPI \_ LineGetDevCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps) o [**TSPI \_ lineGetAddressCaps**](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps). Un único servicio complementario puede estar formado por varias llamadas a funciones y mensajes. Los servicios de dispositivos telefónicos forman parte de la telefonía complementaria.

Los servicios de telefonía extendidos permiten a un proveedor implementar funciones específicas del dispositivo. El proveedor de servicios debe identificar de forma única las extensiones mediante el uso de un *identificador de extensión*. Las aplicaciones recuperan y usan este identificador único para determinar las extensiones que admite el proveedor de servicios.

Las extensiones se pueden aplicar a varios fabricantes. En TAPI se proporcionan funciones especiales y mensajes como [**lineDevSpecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific) y [**phoneDevSpecific**](/windows/win32/api/tapi/nf-tapi-phonedevspecific) . Se utilizan para permitir la extensión del conjunto de funciones (a diferencia de las enumeraciones, las marcas de bits y los miembros de la estructura de datos) admitidos por el proveedor de servicios. El proveedor de servicios también define los parámetros de cada función.

Un identificador se asigna a un conjunto de extensiones (antes de la distribución), no a cada instancia individual de una implementación de esas extensiones. La utilidad EXTIDGEN de TSPI genera identificadores de extensión únicos para los proveedores de servicios. Usa una dirección del adaptador Ethernet, un número aleatorio y la hora del día para generar un identificador, por lo que es muy poco probable que el identificador de la extensión resultante entre en conflicto con cualquier otro proveedor de servicios. Como resultado, no es necesario que los proveedores registren los identificadores de extensión.

La utilidad EXTIDGEN no genera identificadores de extensión a menos que el equipo en el que se ejecuta también ejecute NetBIOS u otro software de red.

 

 
