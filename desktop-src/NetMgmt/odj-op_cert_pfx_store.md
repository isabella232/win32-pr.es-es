---
title: OP_CERT_PFX_STORE
description: Definición de OP_CERT_PFX_STORE IDL
ms.assetid: 10773feb-623c-4256-a973-f006ed66d936
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: b07d0b8e5572763cc42fe2f5b19a4dde2cfe2157
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/14/2020
ms.locfileid: "105720190"
---
# <a name="op_cert_pfx_store-structure"></a><span data-ttu-id="82026-103">Estructura de OP_CERT_PFX_STORE</span><span class="sxs-lookup"><span data-stu-id="82026-103">OP_CERT_PFX_STORE structure</span></span>

<span data-ttu-id="82026-104">Contiene una estructura PFX serializada.</span><span class="sxs-lookup"><span data-stu-id="82026-104">Contains a serialized PFX structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="82026-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="82026-105">Syntax</span></span>

```C++
typedef struct _OP_CERT_PFX_STORE
{
    [string] wchar_t            *pTemplateName;
    ULONG                       ulPrivateKeyExportPolicy;
    [string] wchar_t            *pPolicyServerUrl;
    ULONG                       ulPolicyServerUrlFlags;
    [string] wchar_t            *pPolicyServerId;
    ULONG                       cbPfx;
    [size_is(cbPfx)]    PBYTE   pPfx;
} OP_CERT_PFX_STORE, *POP_CERT_PFX_STORE;
```

## <a name="members"></a><span data-ttu-id="82026-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="82026-106">Members</span></span>

### <a name="ptemplatename"></a><span data-ttu-id="82026-107">pTemplateName</span><span class="sxs-lookup"><span data-stu-id="82026-107">pTemplateName</span></span>

<span data-ttu-id="82026-108">Debe establecerse en el nombre de la plantilla de certificado que se usa para crear el certificado.</span><span class="sxs-lookup"><span data-stu-id="82026-108">Must be set to the name of the certificate template used to create the certificate.</span></span>

### <a name="ulprivatekeyexportpolicy"></a><span data-ttu-id="82026-109">ulPrivateKeyExportPolicy</span><span class="sxs-lookup"><span data-stu-id="82026-109">ulPrivateKeyExportPolicy</span></span>

<span data-ttu-id="82026-110">Contiene un valor de la enumeración [**X509PrivateKeyExportFlags**](/windows/win32/api/certenroll/ne-certenroll-x509privatekeyexportflags) .</span><span class="sxs-lookup"><span data-stu-id="82026-110">Contains one value from the [**X509PrivateKeyExportFlags**](/windows/win32/api/certenroll/ne-certenroll-x509privatekeyexportflags) enumeration.</span></span>

### <a name="ppolicyserverurl"></a><span data-ttu-id="82026-111">pPolicyServerUrl</span><span class="sxs-lookup"><span data-stu-id="82026-111">pPolicyServerUrl</span></span>

<span data-ttu-id="82026-112">Debe establecer la dirección URL del servidor de directivas.</span><span class="sxs-lookup"><span data-stu-id="82026-112">Must be set the URL of the policy server.</span></span>

### <a name="ulpolicyserverurlflags"></a><span data-ttu-id="82026-113">ulPolicyServerUrlFlags</span><span class="sxs-lookup"><span data-stu-id="82026-113">ulPolicyServerUrlFlags</span></span>

<span data-ttu-id="82026-114">Contiene un valor de la enumeración [**PolicyServerUrlFlags**](/windows/win32/api/certenroll/ne-certenroll-policyserverurlflags) .</span><span class="sxs-lookup"><span data-stu-id="82026-114">Contains one value from the [**PolicyServerUrlFlags**](/windows/win32/api/certenroll/ne-certenroll-policyserverurlflags) enumeration.</span></span>

### <a name="ppolicyserverid"></a><span data-ttu-id="82026-115">pPolicyServerId</span><span class="sxs-lookup"><span data-stu-id="82026-115">pPolicyServerId</span></span>

<span data-ttu-id="82026-116">Contiene una cadena que identifica de forma única el servidor de directivas</span><span class="sxs-lookup"><span data-stu-id="82026-116">Contains a string that uniquely identifies the policy server</span></span>

### <a name="cbpfx"></a><span data-ttu-id="82026-117">cbPfx</span><span class="sxs-lookup"><span data-stu-id="82026-117">cbPfx</span></span>

<span data-ttu-id="82026-118">Contiene el tamaño de pPfx en bytes.</span><span class="sxs-lookup"><span data-stu-id="82026-118">Contains the size of pPfx in bytes.</span></span>

### <a name="ppfx"></a><span data-ttu-id="82026-119">pPfx</span><span class="sxs-lookup"><span data-stu-id="82026-119">pPfx</span></span>

<span data-ttu-id="82026-120">Contiene una estructura PFX serializada (consulte [**RFC 7292**](https://tools.ietf.org/html/rfc7292)).</span><span class="sxs-lookup"><span data-stu-id="82026-120">Contains a serialized PFX structure (see [**RFC 7292**](https://tools.ietf.org/html/rfc7292)).</span></span>

## <a name="see-also"></a><span data-ttu-id="82026-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="82026-121">See also</span></span>

[<span data-ttu-id="82026-122">**Definiciones IDL de unión a dominio sin conexión**</span><span class="sxs-lookup"><span data-stu-id="82026-122">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)
