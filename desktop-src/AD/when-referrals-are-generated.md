---
title: Cuándo se generan las referencias
description: Una referencia es la forma en que un servidor de directorio comunica que no contiene los datos necesarios para completar una consulta, pero tiene una referencia a un servidor que puede contener los datos necesarios.
ms.assetid: 2c11a52a-26e2-4a50-a0a3-5463a0852b27
ms.tgt_platform: multiple
keywords:
- Active Directory de generación de referencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06e47c1e172f3eaed34dad452aa46847980cd66f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103904465"
---
# <a name="when-referrals-are-generated"></a>Cuándo se generan las referencias

Una referencia es la forma en que un servidor de directorio comunica que no contiene los datos necesarios para completar una consulta, pero tiene una referencia a un servidor que puede contener los datos necesarios. Tenga en cuenta que las referencias no se generan simplemente mediante solicitudes de consulta.

Las operaciones siguientes pueden dar lugar a una o varias referencias:

-   Enlazar a un servidor que no contiene el objeto especificado por el nombre distintivo solicitado, pero que tiene datos sobre un servidor o dominio que puede contener ese objeto. Para ADSI, esto puede ocurrir si la aplicación llama a [**ADsGetObject**](/windows/desktop/api/adshlp/nf-adshlp-adsgetobject) o [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject) para enlazar con un objeto que existe en otro dominio del bosque (referencia interna) o un contexto de nomenclatura totalmente independiente del bosque (referencia externa). Para la API LDAP, esto puede ocurrir al realizar operaciones de agregar, modificar, eliminar o buscar que especifican un objeto que existe en otro dominio del bosque (referencia interna) o un contexto de nomenclatura totalmente independiente del bosque (referencia externa).

    Si la resolución de nombres no encuentra un objeto localmente y no hay objetos **crossRef** para esa parte del espacio de nombres, el controlador de dominio intentará construir una referencia externa basada en los componentes de dominio del nombre distintivo. Por ejemplo, si una búsqueda se basa en "CN = a, CN = b, DC = c, DC = d, DC = e", el controlador de dominio construirá una referencia al servidor LDAP en la dirección DNS "c. d. e".

    Todos los controladores de dominio de Windows 2000 (que solo admiten la nomenclatura DC = para los componentes superiores) se reconocen entre sí, y no se requiere ninguna referencia cruzada externa para que un cliente se enlace desde un bosque a otro. Si otros servidores de directorio que no son de Windows 2000, como un servidor de Netscape, usan DC = naming y tienen un RR SRV adecuado registrado en DNS, también obtendrá la ventaja de las referencias automáticas. Si no es así, se debe agregar manualmente un objeto **crossRef** externo.

-   Realización de una búsqueda de subárbol en un dominio que contiene dominios subordinados en el bosque o dominios externos subordinados, esquemas o contenedores de configuración. Se creará una referencia al dominio subordinado, el dominio externo, el esquema o el contenedor de configuración. Si está habilitado el seguimiento de referencias, la referencia será transparente para el autor de la llamada.

 

 