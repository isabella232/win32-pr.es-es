---
title: Propiedad de nombre de usuario ITsSbSession
description: Recupera el nombre de usuario para esta sesión.
ms.assetid: 0034e8cc-b67b-4e30-a059-47a269bab0fd
ms.tgt_platform: multiple
keywords:
- Propiedad username Servicios de Escritorio remoto
- Propiedad username Servicios de Escritorio remoto, interfaz ITsSbSession
- Servicios de Escritorio remoto de la interfaz ITsSbSession, propiedad username
topic_type:
- apiref
api_name:
- ITsSbSession.Username
- ITsSbSession.get_Username
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5fb66f0639d659fcb6800680ffc3b3486ad12b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676972"
---
# <a name="itssbsessionusername-property"></a><span data-ttu-id="1de17-106">ITsSbSession:: username (propiedad)</span><span class="sxs-lookup"><span data-stu-id="1de17-106">ITsSbSession::Username property</span></span>

<span data-ttu-id="1de17-107">Recupera el nombre de usuario para esta sesión.</span><span class="sxs-lookup"><span data-stu-id="1de17-107">Retrieves the user name for this session.</span></span>

<span data-ttu-id="1de17-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="1de17-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="1de17-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1de17-109">Syntax</span></span>


```C++
HRESULT get_Username(
  [out, retval] BSTR *userName
);
```



## <a name="property-value"></a><span data-ttu-id="1de17-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="1de17-110">Property value</span></span>

<span data-ttu-id="1de17-111">Un puntero a una variable **BSTR** que recibe el nombre de usuario para esta sesión.</span><span class="sxs-lookup"><span data-stu-id="1de17-111">A pointer to a **BSTR** variable that receives the user name for this session.</span></span>

## <a name="requirements"></a><span data-ttu-id="1de17-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1de17-112">Requirements</span></span>



| <span data-ttu-id="1de17-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="1de17-113">Requirement</span></span> | <span data-ttu-id="1de17-114">Value</span><span class="sxs-lookup"><span data-stu-id="1de17-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1de17-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1de17-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1de17-116">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="1de17-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="1de17-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1de17-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1de17-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1de17-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="1de17-119">IDL</span><span class="sxs-lookup"><span data-stu-id="1de17-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1de17-120"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1de17-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1de17-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="1de17-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1de17-122">**ITsSbSession**</span><span class="sxs-lookup"><span data-stu-id="1de17-122">**ITsSbSession**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





