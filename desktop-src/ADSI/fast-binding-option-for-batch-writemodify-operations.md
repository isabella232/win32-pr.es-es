---
title: Opción de enlace rápido para operaciones de escritura/modificación por lotes
description: Cuando un objeto de servicio de directorio se enlaza a, ADSI crea un objeto COM que representa el objeto de directorio especificado.
ms.assetid: cf41b0c4-7459-49cf-945b-8462c7d19947
ms.tgt_platform: multiple
keywords:
- Opción de enlace rápido para operaciones de escritura/modificación por lotes ADSI
- ADSI ADSI, usar, opción de enlace rápido para operaciones de escritura/modificación por lotes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 322cf3c8b5f40dc43304f95d08ff53a7c5c14217
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104533501"
---
# <a name="fast-binding-option-for-batch-writemodify-operations"></a>Opción de enlace rápido para operaciones de escritura/modificación por lotes

Cuando un objeto de servicio de directorio se enlaza a, ADSI crea un objeto COM que representa el objeto de directorio especificado. Al enlazar, ADSI normalmente recuperará el atributo **objectClass** para que ADSI pueda exponer las interfaces com adecuadas para esa clase de objeto. Por ejemplo, un objeto de usuario expondría la interfaz [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) además de las interfaces ADSI base admitidas para todos los objetos. En el caso de una sola operación, no debe tener ningún efecto en el rendimiento. Sin embargo, si se realizan operaciones por lotes que requieren cientos o miles de enlaces a través de una conexión lenta y esas operaciones están escribiendo datos en el servicio de directorio, puede ser conveniente intercambiar compatibilidad de objetos completa para un enlace más rápido. Esto se conoce como enlace rápido y se logra especificando la marca de **\_ \_ enlace rápido de ADS** cuando se llama a [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) o [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) .

El enlace rápido tiene las restricciones siguientes:

-   La operación de enlace se debe realizar con la función [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject) o el método [**IADsOpenDSObject:: OpenDSObject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject) . La operación de enlace se dirige al servidor de directorio una vez en lugar de dos veces. ADSI no recupera el atributo **objectClass** y, por tanto, solo expone las interfaces ADSI base para el objeto.
-   Se admiten las siguientes interfaces para el objeto COM:

    -   [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)
    -   [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
    -   [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
    -   [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)
    -   [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist)
    -   [**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions)
    -   [**ISupportErrorInfo**](/windows/win32/api/oaidl/nn-oaidl-isupporterrorinfo)
    -   [**IADsDeleteOps**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops)

-   Si el método [**IADsContainer:: GetObject**](/windows/desktop/api/Iads/nf-iads-iadscontainer-getobject) se usa para enlazar a objetos secundarios, el objeto secundario tiene las mismas características de enlace rápido que el elemento primario.
-   La existencia del objeto que se está enlazando a no se comprueba durante la operación de enlace, por lo que se producirá un error en las llamadas posteriores al método si el objeto no existe. Debido a esto, el enlace rápido solo se debe usar para los objetos que se sabe que existen, por ejemplo, directamente después de realizar una consulta que devolvió los nombres distintivos de los objetos a los que se está enlazando.
-   Las extensiones ADSI se exponen para los objetos de la clase **Top**. Por lo tanto, solo se exponen las extensiones de las interfaces ADSI de base mencionadas anteriormente.

 

 