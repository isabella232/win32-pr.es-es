---
title: IWMPPlaylistCollection Remove (método)
description: El método Remove quita una lista de reproducción de la biblioteca. | IWMPPlaylistCollection Remove (método)
ms.assetid: 40c8ee1d-13fa-40d9-9532-4dc8383c4eb3
keywords:
- quitar Media Player de Windows de método
- quitar método Windows Media Player, interfaz IWMPPlaylistCollection
- Interfaz IWMPPlaylistCollection Windows Media Player, Remove (método)
topic_type:
- apiref
api_name:
- IWMPPlaylistCollection.remove
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c99fbaa2f60c769599bd6173b8e38f4d99e9f42d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105719028"
---
# <a name="iwmpplaylistcollectionremove-method"></a><span data-ttu-id="17c12-107">IWMPPlaylistCollection:: Remove (método)</span><span class="sxs-lookup"><span data-stu-id="17c12-107">IWMPPlaylistCollection::remove method</span></span>

<span data-ttu-id="17c12-108">El método **Remove** quita una lista de reproducción de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="17c12-108">The **remove** method removes a playlist from the library.</span></span>

## <a name="syntax"></a><span data-ttu-id="17c12-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="17c12-109">Syntax</span></span>


```CSharp
public void remove(
  IWMPPlaylist pItem
);
```


```VB

Public Sub remove( _
  ByVal pItem As IWMPPlaylist _
)
Implements IWMPPlaylistCollection.remove
```





## <a name="parameters"></a><span data-ttu-id="17c12-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="17c12-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17c12-111">*pItem* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="17c12-111">*pItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17c12-112">Una interfaz **WMPLib. IWMPPlaylist** para la lista de reproducción que este método va a quitar.</span><span class="sxs-lookup"><span data-stu-id="17c12-112">A **WMPLib.IWMPPlaylist** interface for the playlist that this method will remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17c12-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="17c12-113">Return value</span></span>

<span data-ttu-id="17c12-114">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="17c12-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="17c12-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="17c12-115">Remarks</span></span>

<span data-ttu-id="17c12-116">Antes de llamar a este método, debe tener acceso total a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="17c12-116">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="17c12-117">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="17c12-117">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="17c12-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17c12-118">Requirements</span></span>



| <span data-ttu-id="17c12-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="17c12-119">Requirement</span></span> | <span data-ttu-id="17c12-120">Value</span><span class="sxs-lookup"><span data-stu-id="17c12-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17c12-121">Versión</span><span class="sxs-lookup"><span data-stu-id="17c12-121">Version</span></span><br/>   | <span data-ttu-id="17c12-122">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="17c12-122">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="17c12-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="17c12-123">Namespace</span></span><br/> | <span data-ttu-id="17c12-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="17c12-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="17c12-125">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="17c12-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="17c12-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="17c12-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17c12-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="17c12-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17c12-128">**Interfaz IWMPPlaylist (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="17c12-128">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="17c12-129">**Interfaz IWMPPlaylistCollection (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="17c12-129">**IWMPPlaylistCollection Interface (VB and C#)**</span></span>](iwmpplaylistcollection--vb-and-c.md)
</dt> </dl>

 

 





