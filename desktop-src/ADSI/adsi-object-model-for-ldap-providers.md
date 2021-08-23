---
title: Modelo de objetos ADSI para proveedores LDAP
description: Ilustración en la que se muestran los objetos ADSI usados para el proveedor LDAP y las interfaces que se usan para acceder a estos objetos.
ms.assetid: 109fd42e-201e-4b84-a213-2695d81f005b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68c7c520793f6095bc9d4d9c6379f8ff6f09766f39ae6102f7e0a82d3a3de7cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023802"
---
# <a name="adsi-object-model-for-ldap-providers"></a>Modelo de objetos ADSI para proveedores LDAP

En la ilustración siguiente se muestran los objetos ADSI usados para el proveedor LDAP y las interfaces que se usan para acceder a estos objetos.

![modelo de objetos para el proveedor ldap](images/adsiobjmodldap-gif-1.png)

| Object                        | Interfaz                                                                                                                                                                                                                                                                                      |
|-------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Clase<br/>              | [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [ **IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass)                                                                                                                                                                                                                                           |
| Propiedad<br/>           | [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [ **IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)                                                                                                                                                                                                                                     |
| GenObject<br/>          | [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsContainer,**](/windows/desktop/api/Iads/nn-iads-iadscontainer) [**IADsDeleteOps**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops), [**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions), [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist), [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject), [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) |
| Espacio de nombres<br/>          | [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)                                                                                                                                                                                     |
| Rootdse<br/>            | [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [ **IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist)                                                                                                                                                                                                                             |
| Ruta<br/>           | [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [ **IADsPathname**](/windows/desktop/api/Iads/nn-iads-iadspathname)                                                                                                                                                                                                                                     |
| Esquema<br/>             | [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [ **IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)                                                                                                                                                                                                                                   |
| Syntax<br/>             | [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [ **IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax)                                                                                                                                                                                                                                         |
| Organización<br/>       | [**IADsO**](/windows/desktop/api/Iads/nn-iads-iadso)                                                                                                                                                                                                                                                                         |
| OrganizationalUnit<br/> | [**IADsOU**](/windows/desktop/api/Iads/nn-iads-iadsou)                                                                                                                                                                                                                                                                       |
| GroupCollection<br/>    | [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers)                                                                                                                                                                                                                                                             |
| Group (Grupo)<br/>              | [**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup)                                                                                                                                                                                                                                                                 |
| UserCollection<br/>     | [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers)                                                                                                                                                                                                                                                             |
| Usuario<br/>               | [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser)                                                                                                                                                                                                                                                                   |
| Localidad<br/>           | [**IADsLocality**](/windows/desktop/api/Iads/nn-iads-iadslocality)                                                                                                                                                                                                                                                           |
| NameTranslate<br/>      | [**IADsNameTranslate**](/windows/desktop/api/Iads/nn-iads-iadsnametranslate)                                                                                                                                                                                                                                                 |
| PrintQueue<br/>         | [**IADsPrintQueue**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue), [ **IADsPrintQueueOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations)                                                                                                                                                                                         |



 

 

 





