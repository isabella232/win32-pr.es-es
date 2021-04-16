---
description: Recupera el algoritmo para los datos cifrados.
ms.assetid: 37bebe69-3c62-44c4-a5e5-c8cdbf087fa4
title: EncryptedData. algorithm (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EncryptedData.Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: cd73fbda4a5f77706ac2253782768e8487b8cbff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649946"
---
# <a name="encrypteddataalgorithm-property"></a><span data-ttu-id="c8bfd-103">EncryptedData. algorithm (propiedad)</span><span class="sxs-lookup"><span data-stu-id="c8bfd-103">EncryptedData.Algorithm property</span></span>

<span data-ttu-id="c8bfd-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c8bfd-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="c8bfd-105">En su lugar, use servicios de invocación de plataforma (PInvoke) para llamar a las funciones de la API de Win32 [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) y [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) para cifrar y descifrar los mensajes.</span><span class="sxs-lookup"><span data-stu-id="c8bfd-105">Instead, use Platform Invocation Services (PInvoke) to call the Win32 API functions [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage) and [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage) to encrypt and decrypt messages.</span></span> <span data-ttu-id="c8bfd-106">Para obtener información sobre PInvoke, vea [tutorial de invocación de plataforma](https://msdn.microsoft.com/library/aa288468.aspx).</span><span class="sxs-lookup"><span data-stu-id="c8bfd-106">For information about PInvoke, see [Platform Invoke Tutorial](https://msdn.microsoft.com/library/aa288468.aspx).</span></span> <span data-ttu-id="c8bfd-107">También pueden resultar útiles las subsecciones de [.net y CryptoAPI a través de p/Invoke: parte 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) y [.net y CryptoAPI a través de p/Invoke: parte 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) de la extensión de la [criptografía de .net con CAPICOM y p/Invoke](/previous-versions/ms867087(v=msdn.10)) .\]</span><span class="sxs-lookup"><span data-stu-id="c8bfd-107">The [.NET and CryptoAPI via P/Invoke: Part 1](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5) and [.NET and CryptoAPI via P/Invoke: Part 2](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6) subsections of [Extending .NET Cryptography with CAPICOM and P/Invoke](/previous-versions/ms867087(v=msdn.10)) may also be helpful.\]</span></span>

<span data-ttu-id="c8bfd-108">La propiedad **algorithm** recupera el algoritmo para los datos cifrados.</span><span class="sxs-lookup"><span data-stu-id="c8bfd-108">The **Algorithm** property retrieves the algorithm for the encrypted data.</span></span>

<span data-ttu-id="c8bfd-109">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="c8bfd-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8bfd-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8bfd-110">Syntax</span></span>


```VB
EncryptedData.Algorithm As Algorithm
```



## <a name="property-value"></a><span data-ttu-id="c8bfd-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="c8bfd-111">Property value</span></span>

<span data-ttu-id="c8bfd-112">Objeto de [**algoritmo**](algorithm.md) que representa el algoritmo de cifrado.</span><span class="sxs-lookup"><span data-stu-id="c8bfd-112">An [**Algorithm**](algorithm.md) object that represents the encryption algorithm.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8bfd-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8bfd-113">Requirements</span></span>



| <span data-ttu-id="c8bfd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8bfd-114">Requirement</span></span> | <span data-ttu-id="c8bfd-115">Value</span><span class="sxs-lookup"><span data-stu-id="c8bfd-115">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c8bfd-116">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="c8bfd-116">End of client support</span></span><br/> | <span data-ttu-id="c8bfd-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c8bfd-117">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="c8bfd-118">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="c8bfd-118">End of server support</span></span><br/> | <span data-ttu-id="c8bfd-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c8bfd-119">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="c8bfd-120">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="c8bfd-120">Redistributable</span></span><br/>       | <span data-ttu-id="c8bfd-121">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="c8bfd-121">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="c8bfd-122">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c8bfd-122">DLL</span></span><br/>                   | <dl> <span data-ttu-id="c8bfd-123"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8bfd-123"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8bfd-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8bfd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8bfd-125">**EncryptedData**</span><span class="sxs-lookup"><span data-stu-id="c8bfd-125">**EncryptedData**</span></span>](encrypteddata.md)
</dt> </dl>

 

 
