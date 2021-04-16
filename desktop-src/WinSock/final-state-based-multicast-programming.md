---
description: En esta sección se describe la programación de multidifusión basada en el estado final con ioctl en lugar de las opciones de socket. Para obtener información general sobre el modo en que la programación de multidifusión basada en el estado final difiere de la programación multidifusión basada en cambios, vea programación con multidifusión.
ms.assetid: 71c05393-3f8c-42c0-9060-e0df9b5e2578
title: Programación de multidifusión basada en el estado final
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6abfebfc7efe27f1c5a6d63312c376bd659dce57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705624"
---
# <a name="final-state-based-multicast-programming"></a>Programación de multidifusión basada en el estado final

En esta sección se describe la programación de multidifusión basada en el estado final con ioctl en lugar de las opciones de socket. Para obtener información general sobre el modo en que la programación de multidifusión basada en el estado final difiere de la programación multidifusión basada en cambios, vea [programación con multidifusión](multicast-programming.md).

En la tabla siguiente se describen los ioctl de Windows Sockets usados para la programación de multidifusión en Windows. 

| INSERCIÓN                       | Tipo de argumento                                   |
|-----------------------------|-------------------------------------------------|
| SIOCSMSFILTER               | [**Grupo \_ de**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) Estructura del filtro |
| SIOCGMSFILTER               | [**Grupo \_ de**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) Estructura del filtro |
| SIO \_ obtener \_ filtro de multidifusión \_ | estructura de [**\_ msfilter IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter)   |
| SIO \_ establecer \_ filtro de multidifusión \_ | estructura de [**\_ msfilter IP**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter)   |



 

Tenga en cuenta que los ioctl **SIOCSMSFILTER** y **SIOCGMSFILTER** están disponibles en Windows Vista y versiones posteriores.

El uso de estos ioctl para la programación multidifusión tiene ventajas de rendimiento al trabajar con listas de orígenes de gran tamaño. Para obtener más información acerca de los parámetros y la configuración asociados con el uso de SIO \_ Get \_ Multicast \_ Filter o SiO \_ set \_ Multicast \_ Filter, consulte la página de referencia del [**\_ filtro de grupo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) . Para obtener más información sobre los parámetros y la configuración asociados con el uso de SIO \_ Get \_ Multicast \_ Filter o el \_ filtro de \_ multidifusión set de \_ [**\_ msfilter**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter) , consulte la página de referencia de IP.

 

 



