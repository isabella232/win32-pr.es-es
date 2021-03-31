---
title: Estructura de WINBIO_ACCOUNT_POLICY (Winbio \_ Adapter. h)
description: Contiene una directiva de suplantación predeterminada o específica de la cuenta.
ms.assetid: 7098FC53-E487-42B2-8B4B-EB7E2D296CB6
keywords:
- Plataforma de biometría de Windows API de WINBIO_ACCOUNT_POLICY Structure
- PWINBIO_ACCOUNT_POLICY de puntero de estructura Plataforma de biometría de Windows API
topic_type:
- apiref
api_name:
- WINBIO_ACCOUNT_POLICY
api_location:
- Winbio_adapter.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c734fa6d98615b7708a65ebad1dddc47cdc77cc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996387"
---
# <a name="winbio_account_policy-structure"></a><span data-ttu-id="37953-105">WINBIO \_ estructura de directiva de cuenta \_</span><span class="sxs-lookup"><span data-stu-id="37953-105">WINBIO\_ACCOUNT\_POLICY structure</span></span>

<span data-ttu-id="37953-106">La estructura de **\_ \_ Directiva de cuenta WINBIO** contiene una directiva de suplantación predeterminada o específica de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="37953-106">The **WINBIO\_ACCOUNT\_POLICY** structure contains either a default or account-specific antispoofing policy.</span></span>

## <a name="syntax"></a><span data-ttu-id="37953-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="37953-107">Syntax</span></span>


```C++
typedef struct _WINBIO_ACCOUNT_POLICY {
  WINBIO_IDENTITY                 Identity;
  WINBIO_ANTI_SPOOF_POLICY_ACTION AntiSpoofBehavior;
} WINBIO_ACCOUNT_POLICY, *PWINBIO_ACCOUNT_POLICY;
```



## <a name="members"></a><span data-ttu-id="37953-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="37953-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="37953-109">**Identidad**</span><span class="sxs-lookup"><span data-stu-id="37953-109">**Identity**</span></span>
</dt> <dd>

<span data-ttu-id="37953-110">Estructura [**de \_ identidad de WINBIO**](winbio-identity.md) que especifica la información de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="37953-110">A [**WINBIO\_IDENTITY**](winbio-identity.md) structure that specifies the account information.</span></span>

</dd> <dt>

<span data-ttu-id="37953-111">**AntiSpoofBehavior**</span><span class="sxs-lookup"><span data-stu-id="37953-111">**AntiSpoofBehavior**</span></span>
</dt> <dd>

<span data-ttu-id="37953-112">Uno de los valores de enumeración de [**acciones de directiva de WINBIO \_ anti \_ \_ \_ Spoofing**](winbio-anti-spoof-policy-action.md) que especifica qué acción de directiva de suplantación debe usar para la cuenta.</span><span class="sxs-lookup"><span data-stu-id="37953-112">One of the [**WINBIO\_ANTI\_SPOOF\_POLICY\_ACTION**](winbio-anti-spoof-policy-action.md) enumeration values that specifies what antispoofing policy action to use for the account.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="37953-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="37953-113">Remarks</span></span>

<span data-ttu-id="37953-114">Vea la explicación del método [**EngineAdapterSetAccountPolicy**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_account_policy_fn) para obtener una descripción de cómo se usa esta estructura.</span><span class="sxs-lookup"><span data-stu-id="37953-114">See the discussion of the [**EngineAdapterSetAccountPolicy**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_account_policy_fn) method for a description of how this structure is used.</span></span>

## <a name="requirements"></a><span data-ttu-id="37953-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37953-115">Requirements</span></span>



| <span data-ttu-id="37953-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="37953-116">Requirement</span></span> | <span data-ttu-id="37953-117">Value</span><span class="sxs-lookup"><span data-stu-id="37953-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37953-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37953-118">Minimum supported client</span></span><br/> | <span data-ttu-id="37953-119">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="37953-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="37953-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37953-120">Minimum supported server</span></span><br/> | <span data-ttu-id="37953-121">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="37953-121">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                     |
| <span data-ttu-id="37953-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="37953-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="37953-123"><dt>Winbio \_ Adapter. h (incluir Winbio \_ Adapter. h)</dt></span><span class="sxs-lookup"><span data-stu-id="37953-123"><dt>Winbio\_adapter.h (include Winbio\_adapter.h)</dt></span></span> </dl> |



 

 





