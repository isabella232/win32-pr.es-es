---
title: IWMPControls3 getLanguageName, método
description: El método getLanguageName devuelve el nombre del idioma de audio con el identificador de configuración regional (LCID) especificado.
ms.assetid: a0651e8d-0ba1-4fff-93f0-fe097231723e
keywords:
- método getLanguageName de Windows Media Player
- método getLanguageName Windows Media Player, interfaz IWMPControls3
- Interfaz IWMPControls3 Windows Media Player, método getLanguageName
topic_type:
- apiref
api_name:
- IWMPControls3.getLanguageName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d93bf97c7b5213e3d196897de1c3ebcfa6e6d2c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650137"
---
# <a name="iwmpcontrols3getlanguagename-method"></a><span data-ttu-id="76248-106">IWMPControls3:: getLanguageName (método)</span><span class="sxs-lookup"><span data-stu-id="76248-106">IWMPControls3::getLanguageName method</span></span>

<span data-ttu-id="76248-107">El método **getLanguageName** devuelve el nombre del idioma de audio con el identificador de configuración regional (LCID) especificado.</span><span class="sxs-lookup"><span data-stu-id="76248-107">The **getLanguageName** method returns the name of the audio language with the specified locale identifier (LCID).</span></span>

## <a name="syntax"></a><span data-ttu-id="76248-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="76248-108">Syntax</span></span>


```CSharp
public System.String getLanguageName(
  System.Int32 lLangID
);
```


```VB

Public Function getLanguageName( _
  ByVal lLangID As System.Int32 _
) As System.String
Implements IWMPControls3.getLanguageName
```





## <a name="parameters"></a><span data-ttu-id="76248-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="76248-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76248-110">*lLangID* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="76248-110">*lLangID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="76248-111">**System. Int32** que es el LCID.</span><span class="sxs-lookup"><span data-stu-id="76248-111">A **System.Int32** that is the LCID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76248-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="76248-112">Return value</span></span>

<span data-ttu-id="76248-113">**System. String** que es el nombre del lenguaje de audio.</span><span class="sxs-lookup"><span data-stu-id="76248-113">A **System.String** that is the name of the audio language.</span></span>

## <a name="remarks"></a><span data-ttu-id="76248-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="76248-114">Remarks</span></span>

<span data-ttu-id="76248-115">Un LCID identifica de forma única un dialecto de lenguaje determinado, denominado configuración regional.</span><span class="sxs-lookup"><span data-stu-id="76248-115">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="76248-116">En el caso de contenido basado en Windows Media, las propiedades y los métodos relacionados con la selección de idioma solo admiten una salida única.</span><span class="sxs-lookup"><span data-stu-id="76248-116">For Windows Media-based content, properties and methods related to language selection support only a single output.</span></span>

## <a name="requirements"></a><span data-ttu-id="76248-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76248-117">Requirements</span></span>



| <span data-ttu-id="76248-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="76248-118">Requirement</span></span> | <span data-ttu-id="76248-119">Value</span><span class="sxs-lookup"><span data-stu-id="76248-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76248-120">Versión</span><span class="sxs-lookup"><span data-stu-id="76248-120">Version</span></span><br/>   | <span data-ttu-id="76248-121">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="76248-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="76248-122">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="76248-122">Namespace</span></span><br/> | <span data-ttu-id="76248-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="76248-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="76248-124">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="76248-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="76248-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="76248-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76248-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="76248-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76248-127">**Interfaz IWMPControls3 (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="76248-127">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="76248-128">**IWMPControls3. audioLanguageCount (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="76248-128">**IWMPControls3.audioLanguageCount (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="76248-129">**IWMPControls3. currentAudioLanguage (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="76248-129">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="76248-130">**IWMPControls3. currentAudioLanguageIndex (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="76248-130">**IWMPControls3.currentAudioLanguageIndex (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="76248-131">**IWMPControls3. getAudioLanguageDescription (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="76248-131">**IWMPControls3.getAudioLanguageDescription (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="76248-132">**IWMPControls3. getAudioLanguageID (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="76248-132">**IWMPControls3.getAudioLanguageID (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> </dl>

 

 





