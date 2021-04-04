---
title: Tipos de exclusión mutua
description: Tipos de exclusión mutua
ms.assetid: bfe6cfe6-3df4-49c4-8015-fe4479b693c1
keywords:
- SDK de Windows Media Format, exclusión mutua
- Advanced Systems Format (ASF), exclusión mutua
- ASF (formato de sistemas avanzados), exclusión mutua
- exclusión mutua, tipos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c425e69c2aa3eac012874837a6970dbc26d1a51
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077276"
---
# <a name="mutual-exclusion-types"></a><span data-ttu-id="df46a-107">Tipos de exclusión mutua</span><span class="sxs-lookup"><span data-stu-id="df46a-107">Mutual Exclusion Types</span></span>

<span data-ttu-id="df46a-108">Puede usar tipos de exclusión mutua para identificar la naturaleza de un objeto de exclusión mutua en un perfil.</span><span class="sxs-lookup"><span data-stu-id="df46a-108">You can use mutual exclusion types to identify the nature of a mutual exclusion object in a profile.</span></span> <span data-ttu-id="df46a-109">Los tipos de exclusión mutua se usan como parámetros para [**IWMMutualExclusion:: GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-gettype) y [**IWMMutualExclusion:: SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype).</span><span class="sxs-lookup"><span data-stu-id="df46a-109">Mutual exclusion types are used as parameters for [**IWMMutualExclusion::GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-gettype) and [**IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype).</span></span>

<span data-ttu-id="df46a-110">En la tabla siguiente se enumeran los identificadores de los tipos de exclusión mutua.</span><span class="sxs-lookup"><span data-stu-id="df46a-110">The following table lists the identifiers for mutual exclusion types.</span></span>



| <span data-ttu-id="df46a-111">Constante de tipo de exclusión mutua</span><span class="sxs-lookup"><span data-stu-id="df46a-111">Mutual exclusion type constant</span></span> | <span data-ttu-id="df46a-112">GUID</span><span class="sxs-lookup"><span data-stu-id="df46a-112">GUID</span></span>                                 |
|--------------------------------|--------------------------------------|
| <span data-ttu-id="df46a-113">\_Lenguaje WMMUTEX \_ CLSID</span><span class="sxs-lookup"><span data-stu-id="df46a-113">CLSID\_WMMUTEX\_Language</span></span>       | <span data-ttu-id="df46a-114">D6E22A00-35DA-11D1-9034-00A0C90349BE</span><span class="sxs-lookup"><span data-stu-id="df46a-114">D6E22A00-35DA-11D1-9034-00A0C90349BE</span></span> |
| <span data-ttu-id="df46a-115">\_Velocidad de \_ bits WMMUTEX CLSID</span><span class="sxs-lookup"><span data-stu-id="df46a-115">CLSID\_WMMUTEX\_Bitrate</span></span>        | <span data-ttu-id="df46a-116">D6E22A01-35DA-11D1-9034-00A0C90349BE</span><span class="sxs-lookup"><span data-stu-id="df46a-116">D6E22A01-35DA-11D1-9034-00A0C90349BE</span></span> |
| <span data-ttu-id="df46a-117">\_Presentación de WMMUTEX CLSID \_</span><span class="sxs-lookup"><span data-stu-id="df46a-117">CLSID\_WMMUTEX\_Presentation</span></span>   | <span data-ttu-id="df46a-118">D6E22A02-35DA-11D1-9034-00A0C90349BE</span><span class="sxs-lookup"><span data-stu-id="df46a-118">D6E22A02-35DA-11D1-9034-00A0C90349BE</span></span> |
| <span data-ttu-id="df46a-119">CLSID \_ WMMUTEX \_ desconocido</span><span class="sxs-lookup"><span data-stu-id="df46a-119">CLSID\_WMMUTEX\_Unknown</span></span>        | <span data-ttu-id="df46a-120">D6E22A03-35DA-11D1-9034-00A0C90349BE</span><span class="sxs-lookup"><span data-stu-id="df46a-120">D6E22A03-35DA-11D1-9034-00A0C90349BE</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="df46a-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="df46a-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df46a-122">**Valores GUID**</span><span class="sxs-lookup"><span data-stu-id="df46a-122">**GUID Values**</span></span>](guid-values.md)
</dt> </dl>

 

 




