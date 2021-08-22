---
description: La interfaz IWebProxy define las siguientes propiedades.
ms.assetid: 449b19ec-dc95-40f7-87af-84fb7dacb328
title: Propiedades de IWebProxy
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b0dd5c6600f7fb8593f5cd47f5d02a45a84689bccb206359b8db8ffe6b320b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049133"
---
# <a name="iwebproxy-properties"></a>Propiedades de IWebProxy

La [**interfaz IWebProxy**](/windows/desktop/api/Wuapi/nn-wuapi-iwebproxy) define las siguientes propiedades.



| Propiedad                                                   | Descripción                                                                                                               |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**Dirección**](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_address)                       | Obtiene y establece la dirección y el número de puerto decimal del servidor proxy.                                                |
| [**Autodetect**](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_autodetect)                 | Obtiene y establece un valor booleano que indica si [**IWebProxy**](/windows/desktop/api/Wuapi/nn-wuapi-iwebproxy) detecta automáticamente la configuración del proxy. |
| [**BypassList**](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_bypasslist)                 | Obtiene y establece una colección de direcciones que no usan el servidor proxy.                                                 |
| [**BypassProxyOnLocal**](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_bypassproxyonlocal) | Obtiene y establece un valor booleano que indica si las direcciones locales omiten el servidor proxy.                             |
| [**Readonly**](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_readonly)                     | Obtiene un valor booleano que indica si el [**objeto WebProxy**](/windows/desktop/api/Wuapi/nn-wuapi-iwebproxy) es de solo lectura.                        |
| [**nombre de usuario**](/windows/desktop/api/Wuapi/nf-wuapi-iwebproxy-get_username)                     | Obtiene y establece el nombre de usuario que se va a enviar al servidor proxy para la autenticación.                                             |



 

 

 



