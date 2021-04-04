---
title: Propiedad de etiqueta ITsSbTaskInfo
description: Recupera la etiqueta que describe el propósito de la tarea.
ms.assetid: 075de6a4-53b0-43b0-9bca-03bf312fff6e
ms.tgt_platform: multiple
keywords:
- Propiedad de etiqueta Servicios de Escritorio remoto
- Propiedad etiqueta Servicios de Escritorio remoto, interfaz ITsSbTaskInfo
- Servicios de Escritorio remoto de la interfaz ITsSbTaskInfo, propiedad label
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Label
- ITsSbTaskInfo.get_Label
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1f85aaea366cf002d4ec1bacce8f29a6aa67fdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803781"
---
# <a name="itssbtaskinfolabel-property"></a><span data-ttu-id="c15d5-106">ITsSbTaskInfo:: Label (propiedad)</span><span class="sxs-lookup"><span data-stu-id="c15d5-106">ITsSbTaskInfo::Label property</span></span>

<span data-ttu-id="c15d5-107">Recupera la etiqueta que describe el propósito de la tarea.</span><span class="sxs-lookup"><span data-stu-id="c15d5-107">Retrieves the label that describes the purpose of the task.</span></span>

<span data-ttu-id="c15d5-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c15d5-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c15d5-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c15d5-109">Syntax</span></span>


```C++
HRESULT get_Label(
  [out, retval] BSTR *pLabel
);
```



## <a name="property-value"></a><span data-ttu-id="c15d5-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="c15d5-110">Property value</span></span>

<span data-ttu-id="c15d5-111">Un puntero a un valor **BSTR** que contiene la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="c15d5-111">A pointer to a **BSTR** value that contains the label.</span></span>

## <a name="requirements"></a><span data-ttu-id="c15d5-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c15d5-112">Requirements</span></span>



| <span data-ttu-id="c15d5-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c15d5-113">Requirement</span></span> | <span data-ttu-id="c15d5-114">Value</span><span class="sxs-lookup"><span data-stu-id="c15d5-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c15d5-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c15d5-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c15d5-116">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c15d5-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="c15d5-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c15d5-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c15d5-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c15d5-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="c15d5-119">IDL</span><span class="sxs-lookup"><span data-stu-id="c15d5-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c15d5-120"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c15d5-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c15d5-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="c15d5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c15d5-122">**ITsSbTaskInfo**</span><span class="sxs-lookup"><span data-stu-id="c15d5-122">**ITsSbTaskInfo**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> </dl>

 

 





