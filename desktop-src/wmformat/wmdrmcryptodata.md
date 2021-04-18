---
title: Estructura WMDRMCryptoData (wmdrmsdk. h)
description: La estructura WMDRMCryptoData contiene información sobre el algoritmo criptográfico que se usa para cifrar y descifrar contenido.
ms.assetid: ad14c6d3-4305-47c0-8f67-7ef6d11cc326
keywords:
- Estructura WMDRMCryptoData formato de Windows Media
- Formato de Windows Media de estructura
topic_type:
- apiref
api_name:
- WMDRMCryptoData
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce972cdf41ff1e587d40b5fc95021f568be95f9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699979"
---
# <a name="wmdrmcryptodata-structure"></a><span data-ttu-id="27d65-105">Estructura WMDRMCryptoData</span><span class="sxs-lookup"><span data-stu-id="27d65-105">WMDRMCryptoData structure</span></span>

<span data-ttu-id="27d65-106">La estructura **WMDRMCryptoData** contiene información sobre el algoritmo criptográfico que se usa para cifrar y descifrar contenido.</span><span class="sxs-lookup"><span data-stu-id="27d65-106">The **WMDRMCryptoData** structure contains information about the cryptographic algorithm used to encrypt and decrypt content.</span></span>

## <a name="syntax"></a><span data-ttu-id="27d65-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="27d65-107">Syntax</span></span>


```C++
typedef struct WMDRMCryptoData {
  DRM_CRYPTO_TYPE  cryptoType;
  unsigned __int64 qwCounterID;
  unsigned __int64 qwOffset;
} ;
```



## <a name="members"></a><span data-ttu-id="27d65-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="27d65-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="27d65-109">**cryptoType**</span><span class="sxs-lookup"><span data-stu-id="27d65-109">**cryptoType**</span></span>
</dt> <dd>

<span data-ttu-id="27d65-110">Miembro de la enumeración de [**\_ \_ tipo criptográfico de DRM**](drm-crypto-type.md) que especifica el tipo de algoritmo criptográfico.</span><span class="sxs-lookup"><span data-stu-id="27d65-110">Member of the [**DRM\_CRYPTO\_TYPE**](drm-crypto-type.md) enumeration specifying the type of cryptographic algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="27d65-111">**qwCounterID**</span><span class="sxs-lookup"><span data-stu-id="27d65-111">**qwCounterID**</span></span>
</dt> <dd>

<span data-ttu-id="27d65-112">Los bits 64 altos del modo de contador AES de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="27d65-112">The high 64 bits of the 128-bit AES counter mode.</span></span> <span data-ttu-id="27d65-113">Este miembro solo se utiliza si el miembro **cryptoType** está establecido en el **tipo de cifrado \_ \_ MCE**.</span><span class="sxs-lookup"><span data-stu-id="27d65-113">This member is only used if the **cryptoType** member is set to **CRYPTO\_TYPE\_MCE**.</span></span>

</dd> <dt>

<span data-ttu-id="27d65-114">**qwOffset**</span><span class="sxs-lookup"><span data-stu-id="27d65-114">**qwOffset**</span></span>
</dt> <dd>

<span data-ttu-id="27d65-115">Los bits 64 bajos del modo de contador AES de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="27d65-115">The low 64 bits of the 128-bit AES counter mode.</span></span> <span data-ttu-id="27d65-116">Este miembro solo se utiliza si el miembro **cryptoType** está establecido en el **tipo de cifrado \_ \_ MCE**.</span><span class="sxs-lookup"><span data-stu-id="27d65-116">This member is only used if the **cryptoType** member is set to **CRYPTO\_TYPE\_MCE**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="27d65-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="27d65-117">Requirements</span></span>



| <span data-ttu-id="27d65-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="27d65-118">Requirement</span></span> | <span data-ttu-id="27d65-119">Value</span><span class="sxs-lookup"><span data-stu-id="27d65-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="27d65-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="27d65-120">Header</span></span><br/> | <dl> <span data-ttu-id="27d65-121"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="27d65-121"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27d65-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="27d65-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27d65-123">**Estructuras**</span><span class="sxs-lookup"><span data-stu-id="27d65-123">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





