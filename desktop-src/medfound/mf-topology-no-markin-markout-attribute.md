---
description: Especifica si la canalización recorta los ejemplos.
ms.assetid: 4ba66d18-3854-4994-9509-967303dc7d98
title: MF_TOPOLOGY_NO_MARKIN_MARKOUT atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03d7b0152798379406887619a3e691cc528a6993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275944"
---
# <a name="mf_topology_no_markin_markout-attribute"></a><span data-ttu-id="66ff6-103">\_No se pudo \_ marcar el \_ \_ atributo MARKOUT en la topología MF</span><span class="sxs-lookup"><span data-stu-id="66ff6-103">MF\_TOPOLOGY\_NO\_MARKIN\_MARKOUT attribute</span></span>

<span data-ttu-id="66ff6-104">Especifica si la canalización recorta los ejemplos.</span><span class="sxs-lookup"><span data-stu-id="66ff6-104">Specifies whether the pipeline trims samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="66ff6-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="66ff6-105">Data type</span></span>

<span data-ttu-id="66ff6-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="66ff6-106">**UINT32**</span></span>

<span data-ttu-id="66ff6-107">Trata como un valor booleano.</span><span class="sxs-lookup"><span data-stu-id="66ff6-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="66ff6-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="66ff6-108">Remarks</span></span>

<span data-ttu-id="66ff6-109">De forma predeterminada, la canalización recorta los ejemplos para que coincidan con los tiempos de presentación correctos.</span><span class="sxs-lookup"><span data-stu-id="66ff6-109">By default, the pipeline trims samples to match the correct presentation times.</span></span> <span data-ttu-id="66ff6-110">El recorte se realiza en los nodos de topología que tienen los atributos [**MF \_ TOPONODE \_ avelinot \_ aquí**](mf-toponode-markin-here-attribute.md) y [**MF \_ TOPONODE \_ MARKOUT \_ aquí**](mf-toponode-markout-here-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="66ff6-110">Trimming is done at the topology nodes that have the [**MF\_TOPONODE\_MARKIN\_HERE**](mf-toponode-markin-here-attribute.md) and [**MF\_TOPONODE\_MARKOUT\_HERE**](mf-toponode-markout-here-attribute.md) attributes.</span></span> <span data-ttu-id="66ff6-111">Si el atributo MF de la **\_ topología \_ no \_ \_ MARKOUT** está establecido en **true** en la topología, la canalización no recorta los ejemplos y se omiten los atributos **MF \_ TOPONODE \_ Avelino \_ here** y **MF \_ TOPONODE \_ MARKOUT \_ aquí** .</span><span class="sxs-lookup"><span data-stu-id="66ff6-111">If the **MF\_TOPOLOGY\_NO\_MARKIN\_MARKOUT** attribute is set to **TRUE** on the topology, the pipeline does not trim samples, and the **MF\_TOPONODE\_MARKIN\_HERE** and **MF\_TOPONODE\_MARKOUT\_HERE** attributes are ignored.</span></span> <span data-ttu-id="66ff6-112">Si el atributo no está establecido o tiene el valor **false**, la canalización recorta los ejemplos.</span><span class="sxs-lookup"><span data-stu-id="66ff6-112">If the attribute is not set, or has the value **FALSE**, the pipeline trims samples.</span></span>

<span data-ttu-id="66ff6-113">Una aplicación puede establecer el atributo de la **\_ topología MF \_ sin \_ Marken \_ MARKOUT** en **true** si la aplicación recibe muestras comprimidas de la canalización y necesita obtener todos los fotogramas clave, que de lo contrario se pueden recortar.</span><span class="sxs-lookup"><span data-stu-id="66ff6-113">An application might set the **MF\_TOPOLOGY\_NO\_MARKIN\_MARKOUT** attribute to **TRUE** if the application receives compressed samples from the pipeline and needs to get all of the key frames, which might otherwise be trimmed.</span></span>

<span data-ttu-id="66ff6-114">El valor predeterminado de este atributo es **false**.</span><span class="sxs-lookup"><span data-stu-id="66ff6-114">The default value of this attribute is **FALSE**.</span></span>

<span data-ttu-id="66ff6-115">La constante GUID para este atributo se exporta desde mfuuid. lib.</span><span class="sxs-lookup"><span data-stu-id="66ff6-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="66ff6-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66ff6-116">Requirements</span></span>



| <span data-ttu-id="66ff6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="66ff6-117">Requirement</span></span> | <span data-ttu-id="66ff6-118">Value</span><span class="sxs-lookup"><span data-stu-id="66ff6-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="66ff6-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66ff6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="66ff6-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="66ff6-120">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="66ff6-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66ff6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="66ff6-122">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="66ff6-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="66ff6-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="66ff6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="66ff6-124"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="66ff6-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66ff6-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="66ff6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66ff6-126">Lista alfabética de atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="66ff6-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="66ff6-127">**IMFAttributes:: GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="66ff6-127">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="66ff6-128">**IMFAttributes:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="66ff6-128">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="66ff6-129">**\_TOPONODE MF \_ \_ aquí**</span><span class="sxs-lookup"><span data-stu-id="66ff6-129">**MF\_TOPONODE\_MARKIN\_HERE**</span></span>](mf-toponode-markin-here-attribute.md)
</dt> <dt>

[<span data-ttu-id="66ff6-130">**MF \_ TOPONODE \_ MARKOUT \_ aquí**</span><span class="sxs-lookup"><span data-stu-id="66ff6-130">**MF\_TOPONODE\_MARKOUT\_HERE**</span></span>](mf-toponode-markout-here-attribute.md)
</dt> <dt>

[<span data-ttu-id="66ff6-131">Atributos de topología</span><span class="sxs-lookup"><span data-stu-id="66ff6-131">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




