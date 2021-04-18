---
title: EQUALIZERSETTINGS.nextPreset
description: El método nextPreset aplica el siguiente valor preestablecido del ecualizador.
ms.assetid: 67d40ec9-2744-4d63-aa56-0ee20496e896
keywords:
- EQUALIZERSETTINGS. nextPreset Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.nextPreset
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b464c0fca9b38a14a65a24185e51813e4520eee0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700281"
---
# <a name="equalizersettingsnextpreset"></a><span data-ttu-id="3d95c-104">EQUALIZERSETTINGS.nextPreset</span><span class="sxs-lookup"><span data-stu-id="3d95c-104">EQUALIZERSETTINGS.nextPreset</span></span>

<span data-ttu-id="3d95c-105">El método **nextPreset** aplica el siguiente valor preestablecido del ecualizador.</span><span class="sxs-lookup"><span data-stu-id="3d95c-105">The **nextPreset** method applies the next equalizer preset.</span></span>

``` syntax
        elementID.nextPreset()
```

## <a name="parameters"></a><span data-ttu-id="3d95c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3d95c-106">Parameters</span></span>

<span data-ttu-id="3d95c-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="3d95c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3d95c-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3d95c-108">Return Value</span></span>

<span data-ttu-id="3d95c-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="3d95c-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d95c-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3d95c-110">Remarks</span></span>

<span data-ttu-id="3d95c-111">Si el valor predeterminado actual es el último disponible, el primer valor preestablecido se convierte en actual.</span><span class="sxs-lookup"><span data-stu-id="3d95c-111">If the current preset is the last one available, the first preset is made current.</span></span>

## <a name="examples"></a><span data-ttu-id="3d95c-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="3d95c-112">Examples</span></span>


```JScript
<SUBVIEW id="eqtray">
  <EQUALIZERSETTINGS id="eq"/>
  <BUTTON
    id="nextPreset" 
    onClick="eq.nextPreset();"
  />
  <BUTTON
    id="prevPreset" 
    onClick="eq.previousPreset();"
  />
  <TEXT
    id="currentPreset" 
    value="wmpprop:eq.currentPresetTitle" 
  />
</SUBVIEW>
```



## <a name="requirements"></a><span data-ttu-id="3d95c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d95c-113">Requirements</span></span>



| <span data-ttu-id="3d95c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d95c-114">Requirement</span></span> | <span data-ttu-id="3d95c-115">Value</span><span class="sxs-lookup"><span data-stu-id="3d95c-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="3d95c-116">Versión</span><span class="sxs-lookup"><span data-stu-id="3d95c-116">Version</span></span><br/> | <span data-ttu-id="3d95c-117">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="3d95c-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3d95c-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="3d95c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d95c-119">**Elemento EQUALIZERSETTINGS**</span><span class="sxs-lookup"><span data-stu-id="3d95c-119">**EQUALIZERSETTINGS Element**</span></span>](equalizersettings-element.md)
</dt> <dt>

[<span data-ttu-id="3d95c-120">**EQUALIZERSETTINGS.previousPreset**</span><span class="sxs-lookup"><span data-stu-id="3d95c-120">**EQUALIZERSETTINGS.previousPreset**</span></span>](equalizersettings-previouspreset.md)
</dt> </dl>

 

 





