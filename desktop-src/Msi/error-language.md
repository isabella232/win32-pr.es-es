---
description: La propiedad idioma de solo lectura del objeto error devuelve el LANGID del error actual.
ms.assetid: f47cad5d-8e76-4210-b1ab-377d2d05379e
title: Propiedad error. Language (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Error.Language
- IMsmError.get_Language
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 6c80802c41f076a2b1c0b320b591bc591da8546e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653771"
---
# <a name="errorlanguage-property"></a><span data-ttu-id="71d2c-103">Error. Language (propiedad)</span><span class="sxs-lookup"><span data-stu-id="71d2c-103">Error.Language property</span></span>

<span data-ttu-id="71d2c-104">La propiedad **idioma** de solo lectura del objeto [**error**](error-object.md) devuelve el **LANGID** del error actual.</span><span class="sxs-lookup"><span data-stu-id="71d2c-104">The read-only **Language** property of the [**Error**](error-object.md) object returns the **LANGID** of the current error.</span></span>

<span data-ttu-id="71d2c-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="71d2c-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="71d2c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="71d2c-106">Syntax</span></span>


```JScript
propVal = Error.Language
```



## <a name="property-value"></a><span data-ttu-id="71d2c-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="71d2c-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="71d2c-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="71d2c-108">Remarks</span></span>

<span data-ttu-id="71d2c-109">El valor de la propiedad **Language** es-1, a menos que el error sea de tipo MsmErrorLanguageUnsupported o msmErrorLanguageFailed.</span><span class="sxs-lookup"><span data-stu-id="71d2c-109">The value of the **Language** property is -1 unless the error is of type msmErrorLanguageUnsupported or msmErrorLanguageFailed.</span></span> <span data-ttu-id="71d2c-110">Puede determinar el tipo de error llamando a la propiedad [**Type**](error-type.md) del objeto [**error**](error-object.md) .</span><span class="sxs-lookup"><span data-stu-id="71d2c-110">You can determine the type of error by calling the [**Type**](error-type.md) property of the [**Error**](error-object.md) object.</span></span>

### <a name="c"></a><span data-ttu-id="71d2c-111">C++</span><span class="sxs-lookup"><span data-stu-id="71d2c-111">C++</span></span>

<span data-ttu-id="71d2c-112">Vea [**Get \_ Language function (objeto de error)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_language).</span><span class="sxs-lookup"><span data-stu-id="71d2c-112">See [**get\_Language Function (Error Object)**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_language).</span></span>

## <a name="requirements"></a><span data-ttu-id="71d2c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71d2c-113">Requirements</span></span>



| <span data-ttu-id="71d2c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="71d2c-114">Requirement</span></span> | <span data-ttu-id="71d2c-115">Value</span><span class="sxs-lookup"><span data-stu-id="71d2c-115">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="71d2c-116">Versión</span><span class="sxs-lookup"><span data-stu-id="71d2c-116">Version</span></span><br/> | <span data-ttu-id="71d2c-117">Mergemod.dll 1,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="71d2c-117">Mergemod.dll 1.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="71d2c-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="71d2c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="71d2c-119"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="71d2c-119"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="71d2c-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="71d2c-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="71d2c-121"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71d2c-121"><dt>Mergemod.dll</dt></span></span> </dl> |



 

