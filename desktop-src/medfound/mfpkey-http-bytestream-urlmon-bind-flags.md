---
description: Establece las marcas de enlace del moniker para la secuencia de bytes HTTP Microsoft Media Foundation.
ms.assetid: 9426D235-65E1-40BA-94E9-CF0C49263E6F
title: Propiedad MFPKEY_HTTP_ByteStream_Urlmon_Bind_Flags (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32863929b92f16a809468055db81361f8116196e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699317"
---
# <a name="mfpkey_http_bytestream_urlmon_bind_flags-property"></a><span data-ttu-id="8952f-103">MFPKEY \_ http \_ ByteStream \_ \_ propiedad flags de enlace de urlmon \_</span><span class="sxs-lookup"><span data-stu-id="8952f-103">MFPKEY\_HTTP\_ByteStream\_Urlmon\_Bind\_Flags property</span></span>

<span data-ttu-id="8952f-104">Establece las marcas de enlace del moniker para la secuencia de bytes HTTP Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="8952f-104">Sets the moniker binding flags for the Microsoft Media Foundation HTTP byte stream.</span></span>



<span data-ttu-id="8952f-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="8952f-105">Data type</span></span>

<span data-ttu-id="8952f-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="8952f-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="8952f-107">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="8952f-107">PROPVARIANT member</span></span>

<span data-ttu-id="8952f-108">**ULONG**</span><span class="sxs-lookup"><span data-stu-id="8952f-108">**ULONG**</span></span>

<span data-ttu-id="8952f-109">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="8952f-109">VT\_UI4</span></span>

<span data-ttu-id="8952f-110">**ulVal**</span><span class="sxs-lookup"><span data-stu-id="8952f-110">**ulVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="8952f-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8952f-111">Remarks</span></span>

<span data-ttu-id="8952f-112">Utilice esta propiedad para configurar la secuencia de bytes HTTP Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="8952f-112">Use this property to configure the Media Foundation HTTP byte stream.</span></span> <span data-ttu-id="8952f-113">Para establecer la propiedad, pase un puntero [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) a la resolución de origen.</span><span class="sxs-lookup"><span data-stu-id="8952f-113">To set the property, pass an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to the source resolver.</span></span> <span data-ttu-id="8952f-114">Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="8952f-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="8952f-115">El valor de esta propiedad es **una operación OR bit a bit** de las marcas de la enumeración **BINDF** .</span><span class="sxs-lookup"><span data-stu-id="8952f-115">The value of this property is a bitwise **OR** of flags from the **BINDF** enumeration.</span></span> <span data-ttu-id="8952f-116">Esta propiedad solo se aplica cuando la propiedad [MFPKEY \_ http \_ ByteStream \_ enable \_ urlmon](mfpkey-http-bytestream-enable-urlmon.md) está establecida en **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="8952f-116">This property applies only when the [MFPKEY\_HTTP\_ByteStream\_Enable\_Urlmon](mfpkey-http-bytestream-enable-urlmon.md) property is set to **VARIANT\_TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8952f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8952f-117">Requirements</span></span>



| <span data-ttu-id="8952f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="8952f-118">Requirement</span></span> | <span data-ttu-id="8952f-119">Value</span><span class="sxs-lookup"><span data-stu-id="8952f-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8952f-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8952f-120">Header</span></span><br/> | <dl> <span data-ttu-id="8952f-121"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="8952f-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8952f-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="8952f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8952f-123">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8952f-123">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
