---
title: Interfaces de almacenamiento
description: Interfaces de almacenamiento
ms.assetid: bce0fd46-eeba-4a14-be1f-63d16885c28d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97ad0cc646d45ca0b77a70ecaf47d28eadb4d136
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549270"
---
# <a name="storage-interfaces"></a><span data-ttu-id="695e2-103">Interfaces de almacenamiento</span><span class="sxs-lookup"><span data-stu-id="695e2-103">Storage Interfaces</span></span>

<span data-ttu-id="695e2-104">Los contenedores de controles deben ser capaces de admitir controles que implementen [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)o [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit).</span><span class="sxs-lookup"><span data-stu-id="695e2-104">Control containers must be able to support controls that implement [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream), or [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit).</span></span> <span data-ttu-id="695e2-105">Opcionalmente, un contenedor puede admitir cualquier otra interfaz de persistencia, como [**IPersistMemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag)e [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)) para los controles que proporcionan compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="695e2-105">Optionally, a container can support any other persistence interfaces such as [**IPersistMemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag), and [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)) for those controls that provide support.</span></span>

<span data-ttu-id="695e2-106">Una vez que un contenedor de controles ActiveX ha elegido e inicializado una interfaz de almacenamiento para usar ([**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream), [**IPersistStreamInit,**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit)etc.), esa interfaz de almacenamiento seguirá siendo la interfaz de almacenamiento principal durante la vigencia del control, es decir, el control permanecerá en posesión del almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="695e2-106">Once an ActiveX control container has chosen and initialized a storage interface to use ([**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream), [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), etc), that storage interface will remain the primary storage interface for the lifetime of the control, i.e. the control will remain in possession of the storage.</span></span> <span data-ttu-id="695e2-107">Esto no impide que el contenedor se guarde en otras interfaces de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="695e2-107">This does not preclude the container from saving to other storage interfaces.</span></span>

<span data-ttu-id="695e2-108">Los contenedores de controles ActiveX no necesitan admitir un mecanismo de guardado como texto, por lo que el uso de [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag) y la interfaz del lado contenedor [**asociada IPropertyBag**](/windows/win32/api/oaidl/nn-oaidl-ipropertybag) son opcionales.</span><span class="sxs-lookup"><span data-stu-id="695e2-108">ActiveX control containers do not need to support a save as text mechanism, thus using [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag) and the associated container-side interface [**IPropertyBag**](/windows/win32/api/oaidl/nn-oaidl-ipropertybag) are optional.</span></span>

## <a name="related-topics"></a><span data-ttu-id="695e2-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="695e2-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="695e2-110">Contenedores</span><span class="sxs-lookup"><span data-stu-id="695e2-110">Containers</span></span>](containers.md)
</dt> </dl>

 

 