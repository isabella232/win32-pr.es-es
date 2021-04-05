---
title: Administración de esquemas
description: El componente de proveedor de ejemplo ADSI define las clases de esquema \ 0034; unidad organizativa \ 0034; y \ 0034; Usuario \ 0034; y administra estas clases de esquema de la siguiente manera.
ms.assetid: c3e07846-a11e-46d4-9863-a89810896ad7
ms.tgt_platform: multiple
keywords:
- ADSI de administración de esquemas
- ADSI de administración de esquemas
- administrar esquemas ADSI
- esquemas, administrar ADSI
- administrar un esquema ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99d398f8eb056498977f886e836c0f97c95f0b9b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104558909"
---
# <a name="schema-management"></a>Administración de esquemas

El componente de proveedor de ejemplo ADSI define las clases de esquema "unidad organizativa" y "usuario" y administra estas clases de esquema de la siguiente manera.

La clase de esquema "unidad organizativa" se representa mediante un objeto contenedor de ADs y puede contener otras "unidades organizativas" y "usuarios". El objeto contenedor admite las interfaces [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch), [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)y [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer). La clase de esquema "usuario" se representa mediante un objeto de Active Directory genérico y no contiene otros tipos de objetos. En el componente de proveedor de ejemplo, el objeto de usuario se implementa como un objeto de Active Directory genérico que admite las interfaces **IUnknown**, **IDispatch** y **IADs**. Tenga en cuenta que, en este caso, el objeto de usuario no admite la interfaz [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) .

El componente de proveedor de ejemplo también debe implementar el objeto de espacio de nombres ADs, que admite las interfaces [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)y [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch).

En la siguiente ilustración se muestran los detalles del esquema que representa las dos clases de esquema de componentes de proveedor de ejemplo.

![esquema de componentes de proveedor de ejemplo ADSI](images/dssmsch.png)

Tenga en cuenta que, en la figura anterior, la clase de esquema "unidad organizativa" define tres propiedades: "Description", "headcounts" e "ID". La clase de esquema "usuario" define cuatro propiedades: "ID", "Name", "PhoneNumber" y "title". Las dos clases de esquema comparten la propiedad "ID". Cada propiedad se define mediante el objeto de sintaxis "String" o "integer".

> [!Note]  
> Los objetos de sintaxis no están presentes en la primera versión del componente de proveedor de ejemplo. Sin embargo, en la mayoría de las implementaciones de esquema ADSI de Microsoft, los objetos de sintaxis se incluyen en el objeto contenedor de esquema, de la misma forma que los objetos de propiedad y clase de esquema. Por esta razón, se muestran aquí.

 

Este componente de proveedor hace que los datos del esquema sean accesibles para la aplicación cliente ADSI en forma de objetos de clase ADs, objetos de propiedad ADs y objetos de sintaxis ADs, todo ello dentro de un objeto contenedor de clase de esquema, para que los datos del esquema se puedan recuperar en tiempo de ejecución.

ADsPaths para los objetos de contenedor de clase de esquema definidos para el componente de proveedor de ejemplo son "Sample://Seattle/schema" y "Sample://Toronto/schema". En este ejemplo, el contenido de los esquemas es idéntico.

 

 