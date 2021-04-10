---
description: Especifica un certificado de editor de software (SPC) y una cadena de certificados que se usan para firmar un documento.
ms.assetid: b65b4129-df92-410c-b372-b0c004f8bb03
title: Estructura de SIGNER_SPC_CHAIN_INFO
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_SPC_CHAIN_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 60279a60e6cdfbf43a1e2d9c45735b885d97a055
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156496"
---
# <a name="signer_spc_chain_info-structure"></a><span data-ttu-id="4fd7c-103">Estructura de \_ \_ información de cadena SPC de firmante \_</span><span class="sxs-lookup"><span data-stu-id="4fd7c-103">SIGNER\_SPC\_CHAIN\_INFO structure</span></span>

<span data-ttu-id="4fd7c-104">La estructura de **\_ \_ \_ información de cadena SPC del firmante** especifica un certificado de editor de [*software*](../secgloss/s-gly.md) (SPC) y una cadena de certificados que se usan para firmar un documento.</span><span class="sxs-lookup"><span data-stu-id="4fd7c-104">The **SIGNER\_SPC\_CHAIN\_INFO** structure specifies a [*Software Publisher Certificate*](../secgloss/s-gly.md) (SPC) and certificate chain used to sign a document.</span></span>

> [!Note]  
> <span data-ttu-id="4fd7c-105">Esta estructura no está definida en ningún archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="4fd7c-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="4fd7c-106">Para usar esta estructura, debe definirla usted mismo tal como se muestra en este tema.</span><span class="sxs-lookup"><span data-stu-id="4fd7c-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="4fd7c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4fd7c-107">Syntax</span></span>


```C++
typedef struct _SIGNER_SPC_CHAIN_INFO {
  DWORD      cbSize;
  LPCWSTR    pwszSpcFile;
  DWORD      dwCertPolicy;
  HCERTSTORE hCertStore;
} SIGNER_SPC_CHAIN_INFO, *PSIGNER_SPC_CHAIN_INFO;
```



## <a name="members"></a><span data-ttu-id="4fd7c-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="4fd7c-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="4fd7c-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="4fd7c-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="4fd7c-110">Tamaño de la estructura, en bytes.</span><span class="sxs-lookup"><span data-stu-id="4fd7c-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="4fd7c-111">**pwszSpcFile**</span><span class="sxs-lookup"><span data-stu-id="4fd7c-111">**pwszSpcFile**</span></span>
</dt> <dd>

<span data-ttu-id="4fd7c-112">Nombre del archivo SPC que se va a utilizar para firmar un documento.</span><span class="sxs-lookup"><span data-stu-id="4fd7c-112">The name of the SPC file to use to sign a document.</span></span>

</dd> <dt>

<span data-ttu-id="4fd7c-113">**dwCertPolicy**</span><span class="sxs-lookup"><span data-stu-id="4fd7c-113">**dwCertPolicy**</span></span>
</dt> <dd>

<span data-ttu-id="4fd7c-114">Especifica cómo se agregan los certificados a la firma.</span><span class="sxs-lookup"><span data-stu-id="4fd7c-114">Specifies how certificates are added to the signature.</span></span> <span data-ttu-id="4fd7c-115">Para encontrar la cadena de certificados, se comprueban los almacenes mis, CA, raíz y SPC, además del almacén especificado por el miembro **hCertStore** .</span><span class="sxs-lookup"><span data-stu-id="4fd7c-115">To find the certificate chain, the MY, CA, ROOT, and SPC stores, in addition to the store specified by the **hCertStore** member, are checked.</span></span> <span data-ttu-id="4fd7c-116">Este miembro puede ser uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="4fd7c-116">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="4fd7c-117">Value</span><span class="sxs-lookup"><span data-stu-id="4fd7c-117">Value</span></span>                                                                                                                                                                                                                                                                                   | <span data-ttu-id="4fd7c-118">Significado</span><span class="sxs-lookup"><span data-stu-id="4fd7c-118">Meaning</span></span>                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIGNER_CERT_POLICY_CHAIN"></span><span id="signer_cert_policy_chain"></span><dl> <span data-ttu-id="4fd7c-119"><dt>**Firmante \_ \_ \_ Cadena de directiva de certificado**</dt> <dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="4fd7c-119"><dt>**SIGNER\_CERT\_POLICY\_CHAIN**</dt> <dt>2 (0x2)</dt></span></span> </dl>                           | <span data-ttu-id="4fd7c-120">Agregue solo certificados en la cadena de certificados.</span><span class="sxs-lookup"><span data-stu-id="4fd7c-120">Add only certificates in the certificate chain.</span></span><br/>                                                                                                                                |
| <span id="SIGNER_CERT_POLICY_CHAIN_NO_ROOT"></span><span id="signer_cert_policy_chain_no_root"></span><dl> <span data-ttu-id="4fd7c-121"><dt>**Firmante \_ Cadena de directiva de certificado \_ \_ \_ sin \_ raíz**</dt> <dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="4fd7c-121"><dt>**SIGNER\_CERT\_POLICY\_CHAIN\_NO\_ROOT**</dt> <dt>8 (0x8)</dt></span></span> </dl> | <span data-ttu-id="4fd7c-122">Agregue solo certificados en la cadena de certificados, excluido el certificado raíz.</span><span class="sxs-lookup"><span data-stu-id="4fd7c-122">Add only certificates in the certificate chain, excluding the root certificate.</span></span><br/>                                                                                                |
| <span id="SIGNER_CERT_POLICY_STORE"></span><span id="signer_cert_policy_store"></span><dl> <span data-ttu-id="4fd7c-123"><dt>**Firmante \_ \_ \_ Almacén de directivas de certificado**</dt> <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="4fd7c-123"><dt>**SIGNER\_CERT\_POLICY\_STORE**</dt> <dt>1 (0x1)</dt></span></span> </dl>                           | <span data-ttu-id="4fd7c-124">Agregue todos los certificados en el almacén especificado por el miembro **hCertStore** .</span><span class="sxs-lookup"><span data-stu-id="4fd7c-124">Add all certificates in the store specified by the **hCertStore** member.</span></span> <span data-ttu-id="4fd7c-125">Esta marca puede ser **una combinación OR bit a bit** con cualquiera de los otros valores posibles para este miembro.</span><span class="sxs-lookup"><span data-stu-id="4fd7c-125">This flag can be a bitwise-**OR** combination with any of the other possible values for this member.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4fd7c-126">**hCertStore**</span><span class="sxs-lookup"><span data-stu-id="4fd7c-126">**hCertStore**</span></span>
</dt> <dd>

<span data-ttu-id="4fd7c-127">Opcional.</span><span class="sxs-lookup"><span data-stu-id="4fd7c-127">Optional.</span></span> <span data-ttu-id="4fd7c-128">Identificador de un almacén de certificados adicional.</span><span class="sxs-lookup"><span data-stu-id="4fd7c-128">A handle to an additional certificate store.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4fd7c-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4fd7c-129">Requirements</span></span>



| <span data-ttu-id="4fd7c-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="4fd7c-130">Requirement</span></span> | <span data-ttu-id="4fd7c-131">Value</span><span class="sxs-lookup"><span data-stu-id="4fd7c-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4fd7c-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4fd7c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="4fd7c-133">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="4fd7c-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="4fd7c-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4fd7c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="4fd7c-135">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="4fd7c-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4fd7c-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="4fd7c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fd7c-137">**certificado del firmante \_**</span><span class="sxs-lookup"><span data-stu-id="4fd7c-137">**SIGNER\_CERT**</span></span>](signer-cert.md)
</dt> </dl>

 

 
