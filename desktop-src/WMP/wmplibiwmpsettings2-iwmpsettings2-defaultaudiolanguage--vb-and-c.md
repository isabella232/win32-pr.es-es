---
title: Propiedad defaultAudioLanguage de IWMPSettings2
description: La propiedad defaultAudioLanguage obtiene el identificador de configuración regional (LCID) del idioma de audio predeterminado especificado en Windows Media Player.
ms.assetid: 4b7c9639-9d9f-4ed7-bb70-12cc608dd57a
keywords:
- propiedades de defaultAudioLanguage Media Player de Windows
- propiedad defaultAudioLanguage de Windows Media Player, interfaz IWMPSettings2
- Interfaz IWMPSettings2 Windows Media Player, propiedad defaultAudioLanguage
topic_type:
- apiref
api_name:
- IWMPSettings2.defaultAudioLanguage
- IWMPSettings2.get_defaultAudioLanguage
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc7ac9120437005d9f32388e4d639d2d5893675e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690326"
---
# <a name="iwmpsettings2defaultaudiolanguage-property"></a><span data-ttu-id="e2d31-106">IWMPSettings2::d propiedad efaultAudioLanguage</span><span class="sxs-lookup"><span data-stu-id="e2d31-106">IWMPSettings2::defaultAudioLanguage property</span></span>

<span data-ttu-id="e2d31-107">La propiedad **defaultAudioLanguage** obtiene el identificador de configuración regional (LCID) del idioma de audio predeterminado especificado en Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="e2d31-107">The **defaultAudioLanguage** property gets the locale identifier (LCID) of the default audio language specified in Windows Media Player.</span></span>

<span data-ttu-id="e2d31-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="e2d31-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2d31-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e2d31-109">Syntax</span></span>


```CSharp
public System.Int32 defaultAudioLanguage {get;}
```


```VB

Public ReadOnly Property defaultAudioLanguage As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="e2d31-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="e2d31-110">Property value</span></span>

<span data-ttu-id="e2d31-111">**System. Int32** que es el LCID.</span><span class="sxs-lookup"><span data-stu-id="e2d31-111">A **System.Int32** that is the LCID.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2d31-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e2d31-112">Remarks</span></span>

<span data-ttu-id="e2d31-113">Un LCID identifica de forma única un dialecto de lenguaje determinado, denominado configuración regional.</span><span class="sxs-lookup"><span data-stu-id="e2d31-113">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2d31-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2d31-114">Requirements</span></span>



| <span data-ttu-id="e2d31-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2d31-115">Requirement</span></span> | <span data-ttu-id="e2d31-116">Value</span><span class="sxs-lookup"><span data-stu-id="e2d31-116">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2d31-117">Versión</span><span class="sxs-lookup"><span data-stu-id="e2d31-117">Version</span></span><br/>   | <span data-ttu-id="e2d31-118">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="e2d31-118">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="e2d31-119">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e2d31-119">Namespace</span></span><br/> | <span data-ttu-id="e2d31-120">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="e2d31-120">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="e2d31-121">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="e2d31-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e2d31-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e2d31-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2d31-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="e2d31-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2d31-124">**IWMPControls3. currentAudioLanguage (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="e2d31-124">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e2d31-125">**Interfaz IWMPSettings (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="e2d31-125">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e2d31-126">**Interfaz IWMPSettings2 (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="e2d31-126">**IWMPSettings2 Interface (VB and C#)**</span></span>](iwmpsettings2--vb-and-c.md)
</dt> </dl>

 

 





