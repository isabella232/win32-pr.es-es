---
title: Exponer información adicional no incluida en la interfaz IAccessible
description: En función de sus productos, es posible que los desarrolladores de servidores deban exponer información o funcionalidad además de la compatibilidad con Microsoft Active Accessibility.
ms.assetid: c45009ca-6be3-4645-9097-36671a41dfce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3834c60de8f18fd5ec0719919a1cd79e22f451e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359271"
---
# <a name="exposing-additional-information-not-covered-by-iaccessible-interface"></a><span data-ttu-id="82d93-103">Exponer información adicional no incluida en la interfaz IAccessible</span><span class="sxs-lookup"><span data-stu-id="82d93-103">Exposing Additional Information Not Covered by IAccessible Interface</span></span>

<span data-ttu-id="82d93-104">En función de sus productos, es posible que los desarrolladores de servidores deban exponer información o funcionalidad además de la compatibilidad con Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="82d93-104">Depending on their products, server developers might need to expose information or functionality in addition to Microsoft Active Accessibility support.</span></span> <span data-ttu-id="82d93-105">En este caso, trabaje con los proveedores de tecnología de asistencia (clientes) para asegurarse de que agregan compatibilidad con las características.</span><span class="sxs-lookup"><span data-stu-id="82d93-105">If this is the case, work with assistive technology vendors (clients) to ensure that they add support for the features.</span></span>

<span data-ttu-id="82d93-106">No intente extender la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="82d93-106">Do not attempt to extend the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="82d93-107">Las interfaces no se pueden cambiar una vez que se publican.</span><span class="sxs-lookup"><span data-stu-id="82d93-107">Interfaces cannot be changed once they are published.</span></span> <span data-ttu-id="82d93-108">Para exponer información adicional, use una interfaz personalizada y exposición mediante una de las técnicas siguientes:</span><span class="sxs-lookup"><span data-stu-id="82d93-108">To expose additional information, use a custom interface and expose it by using one of the following techniques:</span></span>

-   [<span data-ttu-id="82d93-109">Usar OBJID \_ NATIVEOM para exponer una interfaz nativa del modelo de objetos para una ventana</span><span class="sxs-lookup"><span data-stu-id="82d93-109">Using OBJID\_NATIVEOM to expose a native object model interface for a window</span></span>](using-objid-nativeom-to-expose-a-native-object-model-interface-for-a-window.md)
-   [<span data-ttu-id="82d93-110">Usar QueryService para exponer una interfaz nativa del modelo de objetos para un objeto IAccessible</span><span class="sxs-lookup"><span data-stu-id="82d93-110">Using QueryService to expose a native object model interface for an IAccessible object</span></span>](using-queryservice-to-expose-a-native-object-model-interface-for-an-iaccessible-object.md)

<span data-ttu-id="82d93-111">Tenga en cuenta que el objetivo de la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) es tener una interfaz bien definida que utilicen los servidores y los clientes.</span><span class="sxs-lookup"><span data-stu-id="82d93-111">Note that the goal of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface is to have a well-defined interface that is used by servers and clients.</span></span> <span data-ttu-id="82d93-112">Antes de exponer las interfaces personalizadas, asegúrese de exponer tanta información como sea posible a través de **IAccessible**.</span><span class="sxs-lookup"><span data-stu-id="82d93-112">Before exposing custom interfaces, be sure to expose as much information as possible through **IAccessible**.</span></span>

<span data-ttu-id="82d93-113">No se puede usar [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) para exponer interfaces personalizadas.</span><span class="sxs-lookup"><span data-stu-id="82d93-113">You cannot use [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to expose custom interfaces.</span></span> <span data-ttu-id="82d93-114">Use **IServiceProvider:: QueryService** tal y como se describe en los procedimientos siguientes.</span><span class="sxs-lookup"><span data-stu-id="82d93-114">Use **IServiceProvider::QueryService** as outlined in the following procedures.</span></span>

 

 