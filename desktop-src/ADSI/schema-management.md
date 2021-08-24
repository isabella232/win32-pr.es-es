---
title: Administración de esquemas
description: El componente de proveedor de ejemplo ADSI define las clases de esquema \ 0034;Unidad organizativa \ 0034; y \ 0034; Usuario \ 0034; y administra estas clases de esquema de la siguiente manera.
ms.assetid: c3e07846-a11e-46d4-9863-a89810896ad7
ms.tgt_platform: multiple
keywords:
- ADSI de administración de esquemas
- ADSI de administración de esquemas
- administrar esquemas ADSI
- esquemas, administración de ADSI
- administrar un ADSI de esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ddb8fcc3d29dce27ac2b74c9c8e79d1cef2f9d2a23307e9b7626861ed3e7dd4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770495"
---
# <a name="schema-management"></a>Administración de esquemas

El componente de proveedor de ejemplo ADSI define las clases de esquema "Unidad organizativa" y "Usuario" y administra estas clases de esquema de la siguiente manera.

La clase de esquema "Unidad organizativa" se representa mediante un objeto contenedor de ADs y puede contener otras "unidades organizativas" y "Usuarios". El objeto contenedor admite las interfaces [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IDispatch,**](/windows/win32/api/oaidl/nn-oaidl-idispatch) [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)e [**IADsContainer.**](/windows/desktop/api/Iads/nn-iads-iadscontainer) La clase de esquema "User" se representa mediante un objeto Active Directory y no contiene otros tipos de objetos. En el componente de proveedor de ejemplo, el objeto User se implementa como un objeto Active Directory genérico que admite las interfaces **IUnknown**, **IDispatch** e **ID**. Tenga en cuenta que el objeto User, en este caso, no admite la [**interfaz IADsUser.**](/windows/desktop/api/Iads/nn-iads-iadsuser)

El componente de proveedor de ejemplo también debe implementar el objeto de espacio de nombres ADs, que admite las interfaces [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsContainer,**](/windows/desktop/api/Iads/nn-iads-iadscontainer) [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)e [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch).

En la ilustración siguiente se muestran los detalles del esquema que representa las dos clases de esquema de componente de proveedor de ejemplo.

![Esquema de componente de proveedor de ejemplo adsi](images/dssmsch.png)

Tenga en cuenta que, en la ilustración anterior, la clase de esquema "Unidad organizativa" define tres propiedades: "Description", "Headcounts" e "ID". La clase de esquema "User" define cuatro propiedades: "ID", "Name", "PhoneNumber" y "Title". Ambas clases de esquema comparten la propiedad "ID". Cada propiedad se define mediante el objeto de sintaxis "String" o "Integer".

> [!Note]  
> Los objetos de sintaxis no están presentes en la primera versión del componente de proveedor de ejemplo. Sin embargo, en la mayoría de las implementaciones de esquema ADSI de Microsoft, los objetos de sintaxis se incluyen en el objeto contenedor de esquema, igual que los objetos de propiedad y clase de esquema. Por este motivo, se muestran aquí.

 

Este componente de proveedor hace que los datos de esquema sean accesibles para la aplicación cliente ADSI en forma de objetos de clase ADs, objetos de propiedad ADs y objetos de sintaxis de ADs, todo dentro de un objeto contenedor de clases de esquema, para que los datos de esquema se puedan recuperar en tiempo de ejecución.

Los ADsPaths para los objetos de contenedor de la clase de esquema definidos para el componente de proveedor de ejemplo son "Sample://Seattle/schema" y "Sample://Toronto/schema". En este ejemplo, el contenido de los esquemas es idéntico.

 

 