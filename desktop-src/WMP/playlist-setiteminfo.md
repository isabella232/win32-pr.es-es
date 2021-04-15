---
title: Método playlist. setItemInfo
description: El método setItemInfo especifica el valor de un atributo de lista de reproducción.
ms.assetid: ffecb43f-343d-4a4f-9356-0e3cfa85ce77
keywords:
- método setItemInfo de Windows Media Player
- método setItemInfo Windows Media Player, clase playlist
- Clase PlayList Windows Media Player, método setItemInfo
topic_type:
- apiref
api_name:
- Playlist.setItemInfo
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ff42e56e549100044db0881bb38ade5f2f1711a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709264"
---
# <a name="playlistsetiteminfo-method"></a><span data-ttu-id="c4289-106">Método playlist. setItemInfo</span><span class="sxs-lookup"><span data-stu-id="c4289-106">Playlist.setItemInfo method</span></span>

<span data-ttu-id="c4289-107">El método **setItemInfo** especifica el valor de un atributo de lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="c4289-107">The **setItemInfo** method specifies the value of a playlist attribute.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4289-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c4289-108">Syntax</span></span>


```JScript
Playlist.setItemInfo(
  name,
  value
)
```



## <a name="parameters"></a><span data-ttu-id="c4289-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c4289-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4289-110">*nombre* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="c4289-110">*name* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4289-111">**Cadena** que contiene el nombre del atributo que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="c4289-111">**String** containing the name of the attribute to be set.</span></span> <span data-ttu-id="c4289-112">Para obtener información acerca de los atributos admitidos por Media Player de Windows, consulte la [referencia](attribute-reference.md)de los atributos de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="c4289-112">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md).</span></span>

</dd> <dt>

<span data-ttu-id="c4289-113">*valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="c4289-113">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4289-114">**Cadena** que contiene el nuevo valor para el atributo.</span><span class="sxs-lookup"><span data-stu-id="c4289-114">**String** containing the new value for the attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4289-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c4289-115">Return value</span></span>

<span data-ttu-id="c4289-116">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="c4289-116">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c4289-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c4289-117">Remarks</span></span>

<span data-ttu-id="c4289-118">Un uso especial del método **setItemInfo** es ordenar los elementos de la lista de reproducción mediante el atributo SortAttribute.</span><span class="sxs-lookup"><span data-stu-id="c4289-118">A special use of the **setItemInfo** method is to sort the items in the playlist by using the SortAttribute attribute.</span></span> <span data-ttu-id="c4289-119">En el siguiente ejemplo de JScript se ordena una lista de reproducción por los valores del atributo UserLastPlayedTime.</span><span class="sxs-lookup"><span data-stu-id="c4289-119">The following JScript example sorts a playlist by the values of the UserLastPlayedTime attribute.</span></span> <span data-ttu-id="c4289-120">La lista de reproducción de variables es una referencia a un objeto de **lista de reproducción** .</span><span class="sxs-lookup"><span data-stu-id="c4289-120">The variable playlist is a reference to a **Playlist** object.</span></span>


```JScript
playlist.setItemInfo("SortAttribute", "UserLastPlayedTime")
```



<span data-ttu-id="c4289-121">Para usar este método, se necesita acceso completo a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="c4289-121">To use this method, full access to the library is required.</span></span> <span data-ttu-id="c4289-122">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="c4289-122">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="c4289-123">**Windows Media Player 10 Mobile:** Este método no se admite.</span><span class="sxs-lookup"><span data-stu-id="c4289-123">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="c4289-124">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c4289-124">Examples</span></span>

<span data-ttu-id="c4289-125">Vea la propiedad [attributeCount](playlist-attributecount.md) para ver el código de ejemplo que usa esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="c4289-125">See the [attributeCount](playlist-attributecount.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4289-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4289-126">Requirements</span></span>



| <span data-ttu-id="c4289-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4289-127">Requirement</span></span> | <span data-ttu-id="c4289-128">Value</span><span class="sxs-lookup"><span data-stu-id="c4289-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c4289-129">Versión</span><span class="sxs-lookup"><span data-stu-id="c4289-129">Version</span></span><br/> | <span data-ttu-id="c4289-130">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="c4289-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="c4289-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c4289-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="c4289-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4289-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4289-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="c4289-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4289-134">**Objeto Playlist**</span><span class="sxs-lookup"><span data-stu-id="c4289-134">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="c4289-135">**Lista de reproducción. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="c4289-135">**Playlist.getItemInfo**</span></span>](playlist-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="c4289-136">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="c4289-136">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="c4289-137">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="c4289-137">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





