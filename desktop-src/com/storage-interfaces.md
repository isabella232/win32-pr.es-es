---
title: Interfaces de almacenamiento
description: Interfaces de almacenamiento
ms.assetid: bce0fd46-eeba-4a14-be1f-63d16885c28d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab06d8d0920ca7b29619df2173aaa0897c6eef6e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104533537"
---
# <a name="storage-interfaces"></a><span data-ttu-id="6b5e8-103">Interfaces de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="6b5e8-103">Storage Interfaces</span></span>

<span data-ttu-id="6b5e8-104">Los contenedores de control deben ser capaces de admitir controles que implementan [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)o [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit).</span><span class="sxs-lookup"><span data-stu-id="6b5e8-104">Control containers must be able to support controls that implement [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream), or [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit).</span></span> <span data-ttu-id="6b5e8-105">Opcionalmente, un contenedor puede admitir cualquier otra interfaz de persistencia como [**IPersistMemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), [**IPersistPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85))y [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)) para los controles que proporcionan compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="6b5e8-105">Optionally, a container can support any other persistence interfaces such as [**IPersistMemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), [**IPersistPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85)), and [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)) for those controls that provide support.</span></span>

<span data-ttu-id="6b5e8-106">Una vez que un contenedor de controles ActiveX ha elegido e inicializado una interfaz de almacenamiento que se va a usar ([**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream), [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), etc.), la interfaz de almacenamiento seguirá siendo la interfaz de almacenamiento principal mientras dure el control, es decir, el control permanecerá en posesión del almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="6b5e8-106">Once an ActiveX control container has chosen and initialized a storage interface to use ([**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream), [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), etc), that storage interface will remain the primary storage interface for the lifetime of the control, i.e. the control will remain in possession of the storage.</span></span> <span data-ttu-id="6b5e8-107">Esto no impide que el contenedor se guarde en otras interfaces de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="6b5e8-107">This does not preclude the container from saving to other storage interfaces.</span></span>

<span data-ttu-id="6b5e8-108">No es necesario que los contenedores de controles ActiveX admitan un mecanismo de texto de guardar como, por lo que el uso de [**IPersistPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85)) y el método [**IPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)) de la interfaz de contenedor asociada son opcionales.</span><span class="sxs-lookup"><span data-stu-id="6b5e8-108">ActiveX control containers do not need to support a save as text mechanism, thus using [**IPersistPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85)) and the associated container-side interface [**IPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768196(v=vs.85)) are optional.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b5e8-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6b5e8-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b5e8-110">Contenedores</span><span class="sxs-lookup"><span data-stu-id="6b5e8-110">Containers</span></span>](containers.md)
</dt> </dl>

 

 