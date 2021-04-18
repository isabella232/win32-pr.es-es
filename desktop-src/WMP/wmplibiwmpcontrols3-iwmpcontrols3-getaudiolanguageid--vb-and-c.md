---
title: IWMPControls3 getAudioLanguageID, método
description: El método getAudioLanguageID devuelve el identificador de configuración regional (LCID) para un índice de idioma de audio especificado.
ms.assetid: 880bbfca-6f69-41ce-a078-467c1939fae5
keywords:
- método getAudioLanguageID de Windows Media Player
- método getAudioLanguageID Windows Media Player, interfaz IWMPControls3
- Interfaz IWMPControls3 Windows Media Player, método getAudioLanguageID
topic_type:
- apiref
api_name:
- IWMPControls3.getAudioLanguageID
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb8112eafec018b12012d20b37bfe30f7b464377
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105650138"
---
# <a name="iwmpcontrols3getaudiolanguageid-method"></a><span data-ttu-id="a4c73-106">IWMPControls3:: getAudioLanguageID (método)</span><span class="sxs-lookup"><span data-stu-id="a4c73-106">IWMPControls3::getAudioLanguageID method</span></span>

<span data-ttu-id="a4c73-107">El método **getAudioLanguageID** devuelve el identificador de configuración regional (LCID) para un índice de idioma de audio especificado.</span><span class="sxs-lookup"><span data-stu-id="a4c73-107">The **getAudioLanguageID** method returns the locale identifier (LCID) for a specified audio language index.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4c73-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a4c73-108">Syntax</span></span>


```CSharp
public System.Int32 getAudioLanguageID(
  System.Int32 lIndex
);
```


```VB

Public Function getAudioLanguageID( _
  ByVal lIndex As System.Int32 _
) As System.Int32
Implements IWMPControls3.getAudioLanguageID
```





## <a name="parameters"></a><span data-ttu-id="a4c73-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a4c73-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4c73-110">*lIndex* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a4c73-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4c73-111">**System. Int32** que es el índice de base uno del lenguaje de audio.</span><span class="sxs-lookup"><span data-stu-id="a4c73-111">A **System.Int32** that is the one-based index of the audio language.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4c73-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a4c73-112">Return value</span></span>

<span data-ttu-id="a4c73-113">**System. Int32** que es el LCID.</span><span class="sxs-lookup"><span data-stu-id="a4c73-113">A **System.Int32** that is the LCID.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4c73-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a4c73-114">Remarks</span></span>

<span data-ttu-id="a4c73-115">Un LCID identifica de forma única un dialecto de lenguaje determinado, denominado configuración regional.</span><span class="sxs-lookup"><span data-stu-id="a4c73-115">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="a4c73-116">En el caso de contenido basado en Windows Media, las propiedades y los métodos relacionados con la selección de idioma solo admiten una salida única.</span><span class="sxs-lookup"><span data-stu-id="a4c73-116">For Windows Media based content, properties and methods related to language selection support only a single output.</span></span>

<span data-ttu-id="a4c73-117">Use la propiedad **audioLanguageCount** para obtener el número de idiomas de audio admitidos y, a continuación, acceda a un idioma de audio individualmente mediante un índice basado en uno.</span><span class="sxs-lookup"><span data-stu-id="a4c73-117">Use the **audioLanguageCount** property to get the number of supported audio languages, and then access an audio language individually by using a one-based index.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4c73-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4c73-118">Requirements</span></span>



| <span data-ttu-id="a4c73-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a4c73-119">Requirement</span></span> | <span data-ttu-id="a4c73-120">Value</span><span class="sxs-lookup"><span data-stu-id="a4c73-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4c73-121">Versión</span><span class="sxs-lookup"><span data-stu-id="a4c73-121">Version</span></span><br/>   | <span data-ttu-id="a4c73-122">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="a4c73-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="a4c73-123">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a4c73-123">Namespace</span></span><br/> | <span data-ttu-id="a4c73-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="a4c73-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a4c73-125">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="a4c73-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a4c73-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a4c73-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4c73-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="a4c73-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4c73-128">**Interfaz IWMPControls3 (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="a4c73-128">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a4c73-129">**IWMPControls3. audioLanguageCount (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="a4c73-129">**IWMPControls3.audioLanguageCount (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a4c73-130">**IWMPControls3. currentAudioLanguage (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="a4c73-130">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a4c73-131">**IWMPControls3. currentAudioLanguageIndex (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="a4c73-131">**IWMPControls3.currentAudioLanguageIndex (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a4c73-132">**IWMPControls3. getAudioLanguageDescription (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="a4c73-132">**IWMPControls3.getAudioLanguageDescription (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a4c73-133">**IWMPControls3. getLanguageName (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="a4c73-133">**IWMPControls3.getLanguageName (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





