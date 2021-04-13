---
title: DRM_ActionAllowed_CollaborativePlay
description: El \_ atributo CollaborativePlay de DRM ActionAllowed \_ indica si la licencia permite reproducir el contenido en colaboración.
ms.assetid: 111e8fa7-ef5a-483a-b930-8a8e5b4d120a
keywords:
- DRM_ActionAllowed_CollaborativePlay formato de Windows Media
topic_type:
- apiref
api_name:
- DRM_ActionAllowed_CollaborativePlay
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0268c9c3d70a8f51db390544bf854e5acd5b9e88
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420307"
---
# <a name="drm_actionallowed_collaborativeplay"></a><span data-ttu-id="94cc1-104">\_CollaborativePlay ACTIONALLOWED \_ DRM</span><span class="sxs-lookup"><span data-stu-id="94cc1-104">DRM\_ActionAllowed\_CollaborativePlay</span></span>

<span data-ttu-id="94cc1-105">El **atributo \_ \_ CollaborativePlay de DRM ActionAllowed** indica si la licencia permite reproducir el contenido en colaboración.</span><span class="sxs-lookup"><span data-stu-id="94cc1-105">The **DRM\_ActionAllowed\_CollaborativePlay** attribute indicates whether the license allows the content to be played collaboratively.</span></span>

## <a name="global-constant"></a><span data-ttu-id="94cc1-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="94cc1-106">Global Constant</span></span>

<span data-ttu-id="94cc1-107">g \_ wszWMDRM \_ ActionAllowed \_ CollaborativePlay</span><span class="sxs-lookup"><span data-stu-id="94cc1-107">g\_wszWMDRM\_ActionAllowed\_CollaborativePlay</span></span>

## <a name="data-type"></a><span data-ttu-id="94cc1-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="94cc1-108">Data Type</span></span>

<span data-ttu-id="94cc1-109">**tipo de WMT \_ \_ bool**</span><span class="sxs-lookup"><span data-stu-id="94cc1-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="94cc1-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="94cc1-110">Remarks</span></span>

<span data-ttu-id="94cc1-111">El derecho de reproducción colaborativa se aplica a la reproducción de contenido protegido como parte de una sesión de colaboración mediante servicios punto a punto.</span><span class="sxs-lookup"><span data-stu-id="94cc1-111">The collaborative play right applies to playing protected content as part of a collaborative session using peer-to-peer services.</span></span> <span data-ttu-id="94cc1-112">Por ejemplo, los usuarios de MSN Messenger 2004 pueden reproducir contenido protegido en una sesión de MusicMix.</span><span class="sxs-lookup"><span data-stu-id="94cc1-112">For example, users of MSN Messenger 2004 can play protected content in a MusicMix session.</span></span> <span data-ttu-id="94cc1-113">Este derecho solo se puede usar para contribuir a un archivo protegido en una sola sesión al mismo tiempo, y todos los usuarios que participan en la sesión deben estar en línea para representar el contenido.</span><span class="sxs-lookup"><span data-stu-id="94cc1-113">This right can only be used to contribute a protected file to a single session at one time, and all users participating in the session must be online to render the content.</span></span>

<span data-ttu-id="94cc1-114">Se trata de una propiedad de solo lectura que se recupera mediante [**IWMDRMReader:: GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span><span class="sxs-lookup"><span data-stu-id="94cc1-114">This is a read-only property that is retrieved using [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty).</span></span>

## <a name="see-also"></a><span data-ttu-id="94cc1-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="94cc1-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94cc1-116">**Propiedades de DRM**</span><span class="sxs-lookup"><span data-stu-id="94cc1-116">**DRM Properties**</span></span>](drm-properties.md)
</dt> </dl>

 

 




