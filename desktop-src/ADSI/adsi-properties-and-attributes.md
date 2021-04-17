---
title: Propiedades y atributos ADSI
description: Los atributos a veces se denominan propiedades. Esto puede causar confusión. En esta documentación se usan las siguientes definiciones para propiedades y atributos.
ms.assetid: 8e391d36-5a8d-4960-805a-0caf281cab80
ms.tgt_platform: multiple
keywords:
- Propiedades ADSI y atributos ADSI
- ADSI ADSI, uso, acceso y manipulación de datos, propiedades y atributos
- ADSI de propiedades
- atributos ADSI
- propiedades ADSI, definidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10c7b1dca9882f53b7fa746121ed431ace7f9af7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656199"
---
# <a name="adsi-properties-and-attributes"></a>Propiedades y atributos ADSI

Los atributos a veces se denominan propiedades. Esto puede causar confusión. En esta documentación se usan las siguientes definiciones para propiedades y atributos.

Las propiedades son valores con nombre asociados a un objeto de programación. Por ejemplo, la interfaz [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) expone propiedades como [**Class**](iads-property-methods.md) y **Name**.

Los atributos son los datos asociados a los objetos de un servicio de directorio. Por ejemplo, un objeto de usuario tendrá un atributo denominado **CN** que contiene una cadena que es el nombre distintivo común o relativo del objeto. Se puede obtener acceso a los atributos a través de métodos de interfaz ADSI como [**IADs. Get**](/windows/desktop/api/Iads/nf-iads-iads-get) y [**IADs. put**](/windows/desktop/api/Iads/nf-iads-iads-put).

Para obtener más información acerca de las propiedades y los atributos ADSI, consulte:

-   [La caché de atributos ADSI](the-adsi-attribute-cache.md)
-   [Atributos de valor único frente a varios valores](single-vs--multiple-value-attributes.md)
-   [Active Directory atributos operativos](active-directory-operational-attributes.md)

 

 




