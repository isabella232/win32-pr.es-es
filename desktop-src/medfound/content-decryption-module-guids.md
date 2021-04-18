---
description: Los siguientes GUID admiten implementaciones del módulo de descifrado de contenido (CDM).
title: GUID de módulo de descifrado de contenido (CDM)
ms.topic: reference
ms.date: 01/21/2018
ms.openlocfilehash: e06601fd23d3244d0965d2cfd7cd70a6f73a481f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105721593"
---
# <a name="content-decryption-module-cdm-guids"></a><span data-ttu-id="214b7-103">GUID de módulo de descifrado de contenido (CDM)</span><span class="sxs-lookup"><span data-stu-id="214b7-103">Content Decryption Module (CDM) GUIDs</span></span>

<span data-ttu-id="214b7-104">Los siguientes GUID admiten implementaciones del módulo de descifrado de contenido (CDM).</span><span class="sxs-lookup"><span data-stu-id="214b7-104">The following GUIDs support Content Decryption Module (CDM) implementations.</span></span>

<span data-ttu-id="214b7-105">**MF_CONTENTDECRYPTIONMODULE_SERVICE**</span><span class="sxs-lookup"><span data-stu-id="214b7-105">**MF_CONTENTDECRYPTIONMODULE_SERVICE**</span></span>

<span data-ttu-id="214b7-106">GUID de servicio usado para obtener interfaces de una implementación de [IMFContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule) , como la interfaz [IMediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver) de WinRT.</span><span class="sxs-lookup"><span data-stu-id="214b7-106">Service GUID used to obtain interfaces from an [IMFContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule) implementation,such as the WinRT [IMediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver) interface.</span></span> <span data-ttu-id="214b7-107">Una implementación de **IMFContentDecryptionModule** debe implementar [IMFGetService](/windows/win32/api/mfidl/nn-mfidl-imfgetservice) y admitir este GUID de servicio.</span><span class="sxs-lookup"><span data-stu-id="214b7-107">An implementation of **IMFContentDecryptionModule** should implement [IMFGetService](/windows/win32/api/mfidl/nn-mfidl-imfgetservice) and support this service GUID.</span></span>


## <a name="requirements"></a><span data-ttu-id="214b7-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="214b7-108">Requirements</span></span>



| <span data-ttu-id="214b7-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="214b7-109">Requirement</span></span> | <span data-ttu-id="214b7-110">Value</span><span class="sxs-lookup"><span data-stu-id="214b7-110">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="214b7-111">Encabezado</span><span class="sxs-lookup"><span data-stu-id="214b7-111">Header</span></span><br/> | <dl> <span data-ttu-id="214b7-112"><dt>mfcontentdecryptionmodule. h</dt></span><span class="sxs-lookup"><span data-stu-id="214b7-112"><dt>mfcontentdecryptionmodule.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="214b7-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="214b7-113">See also</span></span>



- [<span data-ttu-id="214b7-114">Constantes de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="214b7-114">Media Foundation Constants</span></span>](media-foundation-constants.md)
- <span data-ttu-id="214b7-115">[IMFContentDecryptionModule] (/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule</span><span class="sxs-lookup"><span data-stu-id="214b7-115">[IMFContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nn-mfcontentdecryptionmodule-imfcontentdecryptionmodule</span></span>
- [<span data-ttu-id="214b7-116">IMediaProtectionPMPServer</span><span class="sxs-lookup"><span data-stu-id="214b7-116">IMediaProtectionPMPServer</span></span>](/uwp/api/windows.media.protection.mediaprotectionpmpserver)
- [<span data-ttu-id="214b7-117">IMFGetService</span><span class="sxs-lookup"><span data-stu-id="214b7-117">IMFGetService</span></span>](/windows/win32/api/mfidl/nn-mfidl-imfgetservice)


 

 




