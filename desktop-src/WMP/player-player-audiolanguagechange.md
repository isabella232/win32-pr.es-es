---
title: Evento Player. AudioLanguageChange
description: El evento AudioLanguageChange se produce cuando cambia el idioma de audio actual. | Evento Player. AudioLanguageChange
ms.assetid: 29006a51-1b72-4fab-9906-8a0af3d92560
keywords:
- Media Player AudioLanguageChange de eventos de Windows
- Evento AudioLanguageChange de Windows Media Player, clase Player
- Clase Player Media Player Windows, evento AudioLanguageChange
topic_type:
- apiref
api_name:
- Player.AudioLanguageChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e84809a966280c379f7051e500b4e385d640f890
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708767"
---
# <a name="playeraudiolanguagechange-event"></a><span data-ttu-id="4fc23-107">Evento Player. AudioLanguageChange</span><span class="sxs-lookup"><span data-stu-id="4fc23-107">Player.AudioLanguageChange event</span></span>

<span data-ttu-id="4fc23-108">El evento **AudioLanguageChange** se produce cuando cambia el idioma de audio actual.</span><span class="sxs-lookup"><span data-stu-id="4fc23-108">The **AudioLanguageChange** event occurs when the current audio language changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fc23-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4fc23-109">Syntax</span></span>


```JScript
Player.AudioLanguageChange(
  LangID
)
```



## <a name="parameters"></a><span data-ttu-id="4fc23-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4fc23-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fc23-111">*Ididioma*</span><span class="sxs-lookup"><span data-stu-id="4fc23-111">*LangID*</span></span> 
</dt> <dd>

<span data-ttu-id="4fc23-112">**Número** (**largo**) que especifica el nuevo identificador de configuración regional (LCID).</span><span class="sxs-lookup"><span data-stu-id="4fc23-112">**Number** (**long**) specifying the new locale identifier (LCID).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fc23-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4fc23-113">Return value</span></span>

<span data-ttu-id="4fc23-114">Este evento no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="4fc23-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fc23-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4fc23-115">Remarks</span></span>

<span data-ttu-id="4fc23-116">Un LCID identifica de forma única un dialecto de lenguaje determinado, denominado configuración regional.</span><span class="sxs-lookup"><span data-stu-id="4fc23-116">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="4fc23-117">El valor de los parámetros de evento lo especifica Windows Media Player y se puede tener acceso a él o pasarlo a un método en un archivo de Microsoft JScript importado mediante el nombre de parámetro dado.</span><span class="sxs-lookup"><span data-stu-id="4fc23-117">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported Microsoft JScript file by using the parameter name given.</span></span> <span data-ttu-id="4fc23-118">Este nombre de parámetro debe escribirse exactamente como se muestra, incluidas las mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4fc23-118">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="4fc23-119">**Windows Media Player 10 Mobile:** Este evento no se admite.</span><span class="sxs-lookup"><span data-stu-id="4fc23-119">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fc23-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4fc23-120">Requirements</span></span>



| <span data-ttu-id="4fc23-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4fc23-121">Requirement</span></span> | <span data-ttu-id="4fc23-122">Value</span><span class="sxs-lookup"><span data-stu-id="4fc23-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4fc23-123">Versión</span><span class="sxs-lookup"><span data-stu-id="4fc23-123">Version</span></span><br/> | <span data-ttu-id="4fc23-124">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="4fc23-124">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="4fc23-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4fc23-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="4fc23-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4fc23-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4fc23-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="4fc23-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fc23-128">**Controls. currentAudioLanguage**</span><span class="sxs-lookup"><span data-stu-id="4fc23-128">**Controls.currentAudioLanguage**</span></span>](controls-currentaudiolanguage.md)
</dt> <dt>

[<span data-ttu-id="4fc23-129">**Objeto Player**</span><span class="sxs-lookup"><span data-stu-id="4fc23-129">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





