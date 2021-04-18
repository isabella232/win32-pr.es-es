---
title: DownloadItem. getItemInfo, método
description: Tenga en cuenta que en esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El método getItemInfo recupera el valor de un atributo para el elemento de descarga.
ms.assetid: da885611-b4a0-4264-8b32-13cc6f87d6e9
keywords:
- método getItemInfo de Windows Media Player
- método getItemInfo de Windows Media Player, clase DownloadItem
- Clase DownloadItem Windows Media Player, método getItemInfo
topic_type:
- apiref
api_name:
- DownloadItem.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1367e5c7a8990a9172ee758d2b811b9074ed02fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699494"
---
# <a name="downloaditemgetiteminfo-method"></a><span data-ttu-id="0a3d1-108">DownloadItem. getItemInfo, método</span><span class="sxs-lookup"><span data-stu-id="0a3d1-108">DownloadItem.getItemInfo method</span></span>

> [!Note]  
> <span data-ttu-id="0a3d1-109">En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="0a3d1-109">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="0a3d1-110">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="0a3d1-110">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="0a3d1-111">El método **getItemInfo** recupera el valor de un atributo para el elemento de descarga.</span><span class="sxs-lookup"><span data-stu-id="0a3d1-111">The **getItemInfo** method retrieves the value of an attribute for the download item.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a3d1-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0a3d1-112">Syntax</span></span>


```JScript
strRetVal = DownloadItem.getItemInfo(
  itemname
)
```



## <a name="parameters"></a><span data-ttu-id="0a3d1-113">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0a3d1-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a3d1-114">*itemname* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0a3d1-114">*itemname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a3d1-115">**Cadena** que contiene el nombre del atributo.</span><span class="sxs-lookup"><span data-stu-id="0a3d1-115">**String** containing the attribute name.</span></span> <span data-ttu-id="0a3d1-116">Los valores admitidos son AlbumArtist, album, Duration, WM/Provider, title, UserRating y WM/TrackNumber.</span><span class="sxs-lookup"><span data-stu-id="0a3d1-116">Supported values are AlbumArtist, Album, Duration, WM/Provider, Title, UserRating, and WM/TrackNumber.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a3d1-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0a3d1-117">Return value</span></span>

<span data-ttu-id="0a3d1-118">Este método devuelve una **cadena** que contiene el valor del atributo especificado por *itemname*.</span><span class="sxs-lookup"><span data-stu-id="0a3d1-118">This method returns a **String** containing the value of the attribute specified by *itemname*.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a3d1-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0a3d1-119">Remarks</span></span>

<span data-ttu-id="0a3d1-120">Este método recupera los atributos especificados mediante la cadena de descripción de BITS.</span><span class="sxs-lookup"><span data-stu-id="0a3d1-120">This method retrieves attributes specified using the BITS description string.</span></span> <span data-ttu-id="0a3d1-121">Vea [Convención de trabajo de Windows Media Player bits](windows-media-player-bits-job-convention.md).</span><span class="sxs-lookup"><span data-stu-id="0a3d1-121">See [Windows Media Player BITS Job Convention](windows-media-player-bits-job-convention.md).</span></span>

<span data-ttu-id="0a3d1-122">Este método es compatible con la descarga en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="0a3d1-122">This method is supported for background downloading.</span></span> <span data-ttu-id="0a3d1-123">El código no debe llamar a este método cuando se usa la descarga en tiempo real.</span><span class="sxs-lookup"><span data-stu-id="0a3d1-123">Your code should not call this method when using real-time downloading.</span></span>

<span data-ttu-id="0a3d1-124">Este método solo puede recuperar información de los trabajos de BITS agregados durante la sesión actual de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="0a3d1-124">This method can retrieve information for BITS jobs added during the current Windows Media Player session only.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a3d1-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a3d1-125">Requirements</span></span>



| <span data-ttu-id="0a3d1-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="0a3d1-126">Requirement</span></span> | <span data-ttu-id="0a3d1-127">Value</span><span class="sxs-lookup"><span data-stu-id="0a3d1-127">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0a3d1-128">Versión</span><span class="sxs-lookup"><span data-stu-id="0a3d1-128">Version</span></span><br/> | <span data-ttu-id="0a3d1-129">Windows Media Player 10 o posterior</span><span class="sxs-lookup"><span data-stu-id="0a3d1-129">Windows Media Player 10 or later</span></span><br/>                                        |
| <span data-ttu-id="0a3d1-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0a3d1-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="0a3d1-131"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a3d1-131"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a3d1-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="0a3d1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a3d1-133">**DownloadItem. tipo**</span><span class="sxs-lookup"><span data-stu-id="0a3d1-133">**DownloadItem.type**</span></span>](downloaditem-type.md)
</dt> <dt>

[<span data-ttu-id="0a3d1-134">**Objeto DownloadItem**</span><span class="sxs-lookup"><span data-stu-id="0a3d1-134">**DownloadItem Object**</span></span>](downloaditem-object.md)
</dt> </dl>

 

 





