---
title: Lista de reproducción. attributeName
description: La propiedad attributeName recupera el nombre de un atributo en un índice especificado.
ms.assetid: 3ff68e78-5fa1-4ca6-aa59-4752dbaee52a
keywords:
- Lista de Media Player de Windows. attributeName
topic_type:
- apiref
api_name:
- Playlist.attributeName
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4560a7ca2766ee0bbadc582af878bca87e0834e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708869"
---
# <a name="playlistattributename"></a><span data-ttu-id="4cfb5-104">Lista de reproducción. attributeName</span><span class="sxs-lookup"><span data-stu-id="4cfb5-104">Playlist.attributeName</span></span>

<span data-ttu-id="4cfb5-105">La propiedad **attributeName** recupera el nombre de un atributo en un índice especificado.</span><span class="sxs-lookup"><span data-stu-id="4cfb5-105">The **attributeName** property retrieves the name of an attribute at a specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cfb5-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4cfb5-106">Syntax</span></span>

<span data-ttu-id="4cfb5-107">*reproductor*. *currentPlaylist*. **attributeName**( *Índice* )</span><span class="sxs-lookup"><span data-stu-id="4cfb5-107">*player*.*currentPlaylist*.**attributeName**( *index* )</span></span>

## <a name="parameters"></a><span data-ttu-id="4cfb5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4cfb5-108">Parameters</span></span>

<span data-ttu-id="4cfb5-109">*índice*</span><span class="sxs-lookup"><span data-stu-id="4cfb5-109">*index*</span></span>

<span data-ttu-id="4cfb5-110">**Número** (**largo**) que contiene el índice.</span><span class="sxs-lookup"><span data-stu-id="4cfb5-110">**Number** (**long**) containing the index.</span></span>

## <a name="possible-values"></a><span data-ttu-id="4cfb5-111">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="4cfb5-111">Possible Values</span></span>

<span data-ttu-id="4cfb5-112">Esta propiedad es una **cadena** de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="4cfb5-112">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cfb5-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4cfb5-113">Remarks</span></span>

<span data-ttu-id="4cfb5-114">La propiedad **attributeCount** recupera el número de atributos.</span><span class="sxs-lookup"><span data-stu-id="4cfb5-114">The number of attributes is retrieved by the **attributeCount** property.</span></span> <span data-ttu-id="4cfb5-115">Dado un índice, **attributeName** devuelve una **cadena** que se puede usar junto con **setItemInfo** o **getItemInfo** para especificar o recuperar un valor para el atributo.</span><span class="sxs-lookup"><span data-stu-id="4cfb5-115">Given an index, **attributeName** returns a **String** that can be used in conjunction with **setItemInfo** or **getItemInfo** to specify or retrieve a value for the attribute.</span></span>

<span data-ttu-id="4cfb5-116">Para recuperar el valor de esta propiedad, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="4cfb5-116">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="4cfb5-117">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="4cfb5-117">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="4cfb5-118">Para obtener información acerca de los atributos admitidos por Media Player de Windows, consulte la [referencia](attribute-reference.md)de los atributos de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="4cfb5-118">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

<span data-ttu-id="4cfb5-119">Vea la propiedad [attributeCount](playlist-attributecount.md) para ver el código de ejemplo que usa esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="4cfb5-119">See the [attributeCount](playlist-attributecount.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cfb5-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4cfb5-120">Requirements</span></span>



| <span data-ttu-id="4cfb5-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4cfb5-121">Requirement</span></span> | <span data-ttu-id="4cfb5-122">Value</span><span class="sxs-lookup"><span data-stu-id="4cfb5-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4cfb5-123">Versión</span><span class="sxs-lookup"><span data-stu-id="4cfb5-123">Version</span></span><br/> | <span data-ttu-id="4cfb5-124">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="4cfb5-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="4cfb5-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4cfb5-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="4cfb5-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4cfb5-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4cfb5-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="4cfb5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cfb5-128">**Objeto Playlist**</span><span class="sxs-lookup"><span data-stu-id="4cfb5-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="4cfb5-129">**Lista de reproducción. attributeCount**</span><span class="sxs-lookup"><span data-stu-id="4cfb5-129">**Playlist.attributeCount**</span></span>](playlist-attributecount.md)
</dt> <dt>

[<span data-ttu-id="4cfb5-130">**Lista de reproducción. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="4cfb5-130">**Playlist.getItemInfo**</span></span>](playlist-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="4cfb5-131">**Lista de reproducción. setItemInfo**</span><span class="sxs-lookup"><span data-stu-id="4cfb5-131">**Playlist.setItemInfo**</span></span>](playlist-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="4cfb5-132">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="4cfb5-132">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="4cfb5-133">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="4cfb5-133">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





