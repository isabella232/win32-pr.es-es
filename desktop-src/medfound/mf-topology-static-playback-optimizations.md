---
description: Habilita las optimizaciones estáticas en la canalización de vídeo.
ms.assetid: 62fb3f0f-ab1f-4c61-8e7f-62908b947788
title: MF_TOPOLOGY_STATIC_PLAYBACK_OPTIMIZATIONS atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6f9f7d884c49078ca02571f8ba141f9a1e13589
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707172"
---
# <a name="mf_topology_static_playback_optimizations-attribute"></a><span data-ttu-id="9663a-103">\_ \_ \_ Atributo de optimizaciones de reproducción estática \_ de topología MF</span><span class="sxs-lookup"><span data-stu-id="9663a-103">MF\_TOPOLOGY\_STATIC\_PLAYBACK\_OPTIMIZATIONS attribute</span></span>

<span data-ttu-id="9663a-104">Habilita las optimizaciones estáticas en la canalización de vídeo.</span><span class="sxs-lookup"><span data-stu-id="9663a-104">Enables static optimizations in the video pipeline.</span></span>

## <a name="data-type"></a><span data-ttu-id="9663a-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="9663a-105">Data type</span></span>

<span data-ttu-id="9663a-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="9663a-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="9663a-107">Obtener o establecer</span><span class="sxs-lookup"><span data-stu-id="9663a-107">Get/set</span></span>

<span data-ttu-id="9663a-108">Para obtener este atributo, llame a [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="9663a-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="9663a-109">Para establecer este atributo, llame a [**IMFAttributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="9663a-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="9663a-110">Se aplica a</span><span class="sxs-lookup"><span data-stu-id="9663a-110">Applies to</span></span>

[<span data-ttu-id="9663a-111">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="9663a-111">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="9663a-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9663a-112">Remarks</span></span>

<span data-ttu-id="9663a-113">Establezca este atributo antes de cargar una topología.</span><span class="sxs-lookup"><span data-stu-id="9663a-113">Set this attribute before loading a topology.</span></span> <span data-ttu-id="9663a-114">Si el atributo es **true**, el cargador de topología intenta optimizar la canalización antes de que se inicie la reproducción.</span><span class="sxs-lookup"><span data-stu-id="9663a-114">If the attribute is **TRUE**, the topology loader attempts to optimize the pipeline before playback starts.</span></span>

<span data-ttu-id="9663a-115">Si establece este atributo, también debe establecer los siguientes atributos:</span><span class="sxs-lookup"><span data-stu-id="9663a-115">If you set this attribute, you should also set the following attributes:</span></span>

-   [<span data-ttu-id="9663a-116">velocidad de reproducción de \_ topología MF \_ \_</span><span class="sxs-lookup"><span data-stu-id="9663a-116">MF\_TOPOLOGY\_PLAYBACK\_FRAMERATE</span></span>](mf-topology-playback-framerate.md)
-   [<span data-ttu-id="9663a-117">\_DiMS de reproducción de topologías \_ \_ máx \_ .</span><span class="sxs-lookup"><span data-stu-id="9663a-117">MF\_TOPOLOGY\_PLAYBACK\_MAX\_DIMS</span></span>](mf-topology-playback-max-dims.md)

<span data-ttu-id="9663a-118">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="9663a-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="examples"></a><span data-ttu-id="9663a-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9663a-119">Examples</span></span>


```C++
HRESULT SetPlaybackOptimizations(IMFTopology *pTopology, HWND hwnd)
{
    HRESULT hr = pTopology->SetUINT32(
        MF_TOPOLOGY_STATIC_PLAYBACK_OPTIMIZATIONS, TRUE);

    if (FAILED(hr))
    {
        return hr;
    }

    HMONITOR hCurrentMon = MonitorFromWindow(hwnd, MONITOR_DEFAULTTOPRIMARY);

    if (hCurrentMon)
    {
        MONITORINFO MonitorInfo = {0};
        MonitorInfo.cbSize = sizeof(MONITORINFO);

        BOOL fSucceeded = GetMonitorInfo(hCurrentMon, &MonitorInfo);

        if (fSucceeded )
        {
            const RECT& rcMonitor = MonitorInfo.rcMonitor;

            LONG width = rcMonitor.right - rcMonitor.left;
            LONG height = rcMonitor.bottom - rcMonitor.top;

            hr = MFSetAttributeSize(
                pTopology, 
                MF_TOPOLOGY_PLAYBACK_MAX_DIMS, 
                (UINT32)width, (UINT32)height
                );

            if (FAILED(hr))
            {
                goto done;
            }

            HDC hdc = GetDC(hwnd);

            hr = MFSetAttributeRatio(
                pTopology,
                MF_TOPOLOGY_PLAYBACK_FRAMERATE,
                GetDeviceCaps(hdc, VREFRESH), 1
                );

            ReleaseDC(hwnd, hdc);
        }
    }
done:
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="9663a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9663a-120">Requirements</span></span>



| <span data-ttu-id="9663a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9663a-121">Requirement</span></span> | <span data-ttu-id="9663a-122">Value</span><span class="sxs-lookup"><span data-stu-id="9663a-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9663a-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9663a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9663a-124">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="9663a-124">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9663a-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9663a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9663a-126">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9663a-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="9663a-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9663a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="9663a-128"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="9663a-128"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9663a-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="9663a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9663a-130">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9663a-130">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9663a-131">Atributos de topología</span><span class="sxs-lookup"><span data-stu-id="9663a-131">Topology Attributes</span></span>](topology-attributes.md)
</dt> <dt>

[<span data-ttu-id="9663a-132">Administración de calidad de vídeo</span><span class="sxs-lookup"><span data-stu-id="9663a-132">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




