---
title: Uso de la interfaz IDirectoryObject
description: Al crear un cliente ADSI en C o C++ que usa el enlace temprano, tendrá una variedad más amplia de tipos de datos ADSI disponibles para su cliente si llama a la interfaz IDirectoryObject en lugar de a la interfaz IADs.
ms.assetid: d2c706ed-a341-4c49-91da-70230192f055
ms.tgt_platform: multiple
keywords:
- IDirectoryObject ADSI , mediante
- ADSI ADSI , mediante, mediante la interfaz IDirectoryObject
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d085344e5d2d1afe975dd347ff9e9cf4cdad99c1177819e0094b7a83f2219fb8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023092"
---
# <a name="using-the-idirectoryobject-interface"></a>Uso de la interfaz IDirectoryObject

Al crear un cliente ADSI en C o C++ que usa el enlace temprano, tendrá una variedad más amplia de tipos de datos ADSI disponibles para su cliente si llama a la interfaz [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) en lugar de a la interfaz [**IADs.**](/windows/desktop/api/Iads/nn-iads-iads) La **interfaz IDirectoryObject** proporciona métodos para admitir un subconjunto de las propiedades de mantenimiento de un objeto y acceder a sus atributos. En la ilustración siguiente se muestran las relaciones entre las estructuras de datos.

![Estructuras de datos de interfaz idirectoryobject](images/ds2dso.png)

En la ilustración anterior, la estructura [**ADS \_ OBJECT \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_object_info) define propiedades que identifican el objeto por nombre distintivo, nombre distintivo relativo, por contenedor (ParentDN), por tipo de objeto (ClassDN) y por definición de esquema (SchemaDN). El descriptor de [**atributo ADS \_ ATTR \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) consta de un nombre, un tipo de datos, una matriz de valores de datos que se muestran en [**ADSVALUE**](/windows/desktop/api/Iads/ns-iads-adsvalue)y una marca que indica al servicio de directorio subyacente que realice determinadas operaciones en los atributos detallados en [constantes \_ ATTR \_ \*](adsi-constants.md)de ADS. Los tipos de datos de estos atributos incluyen los tipos de sintaxis extendida adsi, que se detallan [**en ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum).

 

 




