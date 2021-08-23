---
title: Crear y eliminar objetos
description: Con ADSI, los objetos se crean y eliminan mediante la interfaz IADsContainer o IDirectoryObject.
ms.assetid: 4d1f7ac5-48d3-4ea9-91e4-0cd4bb2ec9f8
ms.tgt_platform: multiple
keywords:
- Creación y eliminación de objetos ADSI
- ADSI, Crear y eliminar objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36bf2e351fb9bae919e8c40b0682b456b793f2e4419a66c64242791fad1d6cae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023653"
---
# <a name="creating-and-deleting-objects"></a>Crear y eliminar objetos

Con ADSI, los objetos se crean y eliminan mediante la [**interfaz IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer) [**o IDirectoryObject.**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)

## <a name="creating-an-object-with-iadscontainer"></a>Crear un objeto con IADsContainer

**Para crear un objeto con la interfaz IADsContainer**

1.  Enlace al contenedor que contendrá el objeto que se va a crear y obtenga la [**interfaz IADsContainer.**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
2.  Use el [**método IADsContainer.Create**](/windows/desktop/api/Iads/nf-iads-iadscontainer-create) para crear un nuevo objeto en el contenedor.
3.  Establezca los valores de todos los atributos necesarios para el objeto mediante el método [**IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put) o [**IADs.PutEx.**](/windows/desktop/api/Iads/nf-iads-iads-putex) Los atributos necesarios para crear un objeto dependerán del servicio de directorio y del tipo de objeto creado. Para obtener más información sobre cómo crear Active Directory objetos , vea [Creating and Deleting Active Directory Objects](/windows/desktop/AD/creating-and-deleting-objects-in-active-directory-domain-services).
4.  Establezca los valores de todos los atributos opcionales deseados para el objeto mediante el método [**IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put) o [**IADs.PutEx.**](/windows/desktop/api/Iads/nf-iads-iads-putex)
5.  Llame al [**método IADs.SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) para confirmar el objeto y sus atributos. El nuevo objeto no se crea realmente en el servicio de directorio subyacente hasta que se llama al método **IADs.SetInfo** para confirmar los atributos.

## <a name="creating-an-object-with-idirectoryobject"></a>Crear un objeto con IDirectoryObject

**Para crear un objeto con la interfaz IDirectoryObject**

1.  Enlace al contenedor que contendrá el objeto que se va a crear y obtenga la [**interfaz IDirectoryObject.**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
2.  Asigne una matriz de [**estructuras \_ ADS ATTR \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) que contenga una estructura para cada atributo que se va a establecer cuando se cree el objeto.
3.  Rellene una estructura [**ADS \_ ATTR \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) para cada atributo necesario para el objeto. Los atributos necesarios para crear un objeto dependerán del servicio de directorio y del tipo de objeto creado. Para obtener más información sobre cómo crear Active Directory objetos , vea [Creating and Deleting Active Directory Objects](/windows/desktop/AD/creating-and-deleting-objects-in-active-directory-domain-services).
4.  Rellene una estructura [**DE \_ INFORMACIÓN DE ATTR \_ de ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) para cada atributo opcional del objeto.
5.  Use el [**método IDirectoryObject::CreateDSObject**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-createdsobject) para crear el objeto en el contenedor. Este método también confirma el objeto en el servicio de directorio subyacente. Si la [**matriz \_ ADS ATTR \_ INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) no contiene todos los atributos necesarios para el objeto, se producirá un error **en IDirectoryObject::CreateDSObject.**

## <a name="deleting-an-object"></a>Eliminación de un objeto

Para eliminar un objeto, use [**el método IADsContainer::D elete**](/windows/desktop/api/Iads/nf-iads-iadscontainer-delete) o [**IDirectoryObject::D eleteDSObject.**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-deletedsobject) Estos métodos producirán un error si el objeto eliminado contiene objetos secundarios. Use el [**método IADsDeleteOps::D eleteObject**](/windows/desktop/api/Iads/nf-iads-iadsdeleteops-deleteobject) para eliminar un contenedor y todos los objetos secundarios del contenedor.

Lo que sucede con un objeto eliminado depende del servicio de directorio subyacente. Para obtener más información sobre cómo eliminar Active Directory, vea Crear y [eliminar Active Directory objetos](/windows/desktop/AD/creating-and-deleting-objects-in-active-directory-domain-services).

 

 