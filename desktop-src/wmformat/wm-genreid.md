---
title: WM/GenreID
description: El atributo WM/GenreID contiene un identificador de género compatible con el contenido de la etiqueta TCON en ID3v2.
ms.assetid: 2f2a87f7-ba2d-465a-a36b-a8f58b5dd2d0
keywords:
- Formato de Windows Media WM/GenreID
topic_type:
- apiref
api_name:
- WM/GenreID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a3b25dffe69471f47eaf20124af48141835540f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104419735"
---
# <a name="wmgenreid"></a><span data-ttu-id="8f8c6-104">WM/GenreID</span><span class="sxs-lookup"><span data-stu-id="8f8c6-104">WM/GenreID</span></span>

<span data-ttu-id="8f8c6-105">El atributo **WM/GenreID** contiene un identificador de género compatible con el contenido de la etiqueta TCON en ID3v2.</span><span class="sxs-lookup"><span data-stu-id="8f8c6-105">The **WM/GenreID** attribute contains a genre identifier compliant with the contents of the TCON tag in ID3v2.</span></span> <span data-ttu-id="8f8c6-106">Este debe contener el ID. de género entre paréntesis y, opcionalmente, un perfeccionamiento que describa el género.</span><span class="sxs-lookup"><span data-stu-id="8f8c6-106">This should contain the genre ID in parentheses, optionally followed by a refinement further describing the genre.</span></span> <span data-ttu-id="8f8c6-107">Para obtener más información, consulte la especificación ID3v2.</span><span class="sxs-lookup"><span data-stu-id="8f8c6-107">For more information, refer to the ID3v2 specification.</span></span>

## <a name="global-constant"></a><span data-ttu-id="8f8c6-108">Constante global</span><span class="sxs-lookup"><span data-stu-id="8f8c6-108">Global Constant</span></span>

<span data-ttu-id="8f8c6-109">g \_ wszWMGenreID</span><span class="sxs-lookup"><span data-stu-id="8f8c6-109">g\_wszWMGenreID</span></span>

## <a name="data-type"></a><span data-ttu-id="8f8c6-110">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="8f8c6-110">Data Type</span></span>

<span data-ttu-id="8f8c6-111">**\_cadena de tipo WMT \_**</span><span class="sxs-lookup"><span data-stu-id="8f8c6-111">**WMT\_TYPE\_STRING**</span></span>

## <a name="remarks"></a><span data-ttu-id="8f8c6-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8f8c6-112">Remarks</span></span>

<span data-ttu-id="8f8c6-113">El atributo preferido para especificar un género es [**WM/Genre**](wm-genre.md).</span><span class="sxs-lookup"><span data-stu-id="8f8c6-113">The preferred attribute for specifying a genre is [**WM/Genre**](wm-genre.md).</span></span> <span data-ttu-id="8f8c6-114">Úselo en preferencia a este atributo.</span><span class="sxs-lookup"><span data-stu-id="8f8c6-114">Use it in preference to this attribute.</span></span>

<span data-ttu-id="8f8c6-115">Si cambia **WM/Genre** o **WM/GenreID** en un archivo mp3, se cambiará el otro atributo para que coincida.</span><span class="sxs-lookup"><span data-stu-id="8f8c6-115">If you change either **WM/Genre** or **WM/GenreID** in an MP3 file, the other attribute will be changed to match.</span></span>

### <a name="example"></a><span data-ttu-id="8f8c6-116">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="8f8c6-116">Example</span></span>



| <span data-ttu-id="8f8c6-117">Tipo de archivo</span><span class="sxs-lookup"><span data-stu-id="8f8c6-117">File type</span></span> | <span data-ttu-id="8f8c6-118">Valor de ejemplo</span><span class="sxs-lookup"><span data-stu-id="8f8c6-118">Example value</span></span>   |
|-----------|-----------------|
| <span data-ttu-id="8f8c6-119">Audio</span><span class="sxs-lookup"><span data-stu-id="8f8c6-119">Audio</span></span>     | <span data-ttu-id="8f8c6-120">"(4) Eurodisco"</span><span class="sxs-lookup"><span data-stu-id="8f8c6-120">"(4) Eurodisco"</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="8f8c6-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="8f8c6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f8c6-122">**Lista de atributos**</span><span class="sxs-lookup"><span data-stu-id="8f8c6-122">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




