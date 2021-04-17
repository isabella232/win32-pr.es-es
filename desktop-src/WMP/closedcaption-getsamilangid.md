---
title: ClosedCaption. getSAMILangID, método
description: El método getSAMILangID recupera el identificador de configuración regional (LCID) de un idioma admitido por el archivo SAMI actual.
ms.assetid: 35f8379a-a2f5-4b22-b1ad-3c5cc5bc5e3d
keywords:
- método getSAMILangID de Windows Media Player
- método getSAMILangID de Windows Media Player, clase ClosedCaption
- Clase ClosedCaption Windows Media Player, método getSAMILangID
topic_type:
- apiref
api_name:
- ClosedCaption.getSAMILangID
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cd543c9cb9d884022d78a875a2f8de078c479b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700429"
---
# <a name="closedcaptiongetsamilangid-method"></a><span data-ttu-id="bb7ec-106">ClosedCaption. getSAMILangID, método</span><span class="sxs-lookup"><span data-stu-id="bb7ec-106">ClosedCaption.getSAMILangID method</span></span>

<span data-ttu-id="bb7ec-107">El método **getSAMILangID** recupera el identificador de configuración regional (LCID) de un idioma admitido por el archivo Sami actual.</span><span class="sxs-lookup"><span data-stu-id="bb7ec-107">The **getSAMILangID** method retrieves the locale identifier (LCID) of a language supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb7ec-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bb7ec-108">Syntax</span></span>


```JScript
retVal = ClosedCaption.getSAMILangID(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="bb7ec-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bb7ec-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb7ec-110">*Índice* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="bb7ec-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bb7ec-111">**Número** (**largo**) que especifica el índice del LCID que se va a recuperar.</span><span class="sxs-lookup"><span data-stu-id="bb7ec-111">**Number** (**long**) specifying the index of the LCID to retrieve.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb7ec-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bb7ec-112">Return value</span></span>

<span data-ttu-id="bb7ec-113">Este método devuelve un **número** (**Long**) que contiene el LCID del idioma con el índice especificado.</span><span class="sxs-lookup"><span data-stu-id="bb7ec-113">This method returns a **Number** (**long**) containing the LCID of the language with the specified index.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb7ec-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bb7ec-114">Remarks</span></span>

<span data-ttu-id="bb7ec-115">Los idiomas de un archivo SAMI se indizan en el orden mostrado en el archivo, empezando por cero.</span><span class="sxs-lookup"><span data-stu-id="bb7ec-115">The languages in a SAMI file are indexed in the order shown in the file, starting with zero.</span></span>

<span data-ttu-id="bb7ec-116">Este método no se puede usar hasta que se abra un archivo multimedia digital (*reproductor*.**openState** es igual a 13).</span><span class="sxs-lookup"><span data-stu-id="bb7ec-116">This method cannot be used until a digital media file is open (*Player*.**openState** is equal to 13).</span></span>

<span data-ttu-id="bb7ec-117">**Windows Media Player 10 Mobile:** Este método no se admite.</span><span class="sxs-lookup"><span data-stu-id="bb7ec-117">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb7ec-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb7ec-118">Requirements</span></span>



| <span data-ttu-id="bb7ec-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb7ec-119">Requirement</span></span> | <span data-ttu-id="bb7ec-120">Value</span><span class="sxs-lookup"><span data-stu-id="bb7ec-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bb7ec-121">Versión</span><span class="sxs-lookup"><span data-stu-id="bb7ec-121">Version</span></span><br/> | <span data-ttu-id="bb7ec-122">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="bb7ec-122">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="bb7ec-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bb7ec-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="bb7ec-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb7ec-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb7ec-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="bb7ec-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb7ec-126">**Agregar subtítulos a medios digitales**</span><span class="sxs-lookup"><span data-stu-id="bb7ec-126">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="bb7ec-127">**Objeto ClosedCaption**</span><span class="sxs-lookup"><span data-stu-id="bb7ec-127">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> </dl>

 

 





