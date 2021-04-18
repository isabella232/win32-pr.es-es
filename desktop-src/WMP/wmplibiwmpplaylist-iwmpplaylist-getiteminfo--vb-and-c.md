---
title: IWMPPlaylist getItemInfo, método
description: El método getItemInfo devuelve el valor de un atributo de lista de reproducción especificado por nombre.
ms.assetid: 62e882d6-66bb-450c-9700-b99d30dd42fa
keywords:
- método getItemInfo de Windows Media Player
- método getItemInfo Windows Media Player, interfaz IWMPPlaylist
- Interfaz IWMPPlaylist Windows Media Player, método getItemInfo
topic_type:
- apiref
api_name:
- IWMPPlaylist.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ced433b13f5af2d1df8c12dba023b7fbb55c5f7d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709049"
---
# <a name="iwmpplaylistgetiteminfo-method"></a><span data-ttu-id="3f789-106">IWMPPlaylist:: getItemInfo (método)</span><span class="sxs-lookup"><span data-stu-id="3f789-106">IWMPPlaylist::getItemInfo method</span></span>

<span data-ttu-id="3f789-107">El método **getItemInfo** devuelve el valor de un atributo de lista de reproducción especificado por nombre.</span><span class="sxs-lookup"><span data-stu-id="3f789-107">The **getItemInfo** method returns the value of a playlist attribute specified by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f789-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3f789-108">Syntax</span></span>


```CSharp
public System.String getItemInfo(
  System.String bstrName
);
```


```VB

Public Function getItemInfo( _
  ByVal bstrName As System.String _
) As System.String
Implements IWMPPlaylist.getItemInfo
```





## <a name="parameters"></a><span data-ttu-id="3f789-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3f789-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f789-110">*bstrName* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="3f789-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f789-111">**System. String** que es el nombre del atributo de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="3f789-111">A **System.String** that is the name of the playlist attribute.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f789-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3f789-112">Return value</span></span>

<span data-ttu-id="3f789-113">**System. String** que es el valor del atributo de lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="3f789-113">A **System.String** that is the value of the playlist attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f789-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3f789-114">Remarks</span></span>

<span data-ttu-id="3f789-115">Antes de utilizar este método, debe tener acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="3f789-115">Before using this method, you must have read access to the library.</span></span> <span data-ttu-id="3f789-116">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="3f789-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="3f789-117">Vea la propiedad [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) para ver el código de ejemplo que usa esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="3f789-117">See the [attributeCount](wmplibiwmpplaylist-iwmpplaylist-attributecount--vb-and-c.md) property for example code that uses this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f789-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f789-118">Requirements</span></span>



| <span data-ttu-id="3f789-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f789-119">Requirement</span></span> | <span data-ttu-id="3f789-120">Value</span><span class="sxs-lookup"><span data-stu-id="3f789-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f789-121">Versión</span><span class="sxs-lookup"><span data-stu-id="3f789-121">Version</span></span><br/>   | <span data-ttu-id="3f789-122">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="3f789-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="3f789-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3f789-123">Namespace</span></span><br/> | <span data-ttu-id="3f789-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="3f789-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="3f789-125">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="3f789-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3f789-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="3f789-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f789-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f789-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f789-128">**Interfaz IWMPPlaylist (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="3f789-128">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3f789-129">**IWMPPlaylist. setItemInfo (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="3f789-129">**IWMPPlaylist.setItemInfo (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-setiteminfo--vb-and-c.md)
</dt> </dl>

 

 





