---
title: Implementación principal
description: Un proveedor adsi admite las siguientes características
ms.assetid: 39798237-a181-43b4-8441-ac711f923d4d
ms.tgt_platform: multiple
keywords:
- ADSI de implementación principal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d78487b701cac0409745ed3a7776dd882f2c37a878dec1d144c3b52a426db487
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962094"
---
# <a name="core-implementation"></a>Implementación principal

Un proveedor adsi admite las siguientes características:

-   Cadenas ADsPath en formato COM y URL. Por definición, puede recuperar un objeto Active Directory mediante un ADsPath. Los proveedores admiten la sintaxis que su servicio de directorio requiere mediante **la implementación parseDisplayName.**
-   Objeto namespace de nivel superior que admite [**IParseDisplayName::P arseDisplayName**](/windows/win32/api/oleidl/nf-oleidl-iparsedisplayname-parsedisplayname) e [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject). Este objeto contiene los nodos raíz de este espacio de nombres. Parte de la **implementación parseDisplayName** debe incluir un analizador que comprueba si hay errores de sintaxis para su propio espacio de nombres. Este objeto también debe admitir [**los IAD e**](/windows/desktop/api/Iads/nn-iads-iads) **IADsOpenDSObject**.
-   Interfaz [**de los IAD.**](/windows/desktop/api/Iads/nn-iads-iads) Esto incluye una implementación de caché de propiedades simple a través [**de IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) e [**IADs::SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo). Las operaciones que obtienen o establecen propiedades de objeto se producen en modo almacenado en caché. Los valores de caché se escriben en el almacén de directorios subyacente **durante los IADs::SetInfo**. Sin embargo, un método ADSI no se almacena en caché, pero se ejecuta inmediatamente.
-   Las [**interfaces IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist), [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) e [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) para acceder directamente a las propiedades y enumerarlas en la caché de propiedades. Para los servicios de directorio que no exponen un esquema, esta interfaz permite manipular las propiedades de un objeto .
-   Interfaz [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) para clientes que no son de Automation. Esto usa el protocolo de conexión por encima de la conexión para obtener el máximo rendimiento y omite la caché de propiedades.
-   Interfaz [**IADsContainer.**](/windows/desktop/api/Iads/nn-iads-iadscontainer) Cada Active Directory objeto tiene un contenedor primario que controla su duración. Tenga en cuenta que, para los objetos de contenedor de ADs, [**IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) solo afecta a las propiedades del contenedor y no a su contenido. SetInfo en objetos de contenedor de ADs solo afecta a las propiedades del contenedor y no afecta a los objetos recién creados ni a los objetos que ya existen dentro del contenedor.
-   Interfaz [**IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) Esta es la interfaz de Automation para lenguajes como Visual Basic Scripting Edition, que no usan el enlace en tiempo de compilación. En relación con esto, se trata de los datos de la biblioteca de tipos que debe proporcionar un proveedor. Para obtener más información, vea [Problemas de implementación para proveedores ADSI.](implementation-issues-for-adsi-providers.md)
-   Objeto contenedor de clase de esquema y los objetos de sintaxis, propiedad y clase de esquema adecuados que [**admiten IADsSyntax,**](/windows/desktop/api/Iads/nn-iads-iadssyntax) [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)e [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) respectivamente. Como mínimo, cada nodo raíz debe contener su propio objeto contenedor de clase de esquema.
-   La [**interfaz IADsMembers,**](/windows/desktop/api/Iads/nn-iads-iadsmembers) si alguno de los atributos admitidos son colecciones de objetos ADSI, como grupos de seguridad.
-   La [**interfaz IADsCollection,**](/windows/desktop/api/Iads/nn-iads-iadscollection) si alguno de los atributos admitidos son colecciones del mismo tipo de elemento de directorio con la funcionalidad [**IADsCollection::Add**](/windows/desktop/api/Iads/nf-iads-iadscollection-add) e [**IADsCollection::Remove.**](/windows/desktop/api/Iads/nf-iads-iadscollection-remove)
-   La **enumeración IEnumXXXX** admite todos los objetos de enumerador específicos.
-   Rutinas para asignar la sintaxis y convertir datos nativos al [**tipo de datos VARIANT.**](/windows/win32/api/oaidl/ns-oaidl-variant)
-   Siga las convenciones adsi para los objetos ADSI proporcionados por el proveedor. Incluya archivos de ayuda y bibliotecas de tipos que documentan las propiedades y los métodos de la interfaz.

Al igual que con cualquier implementación COM, las llamadas a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) deben devolver **E \_ NOINTERFACE** para interfaces no implementadas, **E \_ NOTIMPL** para métodos no implementados de interfaces que se implementan de otro modo y devolver **E ADS PROPERTY NOT \_ \_ \_ \_ SUPPORTED** para propiedades no implementadas. Para obtener más información sobre las interfaces duales y cómo afectan a la implementación de propiedades, vea [Interfaces duales.](dual-interfaces.md)

 

 