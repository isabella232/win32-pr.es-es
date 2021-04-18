---
description: Especifica una cadena de contexto usada por las implementaciones del módulo de descifrado de contenido (CDM) que usan MediaProtectionPMPServer.
title: MF_CONTENTDECRYPTIONMODULE_PMPSTORECONTEXT (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: 49e12aeba9cce988c58fca94c33e7b4179530a56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105720472"
---
# <a name="mf_contentdecryptionmodule_pmpstorecontext-property"></a><span data-ttu-id="5d60f-103">\_ \_ Propiedad PMPSTORECONTEXT de MF CONTENTDECRYPTIONMODULE</span><span class="sxs-lookup"><span data-stu-id="5d60f-103">MF\_CONTENTDECRYPTIONMODULE\_PMPSTORECONTEXT property</span></span>

<span data-ttu-id="5d60f-104">Especifica una cadena de contexto usada por las implementaciones del módulo de descifrado de contenido (CDM) que usan [MediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver).</span><span class="sxs-lookup"><span data-stu-id="5d60f-104">Specifies a context string used by Content Decryption Module (CDM) implementations that use [MediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver).</span></span>


## <a name="data-type"></a><span data-ttu-id="5d60f-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="5d60f-105">Data type</span></span>

<span data-ttu-id="5d60f-106">**LPWStr** (VT_LPWSTR)</span><span class="sxs-lookup"><span data-stu-id="5d60f-106">**LPWSTR** (VT_LPWSTR)</span></span>

## <a name="property-guid"></a><span data-ttu-id="5d60f-107">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="5d60f-107">Property GUID</span></span>

<span data-ttu-id="5d60f-108">**MF \_ CONTENTDECRYPTIONMODULE \_ PMPSTORECONTEXT**</span><span class="sxs-lookup"><span data-stu-id="5d60f-108">**MF\_CONTENTDECRYPTIONMODULE\_PMPSTORECONTEXT**</span></span>

## <a name="property-value"></a><span data-ttu-id="5d60f-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="5d60f-109">Property value</span></span>

<span data-ttu-id="5d60f-110">Una cadena de contexto utilizada por las implementaciones del módulo de descifrado de contenido (CDM).</span><span class="sxs-lookup"><span data-stu-id="5d60f-110">A  a context string used by Content Decryption Module (CDM) implementations.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d60f-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5d60f-111">Remarks</span></span>

<span data-ttu-id="5d60f-112">El implementador de CDM debe buscar este valor y pasar el valor al [constructor MediaProtectionPMPServer](/uwp/api/windows.media.protection.mediaprotectionpmpserver.-ctor) con el nombre de propiedad "Windows. Media. Protection. PMPStoreContext".</span><span class="sxs-lookup"><span data-stu-id="5d60f-112">The CDM implementer should look for this value and pass the value to the [MediaProtectionPMPServer constructor](/uwp/api/windows.media.protection.mediaprotectionpmpserver.-ctor) using the property name "Windows.Media.Protection.PMPStoreContext".</span></span>


<span data-ttu-id="5d60f-113">Las aplicaciones no deben crear esta propiedad al llamar a [IMFContentDecryptionModuleAccess:: CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).</span><span class="sxs-lookup"><span data-stu-id="5d60f-113">Apps should not create this property when calling [IMFContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).</span></span>

## <a name="requirements"></a><span data-ttu-id="5d60f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d60f-114">Requirements</span></span>



| <span data-ttu-id="5d60f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d60f-115">Requirement</span></span> | <span data-ttu-id="5d60f-116">Value</span><span class="sxs-lookup"><span data-stu-id="5d60f-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5d60f-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d60f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5d60f-118">Actualización 2020 de abril de Windows 10</span><span class="sxs-lookup"><span data-stu-id="5d60f-118">Windows 10 April 2020 Update</span></span><br/>                                     |
| <span data-ttu-id="5d60f-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5d60f-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d60f-120"><dt>mfcontentdecryptionmodule. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d60f-120"><dt>mfcontentdecryptionmodule.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d60f-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="5d60f-121">See also</span></span>

- [<span data-ttu-id="5d60f-122">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5d60f-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
- [<span data-ttu-id="5d60f-123">MediaProtectionPMPServer</span><span class="sxs-lookup"><span data-stu-id="5d60f-123">MediaProtectionPMPServer</span></span>](/uwp/api/windows.media.protection.mediaprotectionpmpserver)


 

 




