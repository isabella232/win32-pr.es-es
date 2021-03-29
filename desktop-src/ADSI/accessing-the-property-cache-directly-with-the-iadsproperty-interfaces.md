---
title: Obtener acceso a la memoria caché de propiedades con interfaces IADsProperty
description: Las interfaces IADsProperty se componen de IADsPropertyList, IADsPropertyEntry y IADsPropertyValue.
ms.assetid: ff15eb50-01ab-4b45-bcfd-1df01172f274
ms.tgt_platform: multiple
keywords:
- Acceso directo a la memoria caché de propiedades con las interfaces IADsProperty ADSI
- ADSI cache de propiedades
- ADSI de la caché de propiedades, usar interfaces IADsProperty para tener acceso a la memoria caché de propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b48cd8675f4c439e3d3597e2d4fa59dac57e0896
ms.sourcegitcommit: 460af18ea55f4b12d47d5b8d4b883896e21adf00
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/04/2019
ms.locfileid: "103994857"
---
# <a name="accessing-property-cache-with-iadsproperty-interfaces"></a>Obtener acceso a la memoria caché de propiedades con interfaces IADsProperty

Las interfaces [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) se componen de [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist), [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)y [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue). Estas interfaces proporcionan métodos para tener acceso y manipular directamente las propiedades de una memoria caché de objetos. Una propiedad se conoce como una entrada de propiedad y corresponde a un atributo definido en el esquema. Una entrada de propiedad puede tener uno o varios valores de propiedad. Un conjunto de entradas de propiedad se organiza como una lista de propiedades.

La interfaz [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) administra la lista de propiedades de un objeto ADSI. La interfaz [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) realiza esta operación para una entrada de propiedad. Del mismo modo, la interfaz [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) representa uno o varios valores de propiedad. Juntos, proporcionan un mecanismo para que los usuarios:

-   Trabajar directamente con la memoria caché de propiedades.
-   Trabajar con directorios que no contienen esquemas, como un servidor LDAP versión 2.

Las interfaces [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) \* funcionan estrictamente en la memoria caché de propiedades y no realizan ningún intento de cooperar con el servidor para recuperar o modificar los datos en el almacén persistente. Como tal, estas interfaces solo se usan para examinar y manipular propiedades en la memoria caché del cliente. Antes de utilizar estas interfaces, debe llamar explícitamente al método [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) o el método [**IADs:: GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) para cargar las propiedades del objeto en la memoria caché, si no se ha inicializado la memoria caché. Después de llamar a los métodos de estas interfaces, debe llamar a [**IADs:: SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) para conservar los cambios en el almacén de directorios subyacente.

Para obtener más información y un ejemplo de código que se puede usar para implementar estas interfaces, vea [el código de ejemplo para usar interfaces IADsProperty para tener acceso a la memoria caché de propiedades](example-code-for-using-iadsproperty-interfaces-to-access-the-property-cache.md).

 

 




