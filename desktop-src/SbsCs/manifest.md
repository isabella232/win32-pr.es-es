---
description: La propiedad manifest se usa para establecer u obtener el contexto de activación activo.
ms.assetid: 5ad16c7b-3d66-4083-bc0f-f8294757764f
title: Propiedad ActCtx. manifest
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActCtx.Manifest
api_type:
- COM
api_location:
- Sxsoa.dll
ms.openlocfilehash: 2ebc671bbfcdfc951343e7f92cc0385ace43997e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001063"
---
# <a name="actctxmanifest-property"></a><span data-ttu-id="5a4c7-103">Propiedad ActCtx. manifest</span><span class="sxs-lookup"><span data-stu-id="5a4c7-103">ActCtx.Manifest property</span></span>

<span data-ttu-id="5a4c7-104">La propiedad **manifest** se usa para establecer u obtener el contexto de activación activo.</span><span class="sxs-lookup"><span data-stu-id="5a4c7-104">The **Manifest** property is used to set or get the active activation context.</span></span>

<span data-ttu-id="5a4c7-105">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="5a4c7-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a4c7-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5a4c7-106">Syntax</span></span>


```JScript
propVal = ActCtx.Manifest
```



## <a name="property-value"></a><span data-ttu-id="5a4c7-107">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="5a4c7-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="5a4c7-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5a4c7-108">Remarks</span></span>

<span data-ttu-id="5a4c7-109">Si se puede crear un contexto de activación con el archivo de manifiesto proporcionado, el siguiente script establece la propiedad manifest y activa la constante de activación especificada por el manifiesto.</span><span class="sxs-lookup"><span data-stu-id="5a4c7-109">If an activation context can be created with the manifest file provided, the following script sets the Manifest property and activates the activation constant specified by the manifest.</span></span> <span data-ttu-id="5a4c7-110">Si no se puede crear un contexto de activación a partir del manifiesto, el contexto de activación permanece establecido en el contexto de activación actualmente activo.</span><span class="sxs-lookup"><span data-stu-id="5a4c7-110">If an activation context cannot be created from the manifest, the activation context remains set to the currently active activation context.</span></span>

<span data-ttu-id="5a4c7-111">ActCtxObj. manifest = " *nombre de archivo de manifiesto* de <>";</span><span class="sxs-lookup"><span data-stu-id="5a4c7-111">ActCtxObj.Manifest = "<*manifest file name*>";</span></span>

<span data-ttu-id="5a4c7-112">Si un contexto de activación se ha creado o activado previamente, el siguiente script establece la propiedad **manifest** en el contexto de activación actual.</span><span class="sxs-lookup"><span data-stu-id="5a4c7-112">If an activation context has previously been created or activated, the following script sets the **Manifest** property to the current activation context.</span></span> <span data-ttu-id="5a4c7-113">Si un contexto de activación no se ha creado o activado previamente, establece la propiedad **manifest** en una cadena vacía.</span><span class="sxs-lookup"><span data-stu-id="5a4c7-113">If an activation context has not previously been created or activated, this sets the **Manifest** property to an empty string.</span></span>

<span data-ttu-id="5a4c7-114">"BSTR bstrManifest = ActCtxObj. manifest"</span><span class="sxs-lookup"><span data-stu-id="5a4c7-114">"BSTR bstrManifest = ActCtxObj.Manifest"</span></span>

## <a name="requirements"></a><span data-ttu-id="5a4c7-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a4c7-115">Requirements</span></span>



| <span data-ttu-id="5a4c7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a4c7-116">Requirement</span></span> | <span data-ttu-id="5a4c7-117">Value</span><span class="sxs-lookup"><span data-stu-id="5a4c7-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="5a4c7-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a4c7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5a4c7-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="5a4c7-119">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="5a4c7-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a4c7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5a4c7-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="5a4c7-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="5a4c7-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5a4c7-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a4c7-123"><dt>Sxsoa.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a4c7-123"><dt>Sxsoa.dll</dt></span></span> </dl> |
| <span data-ttu-id="5a4c7-124">IID</span><span class="sxs-lookup"><span data-stu-id="5a4c7-124">IID</span></span><br/>                      | <span data-ttu-id="5a4c7-125">IID \_ IActCtx se define como 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28</span><span class="sxs-lookup"><span data-stu-id="5a4c7-125">IID\_IActCtx is defined as 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28</span></span><br/>           |



 

 




