---
title: arquitectura Active Directory interfaces de servicio
description: Muchos servicios de directorio son jerárquicos y, por tanto, se presta a un modelo de objetos jerárquico. En esta sección se usan representaciones de objetos COM para ilustrar varias características de ADSI.
ms.assetid: ef545aea-a7a5-4f65-9133-e68b94a86311
ms.tgt_platform: multiple
keywords:
- Active Directory ADSI de arquitectura de interfaces de servicio
- ADSI ADSI , acerca de, arquitectura
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41afbc212edbea6491de4cae89f2c8b7c873019b6d5678c5bf1d5b531f519260
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024093"
---
# <a name="active-directory-service-interfaces-architecture"></a>arquitectura Active Directory interfaces de servicio

Muchos servicios de directorio son jerárquicos y, por tanto, se presta a un modelo de objetos jerárquico. En esta sección se usan representaciones de objetos COM para ilustrar varias características de ADSI.

En la siguiente ilustración del modelo de objetos, un objeto del sistema de nivel superior contiene un objeto Namespace para cada proveedor ADSI instalado.

![objeto contenedor namespaces](images/ds2top.png)

Cada uno de los objetos Namespace es en sí mismo un contenedor que contiene los nodos raíz de nivel superior de cada servidor, dominio o cualquier otro tipo de objetos del sistema de directorios que se definan como raíces en cada servicio de directorio.

ADSI proporciona un conjunto de objetos predefinidos e interfaces para que las aplicaciones cliente puedan interactuar con los servicios de directorio mediante un conjunto uniforme de métodos. Sin embargo, ADSI puede no proporcionar acceso a todas las características de un servicio de directorio. Para usar mejor el conjunto de características completo de cada servicio de directorio, ADSI proporciona un modelo de esquema que los proveedores de servicios de directorio y los proveedores de software de terceros pueden usar para ampliar las características más allá de las interfaces proporcionadas en ADSI.

Los objetos de contenedor de nodo raíz, que se encuentran dentro de cada objeto de espacio de nombres del proveedor, incluyen un objeto contenedor de esquema ADSI. Este objeto contiene la definición de todas las características de ese proveedor. Para obtener más información, vea [AdsI Schema Model](adsi-schema-model.md).

Esta sección contiene los siguientes temas:

-   [Active Directory objetos de interfaces de servicio](active-directory-service-interfaces-objects.md)
-   [Espacios de nombres](namespaces.md)
-   [Active Directory proveedor de interfaces de servicio](active-directory-service-interfaces-provider.md)
-   [Modelo de esquema ADSI](adsi-schema-model.md)

 

 




