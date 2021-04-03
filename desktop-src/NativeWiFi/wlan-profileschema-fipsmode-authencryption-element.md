---
description: Indica si está habilitado el modo estándar federal de procesamiento de información (FIPS).
ms.assetid: 4c62c96c-82e7-4174-b833-95ee10b29344
title: Elemento FIPSMode (authEncryption)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FIPSMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 62a60670622084e3179e9720022c68ad5909ab4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810376"
---
# <a name="fipsmode-authencryption-element"></a><span data-ttu-id="9b29a-103">Elemento FIPSMode (authEncryption)</span><span class="sxs-lookup"><span data-stu-id="9b29a-103">FIPSMode (authEncryption) Element</span></span>

<span data-ttu-id="9b29a-104">El elemento **FIPSMode** (authEncryption) indica si está habilitado el modo estándar federal de procesamiento de información (FIPS).</span><span class="sxs-lookup"><span data-stu-id="9b29a-104">The **FIPSMode** (authEncryption) element indicates whether Federal Information Processing Standards (FIPS) mode is enabled.</span></span> <span data-ttu-id="9b29a-105">Cuando una conexión inalámbrica funciona en modo FIPS, el nivel de seguridad de la conexión cumple con el estándar FIPS 140-2.</span><span class="sxs-lookup"><span data-stu-id="9b29a-105">When a wireless connection is operating in FIPS mode, the security level of the connection complies with the FIPS 140-2 standard.</span></span> <span data-ttu-id="9b29a-106">Para obtener más información acerca de FIPS, consulte la [Página principal de FIPS](https://www.itl.nist.gov/fipspubs/).</span><span class="sxs-lookup"><span data-stu-id="9b29a-106">For more information about FIPS, see the [FIPS Home Page](https://www.itl.nist.gov/fipspubs/).</span></span>

<span data-ttu-id="9b29a-107">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="9b29a-107">This element is optional.</span></span> <span data-ttu-id="9b29a-108">Si este elemento no se especifica en un perfil, no se habilita el modo FIPS.</span><span class="sxs-lookup"><span data-stu-id="9b29a-108">If this element is not specified in a profile, then FIPS mode is not enabled.</span></span>

<span data-ttu-id="9b29a-109">**FIPSMode** solo se puede establecer en true cuando se cumplen las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="9b29a-109">**FIPSMode** can be set to TRUE only when the following conditions are met:</span></span>

-   <span data-ttu-id="9b29a-110">El elemento [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) tiene un valor de `ESS` (es decir, la conexión es una conexión de infraestructura).</span><span class="sxs-lookup"><span data-stu-id="9b29a-110">The [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) element has a value of `ESS` (that is, the connection is an infrastructure connection).</span></span>
-   <span data-ttu-id="9b29a-111">El elemento [**Authentication**](wlan-profileschema-authentication-authencryption-element.md) tiene un valor de `WPA2` o `WPA2PSK` .</span><span class="sxs-lookup"><span data-stu-id="9b29a-111">The [**authentication**](wlan-profileschema-authentication-authencryption-element.md) element has a value of `WPA2` or `WPA2PSK`.</span></span>
-   <span data-ttu-id="9b29a-112">El elemento [**Encryption**](wlan-profileschema-encryption-authencryption-element.md) tiene un valor de `AES` .</span><span class="sxs-lookup"><span data-stu-id="9b29a-112">The [**encryption**](wlan-profileschema-encryption-authencryption-element.md) element has a value of `AES`.</span></span>

<span data-ttu-id="9b29a-113">A diferencia de la mayoría de los elementos del esquema de Perfil de WLAN \_ , este elemento se encuentra en el `https://www.microsoft.com/networking/WLAN/profile/v2` espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="9b29a-113">Unlike most elements in the WLAN\_profile schema, this element is in the `https://www.microsoft.com/networking/WLAN/profile/v2` namespace.</span></span>

<span data-ttu-id="9b29a-114">El valor del elemento **FIPSMode** se omite si el controlador de minipuerto para la interfaz inalámbrica no es compatible con el modo FIPS.</span><span class="sxs-lookup"><span data-stu-id="9b29a-114">The value of the **FIPSMode** element is ignored if the miniport driver for the wireless interface does not support FIPS mode.</span></span>

<span data-ttu-id="9b29a-115">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.</span><span class="sxs-lookup"><span data-stu-id="9b29a-115">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span> <span data-ttu-id="9b29a-116">Si **FIPSMode** está presente en un perfil, se omite el elemento.</span><span class="sxs-lookup"><span data-stu-id="9b29a-116">If **FIPSMode** is present in a profile, the element is ignored.</span></span>

``` syntax
<xs:element name="FIPSMode"
    type="boolean"
 />
```

<span data-ttu-id="9b29a-117">El elemento se define mediante el elemento [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="9b29a-117">The element is defined by the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="9b29a-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9b29a-118">Remarks</span></span>

<span data-ttu-id="9b29a-119">Este parámetro se puede establecer en la línea de comandos mediante el comando **netsh wlan set ProfileParameter**</span><span class="sxs-lookup"><span data-stu-id="9b29a-119">This parameter can be set at the command line using the **netsh wlan set profileparameter** command.</span></span> <span data-ttu-id="9b29a-120">Para obtener más información, consulte [comandos Netsh para red de área local inalámbrica (WLAN)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="9b29a-120">For more information, see [Netsh Commands for Wireless Local Area Network (wlan)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span></span>

## <a name="examples"></a><span data-ttu-id="9b29a-121">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9b29a-121">Examples</span></span>

<span data-ttu-id="9b29a-122">Para ver un perfil de ejemplo que usa el elemento **FIPSMode** , vea [ejemplo de Perfil de FIPS](fips-profile-sample.md).</span><span class="sxs-lookup"><span data-stu-id="9b29a-122">To view a sample profile that uses the **FIPSMode** element, see [FIPS Profile Sample](fips-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9b29a-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b29a-123">Requirements</span></span>



| <span data-ttu-id="9b29a-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b29a-124">Requirement</span></span> | <span data-ttu-id="9b29a-125">Value</span><span class="sxs-lookup"><span data-stu-id="9b29a-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="9b29a-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b29a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9b29a-127">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="9b29a-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9b29a-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b29a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9b29a-129">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="9b29a-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9b29a-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b29a-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="9b29a-131">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="9b29a-131">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="9b29a-132">**authEncryption**</span><span class="sxs-lookup"><span data-stu-id="9b29a-132">**authEncryption**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> <dt>

<span data-ttu-id="9b29a-133">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="9b29a-133">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="9b29a-134">**authEncryption (seguridad)**</span><span class="sxs-lookup"><span data-stu-id="9b29a-134">**authEncryption (security)**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> </dl>

 

 
