---
description: Elimina el contenedor de claves privadas al que hace referencia el objeto PrivateKey.
ms.assetid: 80bbe46b-1ec5-4d47-82b0-5a3177f86389
title: PrivateKey. Delete (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.Delete
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: dc5778e631abba9eb8cf122ddb99a4692c988f4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670553"
---
# <a name="privatekeydelete-method"></a><span data-ttu-id="fb456-103">PrivateKey. Delete (método)</span><span class="sxs-lookup"><span data-stu-id="fb456-103">PrivateKey.Delete method</span></span>

<span data-ttu-id="fb456-104">\[El método **Delete** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="fb456-104">\[The **Delete** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="fb456-105">En su lugar, use la [**propiedad X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="fb456-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="fb456-106">El método **Delete** elimina el contenedor de claves privadas al que hace referencia el objeto [**PrivateKey**](privatekey.md) .</span><span class="sxs-lookup"><span data-stu-id="fb456-106">The **Delete** method deletes the private key container referenced by the [**PrivateKey**](privatekey.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb456-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fb456-107">Syntax</span></span>


```VB
PrivateKey.Delete()
```



## <a name="parameters"></a><span data-ttu-id="fb456-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fb456-108">Parameters</span></span>

<span data-ttu-id="fb456-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="fb456-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fb456-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fb456-110">Return value</span></span>

<span data-ttu-id="fb456-111">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="fb456-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb456-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fb456-112">Remarks</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fb456-113">Este método elimina el contenedor de claves privadas al que hace referencia el objeto [**PrivateKey**](privatekey.md) así como todas las claves privadas del contenedor.</span><span class="sxs-lookup"><span data-stu-id="fb456-113">This method deletes the private key container referenced by the [**PrivateKey**](privatekey.md) object as well as all private keys in the container.</span></span> <span data-ttu-id="fb456-114">Cualquier elemento cifrado con las claves públicas correspondientes a las claves privadas eliminadas ya no se podrá descifrar.</span><span class="sxs-lookup"><span data-stu-id="fb456-114">Anything encrypted using the public keys corresponding to the deleted private keys will no longer be able to be decrypted.</span></span>

 

<span data-ttu-id="fb456-115">Este método produce CAPICOM \_ E \_ no \_ se permite cuando se genera un script desde una aplicación basada en Web.</span><span class="sxs-lookup"><span data-stu-id="fb456-115">This method raises CAPICOM\_E\_NOT\_ALLOWED when it is scripted from a web-based application.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb456-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb456-116">Requirements</span></span>



| <span data-ttu-id="fb456-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb456-117">Requirement</span></span> | <span data-ttu-id="fb456-118">Value</span><span class="sxs-lookup"><span data-stu-id="fb456-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb456-119">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="fb456-119">Redistributable</span></span><br/> | <span data-ttu-id="fb456-120">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="fb456-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="fb456-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fb456-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="fb456-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb456-122"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
