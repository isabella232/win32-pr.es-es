---
title: ErrorItem.errorContext
description: La propiedad errorContext recupera un valor que indica el contexto del error.
ms.assetid: 700d2bf0-dd3b-4211-99ea-58f952cf24b0
keywords:
- ErrorItem. errorContext Windows Media Player
topic_type:
- apiref
api_name:
- ErrorItem.errorContext
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9b9ed91d34645f08e7d3d28860ced9ca51420dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698629"
---
# <a name="erroritemerrorcontext"></a><span data-ttu-id="f9ba5-104">ErrorItem.errorContext</span><span class="sxs-lookup"><span data-stu-id="f9ba5-104">ErrorItem.errorContext</span></span>

<span data-ttu-id="f9ba5-105">La propiedad **errorContext** recupera un valor que indica el contexto del error.</span><span class="sxs-lookup"><span data-stu-id="f9ba5-105">The **errorContext** property retrieves a value indicating the context of the error.</span></span>

``` syntax
player.error.item(
        index
        ).errorContext
```

## <a name="possible-values"></a><span data-ttu-id="f9ba5-106">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="f9ba5-106">Possible Values</span></span>

<span data-ttu-id="f9ba5-107">Esta propiedad es una **cadena** de solo lectura que representa el código de contexto del error.</span><span class="sxs-lookup"><span data-stu-id="f9ba5-107">This property is a read-only **String** that represents the error context code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9ba5-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f9ba5-108">Remarks</span></span>

<span data-ttu-id="f9ba5-109">El contexto de error es información que Microsoft usa para proporcionar información adicional para el personal de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="f9ba5-109">The error context is information that is used by Microsoft to provide additional information for technical support personnel.</span></span>

<span data-ttu-id="f9ba5-110">**Windows Media Player 10 Mobile:** Esta propiedad siempre devuelve una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="f9ba5-110">**Windows Media Player 10 Mobile:** This property always returns an empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9ba5-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9ba5-111">Requirements</span></span>



| <span data-ttu-id="f9ba5-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9ba5-112">Requirement</span></span> | <span data-ttu-id="f9ba5-113">Value</span><span class="sxs-lookup"><span data-stu-id="f9ba5-113">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f9ba5-114">Versión</span><span class="sxs-lookup"><span data-stu-id="f9ba5-114">Version</span></span><br/> | <span data-ttu-id="f9ba5-115">Windows Media Player versión 7,0 o posterior</span><span class="sxs-lookup"><span data-stu-id="f9ba5-115">Windows Media Player version 7.0 or later</span></span><br/>                               |
| <span data-ttu-id="f9ba5-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f9ba5-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="f9ba5-117"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9ba5-117"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9ba5-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9ba5-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9ba5-119">**Objeto ErrorItem**</span><span class="sxs-lookup"><span data-stu-id="f9ba5-119">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> </dl>

 

 





