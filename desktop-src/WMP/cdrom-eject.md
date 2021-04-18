---
title: CDROM. EJECT (método)
description: El método EJECT expulsa el CD o DVD de la unidad. | CDROM. EJECT (método)
ms.assetid: f43c7f10-7de2-488c-833a-ecd3ac21744b
keywords:
- método EJECT Media Player de Windows
- método EJECT Media Player de Windows, clase CDROM
- Clase CDROM Windows Media Player, método EJECT
topic_type:
- apiref
api_name:
- Cdrom.eject
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78326ca57dcf097344fc073681fae772222ea9ad
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698078"
---
# <a name="cdromeject-method"></a><span data-ttu-id="d3744-107">CDROM. EJECT (método)</span><span class="sxs-lookup"><span data-stu-id="d3744-107">Cdrom.eject method</span></span>

<span data-ttu-id="d3744-108">El método **EJECT** expulsa el CD o DVD de la unidad.</span><span class="sxs-lookup"><span data-stu-id="d3744-108">The **eject** method ejects the CD or DVD from the drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3744-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d3744-109">Syntax</span></span>


```JScript
Cdrom.eject()
```



## <a name="parameters"></a><span data-ttu-id="d3744-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d3744-110">Parameters</span></span>

<span data-ttu-id="d3744-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="d3744-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d3744-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d3744-112">Return value</span></span>

<span data-ttu-id="d3744-113">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="d3744-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3744-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d3744-114">Remarks</span></span>

<span data-ttu-id="d3744-115">Si la puerta de la unidad está abierta, este método cierra la puerta.</span><span class="sxs-lookup"><span data-stu-id="d3744-115">If the drive door is open, this method closes the door.</span></span>

<span data-ttu-id="d3744-116">Para usar este método, se requiere acceso de lectura a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="d3744-116">To use this method, read access to the library is required.</span></span> <span data-ttu-id="d3744-117">Para obtener más información, vea [acceso a la biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="d3744-117">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="d3744-118">**Windows Media Player 10 Mobile:** Este método no se admite.</span><span class="sxs-lookup"><span data-stu-id="d3744-118">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="examples"></a><span data-ttu-id="d3744-119">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d3744-119">Examples</span></span>

<span data-ttu-id="d3744-120">En el ejemplo siguiente se crea un elemento de botón HTML que usa *CDROM*. **expulsar** para abrir la puerta de la unidad que tiene el especificador de unidad index cero.</span><span class="sxs-lookup"><span data-stu-id="d3744-120">The following example creates an HTML button element that uses *Cdrom*.**eject** to open the door of the drive that has drive specifier index zero.</span></span> <span data-ttu-id="d3744-121">El objeto **Player** se creó con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="d3744-121">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"
       NAME = "EJECTBUTTON"
       VALUE = "EJECT"
       OnClick =  "Player.cdromCollection.item(0).eject()"
>
```



## <a name="requirements"></a><span data-ttu-id="d3744-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3744-122">Requirements</span></span>



| <span data-ttu-id="d3744-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3744-123">Requirement</span></span> | <span data-ttu-id="d3744-124">Value</span><span class="sxs-lookup"><span data-stu-id="d3744-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d3744-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d3744-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d3744-126">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="d3744-126">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d3744-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d3744-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d3744-128">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d3744-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d3744-129">Versión</span><span class="sxs-lookup"><span data-stu-id="d3744-129">Version</span></span><br/>                  | <span data-ttu-id="d3744-130">Windows Media Player versión 7,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="d3744-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="d3744-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d3744-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3744-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3744-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3744-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="d3744-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3744-134">**CDROM (objeto)**</span><span class="sxs-lookup"><span data-stu-id="d3744-134">**Cdrom Object**</span></span>](cdrom-object.md)
</dt> <dt>

[<span data-ttu-id="d3744-135">**Player. playState**</span><span class="sxs-lookup"><span data-stu-id="d3744-135">**Player.playState**</span></span>](player-playstate.md)
</dt> <dt>

[<span data-ttu-id="d3744-136">**Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="d3744-136">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="d3744-137">**Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="d3744-137">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





