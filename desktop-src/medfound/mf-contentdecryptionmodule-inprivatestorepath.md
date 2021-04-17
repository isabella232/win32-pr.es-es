---
description: Especifica una ruta de acceso de archivo que representa una ubicación de almacenamiento que el módulo de descifrado de contenido (CDM) puede usar para datos específicos del contenido.
title: MF_CONTENTDECRYPTIONMODULE_INPRIVATESTOREPATH (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: 0d8ce394f4b7a4e952fc9d5928a80cc5500dcdd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542558"
---
# <a name="mf_contentdecryptionmodule_inprivatestorepath-property"></a><span data-ttu-id="aea38-103">\_ \_ Propiedad INPRIVATESTOREPATH de MF CONTENTDECRYPTIONMODULE</span><span class="sxs-lookup"><span data-stu-id="aea38-103">MF\_CONTENTDECRYPTIONMODULE\_INPRIVATESTOREPATH property</span></span>

<span data-ttu-id="aea38-104">Especifica una ruta de acceso de archivo que representa una ubicación de almacenamiento que el módulo de descifrado de contenido (CDM) puede usar para datos específicos del contenido.</span><span class="sxs-lookup"><span data-stu-id="aea38-104">Specifies a file path representing a storage location the Content Decryption Module (CDM) can use for content-specific data.</span></span>


## <a name="data-type"></a><span data-ttu-id="aea38-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="aea38-105">Data type</span></span>

<span data-ttu-id="aea38-106">**LPWStr** (VT_LPWSTR)</span><span class="sxs-lookup"><span data-stu-id="aea38-106">**LPWSTR** (VT_LPWSTR)</span></span>

## <a name="property-guid"></a><span data-ttu-id="aea38-107">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="aea38-107">Property GUID</span></span>

<span data-ttu-id="aea38-108">**MF \_ CONTENTDECRYPTIONMODULE \_ INPRIVATESTOREPATH**</span><span class="sxs-lookup"><span data-stu-id="aea38-108">**MF\_CONTENTDECRYPTIONMODULE\_INPRIVATESTOREPATH**</span></span>

## <a name="property-value"></a><span data-ttu-id="aea38-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="aea38-109">Property value</span></span>

<span data-ttu-id="aea38-110">Una ruta de acceso de archivo que representa una ubicación de almacenamiento que el módulo de descifrado de contenido (CDM) puede usar para datos específicos del contenido.</span><span class="sxs-lookup"><span data-stu-id="aea38-110">A file path representing a storage location the Content Decryption Module (CDM) can use for content-specific data.</span></span>

## <a name="remarks"></a><span data-ttu-id="aea38-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aea38-111">Remarks</span></span>

<span data-ttu-id="aea38-112">La aplicación debe eliminar la ubicación del almacén una vez liberado el objeto CDM.</span><span class="sxs-lookup"><span data-stu-id="aea38-112">The app should delete the store location after the CDM object has been released.</span></span>

<span data-ttu-id="aea38-113">Si no se establece esta propiedad, el sistema usará la ruta de acceso especificada con la propiedad [MF_CONTENTDECRYPTIONMODULE_STOREPATH](mf-contentdecryptionmodule-storepath.md) para los datos específicos del contenido.</span><span class="sxs-lookup"><span data-stu-id="aea38-113">If this property isn't set, the system will use the path specified with the [MF_CONTENTDECRYPTIONMODULE_STOREPATH](mf-contentdecryptionmodule-storepath.md) property for content-specific data.</span></span>

<span data-ttu-id="aea38-114">Establezca esta propiedad al crear un CDM llamando a [IMFContentDecryptionModuleAccess:: CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).</span><span class="sxs-lookup"><span data-stu-id="aea38-114">Set this property when you create a CDM by calling [IMFContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).</span></span>

## <a name="requirements"></a><span data-ttu-id="aea38-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aea38-115">Requirements</span></span>



| <span data-ttu-id="aea38-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="aea38-116">Requirement</span></span> | <span data-ttu-id="aea38-117">Value</span><span class="sxs-lookup"><span data-stu-id="aea38-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aea38-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aea38-118">Minimum supported client</span></span><br/> | <span data-ttu-id="aea38-119">Actualización 2020 de abril de Windows 10</span><span class="sxs-lookup"><span data-stu-id="aea38-119">Windows 10 April 2020 Update</span></span><br/>                                     |
| <span data-ttu-id="aea38-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aea38-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="aea38-121"><dt>mfcontentdecryptionmodule. h</dt></span><span class="sxs-lookup"><span data-stu-id="aea38-121"><dt>mfcontentdecryptionmodule.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aea38-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="aea38-122">See also</span></span>

- [<span data-ttu-id="aea38-123">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="aea38-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
- [<span data-ttu-id="aea38-124">IMFContentDecryptionModuleAccess::CreateContentDecryptionModule</span><span class="sxs-lookup"><span data-stu-id="aea38-124">IMFContentDecryptionModuleAccess::CreateContentDecryptionModule</span></span>](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)


 

 




