---
description: Para evitar colisiones de nombres entre las propiedades creadas por objetos diferentes, el administrador de propiedades compartidas (SPM) utiliza grupos de propiedades compartidas.
ms.assetid: f73d631e-2552-4358-903a-739e2df3657d
title: Grupos de propiedades compartidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776dafe5c7e9752ce3ed1c88b01fd909b4b145de
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/05/2021
ms.locfileid: "103819839"
---
# <a name="shared-property-groups"></a>Grupos de propiedades compartidas

Para evitar colisiones de nombres entre las propiedades creadas por objetos diferentes, el administrador de propiedades compartidas (SPM) utiliza grupos de propiedades compartidas. Un grupo de propiedades compartidas es simplemente un espacio de nombres para un conjunto de propiedades compartidas. Cada propiedad dentro de un grupo de propiedades compartidas consta de un nombre, un valor y una posición dentro del grupo de propiedades compartidas. Se puede usar el nombre o la posición para recuperar el valor de propiedad. Puede obtener acceso y crear grupos de propiedades compartidas mediante el administrador de grupos de propiedades compartidas.

En la ilustración siguiente se muestra el modelo de objetos SPM.

![Diagrama que muestra el modelo de objetos de SPM: ISharedPropertyGroupManager, ISharedPropertyGroup, a ISharedProperty.](images/1df31cd9-2fc4-48d3-ae68-cae38afb75a6.png)

A continuación se muestran las interfaces del administrador de propiedades compartidas:

-   [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager) se utiliza para crear grupos de propiedades compartidas y para obtener acceso a grupos de propiedades compartidas existentes. Puede tener acceso a la interfaz **ISharedPropertyGroupManager** creando una instancia del objeto [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md) mediante [**IObjectContext:: CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance) o [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

-   [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup) se utiliza para crear y obtener acceso a las propiedades compartidas de un grupo de propiedades compartidas. Puede tener acceso a la interfaz **ISharedPropertyGroup** mediante la creación de un objeto [**SharedPropertyGroup**](sharedpropertygroup.md) con el método [**ISharedPropertyGroupManager:: CreatePropertyGroup**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) . Al igual que con cualquier objeto COM, debe liberar un objeto **SharedPropertyGroup** cuando haya terminado de usarlo.

-   [**ISharedProperty**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty) se utiliza para establecer o recuperar el valor de una propiedad compartida. Una propiedad compartida puede contener cualquier tipo de datos que se pueda representar mediante una variante. Puede tener acceso a la interfaz **ISharedProperty** mediante la creación de un objeto [**SharedProperty**](sharedproperty.md) con el método [**ISharedPropertyGroup:: CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty) o el método [**ISharedPropertyGroup:: CreatePropertyByPosition**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition) . Un objeto **SharedProperty** se puede crear u obtener acceso solo desde dentro de un objeto [**SharedPropertyGroup**](sharedpropertygroup.md) . Una vez más, debe liberar un objeto **SharedProperty** cuando haya terminado de usarlo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administrador de propiedades compartidos de COM+](com--shared-property-manager.md)
</dt> </dl>

 

 
