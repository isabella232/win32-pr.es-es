---
description: Recupera la colección de números de aviso de usuario.
ms.assetid: 5db38a53-e71b-4e80-9374-69b0c044fbc5
title: Propiedad Qualifier. NoticeNumbers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier.NoticeNumbers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2ef9b2c4c70e011cc33f0aa9d9f2bbcc9f530bec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649878"
---
# <a name="qualifiernoticenumbers-property"></a><span data-ttu-id="ca033-103">Propiedad Qualifier. NoticeNumbers</span><span class="sxs-lookup"><span data-stu-id="ca033-103">Qualifier.NoticeNumbers property</span></span>

<span data-ttu-id="ca033-104">\[La propiedad **NoticeNumbers** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="ca033-104">\[The **NoticeNumbers** property is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ca033-105">En su lugar, use la [**clase X509Extension**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) llamando al constructor que toma un OID como parámetro y, a continuación, use el OID para las directivas de certificado para procesar calificadores que formen parte de la información de directivas en la extensión de directivas de certificado.\]</span><span class="sxs-lookup"><span data-stu-id="ca033-105">Instead, use the [**X509Extension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace by calling the constructor that takes an OID as a parameter, and then use the OID for Certificate Policies to process qualifiers that are part of the policy information in the Certificate Policies extension.\]</span></span>

<span data-ttu-id="ca033-106">La propiedad **NoticeNumbers** recupera la colección de números de aviso de usuario.</span><span class="sxs-lookup"><span data-stu-id="ca033-106">The **NoticeNumbers** property retrieves the collection of user notice numbers.</span></span> <span data-ttu-id="ca033-107">Esta propiedad puede estar vacía.</span><span class="sxs-lookup"><span data-stu-id="ca033-107">This property may be empty.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca033-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ca033-108">Syntax</span></span>


```VB
Qualifier.NoticeNumbers As NoticeNumbers
```



## <a name="property-value"></a><span data-ttu-id="ca033-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ca033-109">Property value</span></span>

<span data-ttu-id="ca033-110">La colección de números de aviso de usuario.</span><span class="sxs-lookup"><span data-stu-id="ca033-110">The collection of user notice numbers.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca033-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca033-111">Requirements</span></span>



| <span data-ttu-id="ca033-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca033-112">Requirement</span></span> | <span data-ttu-id="ca033-113">Value</span><span class="sxs-lookup"><span data-stu-id="ca033-113">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ca033-114">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="ca033-114">Redistributable</span></span><br/> | <span data-ttu-id="ca033-115">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="ca033-115">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="ca033-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ca033-116">DLL</span></span><br/>             | <dl> <span data-ttu-id="ca033-117"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca033-117"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca033-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="ca033-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca033-119">**Qualifier**</span><span class="sxs-lookup"><span data-stu-id="ca033-119">**Qualifier**</span></span>](qualifier.md)
</dt> </dl>

 

 
