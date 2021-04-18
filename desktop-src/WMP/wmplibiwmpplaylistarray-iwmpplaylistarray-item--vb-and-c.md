---
title: IWMPPlaylistArray (método del elemento)
description: El método Item devuelve una interfaz IWMPPlaylist que representa la lista de reproducción en el índice especificado.
ms.assetid: 5cb4b89f-b679-4d92-a5f9-5d0fe686775d
keywords:
- Método de elemento Media Player de Windows
- Método de elemento Windows Media Player, interfaz IWMPPlaylistArray
- Interfaz IWMPPlaylistArray Windows Media Player, método Item
topic_type:
- apiref
api_name:
- IWMPPlaylistArray.Item
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 660e919ef51bbb9584971f25bdf92296d331de23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718871"
---
# <a name="iwmpplaylistarrayitem-method"></a><span data-ttu-id="1cc8f-106">IWMPPlaylistArray:: Item (método)</span><span class="sxs-lookup"><span data-stu-id="1cc8f-106">IWMPPlaylistArray::Item method</span></span>

<span data-ttu-id="1cc8f-107">El método **Item** devuelve una interfaz **IWMPPlaylist** que representa la lista de reproducción en el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="1cc8f-107">The **Item** method returns an **IWMPPlaylist** interface representing the playlist at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cc8f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1cc8f-108">Syntax</span></span>


```CSharp
public IWMPPlaylist Item(
  System.Int32 lIndex
);
```


```VB

Public Function Item( _
  ByVal lIndex As System.Int32 _
) As IWMPPlaylist
Implements IWMPPlaylistArray.Item
```





## <a name="parameters"></a><span data-ttu-id="1cc8f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1cc8f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cc8f-110">*lIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1cc8f-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1cc8f-111">**System. Int32** que contiene el índice que identifica la lista de reproducción que el método debe recuperar.</span><span class="sxs-lookup"><span data-stu-id="1cc8f-111">A **System.Int32** containing the index that identifies the playlist that the method should retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cc8f-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1cc8f-112">Return value</span></span>

<span data-ttu-id="1cc8f-113">Una interfaz **WMPLib. IWMPPlaylist** para la lista de reproducción recuperada.</span><span class="sxs-lookup"><span data-stu-id="1cc8f-113">A **WMPLib.IWMPPlaylist** interface for the retrieved playlist.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cc8f-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1cc8f-114">Remarks</span></span>

<span data-ttu-id="1cc8f-115">Antes de llamar a este método, debe tener acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="1cc8f-115">Before calling this method, you must have read access to the library.</span></span> <span data-ttu-id="1cc8f-116">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="1cc8f-116">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1cc8f-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1cc8f-117">Requirements</span></span>



| <span data-ttu-id="1cc8f-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cc8f-118">Requirement</span></span> | <span data-ttu-id="1cc8f-119">Value</span><span class="sxs-lookup"><span data-stu-id="1cc8f-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cc8f-120">Versión</span><span class="sxs-lookup"><span data-stu-id="1cc8f-120">Version</span></span><br/>   | <span data-ttu-id="1cc8f-121">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="1cc8f-121">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="1cc8f-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1cc8f-122">Namespace</span></span><br/> | <span data-ttu-id="1cc8f-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="1cc8f-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="1cc8f-124">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="1cc8f-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="1cc8f-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="1cc8f-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cc8f-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="1cc8f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cc8f-127">**Interfaz IWMPPlaylist (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="1cc8f-127">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="1cc8f-128">**Interfaz IWMPPlaylistArray (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="1cc8f-128">**IWMPPlaylistArray Interface (VB and C#)**</span></span>](iwmpplaylistarray--vb-and-c.md)
</dt> </dl>

 

 





