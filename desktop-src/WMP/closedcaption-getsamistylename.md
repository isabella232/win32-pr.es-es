---
title: ClosedCaption. getSAMIStyleName, método
description: El método getSAMIStyleName recupera el nombre de un estilo compatible con el archivo SAMI actual.
ms.assetid: c2ffedf8-4622-44fe-9d92-b52ed3bf3b9a
keywords:
- método getSAMIStyleName de Windows Media Player
- método getSAMIStyleName de Windows Media Player, clase ClosedCaption
- Clase ClosedCaption Windows Media Player, método getSAMIStyleName
topic_type:
- apiref
api_name:
- ClosedCaption.getSAMIStyleName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96480e28e0341b822aaf6726e63a6038681a577f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699540"
---
# <a name="closedcaptiongetsamistylename-method"></a><span data-ttu-id="52e17-106">ClosedCaption. getSAMIStyleName, método</span><span class="sxs-lookup"><span data-stu-id="52e17-106">ClosedCaption.getSAMIStyleName method</span></span>

<span data-ttu-id="52e17-107">El método **getSAMIStyleName** recupera el nombre de un estilo compatible con el archivo Sami actual.</span><span class="sxs-lookup"><span data-stu-id="52e17-107">The **getSAMIStyleName** method retrieves the name of a style supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="52e17-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="52e17-108">Syntax</span></span>


```JScript
strRetVal = ClosedCaption.getSAMIStyleName(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="52e17-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="52e17-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52e17-110">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="52e17-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52e17-111">**Número** (**largo**) que especifica el índice del nombre de estilo que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="52e17-111">**Number** (**long**) specifying the index of the style name to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52e17-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="52e17-112">Return value</span></span>

<span data-ttu-id="52e17-113">Este método devuelve una **cadena** que contiene el nombre del estilo tal y como se especifica en el archivo Sami.</span><span class="sxs-lookup"><span data-stu-id="52e17-113">This method returns a **String** containing the name of the style as specified in the SAMI file.</span></span>

## <a name="remarks"></a><span data-ttu-id="52e17-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="52e17-114">Remarks</span></span>

<span data-ttu-id="52e17-115">Los estilos de un archivo SAMI se indizan en el orden mostrado en el archivo, empezando por cero.</span><span class="sxs-lookup"><span data-stu-id="52e17-115">The styles in a SAMI file are indexed in the order shown in the file, starting with zero.</span></span>

<span data-ttu-id="52e17-116">Este método no se puede usar hasta que se abra un archivo multimedia digital (*reproductor*.**openState** es igual a 13).</span><span class="sxs-lookup"><span data-stu-id="52e17-116">This method cannot be used until a digital media file is open (*Player*.**openState** is equal to 13).</span></span>

<span data-ttu-id="52e17-117">**Windows Media Player 10 Mobile:** Este método no se admite.</span><span class="sxs-lookup"><span data-stu-id="52e17-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="52e17-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="52e17-118">Requirements</span></span>



| <span data-ttu-id="52e17-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="52e17-119">Requirement</span></span> | <span data-ttu-id="52e17-120">Value</span><span class="sxs-lookup"><span data-stu-id="52e17-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="52e17-121">Versión</span><span class="sxs-lookup"><span data-stu-id="52e17-121">Version</span></span><br/> | <span data-ttu-id="52e17-122">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="52e17-122">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="52e17-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="52e17-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="52e17-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52e17-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52e17-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="52e17-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52e17-126">**Agregar subtítulos a medios digitales**</span><span class="sxs-lookup"><span data-stu-id="52e17-126">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="52e17-127">**Objeto ClosedCaption**</span><span class="sxs-lookup"><span data-stu-id="52e17-127">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> <dt>

[<span data-ttu-id="52e17-128">**ClosedCaption.SAMIStyle**</span><span class="sxs-lookup"><span data-stu-id="52e17-128">**ClosedCaption.SAMIStyle**</span></span>](closedcaption-samistyle.md)
</dt> </dl>

 

 





