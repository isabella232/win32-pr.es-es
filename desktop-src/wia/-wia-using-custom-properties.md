---
description: Usar propiedades personalizadas.
ms.assetid: 09b30c95-0ce2-401c-a4ae-99c801a2048a
title: Usar propiedades personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eca9f8092afa5b8af22080b154fff79a32a6f304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696504"
---
# <a name="using-custom-properties"></a><span data-ttu-id="3dfd6-103">Usar propiedades personalizadas</span><span class="sxs-lookup"><span data-stu-id="3dfd6-103">Using Custom Properties</span></span>

<span data-ttu-id="3dfd6-104">**Usar propiedades personalizadas**.</span><span class="sxs-lookup"><span data-stu-id="3dfd6-104">**Using Custom Properties**.</span></span>

<span data-ttu-id="3dfd6-105">Un controlador de adquisición de imágenes de Windows (WIA) puede definir sus propias propiedades personalizadas.</span><span class="sxs-lookup"><span data-stu-id="3dfd6-105">A Windows Image Acquisition (WIA) driver can define its own custom properties.</span></span> <span data-ttu-id="3dfd6-106">Los llamadores pueden manipular propiedades personalizadas del mismo modo que las propiedades de WIA normales.</span><span class="sxs-lookup"><span data-stu-id="3dfd6-106">Callers can manipulate custom properties just as they would normal WIA properties.</span></span> <span data-ttu-id="3dfd6-107">Sin embargo, solo el módulo de la aplicación o de la interfaz de usuario personalizada puede tener acceso a estas propiedades personalizadas.</span><span class="sxs-lookup"><span data-stu-id="3dfd6-107">However, only your application or custom UI module can access these custom properties.</span></span>

<span data-ttu-id="3dfd6-108">Los controladores WIA deben definir las propiedades personalizadas para tener identificadores de propiedad que se desplacen con WIA \_ Private \_ DEVPROP para las propiedades de dispositivo y usar WIA \_ Private \_ ITEMPROP para las propiedades de elementos normales, como dentro de [IWiaMiniDrv::d rvinititemproperties](https://msdn.microsoft.com/library/ms794131.aspx).</span><span class="sxs-lookup"><span data-stu-id="3dfd6-108">WIA drivers should define the custom properties to have property identifiers that are offset by WIA\_PRIVATE\_DEVPROP for device properties, and use WIA\_PRIVATE\_ITEMPROP for normal item properties, such as inside [IWiaMiniDrv::drvInitItemProperties](https://msdn.microsoft.com/library/ms794131.aspx).</span></span> <span data-ttu-id="3dfd6-109">Para obtener más información, vea [definir propiedades personalizadas](-wia-defining-custom-properties.md).</span><span class="sxs-lookup"><span data-stu-id="3dfd6-109">For more information, see [Defining Custom Properties](-wia-defining-custom-properties.md).</span></span>

<span data-ttu-id="3dfd6-110">Hay dos maneras de pasar parámetros personalizados a los controladores WIA.</span><span class="sxs-lookup"><span data-stu-id="3dfd6-110">There are two ways to pass custom parameters to WIA drivers.</span></span>

<span data-ttu-id="3dfd6-111">La primera opción consiste en usar el método **IWiaItemExtras:: escape** (descrito en la documentación del SDK de la plataforma).</span><span class="sxs-lookup"><span data-stu-id="3dfd6-111">The first option is to use the **IWiaItemExtras::Escape** method (described in the Platform SDK documentation).</span></span> <span data-ttu-id="3dfd6-112">Esto es similar al método [IStiUSD:: escape](https://msdn.microsoft.com/library/ms794396.aspx) , pero permite que los llamadores usen WIA directamente, en lugar de usar métodos STI.</span><span class="sxs-lookup"><span data-stu-id="3dfd6-112">This is similar to the [IStiUSD::Escape](https://msdn.microsoft.com/library/ms794396.aspx) method, but it allows callers to use WIA directly, instead of using STI methods.</span></span> <span data-ttu-id="3dfd6-113">Con **IWiaItemExtras:: escape**, puede pasar cualquier información al controlador y el controlador puede devolver cualquier información.</span><span class="sxs-lookup"><span data-stu-id="3dfd6-113">Using **IWiaItemExtras::Escape**, you can pass any information to the driver, and the driver can pass any information back.</span></span> <span data-ttu-id="3dfd6-114">El servicio WIA solo administra los búferes pasados entre el autor de la llamada y el controlador.</span><span class="sxs-lookup"><span data-stu-id="3dfd6-114">The WIA service manages only those buffers passed between the caller and the driver.</span></span>

<span data-ttu-id="3dfd6-115">La segunda opción consiste en usar las propiedades personalizadas.</span><span class="sxs-lookup"><span data-stu-id="3dfd6-115">The second option is to use custom properties.</span></span> <span data-ttu-id="3dfd6-116">Usar el método **IWiaItemExtras:: escape** es más flexible que usar las propiedades de WIA personalizadas, pero las propiedades de WIA personalizadas permiten almacenar información en el flujo de propiedades del elemento para que el controlador pueda leer la información en otro momento.</span><span class="sxs-lookup"><span data-stu-id="3dfd6-116">Using the **IWiaItemExtras::Escape** method is more flexible than using custom WIA properties, but custom WIA properties allow you to store information in the item's property stream so that the driver can read the information at another time.</span></span>

 

 



