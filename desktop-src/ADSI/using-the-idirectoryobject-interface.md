---
title: Uso de la interfaz IDirectoryObject
description: Al crear un cliente ADSI en C o C++ que use el enlace en tiempo de compilación, tendrá una variedad más amplia de tipos de datos ADSI disponibles para su cliente si llama a la interfaz IDirectoryObject en lugar de a la interfaz IADs.
ms.assetid: d2c706ed-a341-4c49-91da-70230192f055
ms.tgt_platform: multiple
keywords:
- IDirectoryObject ADSI, usar
- ADSI ADSI, usar, uso de la interfaz IDirectoryObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3174402a629bc02df2b1fffe07cc8fba1d73193c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772894"
---
# <a name="using-the-idirectoryobject-interface"></a>Uso de la interfaz IDirectoryObject

Al crear un cliente ADSI en C o C++ que use el enlace en tiempo de compilación, tendrá una variedad más amplia de tipos de datos ADSI disponibles para su cliente si llama a la interfaz [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) en lugar de a la interfaz [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) . La interfaz **IDirectoryObject** proporciona métodos para admitir un subconjunto de las propiedades de mantenimiento de un objeto y para obtener acceso a sus atributos. En la siguiente ilustración se muestran las relaciones entre las estructuras de datos.

![estructuras de datos de la interfaz idirectoryobject](images/ds2dso.png)

En la ilustración anterior, la [**información de \_ objeto \_ de anuncios**](/windows/desktop/api/Iads/ns-iads-ads_object_info) de estructura define propiedades que identifican el objeto por nombre distintivo, nombre distintivo relativo, por contenedor (ParentDN), por tipo de objeto (ClassDN) y por definición de esquema (SchemaDN). El descriptor de atributo [**ADS \_ \_ información**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) de atributos consta de un nombre, un tipo de datos, una matriz de valores de datos que se muestra en [**ADSVALUE**](/windows/desktop/api/Iads/ns-iads-adsvalue)y una marca que dirige el servicio de directorio subyacente para realizar ciertas operaciones en los atributos detallados en las [ \_ \_ \* constantes de ATTR de ADS](adsi-constants.md). Entre los tipos de datos de estos atributos se incluyen los tipos de sintaxis extendida de ADSI, detallados en [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum).

 

 




