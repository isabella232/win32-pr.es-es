---
description: Cada línea tiene uno o varios canales. Normalmente, los proveedores de servicios controlan cómo se exponen los canales como direcciones a una aplicación y el usuario final o el servidor no requieren conocimientos específicos de los canales.
ms.assetid: 8c7d38e0-1863-461f-9225-7a0b419532a3
title: Canal (API de telefonía)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b793a23c945cad79c9e2401ab6944302e908fd73
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127264988"
---
# <a name="channel-telephony-api"></a>Canal (API de telefonía)

Cada línea tiene uno o varios canales. Normalmente, los proveedores de servicios controlan cómo se exponen los canales como direcciones a una aplicación y el usuario final o el servidor no requieren conocimientos específicos de los canales.

Los canales son idénticos y, por tanto, intercambiables. En POTS (Plain Old Telephone Service), existe exactamente un canal en una línea y el canal se usa exclusivamente para voz. Con ISDN, pueden existir al menos tres (y hasta 30 o más) canales en una línea simultáneamente.

Cada canal puede tener su propia dirección, lo que significa que una línea podría tener tantas direcciones como canales. La relación precisa entre los canales y las direcciones expuestas a una aplicación depende de la implementación de un proveedor de servicios.

Algunos proveedores de servicios admiten la asignación de más de una dirección a un único canal. En las líneas de POTS, varios sistemas hacen posibles varias direcciones, como la marcación directa interna (DID) o el anillo distintivo, que son servicios de tarifas adicionales que proporciona la empresa telefónica.

Muchas grandes empresas usan DID para las llamadas entrantes. Antes de que se conecte una llamada, su número de extensión de destino se señala a LA EXTENSIÓN, lo que hace que la extensión suene en lugar del teléfono del operador. Un ejemplo de anillo distintivo en una casa privada sería si los padres usaron una dirección, la otra para los hijos y un equipo de fax un tercero. Dado que solo una línea conecta la casa a la red telefónica, todos los teléfonos suenan cuando aparece una llamada, pero el patrón de anillo es diferente en función del número marcado por la parte que realiza la llamada. Con un anillo distintivo, las personas saben para quién es la llamada entrante y el equipo de fax responde a sus llamadas reconociendo su propio estilo de timbre.

En ISDN, es posible que los distintos canales B no tengan direcciones independientes. Dado que estos canales B pueden estar en la misma dirección, es el proveedor de servicios (y no la aplicación o una persona que ha marcado el número) el que asigna llamadas a estos canales.

 

 



