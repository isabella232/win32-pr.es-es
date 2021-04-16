---
description: Recupera un valor booleano que indica si el certificado es para una entidad de certificación (CA).
ms.assetid: 3ca43475-fe97-4eb4-875d-dbc15a0b953c
title: Propiedad BasicConstraints. IsCertificateAuthority
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints.IsCertificateAuthority
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5d4878a8cb21f89f3abeeb9e4b530948ef12e9aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671413"
---
# <a name="basicconstraintsiscertificateauthority-property"></a><span data-ttu-id="13564-103">Propiedad BasicConstraints. IsCertificateAuthority</span><span class="sxs-lookup"><span data-stu-id="13564-103">BasicConstraints.IsCertificateAuthority property</span></span>

<span data-ttu-id="13564-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="13564-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="13564-105">En su lugar, use la [**clase X509BasicConstraintsExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/previous-versions/windows/) .\]</span><span class="sxs-lookup"><span data-stu-id="13564-105">Instead, use the [**X509BasicConstraintsExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="13564-106">La propiedad **IsCertificateAuthority** recupera un valor booleano que indica si el certificado es para una [*entidad de certificación*](../secgloss/c-gly.md) (CA).</span><span class="sxs-lookup"><span data-stu-id="13564-106">The **IsCertificateAuthority** property retrieves a Boolean value that indicates whether the certificate is for a [*certification authority*](../secgloss/c-gly.md) (CA).</span></span>

<span data-ttu-id="13564-107">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="13564-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="13564-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="13564-108">Syntax</span></span>


```VB
BasicConstraints.IsCertificateAuthority As Boolean
```



## <a name="property-value"></a><span data-ttu-id="13564-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="13564-109">Property value</span></span>

<span data-ttu-id="13564-110">Si es **true**, el certificado solo lo usará una CA.</span><span class="sxs-lookup"><span data-stu-id="13564-110">If **True**, the certificate is to be used only by a CA.</span></span>

## <a name="requirements"></a><span data-ttu-id="13564-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13564-111">Requirements</span></span>



| <span data-ttu-id="13564-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="13564-112">Requirement</span></span> | <span data-ttu-id="13564-113">Value</span><span class="sxs-lookup"><span data-stu-id="13564-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="13564-114">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="13564-114">End of client support</span></span><br/> | <span data-ttu-id="13564-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="13564-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="13564-116">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="13564-116">End of server support</span></span><br/> | <span data-ttu-id="13564-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="13564-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="13564-118">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="13564-118">Redistributable</span></span><br/>       | <span data-ttu-id="13564-119">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="13564-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="13564-120">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="13564-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="13564-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13564-121"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
