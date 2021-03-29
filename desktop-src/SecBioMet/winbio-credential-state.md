---
title: Enumeración WINBIO_CREDENTIAL_STATE (Winbio \_ Types. h)
description: Define valores que especifican si una credencial se ha asociado con los datos biométricos de un usuario final.
ms.assetid: c24f1771-7a1f-403e-8100-dfb3f4cd77a1
keywords:
- WINBIO_CREDENTIAL_STATE enumeración Plataforma de biometría de Windows API
- PWINBIO_CREDENTIAL_STATE de puntero de enumeración Plataforma de biometría de Windows API
topic_type:
- apiref
api_name:
- WINBIO_CREDENTIAL_STATE
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f8b8292cbbaefeeda0f6bf349f55e8f825f1756
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359683"
---
# <a name="winbio_credential_state-enumeration"></a><span data-ttu-id="3486c-105">\_Enumeración de estado de credenciales de WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="3486c-105">WINBIO\_CREDENTIAL\_STATE enumeration</span></span>

<span data-ttu-id="3486c-106">Define valores que especifican si una credencial se ha asociado con los datos biométricos de un usuario final.</span><span class="sxs-lookup"><span data-stu-id="3486c-106">Defines values that specify whether a credential has been associated with the biometric data for an end user.</span></span> <span data-ttu-id="3486c-107">Esta enumeración la usa la función [**WinBioGetCredentialState**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate) .</span><span class="sxs-lookup"><span data-stu-id="3486c-107">This enumeration is used by the [**WinBioGetCredentialState**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="3486c-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3486c-108">Syntax</span></span>


```C++
typedef enum _WINBIO_CREDENTIAL_STATE { 
  WINBIO_CREDENTIAL_NOT_SET  = 0x00000001,
  WINBIO_CREDENTIAL_SET      = 0x00000002
} WINBIO_CREDENTIAL_STATE, *PWINBIO_CREDENTIAL_STATE;
```



## <a name="constants"></a><span data-ttu-id="3486c-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="3486c-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="3486c-110"><span id="WINBIO_CREDENTIAL_NOT_SET"></span><span id="winbio_credential_not_set"></span>**\_credencial WINBIO \_ no \_ establecida**</span><span class="sxs-lookup"><span data-stu-id="3486c-110"><span id="WINBIO_CREDENTIAL_NOT_SET"></span><span id="winbio_credential_not_set"></span>**WINBIO\_CREDENTIAL\_NOT\_SET**</span></span>
</dt> <dd>

<span data-ttu-id="3486c-111">Se ha asociado una credencial con el usuario final.</span><span class="sxs-lookup"><span data-stu-id="3486c-111">A credential has been associated with the end user.</span></span>

</dd> <dt>

<span data-ttu-id="3486c-112"><span id="WINBIO_CREDENTIAL_SET"></span><span id="winbio_credential_set"></span>**\_conjunto de credenciales de WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="3486c-112"><span id="WINBIO_CREDENTIAL_SET"></span><span id="winbio_credential_set"></span>**WINBIO\_CREDENTIAL\_SET**</span></span>
</dt> <dd>

<span data-ttu-id="3486c-113">No se ha asociado ninguna credencial con el usuario final.</span><span class="sxs-lookup"><span data-stu-id="3486c-113">A credential has not been associated with the end user.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3486c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3486c-114">Requirements</span></span>



| <span data-ttu-id="3486c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3486c-115">Requirement</span></span> | <span data-ttu-id="3486c-116">Value</span><span class="sxs-lookup"><span data-stu-id="3486c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3486c-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3486c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3486c-118">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="3486c-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="3486c-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3486c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3486c-120">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="3486c-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="3486c-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3486c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3486c-122"><dt>Winbio \_ Types. h (incluye Winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3486c-122"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3486c-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="3486c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3486c-124">Enumeraciones de aplicación cliente</span><span class="sxs-lookup"><span data-stu-id="3486c-124">Client Application Enumerations</span></span>](client-application-enumerations.md)
</dt> <dt>

[<span data-ttu-id="3486c-125">**WinBioGetCredentialState**</span><span class="sxs-lookup"><span data-stu-id="3486c-125">**WinBioGetCredentialState**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)
</dt> </dl>

 

 





