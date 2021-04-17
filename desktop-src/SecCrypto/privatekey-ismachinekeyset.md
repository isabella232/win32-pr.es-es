---
description: Devuelve un valor booleano que indica si la clave privada pertenece a un conjunto de claves de equipo.
ms.assetid: ea13ba68-30ae-4aa4-b490-29fd4542c621
title: PrivateKey. IsMachineKeyset, método
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PrivateKey.IsMachineKeyset
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2a42e3f932b8294d9671b7901437151d9fbbe5a8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691092"
---
# <a name="privatekeyismachinekeyset-method"></a><span data-ttu-id="c72fd-103">PrivateKey. IsMachineKeyset, método</span><span class="sxs-lookup"><span data-stu-id="c72fd-103">PrivateKey.IsMachineKeyset method</span></span>

<span data-ttu-id="c72fd-104">\[El método **IsMachineKeyset** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="c72fd-104">\[The **IsMachineKeyset** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c72fd-105">En su lugar, use la [**propiedad X509Certificate2. PrivateKey**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="c72fd-105">Instead, use the [**X509Certificate2.PrivateKey Property**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2.privatekey?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="c72fd-106">El método **IsMachineKeyset** devuelve un valor booleano que indica si la clave privada pertenece a un conjunto de claves de equipo.</span><span class="sxs-lookup"><span data-stu-id="c72fd-106">The **IsMachineKeyset** method returns a Boolean value that indicates whether the private key belongs to a machine key set.</span></span>

## <a name="syntax"></a><span data-ttu-id="c72fd-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c72fd-107">Syntax</span></span>


```VB
PrivateKey.IsMachineKeyset()
```



## <a name="parameters"></a><span data-ttu-id="c72fd-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c72fd-108">Parameters</span></span>

<span data-ttu-id="c72fd-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="c72fd-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c72fd-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c72fd-110">Return value</span></span>

<span data-ttu-id="c72fd-111">Si es true, la clave privada pertenece a un conjunto de claves de equipo.</span><span class="sxs-lookup"><span data-stu-id="c72fd-111">If true, the private key belongs to a machine key set.</span></span>

## <a name="remarks"></a><span data-ttu-id="c72fd-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c72fd-112">Remarks</span></span>

<span data-ttu-id="c72fd-113">El valor devuelto de este método depende del [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) utilizado.</span><span class="sxs-lookup"><span data-stu-id="c72fd-113">The return value of this method is dependent on the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) used.</span></span> <span data-ttu-id="c72fd-114">Este método devolverá un valor de confianza si se usa un CSP de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c72fd-114">This method will return a trustworthy value if a Microsoft CSP is used.</span></span> <span data-ttu-id="c72fd-115">Si el CSP no es un CSP de Microsoft, el valor devuelto no puede ser de confianza para ser preciso.</span><span class="sxs-lookup"><span data-stu-id="c72fd-115">If the CSP is not a Microsoft CSP, the return value cannot be trusted to be accurate.</span></span>

## <a name="requirements"></a><span data-ttu-id="c72fd-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c72fd-116">Requirements</span></span>



| <span data-ttu-id="c72fd-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c72fd-117">Requirement</span></span> | <span data-ttu-id="c72fd-118">Value</span><span class="sxs-lookup"><span data-stu-id="c72fd-118">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c72fd-119">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="c72fd-119">Redistributable</span></span><br/> | <span data-ttu-id="c72fd-120">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="c72fd-120">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c72fd-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c72fd-121">DLL</span></span><br/>             | <dl> <span data-ttu-id="c72fd-122"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c72fd-122"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c72fd-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="c72fd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c72fd-124">**PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="c72fd-124">**PrivateKey**</span></span>](privatekey.md)
</dt> </dl>

 

 
