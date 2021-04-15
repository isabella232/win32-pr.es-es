---
description: Especifica una ruta de acceso de archivo que representa una ubicación de almacenamiento que el módulo de descifrado de contenido (CDM) puede utilizar para la inicialización.
title: MF_CONTENTDECRYPTIONMODULE_STOREPATH (mfcontentdecryptionmodule.h)
ms.topic: reference
ms.date: 01/31/2020
ms.openlocfilehash: 8f5ae27fc8ebbdbf0d9e529f1905631b462ff959
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497668"
---
# <a name="mf_contentdecryptionmodule_storepath-property"></a><span data-ttu-id="6c6d2-103">\_ \_ Propiedad STOREPATH de MF CONTENTDECRYPTIONMODULE</span><span class="sxs-lookup"><span data-stu-id="6c6d2-103">MF\_CONTENTDECRYPTIONMODULE\_STOREPATH property</span></span>

<span data-ttu-id="6c6d2-104">Especifica una ruta de acceso de archivo que representa una ubicación de almacenamiento que el módulo de descifrado de contenido (CDM) puede utilizar para la inicialización.</span><span class="sxs-lookup"><span data-stu-id="6c6d2-104">Specifies a file path representing a storage location the Content Decryption Module (CDM) can use for initialization.</span></span>


## <a name="data-type"></a><span data-ttu-id="6c6d2-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="6c6d2-105">Data type</span></span>

<span data-ttu-id="6c6d2-106">**LPWStr** (VT_LPWSTR)</span><span class="sxs-lookup"><span data-stu-id="6c6d2-106">**LPWSTR** (VT_LPWSTR)</span></span>

## <a name="property-guid"></a><span data-ttu-id="6c6d2-107">GUID de propiedad</span><span class="sxs-lookup"><span data-stu-id="6c6d2-107">Property GUID</span></span>

<span data-ttu-id="6c6d2-108">**MF \_ CONTENTDECRYPTIONMODULE \_ STOREPATH**</span><span class="sxs-lookup"><span data-stu-id="6c6d2-108">**MF\_CONTENTDECRYPTIONMODULE\_STOREPATH**</span></span>

## <a name="property-value"></a><span data-ttu-id="6c6d2-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="6c6d2-109">Property value</span></span>

<span data-ttu-id="6c6d2-110">Una ruta de acceso de archivo que representa una ubicación de almacenamiento que el módulo de descifrado de contenido (CDM) puede utilizar para la inicialización.</span><span class="sxs-lookup"><span data-stu-id="6c6d2-110">A file path representing a storage location the Content Decryption Module (CDM) can use for initialization.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c6d2-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6c6d2-111">Remarks</span></span>

<span data-ttu-id="6c6d2-112">La ruta de acceso especificada con esta propiedad también se utilizará para los datos específicos del contenido si no se ha establecido la propiedad [MF_CONTENTDECRYPTIONMODULE_INPRIVATESTOREPATH](mf-contentdecryptionmodule-inprivatestorepath.md) .</span><span class="sxs-lookup"><span data-stu-id="6c6d2-112">The path specified with this property will also be used for content-specific data if the [MF_CONTENTDECRYPTIONMODULE_INPRIVATESTOREPATH](mf-contentdecryptionmodule-inprivatestorepath.md) property isn't set.</span></span>

<span data-ttu-id="6c6d2-113">Para mejorar el rendimiento de COM, la aplicación no debe eliminar la ubicación del almacén una vez liberado el objeto CDM.</span><span class="sxs-lookup"><span data-stu-id="6c6d2-113">To improve COM performance, the app should not delete the store location after the CDM object has been released.</span></span>



<span data-ttu-id="6c6d2-114">Establezca esta propiedad al crear un CDM llamando a [IMFContentDecryptionModuleAccess:: CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).</span><span class="sxs-lookup"><span data-stu-id="6c6d2-114">Set this property when you create a CDM by calling [IMFContentDecryptionModuleAccess::CreateContentDecryptionModule](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule).</span></span>

## <a name="requirements"></a><span data-ttu-id="6c6d2-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c6d2-115">Requirements</span></span>



| <span data-ttu-id="6c6d2-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c6d2-116">Requirement</span></span> | <span data-ttu-id="6c6d2-117">Value</span><span class="sxs-lookup"><span data-stu-id="6c6d2-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6c6d2-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c6d2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6c6d2-119">Actualización 2020 de abril de Windows 10</span><span class="sxs-lookup"><span data-stu-id="6c6d2-119">Windows 10 April 2020 Update</span></span><br/>                                     |
| <span data-ttu-id="6c6d2-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6c6d2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c6d2-121"><dt>mfcontentdecryptionmodule. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c6d2-121"><dt>mfcontentdecryptionmodule.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c6d2-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c6d2-122">See also</span></span>

- [<span data-ttu-id="6c6d2-123">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6c6d2-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
- [<span data-ttu-id="6c6d2-124">IMFContentDecryptionModuleAccess::CreateContentDecryptionModule</span><span class="sxs-lookup"><span data-stu-id="6c6d2-124">IMFContentDecryptionModuleAccess::CreateContentDecryptionModule</span></span>](/windows/win32/api/mfcontentdecryptionmodule/nf-mfcontentdecryptionmodule-imfcontentdecryptionmoduleaccess-createcontentdecryptionmodule)


 

 




