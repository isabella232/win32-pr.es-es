---
title: IWMPPlaylist moveItem (método)
description: El método moveItem cambia la ubicación de un elemento multimedia en la lista de reproducción.
ms.assetid: e82c820f-4640-4289-88c1-79a92e520f00
keywords:
- método moveItem Windows Media Player
- método moveItem Windows Media Player, interfaz IWMPPlaylist
- Interfaz IWMPPlaylist Windows Media Player, método moveItem
topic_type:
- apiref
api_name:
- IWMPPlaylist.moveItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c2d5be745fc3dcf799eb7203e607e493b284b4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709047"
---
# <a name="iwmpplaylistmoveitem-method"></a><span data-ttu-id="639e7-106">IWMPPlaylist:: moveItem (método)</span><span class="sxs-lookup"><span data-stu-id="639e7-106">IWMPPlaylist::moveItem method</span></span>

<span data-ttu-id="639e7-107">El método **moveItem** cambia la ubicación de un elemento multimedia en la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="639e7-107">The **moveItem** method changes the location of a media item in the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="639e7-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="639e7-108">Syntax</span></span>


```CSharp
public void moveItem(
  System.Int32 lIndexOld,
  System.Int32 lIndexNew
);
```


```VB

Public Sub moveItem( _
  ByVal lIndexOld As System.Int32, _
  ByVal lIndexNew As System.Int32 _
)
Implements IWMPPlaylist.moveItem
```





## <a name="parameters"></a><span data-ttu-id="639e7-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="639e7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="639e7-110">*lIndexOld* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="639e7-110">*lIndexOld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="639e7-111">**System. Int32** que es el índice original.</span><span class="sxs-lookup"><span data-stu-id="639e7-111">A **System.Int32** that is the original index.</span></span>

</dd> <dt>

<span data-ttu-id="639e7-112">*lIndexNew* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="639e7-112">*lIndexNew* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="639e7-113">**System. Int32** que es el nuevo índice.</span><span class="sxs-lookup"><span data-stu-id="639e7-113">A **System.Int32** that is the new index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="639e7-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="639e7-114">Return value</span></span>

<span data-ttu-id="639e7-115">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="639e7-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="639e7-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="639e7-116">Remarks</span></span>

<span data-ttu-id="639e7-117">Todos los elementos después del elemento insertado tendrán los números de índice incrementados en uno.</span><span class="sxs-lookup"><span data-stu-id="639e7-117">All items after the inserted item will have their index numbers increased by one.</span></span>

<span data-ttu-id="639e7-118">Antes de llamar a este método, debe tener acceso total a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="639e7-118">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="639e7-119">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="639e7-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="639e7-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="639e7-120">Requirements</span></span>



| <span data-ttu-id="639e7-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="639e7-121">Requirement</span></span> | <span data-ttu-id="639e7-122">Value</span><span class="sxs-lookup"><span data-stu-id="639e7-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="639e7-123">Versión</span><span class="sxs-lookup"><span data-stu-id="639e7-123">Version</span></span><br/>   | <span data-ttu-id="639e7-124">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="639e7-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="639e7-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="639e7-125">Namespace</span></span><br/> | <span data-ttu-id="639e7-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="639e7-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="639e7-127">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="639e7-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="639e7-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="639e7-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="639e7-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="639e7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="639e7-130">**Interfaz IWMPPlaylist (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="639e7-130">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="639e7-131">**IWMPSettings2. mediaAccessRights (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="639e7-131">**IWMPSettings2.mediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-mediaaccessrights--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="639e7-132">**IWMPSettings2. requestMediaAccessRights (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="639e7-132">**IWMPSettings2.requestMediaAccessRights (VB and C#)**</span></span>](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





