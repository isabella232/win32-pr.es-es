---
description: Cierra un almacén de certificados abierto.
ms.assetid: 14db819a-b220-47d4-9030-72157e0e5019
title: Store. Close (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Close
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 2e3deb127ec8b19d9ec5c625f07cfaa2685b776c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671469"
---
# <a name="storeclose-method"></a><span data-ttu-id="4ea10-103">Store. Close (método)</span><span class="sxs-lookup"><span data-stu-id="4ea10-103">Store.Close method</span></span>

<span data-ttu-id="4ea10-104">\[El método **Close** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="4ea10-104">\[The **Close** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4ea10-105">En su lugar, use la [**clase X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="4ea10-105">Instead, use the [**X509Store Class**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="4ea10-106">El método **Close** cierra un almacén de [*certificados*](../secgloss/c-gly.md)abierto.</span><span class="sxs-lookup"><span data-stu-id="4ea10-106">The **Close** method closes an open [*certificate store*](../secgloss/c-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4ea10-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4ea10-107">Syntax</span></span>


```VB
Store.Close()
```



## <a name="parameters"></a><span data-ttu-id="4ea10-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4ea10-108">Parameters</span></span>

<span data-ttu-id="4ea10-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="4ea10-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4ea10-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4ea10-110">Return value</span></span>

<span data-ttu-id="4ea10-111">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="4ea10-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4ea10-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4ea10-112">Remarks</span></span>

<span data-ttu-id="4ea10-113">Después de llamar al método **Close** , se destruye el objeto [**Store**](store.md) .</span><span class="sxs-lookup"><span data-stu-id="4ea10-113">After the **Close** method is called, the [**Store**](store.md) object is destroyed.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ea10-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ea10-114">Requirements</span></span>



| <span data-ttu-id="4ea10-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ea10-115">Requirement</span></span> | <span data-ttu-id="4ea10-116">Value</span><span class="sxs-lookup"><span data-stu-id="4ea10-116">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ea10-117">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="4ea10-117">Redistributable</span></span><br/> | <span data-ttu-id="4ea10-118">CAPICOM 2,1 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="4ea10-118">CAPICOM 2.1 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4ea10-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4ea10-119">DLL</span></span><br/>             | <dl> <span data-ttu-id="4ea10-120"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ea10-120"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ea10-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="4ea10-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ea10-122">**Store**</span><span class="sxs-lookup"><span data-stu-id="4ea10-122">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="4ea10-123">**Objetos de criptografía**</span><span class="sxs-lookup"><span data-stu-id="4ea10-123">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="4ea10-124">**Ábra**</span><span class="sxs-lookup"><span data-stu-id="4ea10-124">**Open**</span></span>](store-open.md)
</dt> </dl>

 

 
