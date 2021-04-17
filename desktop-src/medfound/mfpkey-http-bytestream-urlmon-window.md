---
description: Establece una ventana para el Microsoft Media Foundation secuencia de bytes HTTP.
ms.assetid: 52761AC1-4974-4087-B5EE-A797F5BAD86D
title: Propiedad MFPKEY_HTTP_ByteStream_Urlmon_Window (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9df398d2c6d7655a68a139545d84cee48f9cf7fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709222"
---
# <a name="mfpkey_http_bytestream_urlmon_window-property"></a><span data-ttu-id="a8fdf-103">MFPKEY \_ http \_ ByteStream \_ propiedad de la ventana de urlmon \_</span><span class="sxs-lookup"><span data-stu-id="a8fdf-103">MFPKEY\_HTTP\_ByteStream\_Urlmon\_Window property</span></span>

<span data-ttu-id="a8fdf-104">Establece una ventana para el Microsoft Media Foundation secuencia de bytes HTTP.</span><span class="sxs-lookup"><span data-stu-id="a8fdf-104">Sets a window for the Microsoft Media Foundation HTTP byte stream.</span></span> <span data-ttu-id="a8fdf-105">La ventana se usa para presentar información en la interfaz de usuario durante una operación de enlace.</span><span class="sxs-lookup"><span data-stu-id="a8fdf-105">The window is used to present information in the user interface during a bind operation.</span></span>



<span data-ttu-id="a8fdf-106">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="a8fdf-106">Data type</span></span>

<span data-ttu-id="a8fdf-107">Tipo PROPVARIANT (VT)</span><span class="sxs-lookup"><span data-stu-id="a8fdf-107">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="a8fdf-108">Miembro de PROPVARIANT</span><span class="sxs-lookup"><span data-stu-id="a8fdf-108">PROPVARIANT member</span></span>

<span data-ttu-id="a8fdf-109">**IUnknown\***</span><span class="sxs-lookup"><span data-stu-id="a8fdf-109">**IUnknown\***</span></span>

<span data-ttu-id="a8fdf-110">VT \_ desconocido</span><span class="sxs-lookup"><span data-stu-id="a8fdf-110">VT\_UNKNOWN</span></span>

<span data-ttu-id="a8fdf-111">**punkVal**</span><span class="sxs-lookup"><span data-stu-id="a8fdf-111">**punkVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="a8fdf-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a8fdf-112">Remarks</span></span>

<span data-ttu-id="a8fdf-113">Utilice esta propiedad para configurar la secuencia de bytes HTTP Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="a8fdf-113">Use this property to configure the Media Foundation HTTP byte stream.</span></span> <span data-ttu-id="a8fdf-114">Para establecer la propiedad, pase un puntero [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) a la resolución de origen.</span><span class="sxs-lookup"><span data-stu-id="a8fdf-114">To set the property, pass an [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) pointer to the source resolver.</span></span> <span data-ttu-id="a8fdf-115">Para obtener más información, consulte [configuración de un origen de medios](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="a8fdf-115">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="a8fdf-116">El valor de esta propiedad es un puntero a la interfaz **IWindowForBindingUI** .</span><span class="sxs-lookup"><span data-stu-id="a8fdf-116">The value of this property is a pointer to the **IWindowForBindingUI** interface.</span></span> <span data-ttu-id="a8fdf-117">Esta propiedad solo se aplica cuando la propiedad [MFPKEY \_ http \_ ByteStream \_ enable \_ urlmon](mfpkey-http-bytestream-enable-urlmon.md) está establecida en **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="a8fdf-117">This property applies only when the [MFPKEY\_HTTP\_ByteStream\_Enable\_Urlmon](mfpkey-http-bytestream-enable-urlmon.md) property is set to **VARIANT\_TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8fdf-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8fdf-118">Requirements</span></span>



| <span data-ttu-id="a8fdf-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8fdf-119">Requirement</span></span> | <span data-ttu-id="a8fdf-120">Value</span><span class="sxs-lookup"><span data-stu-id="a8fdf-120">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a8fdf-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a8fdf-121">Header</span></span><br/> | <dl> <span data-ttu-id="a8fdf-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8fdf-122"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8fdf-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="a8fdf-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8fdf-124">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a8fdf-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
