---
description: Establece el identificador de seguridad raíz de la secuencia de bytes HTTP Microsoft Media Foundation.
ms.assetid: DD2B9487-53B0-4753-8C47-4D6BFE113109
title: Propiedad MFPKEY_HTTP_ByteStream_Urlmon_Security_Id (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cf23e0c3d4aa5ab25590cfdb207fd50f04ecaec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700250"
---
# <a name="mfpkey_http_bytestream_urlmon_security_id-property"></a><span data-ttu-id="5f8ce-103">MFPKEY \_ http \_ ByteStream \_ urlmon \_ Security \_ ID (propiedad)</span><span class="sxs-lookup"><span data-stu-id="5f8ce-103">MFPKEY\_HTTP\_ByteStream\_Urlmon\_Security\_Id property</span></span>

<span data-ttu-id="5f8ce-104">Establece el identificador de seguridad raíz de la secuencia de bytes HTTP Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="5f8ce-104">Sets the root security identifier for the Microsoft Media Foundation HTTP byte stream.</span></span>



<span data-ttu-id="5f8ce-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="5f8ce-105">Data type</span></span>

<span data-ttu-id="5f8ce-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="5f8ce-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="5f8ce-107">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="5f8ce-107">PROPVARIANT member</span></span>

<span data-ttu-id="5f8ce-108">**CAUB**</span><span class="sxs-lookup"><span data-stu-id="5f8ce-108">**CAUB**</span></span>

<span data-ttu-id="5f8ce-109">VT \_ Vector \| VT \_ UI1</span><span class="sxs-lookup"><span data-stu-id="5f8ce-109">VT\_VECTOR \| VT\_UI1</span></span>

<span data-ttu-id="5f8ce-110">**caub**</span><span class="sxs-lookup"><span data-stu-id="5f8ce-110">**caub**</span></span>



## <a name="remarks"></a><span data-ttu-id="5f8ce-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5f8ce-111">Remarks</span></span>

<span data-ttu-id="5f8ce-112">Utilice esta propiedad para configurar la secuencia de bytes HTTP Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="5f8ce-112">Use this property to configure the Media Foundation HTTP byte stream.</span></span> <span data-ttu-id="5f8ce-113">Para establecer la propiedad, pase un puntero [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) a la resolución de origen.</span><span class="sxs-lookup"><span data-stu-id="5f8ce-113">To set the property, pass an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to the source resolver.</span></span> <span data-ttu-id="5f8ce-114">Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="5f8ce-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="5f8ce-115">Esta propiedad solo se aplica cuando la propiedad [MFPKEY \_ http \_ ByteStream \_ enable \_ urlmon](mfpkey-http-bytestream-enable-urlmon.md) está establecida en **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="5f8ce-115">This property applies only when the [MFPKEY\_HTTP\_ByteStream\_Enable\_Urlmon](mfpkey-http-bytestream-enable-urlmon.md) property is set to **VARIANT\_TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f8ce-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f8ce-116">Requirements</span></span>



| <span data-ttu-id="5f8ce-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f8ce-117">Requirement</span></span> | <span data-ttu-id="5f8ce-118">Value</span><span class="sxs-lookup"><span data-stu-id="5f8ce-118">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5f8ce-119">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5f8ce-119">Header</span></span><br/> | <dl> <span data-ttu-id="5f8ce-120"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f8ce-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f8ce-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="5f8ce-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f8ce-122">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5f8ce-122">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
