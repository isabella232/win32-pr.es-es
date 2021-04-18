---
description: Importa un certificado previamente codificado de una cadena en el objeto de certificado.
ms.assetid: 8515e034-08aa-4575-9b96-34cdee3ccba8
title: 'ICertificate2:: Import (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Import
- ICertificate2.Import
- ICertificate.Import
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ea639f1cd89b673ecf8da77302e3d812894a202b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670657"
---
# <a name="icertificate2import-method"></a><span data-ttu-id="fc02b-103">ICertificate2:: Import (método)</span><span class="sxs-lookup"><span data-stu-id="fc02b-103">ICertificate2::Import method</span></span>

<span data-ttu-id="fc02b-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fc02b-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="fc02b-105">En su lugar, use la [**clase X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="fc02b-105">Instead, use the [**X509Certificate2 Class**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="fc02b-106">El método **Import** importa un certificado previamente codificado de una cadena en el objeto de [**certificado**](certificate.md) .</span><span class="sxs-lookup"><span data-stu-id="fc02b-106">The **Import** method imports a previously encoded certificate from a string into the [**Certificate**](certificate.md) object.</span></span> <span data-ttu-id="fc02b-107">Al llamar a este método, se restablece el [*Estado*](../secgloss/s-gly.md) de este objeto.</span><span class="sxs-lookup"><span data-stu-id="fc02b-107">Calling this method resets the [*state*](../secgloss/s-gly.md) of this object.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc02b-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fc02b-108">Syntax</span></span>


```VB
Certificate.Import( _
  ByVal EncodedCertificate _
)
```



## <a name="parameters"></a><span data-ttu-id="fc02b-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fc02b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc02b-110">*EncodedCertificate* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="fc02b-110">*EncodedCertificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc02b-111">Cadena que contiene los datos del certificado codificados que se van a importar.</span><span class="sxs-lookup"><span data-stu-id="fc02b-111">A string that contains the encoded certificate data to be imported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc02b-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fc02b-112">Return value</span></span>

<span data-ttu-id="fc02b-113">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="fc02b-113">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc02b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc02b-114">Requirements</span></span>



| <span data-ttu-id="fc02b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc02b-115">Requirement</span></span> | <span data-ttu-id="fc02b-116">Value</span><span class="sxs-lookup"><span data-stu-id="fc02b-116">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc02b-117">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="fc02b-117">End of client support</span></span><br/> | <span data-ttu-id="fc02b-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fc02b-118">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="fc02b-119">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="fc02b-119">End of server support</span></span><br/> | <span data-ttu-id="fc02b-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fc02b-120">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="fc02b-121">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="fc02b-121">Redistributable</span></span><br/>       | <span data-ttu-id="fc02b-122">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="fc02b-122">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="fc02b-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fc02b-123">DLL</span></span><br/>                   | <dl> <span data-ttu-id="fc02b-124"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc02b-124"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc02b-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="fc02b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc02b-126">Objetos de criptografía</span><span class="sxs-lookup"><span data-stu-id="fc02b-126">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="fc02b-127">**Certificado**</span><span class="sxs-lookup"><span data-stu-id="fc02b-127">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
