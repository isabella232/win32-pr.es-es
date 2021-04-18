---
description: Propiedades de extensión MTP
ms.assetid: 58fc8741-261a-4e63-9fd3-8f0ca05866ad
title: Propiedades de extensión MTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86a653d05285d62c7660bd914a785807a2341a01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105720580"
---
# <a name="mtp-extension-properties"></a><span data-ttu-id="1a1fa-103">Propiedades de extensión MTP</span><span class="sxs-lookup"><span data-stu-id="1a1fa-103">MTP Extension Properties</span></span>

<span data-ttu-id="1a1fa-104">Las propiedades describen objetos, propiedades, recursos y dispositivos.</span><span class="sxs-lookup"><span data-stu-id="1a1fa-104">Properties describe objects, properties, resources, and devices.</span></span>

## <a name="vendor-extended-object-properties"></a><span data-ttu-id="1a1fa-105">Propiedades de objetos extendidos de proveedor</span><span class="sxs-lookup"><span data-stu-id="1a1fa-105">Vendor-Extended Object Properties</span></span>

<span data-ttu-id="1a1fa-106">Cuando un fabricante de dispositivos crea una propiedad de proveedor extendida para un objeto de dispositivo, combina el GUID de **\_ propiedades de \_ \_ \_ objetos extendidos del proveedor \_ \_ MTP** de las propiedades de WPD con el código de propiedad del objeto para construir una estructura **PROPERTYKEY** .</span><span class="sxs-lookup"><span data-stu-id="1a1fa-106">When a device manufacturer creates a vendor-extended property for a device object, they combine the **WPD\_PROPERTIES\_MTP\_VENDOR\_EXTENDED\_OBJECT\_PROPS** GUID with the object's property code to construct a **PROPERTYKEY** structure.</span></span>

<span data-ttu-id="1a1fa-107">Por ejemplo, si el código de propiedad del objeto es 0xD801, el **PROPERTYKEY** resultante sería como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="1a1fa-107">For example, if the object's property code is 0xD801, the resulting **PROPERTYKEY** would be as shown in the following example:</span></span>


```C++
{4D545058-4FCE-4578-95C8-8698A9BC0F49}\D801
```



## <a name="vendor-extended-device-properties"></a><span data-ttu-id="1a1fa-108">Propiedades de dispositivo extendido de proveedor</span><span class="sxs-lookup"><span data-stu-id="1a1fa-108">Vendor-Extended Device Properties</span></span>

<span data-ttu-id="1a1fa-109">Cuando un fabricante de dispositivos crea una propiedad de proveedor extendida para un dispositivo, combina el GUID de **\_ propiedades de \_ \_ \_ \_ dispositivo \_ extendido del proveedor MTP** de las propiedades de WPD con el código de propiedad del objeto para crear una estructura **PROPERTYKEY** .</span><span class="sxs-lookup"><span data-stu-id="1a1fa-109">When a device manufacturer creates a vendor-extended property for a device, they combine the **WPD\_PROPERTIES\_MTP\_VENDOR\_EXTENDED\_DEVICE\_PROPS** GUID with the object's property code to construct a **PROPERTYKEY** structure.</span></span>

<span data-ttu-id="1a1fa-110">Por ejemplo, si el código de propiedad del objeto es 0xD001, el **PROPERTYKEY** resultante sería como se muestra en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="1a1fa-110">For example, if the object's property code is 0xD001, the resulting **PROPERTYKEY** would be as shown in the following example:</span></span>


```C++
{4D545058-8900-40b3-8F1D-DC246E1E8370}\D001
```



## <a name="related-topics"></a><span data-ttu-id="1a1fa-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1a1fa-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1a1fa-112">Compatibilidad con extensiones MTP</span><span class="sxs-lookup"><span data-stu-id="1a1fa-112">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 



