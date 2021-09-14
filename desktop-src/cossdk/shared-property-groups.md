---
description: Para evitar conflictos de nombres entre las propiedades creadas por objetos diferentes, el administrador de propiedades compartidas (SPM) usa grupos de propiedades compartidas.
ms.assetid: f73d631e-2552-4358-903a-739e2df3657d
title: Grupos de propiedades compartidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776dafe5c7e9752ce3ed1c88b01fd909b4b145de
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361661"
---
# <a name="shared-property-groups"></a>Grupos de propiedades compartidas

Para evitar conflictos de nombres entre las propiedades creadas por objetos diferentes, el administrador de propiedades compartidas (SPM) usa grupos de propiedades compartidas. Un grupo de propiedades compartidas es simplemente un espacio de nombres para un conjunto de propiedades compartidas. Cada propiedad dentro de un grupo de propiedades compartidas consta de un nombre, un valor y una posición dentro del grupo de propiedades compartidas. El nombre o la posición se pueden usar para recuperar el valor de propiedad. Puede acceder y crear grupos de propiedades compartidos a través del administrador de grupos de propiedades compartidas.

El modelo de objetos SPM se muestra en la ilustración siguiente.

![Diagrama que muestra el modelo de objetos SPM: ISharedPropertyGroupManager, ISharedPropertyGroup, a ISharedProperty.](images/1df31cd9-2fc4-48d3-ae68-cae38afb75a6.png)

Las siguientes son interfaces del administrador de propiedades compartidas:

-   [**ISharedPropertyGroupManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroupmanager) se usa para crear grupos de propiedades compartidas y obtener acceso a los grupos de propiedades compartidos existentes. Puede acceder a la **interfaz ISharedPropertyGroupManager** mediante la creación de una instancia del objeto [**SharedPropertyGroupManager**](sharedpropertygroupmanager.md) mediante [**IObjectContext::CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance) o [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

-   [**ISharedPropertyGroup**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedpropertygroup) se usa para crear y acceder a las propiedades compartidas de un grupo de propiedades compartidas. Puede acceder a la **interfaz ISharedPropertyGroup** mediante la creación de un objeto [**SharedPropertyGroup**](sharedpropertygroup.md) con el método [**ISharedPropertyGroupManager::CreatePropertyGroup.**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroupmanager-createpropertygroup) Al igual que con cualquier objeto COM, debe liberar un **objeto SharedPropertyGroup** cuando haya terminado de usarlo.

-   [**ISharedProperty**](/windows/desktop/api/ComSvcs/nn-comsvcs-isharedproperty) se usa para establecer o recuperar el valor de una propiedad compartida. Una propiedad compartida puede contener cualquier tipo de datos que se pueda representar mediante un variant. Puede acceder a la **interfaz ISharedProperty** mediante la creación de un objeto [**SharedProperty**](sharedproperty.md) con el método [**ISharedPropertyGroup::CreateProperty**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createproperty) o el método [**ISharedPropertyGroup::CreatePropertyByPosition.**](/windows/desktop/api/ComSvcs/nf-comsvcs-isharedpropertygroup-createpropertybyposition) Solo se puede crear o tener acceso a un objeto **SharedProperty** desde dentro de [**un objeto SharedPropertyGroup.**](sharedpropertygroup.md) Una vez más, debe liberar un **objeto SharedProperty** cuando haya terminado de usarlo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Com+ Compartido Administrador de propiedades](com--shared-property-manager.md)
</dt> </dl>

 

 
