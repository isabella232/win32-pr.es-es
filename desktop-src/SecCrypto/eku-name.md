---
description: Establece o recupera un valor de enumeración que especifica el nombre de CAPICOM del EKU. Esta es la propiedad predeterminada.
ms.assetid: afce5553-ef18-4a7f-b1c8-fbe00d3277e0
title: 'IEKU:: Name (propiedad)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEKU.Name
- IEKU.get_Name
- IEKU.put_Name
- EKU.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e0e28a8816d7e4c4f44e3cd1ec0dc479372d66d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649995"
---
# <a name="iekuname-property"></a><span data-ttu-id="5b6ea-104">IEKU:: Name (propiedad)</span><span class="sxs-lookup"><span data-stu-id="5b6ea-104">IEKU::Name property</span></span>

<span data-ttu-id="5b6ea-105">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="5b6ea-105">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="5b6ea-106">En su lugar, use la [**clase X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="5b6ea-106">Instead, use the [**X509EnhancedKeyUsageExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="5b6ea-107">La propiedad **Name** establece o recupera un valor de enumeración que especifica el nombre de CAPICOM del EKU.</span><span class="sxs-lookup"><span data-stu-id="5b6ea-107">The **Name** property sets or retrieves an enumeration value that specifies the CAPICOM name of the EKU.</span></span> <span data-ttu-id="5b6ea-108">Esta es la propiedad predeterminada.</span><span class="sxs-lookup"><span data-stu-id="5b6ea-108">This is the default property.</span></span>

<span data-ttu-id="5b6ea-109">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="5b6ea-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b6ea-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5b6ea-110">Syntax</span></span>


```VB
EKU.Name As CAPICOM_EKU
```



## <a name="property-value"></a><span data-ttu-id="5b6ea-111">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="5b6ea-111">Property value</span></span>

<span data-ttu-id="5b6ea-112">Un valor de la enumeración de [**\_ EKU de CAPICOM**](capicom-eku.md) que especifica el nombre de CAPICOM del EKU.</span><span class="sxs-lookup"><span data-stu-id="5b6ea-112">A value of the [**CAPICOM\_EKU**](capicom-eku.md) enumeration that specifies the CAPICOM name of the EKU.</span></span> <span data-ttu-id="5b6ea-113">En la siguiente tabla se muestran los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="5b6ea-113">The following table shows the possible values.</span></span>



| <span data-ttu-id="5b6ea-114">Valor</span><span class="sxs-lookup"><span data-stu-id="5b6ea-114">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="5b6ea-115">Significado</span><span class="sxs-lookup"><span data-stu-id="5b6ea-115">Meaning</span></span>                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_EKU_OTHER"></span><span id="capicom_eku_other"></span><dl> <span data-ttu-id="5b6ea-116"><dt>**EKU de CAPICOM \_ \_ otro**</dt></span><span class="sxs-lookup"><span data-stu-id="5b6ea-116"><dt>**CAPICOM\_EKU\_OTHER**</dt></span></span> </dl>                                                      | <span data-ttu-id="5b6ea-117">El certificado tiene usos definidos en la directiva local.</span><span class="sxs-lookup"><span data-stu-id="5b6ea-117">Certificate has uses defined in local policy.</span></span> <span data-ttu-id="5b6ea-118">Se usa si el EKU necesario no está predefinido y la aplicación debe establecer el valor de OID.</span><span class="sxs-lookup"><span data-stu-id="5b6ea-118">This is used if the EKU needed is not predefined and the OID value must be set by the application.</span></span><br/> |
| <span id="CAPICOM_EKU_SERVER_AUTH"></span><span id="capicom_eku_server_auth"></span><dl> <span data-ttu-id="5b6ea-119"><dt>**\_autenticación del \_ servidor \_ EKU de CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="5b6ea-119"><dt>**CAPICOM\_EKU\_SERVER\_AUTH**</dt></span></span> </dl>                                   | <span data-ttu-id="5b6ea-120">El certificado se puede usar para autenticar un servidor.</span><span class="sxs-lookup"><span data-stu-id="5b6ea-120">Certificate can be used to authenticate a server.</span></span><br/>                                                                                                |
| <span id="CAPICOM_EKU_CLIENT_AUTH"></span><span id="capicom_eku_client_auth"></span><dl> <span data-ttu-id="5b6ea-121"><dt>**\_autenticación de \_ cliente de EKU de CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5b6ea-121"><dt>**CAPICOM\_EKU\_CLIENT\_AUTH**</dt></span></span> </dl>                                   | <span data-ttu-id="5b6ea-122">El certificado se puede utilizar para autenticar a un cliente.</span><span class="sxs-lookup"><span data-stu-id="5b6ea-122">Certificate can be used to authenticate a client.</span></span><br/>                                                                                                |
| <span id="CAPICOM_EKU_CODE_SIGNING"></span><span id="capicom_eku_code_signing"></span><dl> <span data-ttu-id="5b6ea-123"><dt>**\_firma de \_ código \_ EKU de CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="5b6ea-123"><dt>**CAPICOM\_EKU\_CODE\_SIGNING**</dt></span></span> </dl>                                | <span data-ttu-id="5b6ea-124">El certificado se puede utilizar para crear una firma digital.</span><span class="sxs-lookup"><span data-stu-id="5b6ea-124">Certificate can be used to create a digital signature.</span></span><br/>                                                                                           |
| <span id="CAPICOM_EKU_EMAIL_PROTECTION"></span><span id="capicom_eku_email_protection"></span><dl> <span data-ttu-id="5b6ea-125"><dt>**\_protección de \_ correo electrónico de EKU de CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5b6ea-125"><dt>**CAPICOM\_EKU\_EMAIL\_PROTECTION**</dt></span></span> </dl>                    | <span data-ttu-id="5b6ea-126">El certificado se puede usar para la protección de correo electrónico.</span><span class="sxs-lookup"><span data-stu-id="5b6ea-126">Certificate can be used for email protection.</span></span><br/>                                                                                                    |
| <span id="CAPICOM_EKU_SMARTCARD_LOGON"></span><span id="capicom_eku_smartcard_logon"></span><dl> <span data-ttu-id="5b6ea-127"><dt>**\_Inicio de \_ sesión con tarjeta inteligente EKU de CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5b6ea-127"><dt>**CAPICOM\_EKU\_SMARTCARD\_LOGON**</dt></span></span> </dl>                       | <span data-ttu-id="5b6ea-128">El certificado se puede usar para el inicio de sesión con tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="5b6ea-128">Certificate can be used for smart card logon.</span></span> <span data-ttu-id="5b6ea-129">Introducido en CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="5b6ea-129">Introduced in CAPICOM 2.0.</span></span><br/>                                                                         |
| <span id="CAPICOM_EKU_ENCRYPTING_FILE_SYSTEM"></span><span id="capicom_eku_encrypting_file_system"></span><dl> <span data-ttu-id="5b6ea-130"><dt>**\_sistema de \_ cifrado de \_ archivos \_ EKU de CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="5b6ea-130"><dt>**CAPICOM\_EKU\_ENCRYPTING\_FILE\_SYSTEM**</dt></span></span> </dl> | <span data-ttu-id="5b6ea-131">El certificado se puede usar para EFS.</span><span class="sxs-lookup"><span data-stu-id="5b6ea-131">Certificate can be used for EFS.</span></span> <span data-ttu-id="5b6ea-132">Introducido en CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="5b6ea-132">Introduced in CAPICOM 2.0.</span></span><br/>                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="5b6ea-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5b6ea-133">Remarks</span></span>

<span data-ttu-id="5b6ea-134">Cuando el valor de esta propiedad se restablece, directa o indirectamente, se restablece el [*Estado*](../secgloss/s-gly.md) completo del objeto.</span><span class="sxs-lookup"><span data-stu-id="5b6ea-134">When the value of this property is reset, directly or indirectly, the whole [*state*](../secgloss/s-gly.md) of the object is reset.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b6ea-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b6ea-135">Requirements</span></span>



| <span data-ttu-id="5b6ea-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="5b6ea-136">Requirement</span></span> | <span data-ttu-id="5b6ea-137">Value</span><span class="sxs-lookup"><span data-stu-id="5b6ea-137">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b6ea-138">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="5b6ea-138">End of client support</span></span><br/> | <span data-ttu-id="5b6ea-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5b6ea-139">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="5b6ea-140">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="5b6ea-140">End of server support</span></span><br/> | <span data-ttu-id="5b6ea-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5b6ea-141">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="5b6ea-142">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="5b6ea-142">Redistributable</span></span><br/>       | <span data-ttu-id="5b6ea-143">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="5b6ea-143">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="5b6ea-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5b6ea-144">DLL</span></span><br/>                   | <dl> <span data-ttu-id="5b6ea-145"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b6ea-145"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
