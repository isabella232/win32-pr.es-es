---
title: Arquitectura de interfaces de servicio Active Directory
description: Muchos servicios de directorio son jerárquicos y, por tanto, se prestan a un modelo jerárquico de objetos. En esta sección se usan representaciones de objetos COM para ilustrar diversas características de ADSI.
ms.assetid: ef545aea-a7a5-4f65-9133-e68b94a86311
ms.tgt_platform: multiple
keywords:
- Active Directory arquitectura de interfaces de servicio ADSI
- ADSI ADSI, acerca de, arquitectura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce59d8d6281aa99bd96efa38166ef658972a5f54
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773032"
---
# <a name="active-directory-service-interfaces-architecture"></a>Arquitectura de interfaces de servicio Active Directory

Muchos servicios de directorio son jerárquicos y, por tanto, se prestan a un modelo jerárquico de objetos. En esta sección se usan representaciones de objetos COM para ilustrar diversas características de ADSI.

En la siguiente ilustración del modelo de objetos, un objeto de sistema de nivel superior contiene un objeto de espacio de nombres para cada proveedor ADSI instalado.

![namespaces (objeto contenedor)](images/ds2top.png)

Cada uno de los objetos de espacio de nombres es un contenedor que contiene los nodos raíz de nivel superior de cada servidor, dominio, o cualquier otro tipo de objetos del sistema de directorio definidos como raíces en cada servicio de directorio.

ADSI proporciona un conjunto de interfaces y objetos predefinidos para que las aplicaciones cliente puedan interactuar con los servicios de directorio mediante un conjunto uniforme de métodos. Sin embargo, es posible que ADSI no proporcione acceso a todas las características de un servicio de directorio. Para usar mejor el conjunto completo de características de cada servicio de directorio, ADSI proporciona un modelo de esquema que los proveedores de servicios de directorio y los proveedores de software de terceros pueden usar para extender las características más allá de las interfaces proporcionadas en ADSI.

Los objetos contenedores del nodo raíz, que se encuentran dentro de cada objeto de espacio de nombres del proveedor, incluyen un objeto contenedor de esquema ADSI. Este objeto contiene la definición de todas las características de ese proveedor. Para obtener más información, vea [modelo de esquema ADSI](adsi-schema-model.md).

Esta sección contiene los siguientes temas:

-   [Active Directory objetos de interfaces de servicio](active-directory-service-interfaces-objects.md)
-   [Espacios de nombres](namespaces.md)
-   [Proveedor de interfaces de servicio Active Directory](active-directory-service-interfaces-provider.md)
-   [Modelo de esquema ADSI](adsi-schema-model.md)

 

 




