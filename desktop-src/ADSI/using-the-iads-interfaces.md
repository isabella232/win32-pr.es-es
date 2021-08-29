---
title: Uso de las interfaces de los IAD
description: ADSI, cada elemento de un servicio de directorio se representa mediante un objeto ADSI, que es un objeto del Modelo de objetos componentes (COM) que admite la interfaz IUnknown COM estándar, así como las interfaces IDispatch e IAD.
ms.assetid: bdbf2012-6863-4611-8173-6a3cd9c4960f
ms.tgt_platform: multiple
keywords:
- ADSI de IAD, mediante
- ADSI ADSI , mediante, mediante las interfaces de los IAD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f9759833e538292c6d6f472b05448d197a88164fadbb2ea2df64c4fe48669f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637524"
---
# <a name="using-the-iads-interfaces"></a>Uso de las interfaces de los IAD

ADSI, cada elemento de un servicio de directorio se representa mediante un objeto ADSI, que es un objeto del Modelo de objetos componentes (COM) que admite la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) COM estándar, así como las interfaces [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) e [**IADs.**](/windows/desktop/api/Iads/nn-iads-iads) **Los IAD proporciona** las funciones de mantenimiento básicas para los objetos ADSI.

Cada objeto ADSI debe admitir esta interfaz, que sirve para:

-   Proporcione la identificación de objetos por nombre, clase o ADsPath.
-   Identifique el contenedor de objetos que administra la creación y eliminación de objetos.
-   Obtenga la definición del esquema de objeto.
-   Cargue los atributos del objeto en la caché de propiedades y confirme los cambios en el almacén de directorios persistente.
-   Obtenga acceso y modifique los valores de atributo de objeto en la caché de propiedades.

La [**interfaz IADs**](/windows/desktop/api/Iads/nn-iads-iads) está diseñada para garantizar que los objetos ADSI proporcionan a los administradores de red y proveedores de servicios de directorio una representación eficaz y coherente de los distintos servicios de directorio subyacentes.

![Objeto adsi que admite la interfaz iads](images/ds2iads.png)

En la ilustración anterior se muestra un objeto ADSI genérico que admite las interfaces fundamentales [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsPropertyList,**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) [**IUnknown,**](/windows/win32/api/unknwn/nn-unknwn-iunknown) [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)e [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) Un objeto ADSI como este administra los datos del almacén de datos del servicio de directorio subyacente a través de las interfaces que admite. Estos datos se conocen como las propiedades del objeto y las rutinas que obtienen y establecen estas propiedades se conocen como métodos de propiedad. Las propiedades de solo lectura tienen un método de propiedad que obtiene el valor de propiedad. Las propiedades de lectura y escritura tienen dos métodos: método que establece el valor y otro que obtiene el valor. Las propiedades se implementan en cada objeto ADSI mediante una caché [de propiedades](the-adsi-attribute-cache.md). [**IADs::get \_ ADsPath**](iads-property-methods.md) e **IADs::p ut \_ ADsPath** son ejemplos de métodos de propiedad. Los métodos de propiedad no son evidentes Visual Basic y otros clientes de Automation que habilitan referencias directas a la propiedad. Por ejemplo, Visual Basic hace referencia a **IADs::ADsPath** directamente mediante la **sintaxis Object.ADsPath.** Para obtener más información, vea [Métodos de propiedad de interfaz](interface-property-methods.md).

Además, un objeto ADSI interactúa con otros objetos ADSI y directamente a un espacio de nombres a través de métodos. Los métodos se ejecutan inmediatamente. Algunos ejemplos de [**métodos son IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) e [**IADs::GetInfo.**](/windows/desktop/api/Iads/nf-iads-iads-getinfo)

Se accede a propiedades, métodos de propiedad y métodos a través de interfaces COM estándar.

Un objeto ADSI se identifica de forma única mediante su ADsPath. Por ejemplo, un ADsPath para el espacio de nombres LDAP es "LDAP://MyServer/DC=Fabrikam,DC=COM". Para obtener más información sobre ADsPaths, vea [Enlace ADSI.](binding-to-an-adsi-object.md) Para los programadores familiarizados con los monikers COM, esto es conceptualmente similar al nombre para mostrar del moniker COM.

Cualquier objeto ADSI que contenga otros objetos ADSI, denominado objeto contenedor ADSI, también admite la interfaz [**IADsContainer,**](/windows/desktop/api/Iads/nn-iads-iadscontainer) que proporciona métodos y propiedades que administran la creación, eliminación y enumeración de objetos ADSI contenidos en el objeto. En la ilustración siguiente se muestra un objeto contenedor ADSI.

![adsi container object](images/dsiadsc.png)

La mayoría de los objetos ADSI están contenidos por otros objetos. El único objeto ADSI sin contenedor primario es el objeto espacios de nombres **ADSI** de nivel superior ("ADS:").

El [**método IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) de un objeto contenedor almacena de forma persistente las propiedades almacenadas en caché del objeto contenedor ADSI en el almacenamiento, además de los objetos creados con el método [**IADsContainer::Create.**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) [**IADsContainer::D elete no**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete) afecta a la caché de propiedades, pero elimina el elemento de directorio del espacio de nombres subyacente representado por este objeto.

 

 