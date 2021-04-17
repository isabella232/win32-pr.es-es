---
title: Comentarios (msfeeds. h)
description: Agregue comentarios a los metaarchivos siguiendo la sintaxis de lenguaje de marcado extensible (XML). Los comentarios comienzan con \ 0034; --\ 0034; y terminan con \ 0034;--\ 0034;.
ms.assetid: 3d8dbf13-bd48-4405-804f-57e0f5eff642
keywords:
- Comentarios Media Player de Windows
topic_type:
- apiref
api_name:
- Comments
api_location:
- msfeeds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 701f456cae9f1432ed42235a3a6e13af555b2b8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700415"
---
# <a name="comments-msfeedsh"></a><span data-ttu-id="9fd64-105">Comentarios (msfeeds. h)</span><span class="sxs-lookup"><span data-stu-id="9fd64-105">Comments (Msfeeds.h)</span></span>

<span data-ttu-id="9fd64-106">Agregue comentarios a los metaarchivos siguiendo la sintaxis de lenguaje de marcado extensible (XML).</span><span class="sxs-lookup"><span data-stu-id="9fd64-106">Add comments to metafiles by following Extensible Markup Language (XML) syntax.</span></span> <span data-ttu-id="9fd64-107">Los comentarios comienzan con " &lt; !--" y terminan con "-- &gt; ".</span><span class="sxs-lookup"><span data-stu-id="9fd64-107">Comments begin with "&lt;!--" and end with "--&gt;".</span></span>

``` syntax

<!--Enter your comment text here.-->
```

## <a name="remarks"></a><span data-ttu-id="9fd64-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9fd64-108">Remarks</span></span>

<span data-ttu-id="9fd64-109">Los comentarios pueden aparecer en cualquier lugar excepto en el contenido del elemento (entre las etiquetas de apertura y cierre de elemento,  < >).</span><span class="sxs-lookup"><span data-stu-id="9fd64-109">Comments can appear anywhere except within element content (between element open and close tags, < >).</span></span> <span data-ttu-id="9fd64-110">No forman parte de los datos de caracteres del documento y se omiten cuando se analiza el metarchivo.</span><span class="sxs-lookup"><span data-stu-id="9fd64-110">They are not part of the document's character data and are ignored when the metafile is parsed.</span></span>

## <a name="examples"></a><span data-ttu-id="9fd64-111">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9fd64-111">Examples</span></span>


```XML
<ASX version = "3.0">
<!-- This information is only visible when editing a metafile file. -->
<!--<BANNER HREF="c:\wmsdk\wmssdk\samples\dhtml\asfbutton3.gif">
    </BANNER>-->
    <ENTRY>
        <REF HREF = "mms://proseware.com/pubpt/filename.asf" />
    </ENTRY>

    <ENTRY>
        <TITLE>WMA Port na Pucai</TITLE>
        <!--<DURATION VALUE="00:00:15"/>-->
        <REF href="c:\asfroot\Port na Pucai.wma"/>
    </ENTRY></ASX>

```



## <a name="requirements"></a><span data-ttu-id="9fd64-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9fd64-112">Requirements</span></span>



| <span data-ttu-id="9fd64-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="9fd64-113">Requirement</span></span> | <span data-ttu-id="9fd64-114">Value</span><span class="sxs-lookup"><span data-stu-id="9fd64-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9fd64-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9fd64-115">Header</span></span><br/> | <dl> <span data-ttu-id="9fd64-116"><dt>Msfeeds. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fd64-116"><dt>Msfeeds.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fd64-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="9fd64-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fd64-118">**Referencia de elementos de metarchivo de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="9fd64-118">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 





