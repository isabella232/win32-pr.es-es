---
title: Opción de enlace rápido para operaciones de escritura/modificación por lotes
description: Cuando se enlaza un objeto de servicio de directorio, ADSI crea un objeto COM que representa el objeto de directorio especificado.
ms.assetid: cf41b0c4-7459-49cf-945b-8462c7d19947
ms.tgt_platform: multiple
keywords:
- Opción de enlace rápido para operaciones de escritura o modificación por lotes ADSI
- ADSI ADSI , Usar, Opción de enlace rápido para operaciones de escritura/modificación por lotes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46f27cbbe9ea76089ca1fd460f76c56d10e60664ae39ad28945440c6006acb9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118179904"
---
# <a name="fast-binding-option-for-batch-writemodify-operations"></a>Opción de enlace rápido para operaciones de escritura/modificación por lotes

Cuando se enlaza un objeto de servicio de directorio, ADSI crea un objeto COM que representa el objeto de directorio especificado. Al enlazar, ADSI normalmente recuperará el atributo **objectClass** para que ADSI pueda exponer las interfaces COM adecuadas para esa clase de objeto. Por ejemplo, un objeto de usuario expondría la interfaz [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) además de las interfaces ADSI base admitidas para todos los objetos. Para una sola operación, esto no debería tener ningún efecto en el rendimiento. Sin embargo, si se realizan operaciones por lotes que requieren cientos o miles de enlaces a través de una conexión lenta y esas operaciones escriben datos en el servicio de directorio, puede ser conveniente intercambiar compatibilidad completa con objetos para un enlace más rápido. Esto se conoce como enlace rápido y se logra especificando la marca BIND de **ADS \_ FAST \_ cuando** se llama a [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) o [**IADsOpenDSObject::OpenDSObject.**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject)

El enlace rápido tiene las restricciones siguientes:

-   La operación de enlace debe realizarse con la función [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) o con el método [**IADsOpenDSObject::OpenDSObject.**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) La operación de enlace va al servidor de directorio una vez en lugar de dos veces. ADSI no recupera el atributo **objectClass** y, por tanto, expone solo las interfaces ADSI base para el objeto.
-   Se admiten las interfaces siguientes para el objeto COM:

    -   [**Iads**](/windows/desktop/api/Iads/nn-iads-iads)
    -   [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
    -   [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
    -   [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)
    -   [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist)
    -   [**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions)
    -   [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo)
    -   [**IADsDeleteOps**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops)

-   Si el [**método IADsContainer::GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) se usa para enlazar a objetos secundarios, el objeto secundario tiene las mismas características de enlace rápido que el elemento primario.
-   La existencia del objeto al que se enlaza no se comprueba durante la operación de enlace, por lo que se producirá un error en las llamadas al método subsiguientes si el objeto no existe. Por este problema, el enlace rápido solo debe usarse para objetos que se sabe que existen, por ejemplo, directamente después de realizar una consulta que devuelve los nombres distintivos de los objetos a los que se enlaza.
-   Las extensiones ADSI se exponen para objetos de la clase **superior.** Por lo tanto, solo se exponen las extensiones para las interfaces ADSI base enumeradas anteriormente.

 

 