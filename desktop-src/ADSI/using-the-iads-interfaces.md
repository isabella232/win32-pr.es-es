---
title: Usar las interfaces IADs
description: ADSI, cada elemento de un servicio de directorio se representa mediante un objeto ADSI, que es un objeto de modelo de objetos componentes (COM) que admite la interfaz IUnknown COM estándar, así como las interfaces IDispatch e IADs.
ms.assetid: bdbf2012-6863-4611-8173-6a3cd9c4960f
ms.tgt_platform: multiple
keywords:
- ADSI de IADs, usar
- ADSI ADSI, usar, usar las interfaces de IADs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 878afa9350a45f18238bebb69df1a96eba52715e
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421418"
---
# <a name="using-the-iads-interfaces"></a>Usar las interfaces IADs

ADSI, cada elemento de un servicio de directorio se representa mediante un objeto ADSI, que es un objeto de modelo de objetos componentes (COM) que admite la interfaz [**IUNKNOWN**](/windows/win32/api/unknwn/nn-unknwn-iunknown) com estándar, así como las interfaces [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) e [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) . **IADs** proporciona las funciones de mantenimiento básicas para los objetos ADSI.

Cada objeto ADSI debe admitir esta interfaz, que sirve para:

-   Proporcione la identificación del objeto por nombre, clase o ADsPath.
-   Identifique el contenedor de objetos que administra la creación y eliminación de objetos.
-   Obtener la definición del esquema de objeto.
-   Cargue los atributos del objeto en la caché de propiedades y confirme los cambios en el almacén de directorios persistente.
-   Obtener acceso y modificar los valores de atributo del objeto en la memoria caché de propiedades.

La interfaz [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) está diseñada para garantizar que los objetos ADSI proporcionan a los administradores de red y proveedores de servicios de directorio una representación eficaz y coherente de varios servicios de directorio subyacentes.

![objeto ADSI compatible con la interfaz iAds](images/ds2iads.png)

En la ilustración anterior se muestra un objeto ADSI genérico que admite las interfaces básicas [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist), [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)y [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch). Un objeto ADSI como este administra los datos del almacén de datos del servicio de directorio subyacente a través de las interfaces que admite. Estos datos se conocen como las propiedades del objeto y las rutinas que obtienen y establecen estas propiedades se conocen como métodos de propiedad. Las propiedades de solo lectura tienen un método de propiedad que obtiene el valor de propiedad. Las propiedades de lectura y escritura tienen dos métodos: un método que establece el valor y otro que obtiene el valor. Las propiedades se implementan en cada objeto ADSI mediante una [caché de propiedades](the-adsi-attribute-cache.md). [**IADs:: get \_ ADsPath**](iads-property-methods.md) y **IADs::p el \_ ADsPath de UT** son ejemplos de métodos de propiedad. Los métodos de propiedad no son aparentes para Visual Basic y otros clientes de automatización que habilitan las referencias directas a la propiedad. Por ejemplo, Visual Basic hace referencia a **IADs:: ADsPath** directamente mediante la sintaxis **Object. ADsPath** . Para obtener más información, vea [métodos de propiedad de interfaz](interface-property-methods.md).

Además, un objeto ADSI interactúa con otros objetos ADSI y directamente con un espacio de nombres a través de métodos. Los métodos se ejecutan inmediatamente. Algunos ejemplos de métodos son [**IADs:: SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) y [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo).

Se tiene acceso a las propiedades, métodos de propiedad y métodos a través de interfaces COM estándar.

Un objeto ADSI se identifica de forma única mediante su ADsPath. Por ejemplo, un ADsPath para el espacio de nombres LDAP es "LDAP://MyServer/DC=Fabrikam,DC=COM". Para obtener más información sobre ADsPaths, consulte el [enlace de ADSI](binding-to-an-adsi-object.md). En el caso de los programadores familiarizados con monikers COM, es conceptualmente similar al nombre para mostrar del moniker COM.

Cualquier objeto ADSI que contenga otros objetos ADSI, denominado un objeto contenedor ADSI, también admite la interfaz [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) , que proporciona métodos y propiedades que administran la creación, eliminación y enumeración de objetos ADSI contenidos en el objeto. En la siguiente ilustración se muestra un objeto de contenedor ADSI.

![objeto de contenedor ADSI](images/dsiadsc.png)

La mayoría de los objetos ADSI están incluidos en otros objetos. El único objeto ADSI sin contenedor primario es el objeto de los espacios de **nombres** ADSI de nivel superior ("ADS:").

El método [**IADs:: SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) de un objeto contenedor almacena de forma persistente las propiedades almacenadas en caché del objeto de contenedor ADSI en el almacenamiento, además de los objetos creados con el método [**IADsContainer:: Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) . [**IADsContainer::D iminar**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete) no afecta a la memoria caché de propiedades, pero elimina el elemento de directorio de espacio de nombres subyacente representado por este objeto.

 

 