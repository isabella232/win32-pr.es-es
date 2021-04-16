---
description: Descifra el contenido con doble cifrado.
ms.assetid: 717d0595-e8bb-4725-bd53-fc1281cbc8ee
title: EnvelopedData. Decrypt (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Decrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0c4c71ba0e3e0c2d421ad7bcbc9b1a61bb71d284
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649801"
---
# <a name="envelopeddatadecrypt-method"></a><span data-ttu-id="a82eb-103">EnvelopedData. Decrypt (método)</span><span class="sxs-lookup"><span data-stu-id="a82eb-103">EnvelopedData.Decrypt method</span></span>

<span data-ttu-id="a82eb-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a82eb-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="a82eb-105">En su lugar, use la [**clase EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="a82eb-105">Instead, use the [**EnvelopedCms Class**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="a82eb-106">El método de **descifrado** descifra el contenido con doble cifrado.</span><span class="sxs-lookup"><span data-stu-id="a82eb-106">The **Decrypt** method decrypts enveloped content.</span></span> <span data-ttu-id="a82eb-107">El descifrado se realiza si el destinatario del mensaje tiene acceso a la [*clave privada*](../secgloss/p-gly.md) emparejada con una de las [*claves públicas*](../secgloss/p-gly.md) que se usan para envolver el mensaje.</span><span class="sxs-lookup"><span data-stu-id="a82eb-107">Decryption is done if the recipient of the message has access to the [*private key*](../secgloss/p-gly.md) paired with one of the [*public keys*](../secgloss/p-gly.md) used to envelop the message.</span></span> <span data-ttu-id="a82eb-108">Al llamar al método **Decrypt** se restablece el [*Estado*](../secgloss/s-gly.md) del objeto.</span><span class="sxs-lookup"><span data-stu-id="a82eb-108">Calling the **Decrypt** method resets the [*state*](../secgloss/s-gly.md) of the object.</span></span> <span data-ttu-id="a82eb-109">Si el método de **descifrado** se realiza correctamente, la propiedad [**Content**](envelopeddata-content.md) del objeto [**EnvelopedData**](envelopeddata.md) se establece en el mensaje de texto simple.</span><span class="sxs-lookup"><span data-stu-id="a82eb-109">If the **Decrypt** method succeeds, the [**Content**](envelopeddata-content.md) property of the [**EnvelopedData**](envelopeddata.md) object is set to the plaintext message.</span></span>

## <a name="syntax"></a><span data-ttu-id="a82eb-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a82eb-110">Syntax</span></span>


```VB
EnvelopedData.Decrypt( _
  ByVal EnvelopedMessage _
)
```



## <a name="parameters"></a><span data-ttu-id="a82eb-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a82eb-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a82eb-112">*EnvelopedMessage* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="a82eb-112">*EnvelopedMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a82eb-113">Cadena que contiene los datos con doble cifrado que se van a descifrar.</span><span class="sxs-lookup"><span data-stu-id="a82eb-113">String that contains the enveloped data to be decrypted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a82eb-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a82eb-114">Return value</span></span>

<span data-ttu-id="a82eb-115">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="a82eb-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a82eb-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a82eb-116">Remarks</span></span>

<span data-ttu-id="a82eb-117">Los datos descifrados se convierten en el valor de la propiedad de [**contenido**](envelopeddata-content.md) para el objeto [**EnvelopedData**](envelopeddata.md) .</span><span class="sxs-lookup"><span data-stu-id="a82eb-117">The decrypted data becomes the [**Content**](envelopeddata-content.md) property value for the [**EnvelopedData**](envelopeddata.md) object.</span></span>

<span data-ttu-id="a82eb-118">Si el usuario de este método no tiene acceso a una clave privada que coincida con una de las claves públicas que se usan para envolver el mensaje, se produce un error en el método.</span><span class="sxs-lookup"><span data-stu-id="a82eb-118">If the user of this method does not have access to a private key that matches one of the public keys used to envelop the message, the method fails.</span></span> <span data-ttu-id="a82eb-119">Este método producirá un error si el certificado de la clave privada asociada no está en el almacén del equipo local o en el usuario actual.</span><span class="sxs-lookup"><span data-stu-id="a82eb-119">This method will fail if the certificate for the associated private key is not in either the local computer MY store or the current user MY store.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a82eb-120">Cuando se llama a este método desde un script Web, el script debe usar la [*clave privada*](../secgloss/p-gly.md) para descifrar los datos.</span><span class="sxs-lookup"><span data-stu-id="a82eb-120">When this method is called from a web script, the script needs to use your [*private key*](../secgloss/p-gly.md) to decrypt the data.</span></span> <span data-ttu-id="a82eb-121">Permitir a los sitios web que no son de confianza usar su clave privada es un riesgo para la seguridad.</span><span class="sxs-lookup"><span data-stu-id="a82eb-121">Allowing untrusted websites to use your private key is a security risk.</span></span> <span data-ttu-id="a82eb-122">Un cuadro de diálogo que pregunta si el sitio web puede usar su clave privada aparece cuando se llama por primera vez a este método.</span><span class="sxs-lookup"><span data-stu-id="a82eb-122">A dialog box that asks whether the website can use your private key appears when this method is first called.</span></span> <span data-ttu-id="a82eb-123">Si permite que el script use su clave privada y selecciona "no volver a preguntar", el cuadro de diálogo ya no aparecerá en ningún script que use la clave privada para descifrar los datos dentro de ese dominio.</span><span class="sxs-lookup"><span data-stu-id="a82eb-123">If you allow the script to use your private key and select "Do not ask me this again," the dialog box will no longer appear for any script that uses your private key to decrypt data within that domain.</span></span> <span data-ttu-id="a82eb-124">Sin embargo, los scripts fuera de ese dominio que intenten usar su clave privada para descifrar los datos seguirán generando este cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="a82eb-124">However, scripts outside that domain that attempt to use your private key to decrypt data will still cause this dialog box to appear.</span></span> <span data-ttu-id="a82eb-125">Si no permite que el script use su clave privada y selecciona "no volver a preguntar", se rechazará automáticamente la capacidad de usar la clave privada para descifrar los datos de los scripts dentro de ese dominio.</span><span class="sxs-lookup"><span data-stu-id="a82eb-125">If you do not allow the script to use your private key and select "Do not ask me this again," scripts within that domain will automatically be refused the ability to use your private key to decrypt data.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a82eb-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a82eb-126">Requirements</span></span>



| <span data-ttu-id="a82eb-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a82eb-127">Requirement</span></span> | <span data-ttu-id="a82eb-128">Value</span><span class="sxs-lookup"><span data-stu-id="a82eb-128">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a82eb-129">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="a82eb-129">End of client support</span></span><br/> | <span data-ttu-id="a82eb-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a82eb-130">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a82eb-131">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="a82eb-131">End of server support</span></span><br/> | <span data-ttu-id="a82eb-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a82eb-132">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a82eb-133">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="a82eb-133">Redistributable</span></span><br/>       | <span data-ttu-id="a82eb-134">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="a82eb-134">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a82eb-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a82eb-135">DLL</span></span><br/>                   | <dl> <span data-ttu-id="a82eb-136"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a82eb-136"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a82eb-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="a82eb-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a82eb-138">**Objetos de criptografía**</span><span class="sxs-lookup"><span data-stu-id="a82eb-138">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="a82eb-139">**EnvelopedData**</span><span class="sxs-lookup"><span data-stu-id="a82eb-139">**EnvelopedData**</span></span>](envelopeddata.md)
</dt> </dl>

 

 
