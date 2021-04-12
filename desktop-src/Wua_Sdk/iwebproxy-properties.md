---
description: La interfaz IWebProxy define las siguientes propiedades.
ms.assetid: 449b19ec-dc95-40f7-87af-84fb7dacb328
title: Propiedades de IWebProxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96628e7c799232b741e1834964a3a8ef6f6264c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423667"
---
# <a name="iwebproxy-properties"></a>Propiedades de IWebProxy

La interfaz [**IWebProxy**](/windows/desktop/api/Wuapi/nn-wuapi-iwebproxy) define las siguientes propiedades.



| Propiedad                                                   | Descripción                                                                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**Dirección**](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_address)                       | Obtiene y establece la dirección y el número de Puerto decimal del servidor proxy.                                                |
| [**Detección automática**](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_autodetect)                 | Obtiene y establece un valor booleano que indica si [**IWebProxy**](/windows/desktop/api/Wuapi/nn-wuapi-iwebproxy) detecta automáticamente la configuración de proxy. |
| [**BypassList**](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_bypasslist)                 | Obtiene y establece una colección de direcciones que no utilizan el servidor proxy.                                                 |
| [**BypassProxyOnLocal**](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_bypassproxyonlocal) | Obtiene y establece un valor booleano que indica si las direcciones locales omiten el servidor proxy.                             |
| [**ReadOnly**](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_readonly)                     | Obtiene un valor booleano que indica si el objeto [**WebProxy**](/windows/desktop/api/Wuapi/nn-wuapi-iwebproxy) es de solo lectura.                        |
| [**Nombre**](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_username)                     | Obtiene y establece el nombre de usuario que se va a enviar al servidor proxy para la autenticación.                                             |



 

 

 



