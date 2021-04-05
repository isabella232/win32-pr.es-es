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
# <a name="schema-management"></a><span data-ttu-id="80419-108">Administración de esquemas</span><span class="sxs-lookup"><span data-stu-id="80419-108">Schema Management</span></span>

<span data-ttu-id="80419-109">El componente de proveedor de ejemplo ADSI define las clases de esquema "unidad organizativa" y "usuario" y administra estas clases de esquema de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="80419-109">The ADSI example provider component defines the schema classes "Organizational Unit" and "User" and manages these schema classes in the following way.</span></span>

<span data-ttu-id="80419-110">La clase de esquema "unidad organizativa" se representa mediante un objeto contenedor de ADs y puede contener otras "unidades organizativas" y "usuarios".</span><span class="sxs-lookup"><span data-stu-id="80419-110">The "Organizational Unit" schema class is represented by an ADs container object and can contain other "Organizational Units" and "Users".</span></span> <span data-ttu-id="80419-111">El objeto contenedor admite las interfaces [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch), [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)y [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer).</span><span class="sxs-lookup"><span data-stu-id="80419-111">The container object supports the interfaces [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch), [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), and [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer).</span></span> <span data-ttu-id="80419-112">La clase de esquema "usuario" se representa mediante un objeto de Active Directory genérico y no contiene otros tipos de objetos.</span><span class="sxs-lookup"><span data-stu-id="80419-112">The "User" schema class is represented by a generic Active Directory object and does not contain other types of objects.</span></span> <span data-ttu-id="80419-113">En el componente de proveedor de ejemplo, el objeto de usuario se implementa como un objeto de Active Directory genérico que admite las interfaces **IUnknown**, **IDispatch** y **IADs**.</span><span class="sxs-lookup"><span data-stu-id="80419-113">In the example provider component, the User object is implemented as a generic Active Directory object that supports the interfaces **IUnknown**, **IDispatch**, and **IADs**.</span></span> <span data-ttu-id="80419-114">Tenga en cuenta que, en este caso, el objeto de usuario no admite la interfaz [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) .</span><span class="sxs-lookup"><span data-stu-id="80419-114">Be aware that the User object, in this case, does not support the [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) interface.</span></span>

<span data-ttu-id="80419-115">El componente de proveedor de ejemplo también debe implementar el objeto de espacio de nombres ADs, que admite las interfaces [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)y [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch).</span><span class="sxs-lookup"><span data-stu-id="80419-115">The example provider component must also implement the ADs namespace object, which supports the interfaces [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IADs**](/windows/desktop/api/Iads/nn-iads-iads), [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer), [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject), and [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch).</span></span>

<span data-ttu-id="80419-116">En la siguiente ilustración se muestran los detalles del esquema que representa las dos clases de esquema de componentes de proveedor de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="80419-116">The following figure shows the details of the schema that represents the two example provider component schema classes.</span></span>

![esquema de componentes de proveedor de ejemplo ADSI](images/dssmsch.png)

<span data-ttu-id="80419-118">Tenga en cuenta que, en la figura anterior, la clase de esquema "unidad organizativa" define tres propiedades: "Description", "headcounts" e "ID".</span><span class="sxs-lookup"><span data-stu-id="80419-118">Be aware that in the preceding figure the "Organizational Unit" schema class defines three properties: "Description," "Headcounts," and "ID."</span></span> <span data-ttu-id="80419-119">La clase de esquema "usuario" define cuatro propiedades: "ID", "Name", "PhoneNumber" y "title".</span><span class="sxs-lookup"><span data-stu-id="80419-119">The "User" schema class defines four properties: "ID," "Name," "PhoneNumber," and "Title."</span></span> <span data-ttu-id="80419-120">Las dos clases de esquema comparten la propiedad "ID".</span><span class="sxs-lookup"><span data-stu-id="80419-120">The "ID" property is shared by both schema classes.</span></span> <span data-ttu-id="80419-121">Cada propiedad se define mediante el objeto de sintaxis "String" o "integer".</span><span class="sxs-lookup"><span data-stu-id="80419-121">Each property is defined by either the "String" or the "Integer" syntax object.</span></span>

> [!Note]  
> <span data-ttu-id="80419-122">Los objetos de sintaxis no están presentes en la primera versión del componente de proveedor de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="80419-122">Syntax objects are not present in the first release of the example provider component.</span></span> <span data-ttu-id="80419-123">Sin embargo, en la mayoría de las implementaciones de esquema ADSI de Microsoft, los objetos de sintaxis se incluyen en el objeto contenedor de esquema, de la misma forma que los objetos de propiedad y clase de esquema.</span><span class="sxs-lookup"><span data-stu-id="80419-123">However, in most Microsoft ADSI schema implementations, the syntax objects are included in the schema container object, just as the schema class and property objects are.</span></span> <span data-ttu-id="80419-124">Por esta razón, se muestran aquí.</span><span class="sxs-lookup"><span data-stu-id="80419-124">For this reason, they are shown here.</span></span>

 

<span data-ttu-id="80419-125">Este componente de proveedor hace que los datos del esquema sean accesibles para la aplicación cliente ADSI en forma de objetos de clase ADs, objetos de propiedad ADs y objetos de sintaxis ADs, todo ello dentro de un objeto contenedor de clase de esquema, para que los datos del esquema se puedan recuperar en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="80419-125">This provider component makes schema data accessible to the ADSI client application in the form of ADs class objects, ADs property objects, and ADs syntax objects, all within a schema class container object, so that schema data can be retrieved at run time.</span></span>

<span data-ttu-id="80419-126">ADsPaths para los objetos de contenedor de clase de esquema definidos para el componente de proveedor de ejemplo son "Sample://Seattle/schema" y "Sample://Toronto/schema".</span><span class="sxs-lookup"><span data-stu-id="80419-126">The ADsPaths for the schema class container objects defined for the example provider component are "Sample://Seattle/schema" and "Sample://Toronto/schema".</span></span> <span data-ttu-id="80419-127">En este ejemplo, el contenido de los esquemas es idéntico.</span><span class="sxs-lookup"><span data-stu-id="80419-127">In this example, the contents of the schemas are identical.</span></span>

 

 