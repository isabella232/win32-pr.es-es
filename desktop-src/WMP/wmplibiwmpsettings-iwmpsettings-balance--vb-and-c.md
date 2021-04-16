---
title: Propiedad de equilibrio de IWMPSettings
description: La propiedad saldo obtiene o establece el equilibrio estéreo actual.
ms.assetid: 6b9b6305-3bab-418d-a172-d47ca4dbaba5
keywords:
- equilibrar las ventanas de propiedades Media Player
- propiedad saldo de Windows Media Player, interfaz IWMPSettings
- Interfaz IWMPSettings Windows Media Player, propiedad balance
topic_type:
- apiref
api_name:
- IWMPSettings.balance
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2085f4074d0cd09f475fc031213e3a583747a86b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718879"
---
# <a name="iwmpsettingsbalance-property"></a><span data-ttu-id="27742-106">IWMPSettings:: balance (propiedad)</span><span class="sxs-lookup"><span data-stu-id="27742-106">IWMPSettings::balance property</span></span>

<span data-ttu-id="27742-107">La propiedad **saldo** obtiene o establece el equilibrio estéreo actual.</span><span class="sxs-lookup"><span data-stu-id="27742-107">The **balance** property gets or sets the current stereo balance.</span></span>

## <a name="syntax"></a><span data-ttu-id="27742-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="27742-108">Syntax</span></span>


```CSharp
public System.Int32 balance {get; set;}
```


```VB

Public Property balance As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="27742-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="27742-109">Property value</span></span>

<span data-ttu-id="27742-110">**System. Int32** que es el valor de equilibrio.</span><span class="sxs-lookup"><span data-stu-id="27742-110">A **System.Int32** that is the balance value.</span></span> <span data-ttu-id="27742-111">Este valor puede oscilar entre 100 y 100.</span><span class="sxs-lookup"><span data-stu-id="27742-111">This value can range from  100 to 100.</span></span> <span data-ttu-id="27742-112">El valor predeterminado es cero.</span><span class="sxs-lookup"><span data-stu-id="27742-112">The default value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="27742-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="27742-113">Remarks</span></span>

<span data-ttu-id="27742-114">El valor cero indica que el audio se reproduce en el mismo volumen en los canales izquierdo y derecho.</span><span class="sxs-lookup"><span data-stu-id="27742-114">The value zero indicates that the audio plays at equal volume on both left and right channels.</span></span> <span data-ttu-id="27742-115">Un valor de 100 indica que el audio se reproduce solo en el canal izquierdo.</span><span class="sxs-lookup"><span data-stu-id="27742-115">A value of  100 indicates that audio plays only on the left channel.</span></span> <span data-ttu-id="27742-116">Un valor de 100 indica que el audio se reproduce solo en el canal derecho.</span><span class="sxs-lookup"><span data-stu-id="27742-116">A value of 100 indicates that audio plays only on the right channel.</span></span>

## <a name="requirements"></a><span data-ttu-id="27742-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27742-117">Requirements</span></span>



| <span data-ttu-id="27742-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="27742-118">Requirement</span></span> | <span data-ttu-id="27742-119">Value</span><span class="sxs-lookup"><span data-stu-id="27742-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27742-120">Versión</span><span class="sxs-lookup"><span data-stu-id="27742-120">Version</span></span><br/>   | <span data-ttu-id="27742-121">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="27742-121">Windows Media Player 9 Series or later.</span></span><br/>                                                                     |
| <span data-ttu-id="27742-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="27742-122">Namespace</span></span><br/> | <span data-ttu-id="27742-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="27742-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="27742-124">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="27742-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="27742-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="27742-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27742-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="27742-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27742-127">**Interfaz IWMPSettings (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="27742-127">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





