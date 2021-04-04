---
title: Implementación básica
description: Un proveedor ADSI admite las siguientes características
ms.assetid: 39798237-a181-43b4-8441-ac711f923d4d
ms.tgt_platform: multiple
keywords:
- ADSI de implementación básica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f62068bd77553f89e222422431811da1ef251ccd
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078371"
---
# <a name="core-implementation"></a>Implementación básica

Un proveedor ADSI admite las siguientes características:

-   Cadenas ADsPath en formato COM y URL. Por definición, puede recuperar un objeto de Active Directory mediante una ADsPath. Los proveedores admiten la sintaxis que su servicio de directorio requiere mediante la implementación de **ParseDisplayName** .
-   Un objeto de espacio de nombres de nivel superior que admite [**IParseDisplayName::P arsedisplayname**](/windows/win32/api/oleidl/nf-oleidl-iparsedisplayname-parsedisplayname) y [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject). Este objeto contiene los nodos raíz de este espacio de nombres. Una parte de la implementación de **ParseDisplayName** debe incluir un analizador que compruebe si hay errores de sintaxis para su propio espacio de nombres. Este objeto también debe ser compatible con [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) y **IADsOpenDSObject**.
-   La interfaz [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) . Esto incluye una implementación de caché de propiedades simple a través de [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) y [**IADs:: SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo). Las operaciones que obtienen o establecen propiedades de objeto se producen en el modo de almacenamiento en caché. Los valores de caché se escriben en el almacén de directorios subyacente durante **:: SetInfo**. Sin embargo, un método ADSI no se almacena en caché, pero se ejecuta inmediatamente.
-   Las interfaces [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist), [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry) y [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue) para tener acceso directamente a las propiedades y enumerarlas en la caché de propiedades. En el caso de los servicios de directorio que no exponen un esquema, esta interfaz permite manipular las propiedades de un objeto.
-   La interfaz [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) para los clientes que no son de automatización. Utiliza el Protocolo por cable para obtener el máximo rendimiento y omite la memoria caché de propiedades.
-   Interfaz [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) . Cada Active Directory objeto tiene un contenedor primario que controla su duración. Tenga en cuenta que para los objetos contenedores de ADs, [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) solo afecta a las propiedades del contenedor y no a su contenido. La propiedad SetInfo en los objetos contenedores de ADs solo afecta a las propiedades del contenedor y no afecta a los objetos recién creados u objetos que ya existen dentro del contenedor.
-   Interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Esta es la interfaz de automatización para lenguajes como Visual Basic Scripting Edition, que no utilizan el enlace en tiempo de compilación. Relacionado con esto, se trata de los datos de la biblioteca de tipos que un proveedor debe proporcionar. Para obtener más información, vea [problemas de implementación para proveedores ADSI](implementation-issues-for-adsi-providers.md).
-   Un objeto contenedor de clase de esquema y los objetos de sintaxis, propiedad y clase de esquema adecuados que admiten [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax), [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)y [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) , respectivamente. Como mínimo, cada nodo raíz debe contener su propio objeto contenedor de clase de esquema.
-   La interfaz [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers) , si alguno de los atributos admitidos son colecciones de objetos ADSI, como grupos de seguridad.
-   La interfaz [**IADsCollection**](/windows/desktop/api/Iads/nn-iads-iadscollection) , si alguno de los atributos admitidos son colecciones del mismo tipo de elemento de directorio con la funcionalidad [**IADsCollection:: Add**](/windows/desktop/api/Iads/nf-iads-iadscollection-add) y [**IADsCollection:: Remove**](/windows/desktop/api/Iads/nf-iads-iadscollection-remove) .
-   La enumeración **IEnumXXXX** admite todos los objetos de enumerador concretos.
-   Rutinas para asignar sintaxis y convertir datos nativos en el tipo de datos [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) .
-   Siga las convenciones de ADSI para los objetos ADSI proporcionados por el proveedor. Incluir archivos de ayuda y bibliotecas de tipos documentar las propiedades y los métodos de la interfaz.

Al igual que con cualquier implementación de COM, las llamadas a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) deben devolver **e \_ nointerface** para interfaces no implementadas, **e \_ NOTIMPL** para los métodos no implementados de interfaces que, de otro modo, se implementan y devuelven la **propiedad de \_ ADS \_ \_ no \_ admitida** para las propiedades no implementadas. Para obtener más información sobre las interfaces duales y cómo afectan a la implementación de propiedades, consulte [interfaces duales](dual-interfaces.md).

 

 