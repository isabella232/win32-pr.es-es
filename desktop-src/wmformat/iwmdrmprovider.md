---
title: Interfaz IWMDRMProvider
description: La interfaz IWMDRMProvider proporciona un método que crea los demás objetos de las API extendidas del cliente DRM de Microsoft Windows Media. puede obtener un puntero a una instancia de esta interfaz mediante una llamada a la función WMDRMCreateProvider.
ms.assetid: bcd346e3-a79f-49a8-b5f9-b9ae8b54527a
keywords:
- Interfaz IWMDRMProvider formato de Windows Media
- Interfaz IWMDRMProvider formato de Windows Media, descrito
topic_type:
- apiref
api_name:
- IWMDRMProvider
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9653bc612cdbc865d8e77cb7916b0b8f54d0fd0e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793060"
---
# <a name="iwmdrmprovider-interface"></a><span data-ttu-id="dbf04-105">Interfaz IWMDRMProvider</span><span class="sxs-lookup"><span data-stu-id="dbf04-105">IWMDRMProvider interface</span></span>

<span data-ttu-id="dbf04-106">La interfaz **IWMDRMProvider** proporciona un método que crea los demás objetos de las API extendidas del cliente DRM de Microsoft Windows Media.</span><span class="sxs-lookup"><span data-stu-id="dbf04-106">The **IWMDRMProvider** interface provides a method that creates the other objects of the Microsoft Windows Media DRM Client Extended APIs.</span></span>

<span data-ttu-id="dbf04-107">Puede obtener un puntero a una instancia de esta interfaz mediante una llamada a la función [**WMDRMCreateProvider**](wmdrmcreateprovider.md) .</span><span class="sxs-lookup"><span data-stu-id="dbf04-107">You can obtain a pointer to an instance of this interface by calling the [**WMDRMCreateProvider**](wmdrmcreateprovider.md) function.</span></span> <span data-ttu-id="dbf04-108">Para obtener un puntero a una instancia de esta interfaz que pueda crear objetos seguros, debe llamar a la función [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md) .</span><span class="sxs-lookup"><span data-stu-id="dbf04-108">To obtain a pointer to an instance of this interface that can create secure objects, you must call the [**WMDRMCreateProtectedProvider**](wmdrmcreateprotectedprovider.md) function.</span></span>

## <a name="members"></a><span data-ttu-id="dbf04-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="dbf04-109">Members</span></span>

<span data-ttu-id="dbf04-110">La interfaz **IWMDRMProvider** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="dbf04-110">The **IWMDRMProvider** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="dbf04-111">**IWMDRMProvider** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="dbf04-111">**IWMDRMProvider** also has these types of members:</span></span>

-   [<span data-ttu-id="dbf04-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="dbf04-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="dbf04-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="dbf04-113">Methods</span></span>

<span data-ttu-id="dbf04-114">La interfaz **IWMDRMProvider** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="dbf04-114">The **IWMDRMProvider** interface has these methods.</span></span>



| <span data-ttu-id="dbf04-115">Método</span><span class="sxs-lookup"><span data-stu-id="dbf04-115">Method</span></span>                                              | <span data-ttu-id="dbf04-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="dbf04-116">Description</span></span>                                                                                          |
|:----------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dbf04-117">**DataSpace**</span><span class="sxs-lookup"><span data-stu-id="dbf04-117">**CreateObject**</span></span>](iwmdrmprovider-createobject.md) | <span data-ttu-id="dbf04-118">Recupera un puntero a una interfaz especificada y crea el objeto de implementación si es necesario.</span><span class="sxs-lookup"><span data-stu-id="dbf04-118">Retrieves a pointer to a specified interface, creating the implementing object if needed.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="dbf04-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="dbf04-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dbf04-120">**Interfaces**</span><span class="sxs-lookup"><span data-stu-id="dbf04-120">**Interfaces**</span></span>](drm-interfaces.md)
</dt> </dl>

 

