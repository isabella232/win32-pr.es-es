---
description: El método GetLangFromLangID recupera una cadena inteligible para el usuario cuando se le asigna un identificador de idioma principal.
ms.assetid: 73cff3df-bfcd-4e51-bd41-51545ed82f09
title: Método GetLangFromLangID
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23afddf746852028c26732eb658e786588f7e9ec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906615"
---
# <a name="getlangfromlangid-method"></a><span data-ttu-id="0ea51-103">Método GetLangFromLangID</span><span class="sxs-lookup"><span data-stu-id="0ea51-103">GetLangFromLangID Method</span></span>

> [!Note]  
> <span data-ttu-id="0ea51-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="0ea51-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="0ea51-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="0ea51-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="0ea51-106">El `GetLangFromLangID` método recupera una cadena inteligible para el usuario cuando se le asigna un identificador de idioma principal.</span><span class="sxs-lookup"><span data-stu-id="0ea51-106">The `GetLangFromLangID` method retrieves a human-readable string when given a primary language ID.</span></span>

``` syntax
[ sLanguage = ] MSWebDVD.GetLangFromLangID(iPrimaryLangID)
```

## <a name="parameters"></a><span data-ttu-id="0ea51-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0ea51-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ea51-108"><span id="iPrimaryLangID"></span><span id="iprimarylangid"></span><span id="IPRIMARYLANGID"></span>*iPrimaryLangID*</span><span class="sxs-lookup"><span data-stu-id="0ea51-108"><span id="iPrimaryLangID"></span><span id="iprimarylangid"></span><span id="IPRIMARYLANGID"></span>*iPrimaryLangID*</span></span>
</dt> <dd>

<span data-ttu-id="0ea51-109">Especifica el identificador de idioma principal como un entero.</span><span class="sxs-lookup"><span data-stu-id="0ea51-109">Specifies the primary language ID as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ea51-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0ea51-110">Return Value</span></span>

<span data-ttu-id="0ea51-111">Devuelve una representación de cadena del idioma que se puede mostrar en la interfaz de usuario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0ea51-111">Returns a String representation of the language that can be displayed in the application's user interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ea51-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0ea51-112">Remarks</span></span>

<span data-ttu-id="0ea51-113">Aunque este método se denomina `GetLangFromLangID` , el parámetro que se pasa es realmente el identificador de idioma principal, no el identificador de idioma.</span><span class="sxs-lookup"><span data-stu-id="0ea51-113">Although this method is named `GetLangFromLangID`, the parameter that you pass is actually the primary language ID, not the language ID.</span></span>

## <a name="see-also"></a><span data-ttu-id="0ea51-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ea51-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ea51-115">**GetAudioLanguage**</span><span class="sxs-lookup"><span data-stu-id="0ea51-115">**GetAudioLanguage**</span></span>](getaudiolanguage-method.md)
</dt> <dt>

[<span data-ttu-id="0ea51-116">**GetDVDTextLanguageLCID**</span><span class="sxs-lookup"><span data-stu-id="0ea51-116">**GetDVDTextLanguageLCID**</span></span>](getdvdtextlanguagelcid-method.md)
</dt> </dl>

 

 



