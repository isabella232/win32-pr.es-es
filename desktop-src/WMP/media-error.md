---
title: Media. error
description: La propiedad error recupera un objeto ErrorItem si el elemento multimedia tiene una condición de error.
ms.assetid: cd572688-12f9-4615-8f22-9442d615a2b6
keywords:
- Medio. error de Windows Media Player
topic_type:
- apiref
api_name:
- Media.error
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5845252c817a424b0cbe414612fde47ed8b57328
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653503"
---
# <a name="mediaerror"></a><span data-ttu-id="9b946-104">Media. error</span><span class="sxs-lookup"><span data-stu-id="9b946-104">Media.error</span></span>

<span data-ttu-id="9b946-105">La propiedad **error** recupera un objeto **ErrorItem** si el elemento multimedia tiene una condición de error.</span><span class="sxs-lookup"><span data-stu-id="9b946-105">The **error** property retrieves an **ErrorItem** object if the media item has an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b946-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9b946-106">Syntax</span></span>

<span data-ttu-id="9b946-107">*reproductor*. *currentMedia*. **error** de</span><span class="sxs-lookup"><span data-stu-id="9b946-107">*player*.*currentMedia*.**error**</span></span>

## <a name="possible-values"></a><span data-ttu-id="9b946-108">Valores posibles</span><span class="sxs-lookup"><span data-stu-id="9b946-108">Possible Values</span></span>

<span data-ttu-id="9b946-109">Esta propiedad es un objeto **ErrorItem** de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9b946-109">This property is a read-only **ErrorItem** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b946-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9b946-110">Remarks</span></span>

<span data-ttu-id="9b946-111">Si no se puede reproducir el elemento multimedia, esta propiedad recupera un objeto **ErrorItem** que contiene información sobre el problema encontrado.</span><span class="sxs-lookup"><span data-stu-id="9b946-111">If the media item cannot be played, this property retrieves an **ErrorItem** object that contains information about the problem encountered.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b946-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b946-112">Requirements</span></span>



| <span data-ttu-id="9b946-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b946-113">Requirement</span></span> | <span data-ttu-id="9b946-114">Value</span><span class="sxs-lookup"><span data-stu-id="9b946-114">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9b946-115">Versión</span><span class="sxs-lookup"><span data-stu-id="9b946-115">Version</span></span><br/> | <span data-ttu-id="9b946-116">Windows Media Player para Windows XP o posterior.</span><span class="sxs-lookup"><span data-stu-id="9b946-116">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="9b946-117">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9b946-117">DLL</span></span><br/>     | <dl> <span data-ttu-id="9b946-118"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b946-118"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b946-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b946-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b946-120">**Objeto ErrorItem**</span><span class="sxs-lookup"><span data-stu-id="9b946-120">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> <dt>

[<span data-ttu-id="9b946-121">**Objeto multimedia**</span><span class="sxs-lookup"><span data-stu-id="9b946-121">**Media Object**</span></span>](media-object.md)
</dt> </dl>

 

 





