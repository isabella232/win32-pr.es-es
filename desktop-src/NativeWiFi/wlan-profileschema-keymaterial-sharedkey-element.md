---
description: Contiene una clave o frase de contraseña de red.
ms.assetid: d2ed407e-5eaa-477b-8c4d-a47795048e0b
title: Elemento keyMaterial (sharedKey)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- keyMaterial
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 59f3fc25fda5f4bf4221417636ac25ab7d0f9a15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277027"
---
# <a name="keymaterial-sharedkey-element"></a><span data-ttu-id="a6752-103">Elemento keyMaterial (sharedKey)</span><span class="sxs-lookup"><span data-stu-id="a6752-103">keyMaterial (sharedKey) Element</span></span>

<span data-ttu-id="a6752-104">El elemento keyMaterial (sharedKey) contiene una clave de red o frase de contraseña.</span><span class="sxs-lookup"><span data-stu-id="a6752-104">The keyMaterial (sharedKey) element contains a network key or passphrase.</span></span> <span data-ttu-id="a6752-105">Si el elemento [**protegido**](wlan-profileschema-protected-sharedkey-element.md) tiene un valor de true, se cifra este material de clave. de lo contrario, el material de clave no está cifrado.</span><span class="sxs-lookup"><span data-stu-id="a6752-105">If the [**protected**](wlan-profileschema-protected-sharedkey-element.md) element has a value of TRUE, then this key material is encrypted; otherwise, the key material is unencrypted.</span></span> <span data-ttu-id="a6752-106">El material de clave cifrada se expresa en formato hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="a6752-106">Encrypted key material is expressed in hexadecimal form.</span></span>

``` syntax
<xs:element name="keyMaterial"
    type="string"
 />
```

<span data-ttu-id="a6752-107">El elemento se define mediante el elemento [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a6752-107">The element is defined by the [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6752-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a6752-108">Remarks</span></span>

<span data-ttu-id="a6752-109">El intervalo de valores válidos para el elemento keyMaterial varía según el tipo de autenticación y el cifrado utilizado, tal y como se especifica en los elementos de [**autenticación**](wlan-profileschema-authentication-authencryption-element.md) y [**cifrado**](wlan-profileschema-encryption-authencryption-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a6752-109">The range of valid values for the keyMaterial element varies by the type of authentication and encryption used, as specified by the [**authentication**](wlan-profileschema-authentication-authencryption-element.md) and [**encryption**](wlan-profileschema-encryption-authencryption-element.md) elements.</span></span> <span data-ttu-id="a6752-110">También varía según [**KeyType**](wlan-profileschema-keytype-sharedkey-element.md).</span><span class="sxs-lookup"><span data-stu-id="a6752-110">It also varies by [**keyType**](wlan-profileschema-keytype-sharedkey-element.md).</span></span>

<span data-ttu-id="a6752-111">En la tabla siguiente se muestran los valores válidos de **keyMaterial** para algunos pares de cifrado y autenticación.</span><span class="sxs-lookup"><span data-stu-id="a6752-111">The following table shows valid **keyMaterial** values for some authentication and encryption pairs.</span></span>



| <span data-ttu-id="a6752-112">valor de [**autenticación**](wlan-profileschema-authentication-authencryption-element.md)</span><span class="sxs-lookup"><span data-stu-id="a6752-112">[**authentication**](wlan-profileschema-authentication-authencryption-element.md) value</span></span> | <span data-ttu-id="a6752-113">valor de [**cifrado**](wlan-profileschema-encryption-authencryption-element.md)</span><span class="sxs-lookup"><span data-stu-id="a6752-113">[**encryption**](wlan-profileschema-encryption-authencryption-element.md) value</span></span> | <span data-ttu-id="a6752-114">valor de [**KeyType**](wlan-profileschema-keytype-sharedkey-element.md)</span><span class="sxs-lookup"><span data-stu-id="a6752-114">[**keyType**](wlan-profileschema-keytype-sharedkey-element.md) value</span></span> | <span data-ttu-id="a6752-115">Valores válidos de **keyMaterial**</span><span class="sxs-lookup"><span data-stu-id="a6752-115">Valid **keyMaterial** values</span></span>                                                                                                                                                                   |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6752-116">abrir o compartir</span><span class="sxs-lookup"><span data-stu-id="a6752-116">open or shared</span></span>                                                                           | <span data-ttu-id="a6752-117">WEP</span><span class="sxs-lookup"><span data-stu-id="a6752-117">WEP</span></span>                                                                              | <span data-ttu-id="a6752-118">networkKey</span><span class="sxs-lookup"><span data-stu-id="a6752-118">networkKey</span></span>                                                            | <span data-ttu-id="a6752-119">Este elemento contiene una clave WEP de 5 u 13 caracteres ANSI, o de 10 o 26 caracteres hexadecimales.</span><span class="sxs-lookup"><span data-stu-id="a6752-119">This element contains a WEP key of 5 or 13 ANSI characters, or of 10 or 26 hexadecimal characters.</span></span>                                                                                             |
| <span data-ttu-id="a6752-120">WPAPSK o WPA2PSK</span><span class="sxs-lookup"><span data-stu-id="a6752-120">WPAPSK or WPA2PSK</span></span>                                                                        | <span data-ttu-id="a6752-121">TKIP o AES</span><span class="sxs-lookup"><span data-stu-id="a6752-121">TKIP or AES</span></span>                                                                      | <span data-ttu-id="a6752-122">passPhrase</span><span class="sxs-lookup"><span data-stu-id="a6752-122">passPhrase</span></span>                                                            | <span data-ttu-id="a6752-123">Este elemento contiene una frase de contraseña de 8 a 63 caracteres ASCII, es decir, de 8 a 63 caracteres ANSI en el intervalo de 32 a 126.</span><span class="sxs-lookup"><span data-stu-id="a6752-123">This element contains a passphrase of 8 to 63 ASCII characters, that is, 8 to 63 ANSI characters in the range of 32 to 126.</span></span> <span data-ttu-id="a6752-124">Los valores de clave deben cumplir los requisitos especificados por 802.11 i.</span><span class="sxs-lookup"><span data-stu-id="a6752-124">Key values must comply with the requirements specified by 802.11i.</span></span> |
| <span data-ttu-id="a6752-125">WPAPSK o WPA2PSK</span><span class="sxs-lookup"><span data-stu-id="a6752-125">WPAPSK or WPA2PSK</span></span>                                                                        | <span data-ttu-id="a6752-126">TKIP o AES</span><span class="sxs-lookup"><span data-stu-id="a6752-126">TKIP or AES</span></span>                                                                      | <span data-ttu-id="a6752-127">networkKey</span><span class="sxs-lookup"><span data-stu-id="a6752-127">networkKey</span></span>                                                            | <span data-ttu-id="a6752-128">Este elemento contiene una clave de 64 caracteres hexadecimales.</span><span class="sxs-lookup"><span data-stu-id="a6752-128">This element contains a key of 64 hexadecimal characters.</span></span>                                                                                                                                      |



 

<span data-ttu-id="a6752-129">Se pueden escribir caracteres Unicode donde se especifican los caracteres ANSI o ASCII anteriores.</span><span class="sxs-lookup"><span data-stu-id="a6752-129">Unicode characters may be entered where ANSI or ASCII characters are specified above.</span></span> <span data-ttu-id="a6752-130">Sin embargo, si los caracteres Unicode proporcionados no se pueden asignar a caracteres ANSI o ASCII, se rechazará el material de clave proporcionado.</span><span class="sxs-lookup"><span data-stu-id="a6752-130">However, if the supplied Unicode characters cannot be mapped to ANSI or ASCII characters, then the supplied key material is rejected.</span></span>

<span data-ttu-id="a6752-131">El material de clave devuelto por [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile) está siempre cifrado.</span><span class="sxs-lookup"><span data-stu-id="a6752-131">Key material returned by [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile) is always encrypted.</span></span> <span data-ttu-id="a6752-132">Además, si el material de clave sin cifrado se pasa a [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile), el material de clave se cifra automáticamente antes de almacenarse en el almacén de perfiles.</span><span class="sxs-lookup"><span data-stu-id="a6752-132">Also, if unencrypted key material is passed to [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile), the key material is automatically encrypted before it is stored in the profile store.</span></span>

<span data-ttu-id="a6752-133">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** El material de clave nunca está cifrado.</span><span class="sxs-lookup"><span data-stu-id="a6752-133">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** The key material is never encrypted.</span></span>

<span data-ttu-id="a6752-134">Si el proceso se ejecuta en el contexto de la cuenta LocalSystem, puede descifrar el material de clave llamando a [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata).</span><span class="sxs-lookup"><span data-stu-id="a6752-134">If your process runs in the context of the LocalSystem account, then you can unencrypt key material by calling [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata).</span></span>

## <a name="examples"></a><span data-ttu-id="a6752-135">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a6752-135">Examples</span></span>

<span data-ttu-id="a6752-136">Para ver los perfiles de ejemplo que usan el elemento **keyMaterial** , vea ejemplo [de perfil sin difusión](non-broadcast-profile-sample.md), ejemplo de perfil [de WPA-Personal](wpa-personal-profile-sample.md)y [ejemplo de perfil WPA2-Personal](wpa2-personal-profile-sample.md).</span><span class="sxs-lookup"><span data-stu-id="a6752-136">To view sample profiles that use the **keyMaterial** element, see [Non-Broadcast Profile Sample](non-broadcast-profile-sample.md), [WPA-Personal Profile Sample](wpa-personal-profile-sample.md), and [WPA2-Personal Profile Sample](wpa2-personal-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a6752-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6752-137">Requirements</span></span>



| <span data-ttu-id="a6752-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6752-138">Requirement</span></span> | <span data-ttu-id="a6752-139">Value</span><span class="sxs-lookup"><span data-stu-id="a6752-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="a6752-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6752-140">Minimum supported client</span></span><br/> | <span data-ttu-id="a6752-141">Windows Vista, Windows XP con SP3 \[ solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="a6752-141">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a6752-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a6752-142">Minimum supported server</span></span><br/> | <span data-ttu-id="a6752-143">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="a6752-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="a6752-144">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="a6752-144">Redistributable</span></span><br/>          | <span data-ttu-id="a6752-145">API de LAN inalámbrica para Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="a6752-145">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="a6752-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="a6752-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="a6752-147">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="a6752-147">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a6752-148">**sharedKey**</span><span class="sxs-lookup"><span data-stu-id="a6752-148">**sharedKey**</span></span>](wlan-profileschema-sharedkey-security-element.md)
</dt> <dt>

<span data-ttu-id="a6752-149">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="a6752-149">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="a6752-150">**sharedKey (seguridad)**</span><span class="sxs-lookup"><span data-stu-id="a6752-150">**sharedKey (security)**</span></span>](wlan-profileschema-sharedkey-security-element.md)
</dt> </dl>

 

 
