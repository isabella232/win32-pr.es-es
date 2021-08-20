---
title: Propiedades y atributos adsi
description: A veces se hace referencia a los atributos como propiedades. Esto puede causar confusión. En esta documentación se usan las siguientes definiciones para propiedades y atributos.
ms.assetid: 8e391d36-5a8d-4960-805a-0caf281cab80
ms.tgt_platform: multiple
keywords:
- ADSI properties and attributes ADSI
- ADSI ADSI, uso, acceso y manipulación de datos, propiedades y atributos
- ADSI de propiedades
- adsi de atributos
- propiedades ADSI , definidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b05637cada9a62cee129e9645385233b4700cbf2762b9446ba9a871d1897d440
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082799"
---
# <a name="adsi-properties-and-attributes"></a>Propiedades y atributos adsi

A veces se hace referencia a los atributos como propiedades. Esto puede causar confusión. En esta documentación se usan las siguientes definiciones para propiedades y atributos.

Las propiedades son valores con nombre asociados a un objeto de programación. Por ejemplo, la [**interfaz IADs**](/windows/desktop/api/Iads/nn-iads-iads) expone propiedades como [**Class**](iads-property-methods.md) y **Name**.

Los atributos son los datos asociados a objetos de un servicio de directorio. Por ejemplo, un objeto de usuario tendrá un atributo denominado **cn** que contiene una cadena que es el nombre distintivo común o relativo del objeto. Los atributos son accesibles a través de métodos de interfaz ADSI [**como IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) e [**IADs.Put.**](/windows/desktop/api/Iads/nf-iads-iads-put)

Para obtener más información sobre las propiedades y atributos de ADSI, consulte:

-   [La caché de atributos ADSI](the-adsi-attribute-cache.md)
-   [Atributos de valor único frente a varios](single-vs--multiple-value-attributes.md)
-   [Active Directory atributos operativos](active-directory-operational-attributes.md)

 

 




