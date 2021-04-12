---
title: Parámetro MSWMExt (obsoleto)
description: Parámetro MSWMExt (obsoleto)
ms.assetid: cc52da1a-26d1-4321-b421-b0d6f44635cc
keywords:
- Metaarchivos de Windows Media, parámetro MSWMExt
- metaarchivos, parámetro MSWMExt
- Parámetro MSWMExt
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 745ecfb2cf716e973aec3d574247e3e45d8f49ff
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104420355"
---
# <a name="mswmext-parameter-deprecated"></a><span data-ttu-id="10295-106">Parámetro MSWMExt (obsoleto)</span><span class="sxs-lookup"><span data-stu-id="10295-106">MSWMExt Parameter (deprecated)</span></span>

<span data-ttu-id="10295-107">El parámetro *MSWMExt* indica a un programa cliente el formato de un archivo al que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="10295-107">The *MSWMExt* parameter indicates to a client program the format of a referenced file.</span></span>

<span data-ttu-id="10295-108">**Sintaxis**</span><span class="sxs-lookup"><span data-stu-id="10295-108">**Syntax**</span></span>


```XML

URL?MSWMExt=.
ext
```



<span data-ttu-id="10295-109">**Código de ejemplo**</span><span class="sxs-lookup"><span data-stu-id="10295-109">**Example Code**</span></span>


```XML
[reference]
Ref01 = https://example.com/GenerateASFFile.aspx?MSWMExt=.asf

```



## <a name="remarks"></a><span data-ttu-id="10295-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="10295-110">Remarks</span></span>

<span data-ttu-id="10295-111">A veces, los programas cliente usan una extensión de nombre de archivo o un tipo MIME para determinar si se debe representar un archivo multimedia como una secuencia, representar el archivo después de una descarga completa o rechazar el procesamiento del archivo.</span><span class="sxs-lookup"><span data-stu-id="10295-111">Client programs sometimes use a file name extension or a MIME type to determine whether to render a media file as a stream, render the file after a full download, or refuse to render the file at all.</span></span> <span data-ttu-id="10295-112">Si un programa cliente no puede determinar cómo tratar un archivo multimedia en función de la extensión de nombre de archivo o el tipo MIME, puede determinar cómo tratar el archivo mediante la inspección del parámetro *MSWMExt* .</span><span class="sxs-lookup"><span data-stu-id="10295-112">If a client program cannot determine how to treat a media file based on the file name extension or the MIME type, it can determine how to treat the file by inspecting the *MSWMExt* parameter.</span></span> <span data-ttu-id="10295-113">Por ejemplo, el cliente podría tratar el archivo como si tuviera una extensión igual al valor del parámetro *MSWMExt* .</span><span class="sxs-lookup"><span data-stu-id="10295-113">For example, the client could treat the file as if it had an extension equal to the value of the *MSWMExt* parameter.</span></span> <span data-ttu-id="10295-114">Para obtener más información sobre los tipos MIME y las extensiones de nombre de archivo, vea [extensiones de nombre de archivo](file-name-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="10295-114">For more information about MIME types and file name extensions, see [File Name Extensions](file-name-extensions.md).</span></span> <span data-ttu-id="10295-115">Para obtener más información acerca del parámetro *MSWMExt* , consulte el artículo [236895](https://support.microsoft.com/kb/236895) en Microsoft Knowledge base.</span><span class="sxs-lookup"><span data-stu-id="10295-115">For more information about the *MSWMExt* parameter, see article [236895](https://support.microsoft.com/kb/236895) in the Microsoft Knowledge Base.</span></span>

## <a name="related-topics"></a><span data-ttu-id="10295-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="10295-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10295-117">**Versiones anteriores de los metaarchivos de Windows Media (en desuso)**</span><span class="sxs-lookup"><span data-stu-id="10295-117">**Previous Versions of Windows Media Metafiles (deprecated)**</span></span>](previous-versions-of-windows-media-metafiles--deprecated.md)
</dt> </dl>

 

 




