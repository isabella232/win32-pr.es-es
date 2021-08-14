---
title: Acceso y manipulación de datos con ADSI
description: Todos los objetos tienen propiedades.
ms.assetid: 366a1fbc-3089-406a-9819-cf2ba7636c5f
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, acceso y manipulación de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03ed09c1717f4f9a9c1c75372e7efdc23d2cce1adb39242197346061ae4df00f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118181635"
---
# <a name="accessing-and-manipulating-data-with-adsi"></a>Acceso y manipulación de datos con ADSI

Todos los objetos tienen propiedades. Todos Active Directory com de la interfaz de servicio (ADSI) tienen una o varias interfaces con métodos que recuperan las propiedades del objeto de directorio que representa el objeto COM. Hay varias maneras de leer propiedades de un objeto:

-   Obtener una propiedad específica por nombre: la interfaz [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) tiene dos [**métodos: IADs::Get**](/windows/desktop/api/Iads/nf-iads-iads-get) e [**IADs::GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) para leer una propiedad específica. Cada objeto COM ADSI tiene una **interfaz IAD.**
-   Obtener una lista especificada de propiedades: la interfaz [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) tiene el método [**IDirectoryObject::GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) que permite especificar una lista que contiene los nombres de las propiedades que se leerán y devuelve una matriz de estructuras que contienen los valores de propiedad solicitados.
-   Enumerar todas las propiedades del objeto: la [**interfaz IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) permite enumerar todas las propiedades de un objeto .
-   Obtener propiedades especiales: las interfaces de Automation [**(IAD)**](/windows/desktop/api/Iads/nn-iads-iads)tienen métodos de propiedad que permiten obtener propiedades especiales que no están almacenadas \* en un objeto . O bien, los métodos de propiedad pueden permitirle obtener una propiedad de objeto en un formato de datos que difiere del tipo de datos real almacenado. Por ejemplo, la **interfaz IADs** tiene métodos de propiedad como [**IADs::get \_ Name**](iads-property-methods.md), que recupera el nombre distintivo relativo (RDN) de un objeto. **IADs::get \_ Clase**, que recupera la clase de un objeto e **IADs::get \_ Parent**, que recupera el ADsPath al elemento primario del objeto.

ADSI permite almacenar en caché las propiedades localmente después de que se hayan leído desde el servidor de directorios. Esto le permite leer las propiedades de la caché de propiedades local o recuperar las propiedades directamente desde el servidor de directorios. ADSI también tiene métodos para actualizar la memoria caché, así como para especificar si todas las propiedades de un objeto se almacenan en caché o solo las que ha especificado.

Una vez que haya recuperado una propiedad, lea su valor. El tipo de datos de una propiedad depende de la definición de la propiedad (también conocida como atributo) en el Active Directory esquema. Para cada tipo de propiedad que puede existir en Active Directory, hay un **objeto attributeSchema** en el Active Directory esquema. Un **objeto attributeSchema** define las características del atributo. Una de estas características es la sintaxis del atributo, que determina el tipo de datos de los valores del atributo. Para obtener más información, vea [Características de atributos y](/windows/desktop/AD/characteristics-of-attributes) [sintaxis para Active Directory atributos](/windows/desktop/AD/syntaxes-for-attributes-in-active-directory-domain-services).

Las interfaces de Automation [**(IAD)**](/windows/desktop/api/Iads/nn-iads-iads)devuelven un valor de propiedad como VARIANT o un puntero a una interfaz de Automation en un objeto COM que \* representa la propiedad [](/windows/win32/api/oaidl/ns-oaidl-variant) . Las [**interfaces IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) e [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) devuelven una propiedad como puntero a una estructura que contiene un valor de propiedad con tipo o un puntero a una cadena de bytes. Además, **IDirectoryObject** e **IDirectorySearch** recuperan propiedades directamente desde el servidor de directorios en lugar de usar una caché de propiedades local.

En esta sección se describen los temas siguientes:

-   [Interfaces IAD e IDirectoryObject](the-iads-and-idirectoryobject-interfaces.md)
-   [Acceso a atributos con ADSI](accessing-attributes-with-adsi.md)
-   [Modificar atributos con ADSI](modifying-attributes-with-adsi.md)
-   [Acceso a la caché de propiedades directamente con las interfaces IADsProperty](accessing-the-property-cache-directly-with-the-iadsproperty-interfaces.md)
-   [Sintaxis de atributos ADSI](adsi-attribute-syntax.md)

 

 