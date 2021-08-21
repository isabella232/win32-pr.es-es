---
title: Acceso a la caché de propiedades con interfaces IADsProperty
description: Las interfaces IADsProperty constan de IADsPropertyList, IADsPropertyEntry e IADsPropertyValue.
ms.assetid: ff15eb50-01ab-4b45-bcfd-1df01172f274
ms.tgt_platform: multiple
keywords:
- Acceso a la caché de propiedades directamente con los IADsProperty Interfaces ADSI
- ADSI de caché de propiedades
- ADSI de caché de propiedades, mediante interfaces IADsProperty para acceder a la caché de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a68cd77a10d6631b52e48ed19650dd5cd18dff0ee59ba2332db73b7fce1a8bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024123"
---
# <a name="accessing-property-cache-with-iadsproperty-interfaces"></a>Acceso a la caché de propiedades con interfaces IADsProperty

Las [**interfaces IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) constan de [**IADsPropertyList,**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)y [**IADsPropertyValue.**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) Estas interfaces proporcionan métodos para acceder directamente y manipular las propiedades de una caché de objetos. Una propiedad se conoce como entrada de propiedad y corresponde a un atributo definido en el esquema. Una entrada de propiedad puede tener uno o varios valores de propiedad. Un conjunto de entradas de propiedad se organizan como una lista de propiedades.

La [**interfaz IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) administra la lista de propiedades de un objeto ADSI. La [**interfaz IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) realiza esta operación para una entrada de propiedad. De forma similar, [**la interfaz IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) representa uno o varios valores de propiedad. Juntos, proporcionan un mecanismo para que los usuarios:

-   Trabaje directamente con la caché de propiedades.
-   Trabaje con directorios que no contengan esquemas, como un servidor LDAP versión 2.

Las [**interfaces IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) funcionan estrictamente en la caché de propiedades y no intentan colaborar con el servidor para recuperar o modificar los datos del \* almacén persistente. Por lo tanto, estas interfaces solo se usan para examinar y manipular propiedades en la memoria caché del cliente. Antes de usar estas interfaces, debe llamar al método [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) o al método [**IADs::GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) explícitamente para cargar las propiedades del objeto en la memoria caché, si no se ha inicializado la memoria caché. Después de llamar a los métodos de estas interfaces, debe llamar a [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) para conservar los cambios en el almacén de directorios subyacente.

Para obtener más información y un ejemplo de código que se puede usar para implementar estas interfaces, vea Ejemplo de código para usar [interfaces IADsProperty](example-code-for-using-iadsproperty-interfaces-to-access-the-property-cache.md)para acceder a la caché de propiedades .

 

 




