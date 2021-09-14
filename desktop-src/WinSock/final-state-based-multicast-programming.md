---
description: En esta sección se describe la programación de multidifusión basada en estado final mediante IOCTLs en lugar de opciones de socket. Para obtener información general sobre cómo la programación de multidifusión basada en estado final difiere de la programación de multidifusión basada en cambios, vea Programación de multidifusión.
ms.assetid: 71c05393-3f8c-42c0-9060-e0df9b5e2578
title: Programación de multidifusión basada en estado final
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6abfebfc7efe27f1c5a6d63312c376bd659dce57
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068281"
---
# <a name="final-state-based-multicast-programming"></a>Programación de multidifusión basada en estado final

En esta sección se describe la programación de multidifusión basada en estado final mediante IOCTLs en lugar de opciones de socket. Para obtener información general sobre cómo la programación de multidifusión basada en estado final difiere de la programación de multidifusión basada en cambios, vea Programación de [multidifusión.](multicast-programming.md)

En la tabla siguiente se describen las Windows IOCTLs de sockets que se usan para la programación de multidifusión en Windows. 

| IOCTL                       | Tipo de argumento                                   |
|-----------------------------|-------------------------------------------------|
| SIOCSMSFILTER               | [**GROUP \_ Filter (estructura)**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) |
| SIOCGMSFILTER               | [**GROUP \_ Filter (estructura)**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) |
| FILTRO DE \_ \_ MULTIDIFUSIÓN GET DE SIO \_ | [**ip \_ msfilter (estructura)**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter)   |
| FILTRO DE \_ MULTIDIFUSIÓN DE SIO \_ \_ SET | [**ip \_ msfilter (estructura)**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter)   |



 

Tenga en cuenta **que SIOCSMSFILTER** y **SIOCGMSFILTER** IOCTLS están disponibles en Windows Vista y versiones posteriores.

El uso de estas ICTL para la programación de multidifusión tiene ventajas de rendimiento al trabajar con listas de origen grandes. Para obtener más información sobre los parámetros y la configuración asociados al uso de SIO GET MULTICAST FILTER o \_ \_ \_ SIO \_ SET MULTICAST FILTER, \_ consulte \_ [**\_**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-group_filter) la página de referencia de GROUP FILTER. Para obtener más información sobre los parámetros y la configuración asociados con el uso de SIO GET MULTICAST FILTER o SIO SET MULTICAST FILTER, consulte la página de referencia \_ \_ de ip \_ \_ \_ \_ [**\_ msfilter.**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-ip_msfilter)

 

 



