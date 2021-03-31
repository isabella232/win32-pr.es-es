---
description: Contiene un puntero a la interfaz de devolución de llamada IMFNetResourceFilter para la secuencia de bytes HTTP Microsoft Media Foundation.
ms.assetid: C035B4AD-CF99-4A4F-9384-F80A3620BD27
title: Propiedad MFNETSOURCE_RESOURCE_FILTER (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da94e8bc0bedba3e47dc2784119a5b30d2bffcb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811845"
---
# <a name="mfnetsource_resource_filter-property"></a><span data-ttu-id="86eed-103">Propiedad de filtro de \_ recursos MFNETSOURCE \_</span><span class="sxs-lookup"><span data-stu-id="86eed-103">MFNETSOURCE\_RESOURCE\_FILTER property</span></span>

<span data-ttu-id="86eed-104">Contiene un puntero a la interfaz de devolución de llamada [**IMFNetResourceFilter**](/windows/desktop/api/mfidl/nn-mfidl-imfnetresourcefilter) para la secuencia de bytes http Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="86eed-104">Contains a pointer to the [**IMFNetResourceFilter**](/windows/desktop/api/mfidl/nn-mfidl-imfnetresourcefilter) callback interface for the Microsoft Media Foundation HTTP byte stream.</span></span>



<span data-ttu-id="86eed-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="86eed-105">Data type</span></span>

<span data-ttu-id="86eed-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="86eed-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="86eed-107">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="86eed-107">PROPVARIANT member</span></span>

<span data-ttu-id="86eed-108">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="86eed-108">\**IUnknown\** _</span></span>

<span data-ttu-id="86eed-109">VT \_ desconocido</span><span class="sxs-lookup"><span data-stu-id="86eed-109">VT\_UNKNOWN</span></span>

<span data-ttu-id="86eed-110">_ *punkVal*\*</span><span class="sxs-lookup"><span data-stu-id="86eed-110">_ *punkVal*\*</span></span>



## <a name="remarks"></a><span data-ttu-id="86eed-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="86eed-111">Remarks</span></span>

<span data-ttu-id="86eed-112">Utilice esta propiedad para configurar la secuencia de bytes HTTP Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="86eed-112">Use this property to configure the Media Foundation HTTP byte stream.</span></span> <span data-ttu-id="86eed-113">Para establecer la propiedad, pase un puntero [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) a la resolución de origen.</span><span class="sxs-lookup"><span data-stu-id="86eed-113">To set the property, pass an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to the source resolver.</span></span> <span data-ttu-id="86eed-114">Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="86eed-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="86eed-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="86eed-115">Requirements</span></span>



| <span data-ttu-id="86eed-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="86eed-116">Requirement</span></span> | <span data-ttu-id="86eed-117">Value</span><span class="sxs-lookup"><span data-stu-id="86eed-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="86eed-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86eed-118">Minimum supported client</span></span><br/> | <span data-ttu-id="86eed-119">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="86eed-119">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="86eed-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="86eed-120">Minimum supported server</span></span><br/> | <span data-ttu-id="86eed-121">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="86eed-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="86eed-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="86eed-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="86eed-123"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="86eed-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86eed-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="86eed-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86eed-125">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="86eed-125">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
