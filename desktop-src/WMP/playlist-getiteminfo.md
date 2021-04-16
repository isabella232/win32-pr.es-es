---
title: Método playlist. getItemInfo
description: El método getItemInfo recupera el valor de un atributo de lista de reproducción.
ms.assetid: 888c0ab7-c225-4246-b1a1-94da7e19fa1a
keywords:
- método getItemInfo de Windows Media Player
- método getItemInfo Windows Media Player, clase playlist
- Clase PlayList Windows Media Player, método getItemInfo
topic_type:
- apiref
api_name:
- Playlist.getItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b1151528d6cf4e36aaed1cb4dc48a70f4083c4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649515"
---
# <a name="playlistgetiteminfo-method"></a><span data-ttu-id="1e76e-106">Método playlist. getItemInfo</span><span class="sxs-lookup"><span data-stu-id="1e76e-106">Playlist.getItemInfo method</span></span>

<span data-ttu-id="1e76e-107">El método **getItemInfo** recupera el valor de un atributo de lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="1e76e-107">The **getItemInfo** method retrieves the value of a playlist attribute.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e76e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1e76e-108">Syntax</span></span>


```JScript
strRetVal = Playlist.getItemInfo(
  name
)
```



## <a name="parameters"></a><span data-ttu-id="1e76e-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1e76e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e76e-110">*nombre* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="1e76e-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1e76e-111">**Cadena** que contiene el nombre del atributo que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="1e76e-111">**String** containing the name of the attribute to be retrieved.</span></span> <span data-ttu-id="1e76e-112">Para obtener información acerca de los atributos admitidos por Media Player de Windows, consulte la [referencia](attribute-reference.md)de los atributos de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="1e76e-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e76e-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1e76e-113">Return value</span></span>

<span data-ttu-id="1e76e-114">Este método devuelve una **cadena**.</span><span class="sxs-lookup"><span data-stu-id="1e76e-114">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e76e-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1e76e-115">Remarks</span></span>

<span data-ttu-id="1e76e-116">Para usar este método, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="1e76e-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="1e76e-117">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="1e76e-117">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="1e76e-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="1e76e-118">Examples</span></span>

<span data-ttu-id="1e76e-119">Vea la propiedad [attributeCount](playlist-attributecount.md) para ver el código de ejemplo que usa esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="1e76e-119">See the [attributeCount](playlist-attributecount.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e76e-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e76e-120">Requirements</span></span>



| <span data-ttu-id="1e76e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e76e-121">Requirement</span></span> | <span data-ttu-id="1e76e-122">Value</span><span class="sxs-lookup"><span data-stu-id="1e76e-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1e76e-123">Versión</span><span class="sxs-lookup"><span data-stu-id="1e76e-123">Version</span></span><br/> | <span data-ttu-id="1e76e-124">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="1e76e-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="1e76e-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1e76e-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="1e76e-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e76e-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e76e-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="1e76e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e76e-128">**Objeto Playlist**</span><span class="sxs-lookup"><span data-stu-id="1e76e-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="1e76e-129">**Lista de reproducción. setItemInfo**</span><span class="sxs-lookup"><span data-stu-id="1e76e-129">**Playlist.setItemInfo**</span></span>](playlist-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="1e76e-130">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="1e76e-130">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="1e76e-131">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="1e76e-131">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





