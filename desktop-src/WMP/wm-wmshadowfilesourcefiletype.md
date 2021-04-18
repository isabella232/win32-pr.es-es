---
title: WM/WMShadowFileSourceFileType (SDK de Windows Media Player)
description: WM/WMShadowFileSourceFileType es el tipo de archivo del archivo que se encuentra en el archivo de instantáneas.
ms.assetid: 4c4b70b6-0e26-49f3-b7c1-f6e1fe791e48
keywords:
- Media Player Windows WM/WMShadowFileSourceFileType
topic_type:
- apiref
api_name:
- WM/WMShadowFileSourceFileType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01fc2eb3d91cd05493f98c75d3b7ada3132816ed
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660813"
---
# <a name="wmwmshadowfilesourcefiletype-windows-media-player-sdk"></a><span data-ttu-id="2b0a2-104">WM/WMShadowFileSourceFileType (SDK de Windows Media Player)</span><span class="sxs-lookup"><span data-stu-id="2b0a2-104">WM/WMShadowFileSourceFileType (Windows Media Player SDK)</span></span>

<span data-ttu-id="2b0a2-105">**WM/WMShadowFileSourceFileType** es el tipo de archivo del archivo que se encuentra en el archivo de instantáneas.</span><span class="sxs-lookup"><span data-stu-id="2b0a2-105">The **WM/WMShadowFileSourceFileType** is the file type of the file contained in the shadow file.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b0a2-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2b0a2-106">Remarks</span></span>

<span data-ttu-id="2b0a2-107">Un archivo de instantáneas puede ser un contenedor para un archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="2b0a2-107">A shadow file can be a wrapper for a source file.</span></span> <span data-ttu-id="2b0a2-108">Este atributo es una cadena que contiene la extensión de nombre de archivo (sin el delimitador de punto) del archivo de código fuente.</span><span class="sxs-lookup"><span data-stu-id="2b0a2-108">This attribute is a string that contains the file name extension (without the dot delimiter) for the source file.</span></span> <span data-ttu-id="2b0a2-109">Por ejemplo, si el archivo de origen es un archivo AAC, este atributo contiene la cadena "AAC".</span><span class="sxs-lookup"><span data-stu-id="2b0a2-109">For example, if the source file is an AAC file, this attribute contains the string "aac".</span></span>

<span data-ttu-id="2b0a2-110">El archivo de sombra se especifica mediante el atributo [ShadowFilePath](shadowfilepath-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="2b0a2-110">The shadow file is specified by using the [ShadowFilePath](shadowfilepath-attribute.md) attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b0a2-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b0a2-111">Requirements</span></span>



| <span data-ttu-id="2b0a2-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b0a2-112">Requirement</span></span> | <span data-ttu-id="2b0a2-113">Value</span><span class="sxs-lookup"><span data-stu-id="2b0a2-113">Value</span></span> |
|--------------------|------------------------------------|
| <span data-ttu-id="2b0a2-114">Versión</span><span class="sxs-lookup"><span data-stu-id="2b0a2-114">Version</span></span><br/> | <span data-ttu-id="2b0a2-115">Reproductor de Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="2b0a2-115">Windows Media Player 11</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2b0a2-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="2b0a2-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b0a2-117">**Acerca de los complementos de conversión**</span><span class="sxs-lookup"><span data-stu-id="2b0a2-117">**About Conversion Plug-ins**</span></span>](about-conversion-plug-ins.md)
</dt> <dt>

[<span data-ttu-id="2b0a2-118">**Referencia de atributo**</span><span class="sxs-lookup"><span data-stu-id="2b0a2-118">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





