---
title: Propiedad burnPlaylist de IWMPCdromBurn
description: La propiedad burnPlaylist obtiene la lista de reproducción actual para grabarla en el CD.
ms.assetid: 973032de-7249-4ccd-9909-ccc888f4490f
keywords:
- propiedades de burnPlaylist Media Player de Windows
- propiedad burnPlaylist de Windows Media Player, interfaz IWMPCdromBurn
- Interfaz IWMPCdromBurn Windows Media Player, propiedad burnPlaylist
topic_type:
- apiref
api_name:
- IWMPCdromBurn.burnPlaylist
- IWMPCdromBurn.get_burnPlaylist
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cae095696b9c106926fb7f363430574b2eb87cea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718842"
---
# <a name="iwmpcdromburnburnplaylist-property"></a><span data-ttu-id="107bd-106">IWMPCdromBurn:: burnPlaylist (propiedad)</span><span class="sxs-lookup"><span data-stu-id="107bd-106">IWMPCdromBurn::burnPlaylist property</span></span>

<span data-ttu-id="107bd-107">La propiedad **burnPlaylist** obtiene la lista de reproducción actual para grabarla en el CD.</span><span class="sxs-lookup"><span data-stu-id="107bd-107">The **burnPlaylist** property gets the current playlist to burn to the CD.</span></span>

<span data-ttu-id="107bd-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="107bd-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="107bd-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="107bd-109">Syntax</span></span>


```CSharp
public IWMPPlaylist burnPlaylist {get;}
```


```VB

Public ReadOnly Property burnPlaylist As IWMPPlaylist
```





## <a name="property-value"></a><span data-ttu-id="107bd-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="107bd-110">Property value</span></span>

<span data-ttu-id="107bd-111">La interfaz **WMPLib. IWMPPlaylist** de la lista de reproducción que se va a grabar.</span><span class="sxs-lookup"><span data-stu-id="107bd-111">The **WMPLib.IWMPPlaylist** interface of the playlist to burn.</span></span>

## <a name="requirements"></a><span data-ttu-id="107bd-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="107bd-112">Requirements</span></span>



| <span data-ttu-id="107bd-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="107bd-113">Requirement</span></span> | <span data-ttu-id="107bd-114">Value</span><span class="sxs-lookup"><span data-stu-id="107bd-114">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="107bd-115">Versión</span><span class="sxs-lookup"><span data-stu-id="107bd-115">Version</span></span><br/>   | <span data-ttu-id="107bd-116">Reproductor de Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="107bd-116">Windows Media Player 11</span></span><br/>                                                                                     |
| <span data-ttu-id="107bd-117">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="107bd-117">Namespace</span></span><br/> | <span data-ttu-id="107bd-118">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="107bd-118">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="107bd-119">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="107bd-119">Assembly</span></span><br/>  | <dl> <span data-ttu-id="107bd-120"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="107bd-120"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="107bd-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="107bd-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="107bd-122">**Interfaz IWMPCdromBurn (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="107bd-122">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="107bd-123">**Interfaz IWMPPlaylist (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="107bd-123">**IWMPPlaylist Interface (VB and C#)**</span></span>](iwmpplaylist--vb-and-c.md)
</dt> </dl>

 

 





