---
description: Todas las propiedades de una clase de vista deben tener un calificador de matriz de cadenas denominado PropertySources.
ms.assetid: df89680b-8ea7-4f38-81ba-c4132b944f37
ms.tgt_platform: multiple
title: Calificador PropertySources
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PropertySources
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3809977282a2bdf82d0b51ef8f566541b74fe28a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715465"
---
# <a name="propertysources-qualifier"></a><span data-ttu-id="936e0-103">Calificador PropertySources</span><span class="sxs-lookup"><span data-stu-id="936e0-103">PropertySources Qualifier</span></span>

<span data-ttu-id="936e0-104">Todas las propiedades de una clase de vista deben tener un calificador de matriz de cadenas denominado **PropertySources**.</span><span class="sxs-lookup"><span data-stu-id="936e0-104">Every property in a view class must have a string array qualifier called **PropertySources**.</span></span> <span data-ttu-id="936e0-105">El calificador **PropertySources** contiene el nombre de la propiedad o propiedades de clase de origen de la que obtiene datos esta propiedad de clase de vista.</span><span class="sxs-lookup"><span data-stu-id="936e0-105">The **PropertySources** qualifier contains the name of the source class property or properties from which this view class property gets data.</span></span> <span data-ttu-id="936e0-106">El orden de los valores de esta matriz se corresponde con el orden de las clases de origen definidas para el [calificador ViewSources](viewsources-qualifier.md).</span><span class="sxs-lookup"><span data-stu-id="936e0-106">The order of the values in this array correspond to the order of the source classes defined for the [ViewSources qualifier](viewsources-qualifier.md).</span></span> <span data-ttu-id="936e0-107">En el ejemplo siguiente se muestra cómo definir una propiedad para una clase de vista de Unión que es la Unión de la clase [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) de dos equipos diferentes:</span><span class="sxs-lookup"><span data-stu-id="936e0-107">The following example shows how to define a property for a union view class that is the union of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class from two different computers:</span></span>


```mof
[PropertySources{"DeviceID", "DeviceID"},key] String Devname;
```



<span data-ttu-id="936e0-108">La primera propiedad **DeviceID** corresponde a la propiedad **DeviceID** de la clase en la primera consulta de origen.</span><span class="sxs-lookup"><span data-stu-id="936e0-108">The first **DeviceID** property corresponds to the **DeviceID** property from the class in the first source query.</span></span> <span data-ttu-id="936e0-109">La segunda propiedad **DeviceID** es la propiedad **DeviceID** de la clase en la segunda consulta de origen.</span><span class="sxs-lookup"><span data-stu-id="936e0-109">The second **DeviceID** property is the **DeviceID** property from the class in the second source query.</span></span>

<span data-ttu-id="936e0-110">Al definir las propiedades de las clases de vista de combinación, debe definir una propiedad de vista independiente para cada una de las propiedades de la clase de origen a menos que las propiedades de la clase de origen sean la base de la clase de vista de combinación.</span><span class="sxs-lookup"><span data-stu-id="936e0-110">When defining properties for join view classes, you must define a separate view property for each of the source class properties unless the source class properties are the basis of the join view class.</span></span> <span data-ttu-id="936e0-111">En el ejemplo siguiente se crean propiedades en una clase de vista de combinación en propiedades similares de la clase de origen de [**\_ impresora Win32**](/windows/desktop/CIMWin32Prov/win32-printer) y la clase de origen [**\_ PrinterConfiguration de Win32**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) :</span><span class="sxs-lookup"><span data-stu-id="936e0-111">The following example creates properties in a join view class on similar properties from the [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer) source class and the [**Win32\_PrinterConfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) source class:</span></span>


```mof
[PropertySources{"VerticalResolution", ""}] Uint32 Vres;
[PropertySources{"", "YResolution"}] Uint32 Yres;
```



<span data-ttu-id="936e0-112">Si las dos clases de origen se combinan mediante una propiedad común, solo se puede definir una propiedad de clase de vista, ya que el valor de ambas propiedades de clase de origen siempre es el mismo.</span><span class="sxs-lookup"><span data-stu-id="936e0-112">If the two source classes are being joined by a common property, you can only define a single view class property because the value of both source class properties is always the same.</span></span> <span data-ttu-id="936e0-113">En el ejemplo siguiente se muestra cómo unir la clase de [**\_ impresora Win32**](/windows/desktop/CIMWin32Prov/win32-printer) y la [**\_ PrinterConfiguration Win32**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) mediante un valor de propiedad común:</span><span class="sxs-lookup"><span data-stu-id="936e0-113">The following example shows how to join the [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer) class and the [**Win32\_PrinterConfiguration**](/windows/desktop/CIMWin32Prov/win32-printerconfiguration) by a common property value:</span></span>


```mof
[PropertySources{"DeviceId", "DeviceName "}] String Name;
```



## <a name="requirements"></a><span data-ttu-id="936e0-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="936e0-114">Requirements</span></span>



| <span data-ttu-id="936e0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="936e0-115">Requirement</span></span> | <span data-ttu-id="936e0-116">Value</span><span class="sxs-lookup"><span data-stu-id="936e0-116">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="936e0-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="936e0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="936e0-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="936e0-118">Windows Vista</span></span><br/>       |
| <span data-ttu-id="936e0-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="936e0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="936e0-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="936e0-120">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="936e0-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="936e0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="936e0-122">**Calificadores específicos del proveedor de vistas**</span><span class="sxs-lookup"><span data-stu-id="936e0-122">**Qualifiers Specific to the View Provider**</span></span>](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

