---
title: Métodos de propiedad de interfaz
description: Muchas interfaces ADSI están diseñadas para admitir la automatización y, por tanto, son interfaces duales que admiten el acceso de cliente a través de interfaces IUnknown e IDispatch.
ms.assetid: b2831fa4-b58d-4b65-8deb-5fb7cd50c724
ms.tgt_platform: multiple
keywords:
- Métodos de propiedad de interfaz
- ADSI ADSI, referencia y métodos de propiedad explicados
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 018999d4834859cdb465bba2e6cdb9a05bd38a98
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105656415"
---
# <a name="interface-property-methods"></a><span data-ttu-id="b4a26-105">Métodos de propiedad de interfaz</span><span class="sxs-lookup"><span data-stu-id="b4a26-105">Interface Property Methods</span></span>

<span data-ttu-id="b4a26-106">Muchas interfaces ADSI están diseñadas para admitir la automatización y, por tanto, son interfaces duales que admiten el acceso de cliente a través de interfaces [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) e [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="b4a26-106">Many ADSI interfaces are designed to support Automation and thus are dual interfaces in that they support client access through both [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) and [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interfaces.</span></span> <span data-ttu-id="b4a26-107">Los clientes que no son de automatización, como los escritos en C/C++, resuelven la invocación de métodos directamente mediante el método [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) y llaman al método directamente.</span><span class="sxs-lookup"><span data-stu-id="b4a26-107">Non-Automation clients, such as those written in C/C++, resolve method invocation directly, using the [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method, and call the method directly.</span></span> <span data-ttu-id="b4a26-108">Los clientes de automatización, también conocidos como clientes enlazados a nombres, como los escritos en Visual Basic o Visual Basic Scripting Edition (VBScript), deben resolver indirectamente la invocación de métodos mediante el método [**dispinterface**](/previous-versions/windows/desktop/automat/dispinterface) .</span><span class="sxs-lookup"><span data-stu-id="b4a26-108">Automation clients, also known as name-bound clients, such as those written in Visual Basic, or Visual Basic Scripting Edition (VBScript), must resolve method invocation indirectly using the [**dispinterface**](/previous-versions/windows/desktop/automat/dispinterface) method.</span></span>

<span data-ttu-id="b4a26-109">Una interfaz ADSI que admite la automatización define métodos de propiedad para recuperar y modificar propiedades de un objeto que implementa la interfaz.</span><span class="sxs-lookup"><span data-stu-id="b4a26-109">An ADSI interface supporting Automation defines property methods for retrieving and modifying properties of an object implementing the interface.</span></span> <span data-ttu-id="b4a26-110">Los métodos de propiedad tienen nombres que tienen **Get** \_ y **Put** \_ antepuesto a los nombres de propiedad adecuados, por ejemplo, **Get \_ User** y **Put \_ Name**.</span><span class="sxs-lookup"><span data-stu-id="b4a26-110">The property methods have names that have **get**\_ and **put**\_ prepended to the appropriate property names, for example, **get\_User** and **put\_Name**.</span></span>

<span data-ttu-id="b4a26-111">Cada **método \_ Get** toma un parámetro único como output.</span><span class="sxs-lookup"><span data-stu-id="b4a26-111">Each **get\_** method takes a single parameter as output.</span></span> <span data-ttu-id="b4a26-112">Este parámetro es una dirección asignada por un método de una variable del tipo de datos de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="b4a26-112">This parameter is a method-allocated address of a variable of the property data type.</span></span> <span data-ttu-id="b4a26-113">Al devolverse, esta variable asume el valor actual de la propiedad solicitada.</span><span class="sxs-lookup"><span data-stu-id="b4a26-113">On return, this variable assumes the current value of the requested property.</span></span> <span data-ttu-id="b4a26-114">El llamador debe liberar la memoria asignada de la variable cuando ya no se necesite la propiedad.</span><span class="sxs-lookup"><span data-stu-id="b4a26-114">The caller must release the allocated memory of the variable when the property is no longer required.</span></span>

<span data-ttu-id="b4a26-115">Cada **método \_ Put** toma un parámetro único como entrada para el tipo de datos de la propiedad correspondiente.</span><span class="sxs-lookup"><span data-stu-id="b4a26-115">Each **put\_** method takes a single parameter as input for the data type of the corresponding property.</span></span> <span data-ttu-id="b4a26-116">El parámetro contiene un nuevo valor de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="b4a26-116">The parameter holds a new value of the property.</span></span>

<span data-ttu-id="b4a26-117">En el ejemplo de código siguiente se muestra la invocación de los métodos de propiedad que siguen el procedimiento habitual para llamar a la función miembro de un objeto.</span><span class="sxs-lookup"><span data-stu-id="b4a26-117">The following code example shows the invocation of the property methods that follow the usual procedure to call the member function of an object.</span></span>


```C++
IADs *pADs;
BSTR bstrName;
pADs->get_Name(&bstrName);
```



<span data-ttu-id="b4a26-118">En el ejemplo de código siguiente se muestra la invocación de los métodos de propiedad en los clientes de automatización, que puede ser algo diferente.</span><span class="sxs-lookup"><span data-stu-id="b4a26-118">The following code example shows the invocation of the property methods in automation clients, which can be somewhat different.</span></span> <span data-ttu-id="b4a26-119">Por ejemplo, Visual Basic usa la notación de puntos.</span><span class="sxs-lookup"><span data-stu-id="b4a26-119">For example, Visual Basic uses dot notation.</span></span>


```VB
Dim Obj As IADs
Dim objName As String
objName = Obj.Name
```



<span data-ttu-id="b4a26-120">Todos los parámetros y tipos devueltos deben ser de los que define el tipo de datos VARIANT.</span><span class="sxs-lookup"><span data-stu-id="b4a26-120">All parameters and return types must be of those that the VARIANT data type defines.</span></span> <span data-ttu-id="b4a26-121">Todos los métodos de una interfaz dual devuelven un valor HRESULT para indicar si se ha realizado correctamente o no.</span><span class="sxs-lookup"><span data-stu-id="b4a26-121">All methods on a dual interface return an HRESULT value to indicate success or failure.</span></span>

<span data-ttu-id="b4a26-122">Para obtener más información sobre cómo obtener y establecer las propiedades de los objetos ADSI, vea [caché de propiedades](property-cache-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="b4a26-122">For more information about getting and setting properties on ADSI objects, see [Property Cache](property-cache-interfaces.md).</span></span>

 

 