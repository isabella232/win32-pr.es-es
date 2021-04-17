---
title: ClosedCaption. getSAMILangName, método
description: El método getSAMILangName recupera el nombre de un idioma admitido por el archivo SAMI actual.
ms.assetid: 20cf8faf-3a8c-4d7b-9bd1-2366672f0e67
keywords:
- método getSAMILangName de Windows Media Player
- método getSAMILangName de Windows Media Player, clase ClosedCaption
- Clase ClosedCaption Windows Media Player, método getSAMILangName
topic_type:
- apiref
api_name:
- ClosedCaption.getSAMILangName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccd4b481de808ac8814e596cfc038aec38c7f19b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699789"
---
# <a name="closedcaptiongetsamilangname-method"></a><span data-ttu-id="095ef-106">ClosedCaption. getSAMILangName, método</span><span class="sxs-lookup"><span data-stu-id="095ef-106">ClosedCaption.getSAMILangName method</span></span>

<span data-ttu-id="095ef-107">El método **getSAMILangName** recupera el nombre de un idioma admitido por el archivo Sami actual.</span><span class="sxs-lookup"><span data-stu-id="095ef-107">The **getSAMILangName** method retrieves the name of a language supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="095ef-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="095ef-108">Syntax</span></span>


```JScript
strRetVal = ClosedCaption.getSAMILangName(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="095ef-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="095ef-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="095ef-110">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="095ef-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="095ef-111">**Número** (**largo**) que especifica el índice del nombre del idioma que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="095ef-111">**Number** (**long**) specifying the index of the language name to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="095ef-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="095ef-112">Return value</span></span>

<span data-ttu-id="095ef-113">Este método devuelve una **cadena** que contiene el nombre del idioma tal como se especifica en el archivo Sami.</span><span class="sxs-lookup"><span data-stu-id="095ef-113">This method returns a **String** containing the name of the language as specified in the SAMI file.</span></span>

## <a name="remarks"></a><span data-ttu-id="095ef-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="095ef-114">Remarks</span></span>

<span data-ttu-id="095ef-115">Los idiomas de un archivo SAMI se indizan en el orden mostrado en el archivo, empezando por cero.</span><span class="sxs-lookup"><span data-stu-id="095ef-115">The languages in a SAMI file are indexed in the order shown in the file, starting with zero.</span></span>

<span data-ttu-id="095ef-116">Este método no se puede usar hasta que se abra un archivo multimedia digital (*reproductor*.**openState** es igual a 13).</span><span class="sxs-lookup"><span data-stu-id="095ef-116">This method cannot be used until a digital media file is open (*Player*.**openState** is equal to 13).</span></span>

<span data-ttu-id="095ef-117">**Windows Media Player 10 Mobile:** Este método no se admite.</span><span class="sxs-lookup"><span data-stu-id="095ef-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="095ef-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="095ef-118">Requirements</span></span>



| <span data-ttu-id="095ef-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="095ef-119">Requirement</span></span> | <span data-ttu-id="095ef-120">Value</span><span class="sxs-lookup"><span data-stu-id="095ef-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="095ef-121">Versión</span><span class="sxs-lookup"><span data-stu-id="095ef-121">Version</span></span><br/> | <span data-ttu-id="095ef-122">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="095ef-122">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="095ef-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="095ef-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="095ef-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="095ef-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="095ef-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="095ef-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="095ef-126">**Agregar subtítulos a medios digitales**</span><span class="sxs-lookup"><span data-stu-id="095ef-126">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="095ef-127">**Objeto ClosedCaption**</span><span class="sxs-lookup"><span data-stu-id="095ef-127">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> <dt>

[<span data-ttu-id="095ef-128">**ClosedCaption.SAMILang**</span><span class="sxs-lookup"><span data-stu-id="095ef-128">**ClosedCaption.SAMILang**</span></span>](closedcaption-samilang.md)
</dt> </dl>

 

 





