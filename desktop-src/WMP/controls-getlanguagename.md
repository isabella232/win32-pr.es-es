---
title: Controls. getLanguageName (método)
description: El método getLanguageName recupera el nombre del idioma de audio con el identificador de configuración regional (LCID) especificado.
ms.assetid: 9e142c89-92bf-476f-bae7-b94f5b5ebe01
keywords:
- método getLanguageName de Windows Media Player
- método getLanguageName Windows Media Player, clase Controls
- Clase Controls Windows Media Player, método getLanguageName
topic_type:
- apiref
api_name:
- Controls.getLanguageName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 798a6b22f344953df716e4df4ed8a9a0daff2a7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700039"
---
# <a name="controlsgetlanguagename-method"></a><span data-ttu-id="92c25-106">Controls. getLanguageName (método)</span><span class="sxs-lookup"><span data-stu-id="92c25-106">Controls.getLanguageName method</span></span>

<span data-ttu-id="92c25-107">El método **getLanguageName** recupera el nombre del idioma de audio con el identificador de configuración regional (LCID) especificado.</span><span class="sxs-lookup"><span data-stu-id="92c25-107">The **getLanguageName** method retrieves the name of the audio language with the specified locale identifier (LCID).</span></span>

## <a name="syntax"></a><span data-ttu-id="92c25-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92c25-108">Syntax</span></span>


```JScript
strRetVal = Controls.getLanguageName(
  LCID
)
```



## <a name="parameters"></a><span data-ttu-id="92c25-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="92c25-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92c25-110">*LCID* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="92c25-110">*LCID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92c25-111">**Número** (**largo**) que especifica el LCID.</span><span class="sxs-lookup"><span data-stu-id="92c25-111">**Number** (**long**) specifying the LCID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92c25-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="92c25-112">Return value</span></span>

<span data-ttu-id="92c25-113">Este método devuelve una **cadena**.</span><span class="sxs-lookup"><span data-stu-id="92c25-113">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="92c25-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="92c25-114">Remarks</span></span>

<span data-ttu-id="92c25-115">Un LCID identifica de forma única un dialecto de lenguaje determinado, denominado configuración regional.</span><span class="sxs-lookup"><span data-stu-id="92c25-115">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="92c25-116">En el caso de contenido basado en Windows Media, las propiedades y los métodos relacionados con la selección de idioma solo admiten una salida única.</span><span class="sxs-lookup"><span data-stu-id="92c25-116">For Windows Media-based content, properties and methods related to language selection only support a single output.</span></span>

## <a name="requirements"></a><span data-ttu-id="92c25-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92c25-117">Requirements</span></span>



| <span data-ttu-id="92c25-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="92c25-118">Requirement</span></span> | <span data-ttu-id="92c25-119">Value</span><span class="sxs-lookup"><span data-stu-id="92c25-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="92c25-120">Versión</span><span class="sxs-lookup"><span data-stu-id="92c25-120">Version</span></span><br/> | <span data-ttu-id="92c25-121">Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="92c25-121">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="92c25-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="92c25-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="92c25-123"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92c25-123"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92c25-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="92c25-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92c25-125">**Controls (objeto)**</span><span class="sxs-lookup"><span data-stu-id="92c25-125">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="92c25-126">**Controls. audioLanguageCount**</span><span class="sxs-lookup"><span data-stu-id="92c25-126">**Controls.audioLanguageCount**</span></span>](controls-audiolanguagecount.md)
</dt> <dt>

[<span data-ttu-id="92c25-127">**Controls. currentAudioLanguage**</span><span class="sxs-lookup"><span data-stu-id="92c25-127">**Controls.currentAudioLanguage**</span></span>](controls-currentaudiolanguage.md)
</dt> <dt>

[<span data-ttu-id="92c25-128">**Controls. currentAudioLanguageIndex**</span><span class="sxs-lookup"><span data-stu-id="92c25-128">**Controls.currentAudioLanguageIndex**</span></span>](controls-currentaudiolanguageindex.md)
</dt> <dt>

[<span data-ttu-id="92c25-129">**Controls. getAudioLanguageDescription**</span><span class="sxs-lookup"><span data-stu-id="92c25-129">**Controls.getAudioLanguageDescription**</span></span>](controls-getaudiolanguagedescription.md)
</dt> <dt>

[<span data-ttu-id="92c25-130">**Controls. getAudioLanguageID**</span><span class="sxs-lookup"><span data-stu-id="92c25-130">**Controls.getAudioLanguageID**</span></span>](controls-getaudiolanguageid.md)
</dt> </dl>

 

 





