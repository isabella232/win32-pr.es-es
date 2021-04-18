---
description: Recupera el nombre del proveedor de servicios criptográficos (CSP).
ms.assetid: b06d2839-0eaa-4f3f-99f7-d77e001fe4ea
title: Propiedad PrivateKey. ProviderName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.ProviderName
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 528117db072b80ab6d9203b8b2fc2786175499ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671663"
---
# <a name="privatekeyprovidername-property"></a><span data-ttu-id="3a2e1-103">Propiedad PrivateKey. ProviderName</span><span class="sxs-lookup"><span data-stu-id="3a2e1-103">PrivateKey.ProviderName property</span></span>

<span data-ttu-id="3a2e1-104">\[La propiedad **providerName** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="3a2e1-104">\[The **ProviderName** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="3a2e1-105">En su lugar, use la [**propiedad X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="3a2e1-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="3a2e1-106">La propiedad **providerName** recupera el nombre del proveedor de [*servicios criptográficos*](../secgloss/c-gly.md) (CSP).</span><span class="sxs-lookup"><span data-stu-id="3a2e1-106">The **ProviderName** property retrieves the name of the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

## <a name="syntax"></a><span data-ttu-id="3a2e1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3a2e1-107">Syntax</span></span>


```VB
PrivateKey.ProviderName As String
```



## <a name="property-value"></a><span data-ttu-id="3a2e1-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="3a2e1-108">Property value</span></span>

<span data-ttu-id="3a2e1-109">Cadena que contiene el nombre del CSP.</span><span class="sxs-lookup"><span data-stu-id="3a2e1-109">A string that contains the name of the CSP.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a2e1-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a2e1-110">Requirements</span></span>



| <span data-ttu-id="3a2e1-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a2e1-111">Requirement</span></span> | <span data-ttu-id="3a2e1-112">Value</span><span class="sxs-lookup"><span data-stu-id="3a2e1-112">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a2e1-113">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="3a2e1-113">Redistributable</span></span><br/> | <span data-ttu-id="3a2e1-114">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="3a2e1-114">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="3a2e1-115">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3a2e1-115">DLL</span></span><br/>             | <dl> <span data-ttu-id="3a2e1-116"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a2e1-116"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a2e1-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="3a2e1-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a2e1-118">**PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="3a2e1-118">**PrivateKey**</span></span>](privatekey.md)
</dt> </dl>

 

 
