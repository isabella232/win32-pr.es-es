---
title: Obtener acceso a los datos y manipularlos con ADSI
description: Todos los objetos tienen propiedades.
ms.assetid: 366a1fbc-3089-406a-9819-cf2ba7636c5f
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, acceso y manipulación de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3291db7490c79aae6363f619582ed24339fb83d
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105656400"
---
# <a name="accessing-and-manipulating-data-with-adsi"></a>Obtener acceso a los datos y manipularlos con ADSI

Todos los objetos tienen propiedades. Todos los objetos COM de la interfaz de servicio de Active Directory (ADSI) tienen una o varias interfaces con métodos que recuperan las propiedades del objeto de directorio que representa el objeto COM. Hay varias maneras de leer las propiedades de un objeto:

-   Obtener una propiedad específica por nombre: la interfaz [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) tiene dos métodos [**IADs:: get**](/windows/desktop/api/Iads/nf-iads-iads-get) y [**IADs:: GETEX**](/windows/desktop/api/Iads/nf-iads-iads-getex) para leer una propiedad concreta. Cada objeto COM ADSI tiene una interfaz **IADs** .
-   Obtiene una lista de propiedades especificada: la interfaz [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) tiene el método [**IDirectoryObject:: GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) , que permite especificar una lista que contiene los nombres de las propiedades que se van a leer y devuelve una matriz de estructuras que contienen los valores de propiedad solicitados.
-   Enumerar todas las propiedades del objeto: la interfaz [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) permite enumerar todas las propiedades de un objeto.
-   Obtener propiedades especiales: las interfaces de automatización ([**IADs**](/windows/desktop/api/Iads/nn-iads-iads) \* ) tienen métodos de propiedad que permiten obtener propiedades especiales que no se almacenan en un objeto. O los métodos de propiedad pueden permitirle obtener una propiedad de objeto en un formato de datos que difiere del tipo de datos real almacenado. Por ejemplo, la interfaz **IADs** tiene métodos de propiedad como [**IADs:: get \_ Name**](iads-property-methods.md), que recupera el nombre distintivo relativo (RDN) de un objeto; **IADs:: get \_ La clase**, que recupera la clase de un objeto, y **IADs:: get \_ Parent**, que recupera el ADsPath al elemento primario del objeto.

ADSI le permite almacenar en caché las propiedades localmente después de que se hayan leído desde el servidor de directorio. Esto le permite elegir entre leer las propiedades de la caché de propiedades local o recuperar las propiedades directamente desde el servidor de directorio. ADSI también tiene métodos para actualizar la memoria caché y especifica si todas las propiedades de un objeto se almacenan en caché o solo las que se han especificado.

Después de recuperar una propiedad, lea su valor. El tipo de datos de una propiedad depende de la definición de la propiedad (también conocida como atributo) en el esquema de Active Directory. Para cada tipo de propiedad que puede existir en Active Directory, hay un objeto **attributeSchema** en el esquema Active Directory. Un objeto **attributeSchema** define las características del atributo. Una de estas características es la sintaxis del atributo, que determina el tipo de datos de los valores del atributo. Para obtener más información, vea [características de atributos](/windows/desktop/AD/characteristics-of-attributes) y [sintaxis para los atributos de Active Directory](/windows/desktop/AD/syntaxes-for-attributes-in-active-directory-domain-services).

Las interfaces de automatización ([**IADs**](/windows/desktop/api/Iads/nn-iads-iads) \* ) devuelven un valor de propiedad como una [**variante**](/windows/win32/api/oaidl/ns-oaidl-variant) o un puntero a una interfaz de automatización en un objeto com que representa la propiedad. Las interfaces [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) y [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) devuelven una propiedad como un puntero a una estructura que contiene un valor de propiedad con tipo o un puntero a una cadena de bytes. Además, **IDirectoryObject** y **IDirectorySearch** recuperan propiedades directamente del servidor de directorio en lugar de usar una memoria caché de propiedades local.

En esta sección se describen los temas siguientes:

-   [Las interfaces IADs y IDirectoryObject](the-iads-and-idirectoryobject-interfaces.md)
-   [Obtener acceso a atributos con ADSI](accessing-attributes-with-adsi.md)
-   [Modificar atributos con ADSI](modifying-attributes-with-adsi.md)
-   [Acceso directo a la memoria caché de propiedades con las interfaces IADsProperty](accessing-the-property-cache-directly-with-the-iadsproperty-interfaces.md)
-   [Sintaxis de atributo ADSI](adsi-attribute-syntax.md)

 

 