---
title: WM/MediaClassPrimaryID
description: El atributo WM/MediaClassPrimaryID contiene el GUID de la clase de medio principal.
ms.assetid: 1d01e273-e6ec-49f1-90af-5c2ae171b199
keywords:
- Formato de Windows Media WM/MediaClassPrimaryID
topic_type:
- apiref
api_name:
- WM/MediaClassPrimaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8f84d987d57b1d825fac54e6a7de41b0154952e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "103904191"
---
# <a name="wmmediaclassprimaryid"></a><span data-ttu-id="16989-104">WM/MediaClassPrimaryID</span><span class="sxs-lookup"><span data-stu-id="16989-104">WM/MediaClassPrimaryID</span></span>

<span data-ttu-id="16989-105">El atributo **WM/MediaClassPrimaryID** contiene el GUID de la clase de medio principal.</span><span class="sxs-lookup"><span data-stu-id="16989-105">The **WM/MediaClassPrimaryID** attribute contains the GUID of the primary media class.</span></span>

## <a name="global-constant"></a><span data-ttu-id="16989-106">Constante global</span><span class="sxs-lookup"><span data-stu-id="16989-106">Global Constant</span></span>

<span data-ttu-id="16989-107">g \_ wszWMMediaClassPrimaryID</span><span class="sxs-lookup"><span data-stu-id="16989-107">g\_wszWMMediaClassPrimaryID</span></span>

## <a name="data-type"></a><span data-ttu-id="16989-108">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="16989-108">Data Type</span></span>

<span data-ttu-id="16989-109">**\_GUID de tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="16989-109">**WMT\_TYPE\_GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="16989-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="16989-110">Remarks</span></span>

<span data-ttu-id="16989-111">Este atributo debe establecerse en uno de los valores de la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="16989-111">This attribute should be set to one of the values in the following table.</span></span>



| <span data-ttu-id="16989-112">GUID de clase principal</span><span class="sxs-lookup"><span data-stu-id="16989-112">Primary class GUID</span></span>                     | <span data-ttu-id="16989-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="16989-113">Description</span></span>                                                  |
|----------------------------------------|--------------------------------------------------------------|
| <span data-ttu-id="16989-114">"D1607DBC-E323-4BE2-86A1-48A42A28441E"</span><span class="sxs-lookup"><span data-stu-id="16989-114">"D1607DBC-E323-4BE2-86A1-48A42A28441E"</span></span> | <span data-ttu-id="16989-115">Se usa para archivos de música.</span><span class="sxs-lookup"><span data-stu-id="16989-115">Use for music files.</span></span> <span data-ttu-id="16989-116">No se usa para audio que no sea música.</span><span class="sxs-lookup"><span data-stu-id="16989-116">Do not use for audio that is not music.</span></span> |
| <span data-ttu-id="16989-117">"DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B"</span><span class="sxs-lookup"><span data-stu-id="16989-117">"DB9830BD-3AB3-4FAB-8A37-1A995F7FF74B"</span></span> | <span data-ttu-id="16989-118">Se usa para archivos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="16989-118">Use for video files.</span></span>                                         |
| <span data-ttu-id="16989-119">"01CD0F29-DA4E-4157-897B-6275D50C4F11"</span><span class="sxs-lookup"><span data-stu-id="16989-119">"01CD0F29-DA4E-4157-897B-6275D50C4F11"</span></span> | <span data-ttu-id="16989-120">Se usa para archivos de audio que no son música.</span><span class="sxs-lookup"><span data-stu-id="16989-120">Use for audio files that are not music.</span></span>                      |
| <span data-ttu-id="16989-121">"FCF24A76-9A57-4036-990D-E35DD8B244E1"</span><span class="sxs-lookup"><span data-stu-id="16989-121">"FCF24A76-9A57-4036-990D-E35DD8B244E1"</span></span> | <span data-ttu-id="16989-122">Se usa para los archivos que no son de audio o de vídeo.</span><span class="sxs-lookup"><span data-stu-id="16989-122">Use for files that are neither audio or video.</span></span>               |



 

<span data-ttu-id="16989-123">Cuando se especifica un identificador de clase principal, también se debe establecer un identificador de clase secundaria para aclarar el tipo de contenido del archivo.</span><span class="sxs-lookup"><span data-stu-id="16989-123">When you specify a primary class identifier, you should also set a secondary class identifier to clarify the type of content in the file.</span></span>

## <a name="see-also"></a><span data-ttu-id="16989-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="16989-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16989-125">**Lista de atributos**</span><span class="sxs-lookup"><span data-stu-id="16989-125">**Attribute List**</span></span>](attribute-list.md)
</dt> <dt>

[<span data-ttu-id="16989-126">**WM/MediaClassSecondaryID**</span><span class="sxs-lookup"><span data-stu-id="16989-126">**WM/MediaClassSecondaryID**</span></span>](wm-mediasecondaryid.md)
</dt> </dl>

 

 




