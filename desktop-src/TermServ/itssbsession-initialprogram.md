---
title: Propiedad InitialProgram de ITsSbSession
description: Recupera o especifica el programa inicial para esta sesión.
ms.assetid: c299c4f7-3c5f-468f-9fc7-81eac322dfa2
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad InitialProgram
- Propiedad InitialProgram Servicios de Escritorio remoto, interfaz ITsSbSession
- Servicios de Escritorio remoto de la interfaz ITsSbSession, propiedad InitialProgram
topic_type:
- apiref
api_name:
- ITsSbSession.InitialProgram
- ITsSbSession.get_InitialProgram
- ITsSbSession.put_InitialProgram
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 307f8bb4330caf4b84b8650c9ccc2551c94da76d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490619"
---
# <a name="itssbsessioninitialprogram-property"></a><span data-ttu-id="321c2-106">ITsSbSession:: InitialProgram (propiedad)</span><span class="sxs-lookup"><span data-stu-id="321c2-106">ITsSbSession::InitialProgram property</span></span>

<span data-ttu-id="321c2-107">Recupera o especifica el programa inicial para esta sesión.</span><span class="sxs-lookup"><span data-stu-id="321c2-107">Retrieves or specifies the initial program for this session.</span></span> <span data-ttu-id="321c2-108">El programa inicial es el programa que se inicia cuando se inicia la sesión de usuario.</span><span class="sxs-lookup"><span data-stu-id="321c2-108">The initial program is the program that is launched when the user session starts.</span></span>

<span data-ttu-id="321c2-109">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="321c2-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="321c2-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="321c2-110">Syntax</span></span>


```C++
HRESULT put_InitialProgram(
  [in]          BSTR Application
);

HRESULT get_InitialProgram(
  [out, retval] BSTR *app
);
```



## <a name="property-value"></a><span data-ttu-id="321c2-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="321c2-111">Property value</span></span>

<span data-ttu-id="321c2-112">Variable **BSTR** que contiene el programa inicial.</span><span class="sxs-lookup"><span data-stu-id="321c2-112">A **BSTR** variable that contains the initial program.</span></span>

## <a name="requirements"></a><span data-ttu-id="321c2-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="321c2-113">Requirements</span></span>



| <span data-ttu-id="321c2-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="321c2-114">Requirement</span></span> | <span data-ttu-id="321c2-115">Value</span><span class="sxs-lookup"><span data-stu-id="321c2-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="321c2-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="321c2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="321c2-117">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="321c2-117">None supported</span></span><br/>                                                            |
| <span data-ttu-id="321c2-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="321c2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="321c2-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="321c2-119">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="321c2-120">IDL</span><span class="sxs-lookup"><span data-stu-id="321c2-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="321c2-121"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="321c2-121"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="321c2-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="321c2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="321c2-123">**ITsSbSession**</span><span class="sxs-lookup"><span data-stu-id="321c2-123">**ITsSbSession**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





