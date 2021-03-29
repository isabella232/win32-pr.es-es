---
description: Proporciona una instancia de IMFMuxStreamAttributesManager que administra el IMFAttributes que describe las subsecuencias de un origen de medios multiplexado.
ms.assetid: 0149BD8B-8C9D-47FD-9EC1-BEBEE73BC73E
title: MF_DEVICESTREAM_MULTIPLEXED_MANAGER atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b495b4054337aaa709bee430ae78ff4bed658911
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648262"
---
# <a name="mf_devicestream_multiplexed_manager-attribute"></a><span data-ttu-id="00f10-103">MF \_ DEVICESTREAM \_ atributo de \_ Administrador multiplexado</span><span class="sxs-lookup"><span data-stu-id="00f10-103">MF\_DEVICESTREAM\_MULTIPLEXED\_MANAGER attribute</span></span>

<span data-ttu-id="00f10-104">Proporciona una instancia de [**IMFMuxStreamAttributesManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager) que administra el [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) que describe las subsecuencias de un origen de medios multiplexado.</span><span class="sxs-lookup"><span data-stu-id="00f10-104">Provides an instance of [**IMFMuxStreamAttributesManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager) which manages the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) describing the substreams of a multiplexed media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="00f10-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="00f10-105">Data type</span></span>

<span data-ttu-id="00f10-106">**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**</span><span class="sxs-lookup"><span data-stu-id="00f10-106">**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**</span></span>

## <a name="remarks"></a><span data-ttu-id="00f10-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="00f10-107">Remarks</span></span>

<span data-ttu-id="00f10-108">Pase este valor a [**IMFAttributes:: GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) para determinar si el origen multimedia proporciona secuencias multiplexadas y, si es así, obtener una instancia de [**IMFMuxStreamAttributesManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager).</span><span class="sxs-lookup"><span data-stu-id="00f10-108">Pass this value into [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) to determine if the media source provides multiplexed streams and, if so, get an instance of [**IMFMuxStreamAttributesManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreamattributesmanager).</span></span>

## <a name="requirements"></a><span data-ttu-id="00f10-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00f10-109">Requirements</span></span>



| <span data-ttu-id="00f10-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="00f10-110">Requirement</span></span> | <span data-ttu-id="00f10-111">Value</span><span class="sxs-lookup"><span data-stu-id="00f10-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="00f10-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="00f10-112">Minimum supported client</span></span><br/> | <span data-ttu-id="00f10-113">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="00f10-113">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="00f10-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="00f10-114">Minimum supported server</span></span><br/> | <span data-ttu-id="00f10-115">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="00f10-115">None supported</span></span><br/>                                                          |
| <span data-ttu-id="00f10-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="00f10-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="00f10-117"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="00f10-117"><dt>Mfidl.h</dt></span></span> </dl> |



 

 
