---
description: Proporciona una instancia de IMFMuxStreamMediaTypeManager que se puede utilizar para obtener los tipos de medios de las subsecuencias de un origen de medios multiplexados, así como para controlar la combinación de subflujos multiplexados por el origen.
ms.assetid: 5C36956D-336A-4956-8793-D86DC792E906
title: MF_MEDIATYPE_MULTIPLEXED_MANAGER atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa96c74bbff8f4858c8467fcd13253cfedf2f5dc
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104279790"
---
# <a name="mf_mediatype_multiplexed_manager-attribute"></a><span data-ttu-id="0d587-103">\_Atributo de \_ Administrador multiplexado de MEDIATYPE de MF \_</span><span class="sxs-lookup"><span data-stu-id="0d587-103">MF\_MEDIATYPE\_MULTIPLEXED\_MANAGER attribute</span></span>

<span data-ttu-id="0d587-104">Proporciona una instancia de [**IMFMuxStreamMediaTypeManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager) que se puede utilizar para obtener los tipos de medios de las subsecuencias de un origen de medios multiplexados, así como para controlar la combinación de subflujos multiplexados por el origen.</span><span class="sxs-lookup"><span data-stu-id="0d587-104">Provides an instance of [**IMFMuxStreamMediaTypeManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager) which can be used to get the media types of the substreams of a multiplexed media source as well as control the combination of substreams that are multiplexed by the source.</span></span>

## <a name="data-type"></a><span data-ttu-id="0d587-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0d587-105">Data type</span></span>

<span data-ttu-id="0d587-106">**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**</span><span class="sxs-lookup"><span data-stu-id="0d587-106">**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)**</span></span>

## <a name="remarks"></a><span data-ttu-id="0d587-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0d587-107">Remarks</span></span>

<span data-ttu-id="0d587-108">Pase este valor a [**IMFAttributes:: GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) para obtener una instancia de [**IMFMuxStreamMediaTypeManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager).</span><span class="sxs-lookup"><span data-stu-id="0d587-108">Pass this value into [**IMFAttributes::GetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown) to get an instance of [**IMFMuxStreamMediaTypeManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmuxstreammediatypemanager).</span></span>

## <a name="requirements"></a><span data-ttu-id="0d587-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d587-109">Requirements</span></span>



| <span data-ttu-id="0d587-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d587-110">Requirement</span></span> | <span data-ttu-id="0d587-111">Value</span><span class="sxs-lookup"><span data-stu-id="0d587-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0d587-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d587-112">Minimum supported client</span></span><br/> | <span data-ttu-id="0d587-113">Solo aplicaciones de escritorio de Windows 10, versión 1703 \[\]</span><span class="sxs-lookup"><span data-stu-id="0d587-113">Windows 10, version 1703 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0d587-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d587-114">Minimum supported server</span></span><br/> | <span data-ttu-id="0d587-115">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="0d587-115">None supported</span></span><br/>                                                          |
| <span data-ttu-id="0d587-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0d587-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d587-117"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d587-117"><dt>Mfidl.h</dt></span></span> </dl> |



 

 
