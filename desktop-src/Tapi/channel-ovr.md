---
description: Cada línea tiene uno o más canales. Normalmente, los proveedores de servicios controlan cómo se exponen los canales como direcciones a una aplicación y el usuario final o el servidor no requiere un conocimiento específico de los canales.
ms.assetid: 8c7d38e0-1863-461f-9225-7a0b419532a3
title: Canal (API de telefonía)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b793a23c945cad79c9e2401ab6944302e908fd73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104543006"
---
# <a name="channel-telephony-api"></a>Canal (API de telefonía)

Cada línea tiene uno o más canales. Normalmente, los proveedores de servicios controlan cómo se exponen los canales como direcciones a una aplicación y el usuario final o el servidor no requiere un conocimiento específico de los canales.

Los canales son idénticos y, por tanto, intercambiables. En POTS (servicio telefónico anterior), hay exactamente un canal en una línea y el canal se usa exclusivamente para la voz. Con ISDN, pueden existir al menos tres canales (y hasta un máximo de 30 o más) en una línea simultáneamente.

Cada canal puede tener su propia dirección, lo que significa que una línea podría tener tantas direcciones como el número de canales. La relación exacta entre los canales y las direcciones que se exponen a una aplicación depende de la implementación de un proveedor de servicios.

Algunos proveedores de servicios admiten la asignación de más de una dirección a un solo canal. En las líneas de POTS, varios sistemas hacen posibles varias direcciones, como el marcado entrante directo (DID) o el timbre distintivo, que son servicios de tarifa adicional que proporciona la compañía telefónica.

Muchas grandes corporaciones usan las llamadas entrantes. Antes de que una llamada esté conectada, su número de extensión de destino se señala a la PBX, lo que hace que la extensión suene en lugar del teléfono del operador. Un ejemplo de timbre distintivo en un hogar privado sería si los elementos primarios usaban una dirección, los secundarios y una tercera. Dado que solo una línea conecta la casa con la red telefónica, todos los teléfonos se conectan cuando aparece una llamada, pero el patrón de anillo es diferente en función del número marcado por la parte que realiza la llamada. Con timbres distintivos, las personas saben quién es la llamada entrante y el equipo de fax responde a sus llamadas al reconocer su propio estilo de timbre.

En ISDN, es posible que los distintos canales B no tengan direcciones independientes. Dado que estos canales B pueden estar en la misma dirección, es el proveedor de servicios (y no la aplicación o la persona que ha marcado el número) que asigna llamadas a estos canales.

 

 



