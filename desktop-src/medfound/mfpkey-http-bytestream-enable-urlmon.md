---
description: Habilita el Microsoft Media Foundation secuencia de bytes HTTP para usar monikers de dirección URL (también denominado urlmon).
ms.assetid: 8B7D2FF7-D8A8-49E9-8CED-D37853B97A8F
title: Propiedad MFPKEY_HTTP_ByteStream_Enable_Urlmon (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1858f34a5f719caba1a48f049b95f2031b400240
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679109"
---
# <a name="mfpkey_http_bytestream_enable_urlmon-property"></a><span data-ttu-id="c17dd-103">MFPKEY \_ http \_ ByteStream \_ habilitar \_ propiedad de urlmon</span><span class="sxs-lookup"><span data-stu-id="c17dd-103">MFPKEY\_HTTP\_ByteStream\_Enable\_Urlmon property</span></span>

<span data-ttu-id="c17dd-104">Habilita el Microsoft Media Foundation secuencia de bytes HTTP para usar monikers de dirección URL (también denominado *urlmon*).</span><span class="sxs-lookup"><span data-stu-id="c17dd-104">Enables the Microsoft Media Foundation HTTP byte stream to use URL monikers (also called *Urlmon*).</span></span>



<span data-ttu-id="c17dd-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="c17dd-105">Data type</span></span>

<span data-ttu-id="c17dd-106">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="c17dd-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="c17dd-107">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="c17dd-107">PROPVARIANT member</span></span>

<span data-ttu-id="c17dd-108">**VARIANTE \_ bool**</span><span class="sxs-lookup"><span data-stu-id="c17dd-108">**VARIANT\_BOOL**</span></span>

<span data-ttu-id="c17dd-109">VT \_ bool</span><span class="sxs-lookup"><span data-stu-id="c17dd-109">VT\_BOOL</span></span>

<span data-ttu-id="c17dd-110">**boolVal**</span><span class="sxs-lookup"><span data-stu-id="c17dd-110">**boolVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="c17dd-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c17dd-111">Remarks</span></span>

<span data-ttu-id="c17dd-112">Utilice esta propiedad para configurar la secuencia de bytes HTTP Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="c17dd-112">Use this property to configure the Media Foundation HTTP byte stream.</span></span> <span data-ttu-id="c17dd-113">Para establecer la propiedad, pase un puntero [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) a la resolución de origen.</span><span class="sxs-lookup"><span data-stu-id="c17dd-113">To set the property, pass an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to the source resolver.</span></span> <span data-ttu-id="c17dd-114">Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="c17dd-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="c17dd-115">Si el valor es **Variant \_ true**, el flujo de bytes http usa urlmon para el transporte http.</span><span class="sxs-lookup"><span data-stu-id="c17dd-115">If the value is **VARIANT\_TRUE**, the HTTP byte stream uses Urlmon for HTTP transport.</span></span> <span data-ttu-id="c17dd-116">De lo contrario, si el valor es **Variant \_ false**, el flujo de bytes usa winhttp.</span><span class="sxs-lookup"><span data-stu-id="c17dd-116">Otherwise, if the value is **VARIANT\_FALSE**, the byte stream uses WinHTTP.</span></span>

<span data-ttu-id="c17dd-117">El valor predeterminado es **Variant \_ true** para las aplicaciones de la tienda Windows y **Variant \_ false** para la aplicación de escritorio de Windows.</span><span class="sxs-lookup"><span data-stu-id="c17dd-117">The default value is **VARIANT\_TRUE** for Windows Store apps and **VARIANT\_FALSE** for Windows desktop application.</span></span>

## <a name="requirements"></a><span data-ttu-id="c17dd-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c17dd-118">Requirements</span></span>



| <span data-ttu-id="c17dd-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c17dd-119">Requirement</span></span> | <span data-ttu-id="c17dd-120">Value</span><span class="sxs-lookup"><span data-stu-id="c17dd-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c17dd-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c17dd-121">Header</span></span><br/> | <dl> <span data-ttu-id="c17dd-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="c17dd-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c17dd-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="c17dd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c17dd-124">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c17dd-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
