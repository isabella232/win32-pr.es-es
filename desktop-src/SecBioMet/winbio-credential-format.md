---
title: Enumeración WINBIO_CREDENTIAL_FORMAT (Winbio \_ Types. h)
description: Define las marcas que se pueden usar para especificar el formato de credenciales de usuario final.
ms.assetid: f107e000-98a2-44f0-aa5e-d13b5d9c8d43
keywords:
- WINBIO_CREDENTIAL_FORMAT enumeración Plataforma de biometría de Windows API
topic_type:
- apiref
api_name:
- WINBIO_CREDENTIAL_FORMAT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa28ea56c7af9f78947e64587740300a70f763ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150291"
---
# <a name="winbio_credential_format-enumeration"></a><span data-ttu-id="bc87b-104">\_Enumeración del formato de credenciales WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="bc87b-104">WINBIO\_CREDENTIAL\_FORMAT enumeration</span></span>

<span data-ttu-id="bc87b-105">Define las marcas que se pueden usar para especificar el formato de credenciales de usuario final.</span><span class="sxs-lookup"><span data-stu-id="bc87b-105">Defines flags that can be used to specify the end-user credential format.</span></span> <span data-ttu-id="bc87b-106">Esta enumeración la usa la función [**WinBioSetCredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential) .</span><span class="sxs-lookup"><span data-stu-id="bc87b-106">This enumeration is used by the [**WinBioSetCredential**](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc87b-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bc87b-107">Syntax</span></span>


```C++
typedef enum _WINBIO_CREDENTIAL_FORMAT { 
  WINBIO_PASSWORD_GENERIC    = 0x00000001,
  WINBIO_PASSWORD_PACKED     = 0x00000002,
  WINBIO_PASSWORD_PROTECTED  = 0x00000003
} WINBIO_CREDENTIAL_FORMAT;
```



## <a name="constants"></a><span data-ttu-id="bc87b-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="bc87b-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="bc87b-109"><span id="WINBIO_PASSWORD_GENERIC"></span><span id="winbio_password_generic"></span>**WINBIO \_ contraseña \_ genérica**</span><span class="sxs-lookup"><span data-stu-id="bc87b-109"><span id="WINBIO_PASSWORD_GENERIC"></span><span id="winbio_password_generic"></span>**WINBIO\_PASSWORD\_GENERIC**</span></span>
</dt> <dd>

<span data-ttu-id="bc87b-110">La contraseña está en un formato genérico.</span><span class="sxs-lookup"><span data-stu-id="bc87b-110">The password is in a generic format.</span></span>

</dd> <dt>

<span data-ttu-id="bc87b-111"><span id="WINBIO_PASSWORD_PACKED"></span><span id="winbio_password_packed"></span>**contraseña de WINBIO \_ \_ empaquetada**</span><span class="sxs-lookup"><span data-stu-id="bc87b-111"><span id="WINBIO_PASSWORD_PACKED"></span><span id="winbio_password_packed"></span>**WINBIO\_PASSWORD\_PACKED**</span></span>
</dt> <dd>

<span data-ttu-id="bc87b-112">La contraseña está en un formato comprimido.</span><span class="sxs-lookup"><span data-stu-id="bc87b-112">The password is in a compressed format.</span></span>

</dd> <dt>

<span data-ttu-id="bc87b-113"><span id="WINBIO_PASSWORD_PROTECTED"></span><span id="winbio_password_protected"></span>**WINBIO \_ contraseña \_ protegida**</span><span class="sxs-lookup"><span data-stu-id="bc87b-113"><span id="WINBIO_PASSWORD_PROTECTED"></span><span id="winbio_password_protected"></span>**WINBIO\_PASSWORD\_PROTECTED**</span></span>
</dt> <dd>

<span data-ttu-id="bc87b-114">La credencial de contraseña se incluyó con [**CredProtect**](/windows/desktop/api/wincred/nf-wincred-credprotecta).</span><span class="sxs-lookup"><span data-stu-id="bc87b-114">The password credential was wrapped with [**CredProtect**](/windows/desktop/api/wincred/nf-wincred-credprotecta).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bc87b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc87b-115">Requirements</span></span>



| <span data-ttu-id="bc87b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc87b-116">Requirement</span></span> | <span data-ttu-id="bc87b-117">Value</span><span class="sxs-lookup"><span data-stu-id="bc87b-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc87b-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc87b-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bc87b-119">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="bc87b-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                                  |
| <span data-ttu-id="bc87b-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bc87b-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bc87b-121">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="bc87b-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="bc87b-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="bc87b-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc87b-123"><dt>Winbio \_ Types. h (incluye Winbio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bc87b-123"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc87b-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="bc87b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc87b-125">Enumeraciones de aplicación cliente</span><span class="sxs-lookup"><span data-stu-id="bc87b-125">Client Application Enumerations</span></span>](client-application-enumerations.md)
</dt> <dt>

[<span data-ttu-id="bc87b-126">**WinBioSetCredential**</span><span class="sxs-lookup"><span data-stu-id="bc87b-126">**WinBioSetCredential**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiosetcredential)
</dt> </dl>

 

