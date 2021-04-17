---
description: Define un algoritmo de cifrado para el cifrado y descifrado de datos.
ms.assetid: 6b634d76-a159-438e-8fc6-5f05b326ed68
title: Enumeración DOT11_CIPHER_ALGORITHM (Wlantypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_CIPHER_ALGORITHM
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: fcbd61476458b5ed906ee57af6ab22b35f0378d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678015"
---
# <a name="dot11_cipher_algorithm-enumeration"></a><span data-ttu-id="1b2ce-103">\_Enumeración de algoritmos de cifrado de DOT11 \_</span><span class="sxs-lookup"><span data-stu-id="1b2ce-103">DOT11\_CIPHER\_ALGORITHM enumeration</span></span>

<span data-ttu-id="1b2ce-104">El tipo enumerado del **\_ \_ algoritmo de cifrado de DOT11** define un algoritmo de cifrado para el cifrado y descifrado de datos.</span><span class="sxs-lookup"><span data-stu-id="1b2ce-104">The **DOT11\_CIPHER\_ALGORITHM** enumerated type defines a cipher algorithm for data encryption and decryption.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b2ce-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1b2ce-105">Syntax</span></span>


```C++
typedef enum _DOT11_CIPHER_ALGORITHM { 
  DOT11_CIPHER_ALGO_NONE           = 0x00,
  DOT11_CIPHER_ALGO_WEP40          = 0x01,
  DOT11_CIPHER_ALGO_TKIP           = 0x02,
  DOT11_CIPHER_ALGO_CCMP           = 0x04,
  DOT11_CIPHER_ALGO_WEP104         = 0x05,
  DOT11_CIPHER_ALGO_WPA_USE_GROUP  = 0x100,
  DOT11_CIPHER_ALGO_RSN_USE_GROUP  = 0x100,
  DOT11_CIPHER_ALGO_WEP            = 0x101,
  DOT11_CIPHER_ALGO_IHV_START      = 0x80000000,
  DOT11_CIPHER_ALGO_IHV_END        = 0xffffffff
} DOT11_CIPHER_ALGORITHM, *PDOT11_CIPHER_ALGORITHM;
```



## <a name="constants"></a><span data-ttu-id="1b2ce-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="1b2ce-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1b2ce-107"><span id="DOT11_CIPHER_ALGO_NONE"></span><span id="dot11_cipher_algo_none"></span>**\_Cifrado de DOT11 \_ algo \_ ninguno**</span><span class="sxs-lookup"><span data-stu-id="1b2ce-107"><span id="DOT11_CIPHER_ALGO_NONE"></span><span id="dot11_cipher_algo_none"></span>**DOT11\_CIPHER\_ALGO\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="1b2ce-108">Especifica que no se habilita ni se admite ningún algoritmo de cifrado.</span><span class="sxs-lookup"><span data-stu-id="1b2ce-108">Specifies that no cipher algorithm is enabled or supported.</span></span>

</dd> <dt>

<span data-ttu-id="1b2ce-109"><span id="DOT11_CIPHER_ALGO_WEP40"></span><span id="dot11_cipher_algo_wep40"></span>**\_Cifrado de \_ algo \_ WEP40 de DOT11**</span><span class="sxs-lookup"><span data-stu-id="1b2ce-109"><span id="DOT11_CIPHER_ALGO_WEP40"></span><span id="dot11_cipher_algo_wep40"></span>**DOT11\_CIPHER\_ALGO\_WEP40**</span></span>
</dt> <dd>

<span data-ttu-id="1b2ce-110">Especifica un algoritmo de privacidad equivalente por cable (WEP), que es el algoritmo basado en RC4 que se especifica en el estándar 802.11-1999.</span><span class="sxs-lookup"><span data-stu-id="1b2ce-110">Specifies a Wired Equivalent Privacy (WEP) algorithm, which is the RC4-based algorithm that is specified in the 802.11-1999 standard.</span></span> <span data-ttu-id="1b2ce-111">Este enumerador especifica el algoritmo de cifrado de WEP con una clave de cifrado de 40 bits.</span><span class="sxs-lookup"><span data-stu-id="1b2ce-111">This enumerator specifies the WEP cipher algorithm with a 40-bit cipher key.</span></span>

</dd> <dt>

<span data-ttu-id="1b2ce-112"><span id="DOT11_CIPHER_ALGO_TKIP"></span><span id="dot11_cipher_algo_tkip"></span>**\_Cifrado de \_ algo \_ TKIP de DOT11**</span><span class="sxs-lookup"><span data-stu-id="1b2ce-112"><span id="DOT11_CIPHER_ALGO_TKIP"></span><span id="dot11_cipher_algo_tkip"></span>**DOT11\_CIPHER\_ALGO\_TKIP**</span></span>
</dt> <dd>

<span data-ttu-id="1b2ce-113">Especifica un algoritmo del Protocolo de integridad de clave temporal (TKIP), que es el conjunto de cifrado basado en RC4 que se basa en los algoritmos definidos en la especificación de WPA y el estándar IEEE 802.11 i-2004.</span><span class="sxs-lookup"><span data-stu-id="1b2ce-113">Specifies a Temporal Key Integrity Protocol (TKIP) algorithm, which is the RC4-based cipher suite that is based on the algorithms that are defined in the WPA specification and IEEE 802.11i-2004 standard.</span></span> <span data-ttu-id="1b2ce-114">Este cifrado también usa el algoritmo de código de integridad del mensaje (MIC) de Michael para la protección de falsificación.</span><span class="sxs-lookup"><span data-stu-id="1b2ce-114">This cipher also uses the Michael Message Integrity Code (MIC) algorithm for forgery protection.</span></span>

</dd> <dt>

<span data-ttu-id="1b2ce-115"><span id="DOT11_CIPHER_ALGO_CCMP"></span><span id="dot11_cipher_algo_ccmp"></span>**\_Cifrado de DOT11 \_ algo \_ CCMP**</span><span class="sxs-lookup"><span data-stu-id="1b2ce-115"><span id="DOT11_CIPHER_ALGO_CCMP"></span><span id="dot11_cipher_algo_ccmp"></span>**DOT11\_CIPHER\_ALGO\_CCMP**</span></span>
</dt> <dd>

<span data-ttu-id="1b2ce-116">Especifica un algoritmo AES-CCMP, tal y como se especifica en el estándar IEEE 802.11 i-2004 y RFC 3610.</span><span class="sxs-lookup"><span data-stu-id="1b2ce-116">Specifies an AES-CCMP algorithm, as specified in the IEEE 802.11i-2004 standard and RFC 3610.</span></span> <span data-ttu-id="1b2ce-117">Estándar de cifrado avanzado (AES) es el algoritmo de cifrado definido en FIPS PUB 197.</span><span class="sxs-lookup"><span data-stu-id="1b2ce-117">Advanced Encryption Standard (AES) is the encryption algorithm defined in FIPS PUB 197.</span></span>

</dd> <dt>

<span data-ttu-id="1b2ce-118"><span id="DOT11_CIPHER_ALGO_WEP104"></span><span id="dot11_cipher_algo_wep104"></span>**\_Cifrado de \_ algo \_ WEP104 de DOT11**</span><span class="sxs-lookup"><span data-stu-id="1b2ce-118"><span id="DOT11_CIPHER_ALGO_WEP104"></span><span id="dot11_cipher_algo_wep104"></span>**DOT11\_CIPHER\_ALGO\_WEP104**</span></span>
</dt> <dd>

<span data-ttu-id="1b2ce-119">Especifica un algoritmo de cifrado de WEP con una clave de cifrado de 104 bits.</span><span class="sxs-lookup"><span data-stu-id="1b2ce-119">Specifies a WEP cipher algorithm with a 104-bit cipher key.</span></span>

</dd> <dt>

<span data-ttu-id="1b2ce-120"><span id="DOT11_CIPHER_ALGO_WPA_USE_GROUP"></span><span id="dot11_cipher_algo_wpa_use_group"></span>**\_Cifrado de DOT11 \_ algo \_ grupo de uso de WPA \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b2ce-120"><span id="DOT11_CIPHER_ALGO_WPA_USE_GROUP"></span><span id="dot11_cipher_algo_wpa_use_group"></span>**DOT11\_CIPHER\_ALGO\_WPA\_USE\_GROUP**</span></span>
</dt> <dd>

<span data-ttu-id="1b2ce-121">Especifica un conjunto de cifrado de claves de grupo de uso de Wi-Fi protegido (WPA).</span><span class="sxs-lookup"><span data-stu-id="1b2ce-121">Specifies a Wi-Fi Protected Access (WPA) Use Group Key cipher suite.</span></span> <span data-ttu-id="1b2ce-122">Para obtener más información sobre el conjunto de cifrado de claves de grupo, consulte la cláusula 7.3.2.25.1 del estándar IEEE 802.11 i-2004.</span><span class="sxs-lookup"><span data-stu-id="1b2ce-122">For more information about the Use Group Key cipher suite, refer to Clause 7.3.2.25.1 of the IEEE 802.11i-2004 standard.</span></span>

</dd> <dt>

<span data-ttu-id="1b2ce-123"><span id="DOT11_CIPHER_ALGO_RSN_USE_GROUP"></span><span id="dot11_cipher_algo_rsn_use_group"></span>**\_Cifrado de DOT11 \_ algo de uso de \_ RSN \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1b2ce-123"><span id="DOT11_CIPHER_ALGO_RSN_USE_GROUP"></span><span id="dot11_cipher_algo_rsn_use_group"></span>**DOT11\_CIPHER\_ALGO\_RSN\_USE\_GROUP**</span></span>
</dt> <dd>

<span data-ttu-id="1b2ce-124">Especifica un conjunto de cifrado de claves de grupo de uso de redes de seguridad sólidas (RSN).</span><span class="sxs-lookup"><span data-stu-id="1b2ce-124">Specifies a Robust Security Network (RSN) Use Group Key cipher suite.</span></span> <span data-ttu-id="1b2ce-125">Para obtener más información sobre el conjunto de cifrado de claves de grupo, consulte la cláusula 7.3.2.25.1 del estándar IEEE 802.11 i-2004.</span><span class="sxs-lookup"><span data-stu-id="1b2ce-125">For more information about the Use Group Key cipher suite, refer to Clause 7.3.2.25.1 of the IEEE 802.11i-2004 standard.</span></span>

</dd> <dt>

<span data-ttu-id="1b2ce-126"><span id="DOT11_CIPHER_ALGO_WEP"></span><span id="dot11_cipher_algo_wep"></span>**\_Cifrado de algo de DOT11 \_ \_ WEP**</span><span class="sxs-lookup"><span data-stu-id="1b2ce-126"><span id="DOT11_CIPHER_ALGO_WEP"></span><span id="dot11_cipher_algo_wep"></span>**DOT11\_CIPHER\_ALGO\_WEP**</span></span>
</dt> <dd>

<span data-ttu-id="1b2ce-127">Especifica un algoritmo de cifrado WEP con una clave de cifrado de cualquier longitud.</span><span class="sxs-lookup"><span data-stu-id="1b2ce-127">Specifies a WEP cipher algorithm with a cipher key of any length.</span></span>

</dd> <dt>

<span data-ttu-id="1b2ce-128"><span id="DOT11_CIPHER_ALGO_IHV_START"></span><span id="dot11_cipher_algo_ihv_start"></span>**\_Inicio de \_ \_ IHV algo de CIFRAdo de DOT11 \_**</span><span class="sxs-lookup"><span data-stu-id="1b2ce-128"><span id="DOT11_CIPHER_ALGO_IHV_START"></span><span id="dot11_cipher_algo_ihv_start"></span>**DOT11\_CIPHER\_ALGO\_IHV\_START**</span></span>
</dt> <dd>

<span data-ttu-id="1b2ce-129">Especifica el inicio del intervalo que se usa para definir los algoritmos de cifrado de propiedad desarrollados por un fabricante de hardware independiente (IHV).</span><span class="sxs-lookup"><span data-stu-id="1b2ce-129">Specifies the start of the range that is used to define proprietary cipher algorithms that are developed by an independent hardware vendor (IHV).</span></span>

</dd> <dt>

<span data-ttu-id="1b2ce-130"><span id="DOT11_CIPHER_ALGO_IHV_END"></span><span id="dot11_cipher_algo_ihv_end"></span>**\_Fin de \_ algo \_ IHV de CIFRAdo de DOT11 \_**</span><span class="sxs-lookup"><span data-stu-id="1b2ce-130"><span id="DOT11_CIPHER_ALGO_IHV_END"></span><span id="dot11_cipher_algo_ihv_end"></span>**DOT11\_CIPHER\_ALGO\_IHV\_END**</span></span>
</dt> <dd>

<span data-ttu-id="1b2ce-131">Especifica el final del intervalo que se utiliza para definir los algoritmos de cifrado de propiedad desarrollados por un IHV.</span><span class="sxs-lookup"><span data-stu-id="1b2ce-131">Specifies the end of the range that is used to define proprietary cipher algorithms that are developed by an IHV.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1b2ce-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b2ce-132">Requirements</span></span>



| <span data-ttu-id="1b2ce-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b2ce-133">Requirement</span></span> | <span data-ttu-id="1b2ce-134">Value</span><span class="sxs-lookup"><span data-stu-id="1b2ce-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b2ce-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b2ce-135">Minimum supported client</span></span><br/> | <span data-ttu-id="1b2ce-136">Windows Vista, Windows XP con SP3 \[ solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="1b2ce-136">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1b2ce-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b2ce-137">Minimum supported server</span></span><br/> | <span data-ttu-id="1b2ce-138">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="1b2ce-138">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="1b2ce-139">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="1b2ce-139">Redistributable</span></span><br/>          | <span data-ttu-id="1b2ce-140">API de LAN inalámbrica para Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="1b2ce-140">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                         |
| <span data-ttu-id="1b2ce-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1b2ce-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b2ce-142"><dt>Wlantypes. h (incluye Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1b2ce-142"><dt>Wlantypes.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b2ce-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="1b2ce-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b2ce-144">**\_Par de \_ cifrado de autenticación de DOT11 \_**</span><span class="sxs-lookup"><span data-stu-id="1b2ce-144">**DOT11\_AUTH\_CIPHER\_PAIR**</span></span>](dot11-auth-cipher-pair.md)
</dt> <dt>

[<span data-ttu-id="1b2ce-145">**\_red disponible de WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="1b2ce-145">**WLAN\_AVAILABLE\_NETWORK**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_available_network)
</dt> <dt>

[<span data-ttu-id="1b2ce-146">**\_atributos de seguridad de WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="1b2ce-146">**WLAN\_SECURITY\_ATTRIBUTES**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_security_attributes)
</dt> </dl>

 

 




