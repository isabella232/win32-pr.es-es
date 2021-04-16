---
title: Método insertItem IWMPPlaylist
description: El método insertItem inserta un elemento multimedia en una ubicación especificada de una lista de reproducción.
ms.assetid: 6e472f0a-13df-41d9-8e6f-8430d87fe978
keywords:
- método insertItem Media Player Windows
- método insertItem Windows Media Player, interfaz IWMPPlaylist
- Interfaz IWMPPlaylist Windows Media Player, método insertItem
topic_type:
- apiref
api_name:
- IWMPPlaylist.insertItem
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1ef167a5f3931f34d4cd6fb91b3d044affb9484
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709048"
---
# <a name="iwmpplaylistinsertitem-method"></a><span data-ttu-id="b8174-106">IWMPPlaylist:: insertItem (método)</span><span class="sxs-lookup"><span data-stu-id="b8174-106">IWMPPlaylist::insertItem method</span></span>

<span data-ttu-id="b8174-107">El método **insertItem** inserta un elemento multimedia en una ubicación especificada de una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="b8174-107">The **insertItem** method inserts a media item at a specified location in a playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8174-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b8174-108">Syntax</span></span>


```CSharp
public void insertItem(
  System.Int32 lIndex,
  IWMPMedia pIWMPMedia
);
```


```VB

Public Sub insertItem( _
  ByVal lIndex As System.Int32, _
  ByVal pIWMPMedia As IWMPMedia _
)
Implements IWMPPlaylist.insertItem
```





## <a name="parameters"></a><span data-ttu-id="b8174-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b8174-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8174-110">*lIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b8174-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8174-111">**System. Int32** que es el índice de base cero en el que se insertará el elemento multimedia en la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="b8174-111">A **System.Int32** that is the zero-based index at which the media item will be inserted in the playlist.</span></span>

</dd> <dt>

<span data-ttu-id="b8174-112">*pIWMPMedia* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b8174-112">*pIWMPMedia* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8174-113">Una interfaz **WMPLib. IWMPMedia** que representa el elemento multimedia que se va a insertar.</span><span class="sxs-lookup"><span data-stu-id="b8174-113">A **WMPLib.IWMPMedia** interface that represents the media item to be inserted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8174-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b8174-114">Return value</span></span>

<span data-ttu-id="b8174-115">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b8174-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8174-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b8174-116">Remarks</span></span>

<span data-ttu-id="b8174-117">Todos los elementos multimedia después del elemento insertado tendrán sus índices aumentado en uno.</span><span class="sxs-lookup"><span data-stu-id="b8174-117">All media items after the inserted item will have their indexes increased by one.</span></span>

<span data-ttu-id="b8174-118">Antes de llamar a este método, debe tener acceso total a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="b8174-118">Before calling this method, you must have full access to the library.</span></span> <span data-ttu-id="b8174-119">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="b8174-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b8174-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8174-120">Requirements</span></span>



| <span data-ttu-id="b8174-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8174-121">Requirement</span></span> | <span data-ttu-id="b8174-122">Value</span><span class="sxs-lookup"><span data-stu-id="b8174-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8174-123">Versión</span><span class="sxs-lookup"><span data-stu-id="b8174-123">Version</span></span><br/>   | <span data-ttu-id="b8174-124">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="b8174-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="b8174-125">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b8174-125">Namespace</span></span><br/> | <span data-ttu-id="b8174-126">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="b8174-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="b8174-127">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="b8174-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b8174-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b8174-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8174-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="b8174-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8174-130">**Interfaz IWMPMedia (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="b8174-130">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b8174-131">**Interfaz IWMPPlaylist (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="b8174-131">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b8174-132">**IWMPPlaylist. removeItem (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="b8174-132">**IWMPPlaylist.removeItem (VB and C#)**</span></span>](wmplibiwmpplaylist-iwmpplaylist-removeitem--vb-and-c.md)
</dt> </dl>

 

 





