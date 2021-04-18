---
description: Copia un certificado en una cadena codificada.
ms.assetid: bae7fb57-6b44-4aac-a635-b5b82de1f68d
title: 'ICertificate2:: Export (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Export
- ICertificate2.Export
- ICertificate.Export
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: aee48fe3d9ba56cba90c9645a3fb9752e3367a20
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671517"
---
# <a name="icertificate2export-method"></a><span data-ttu-id="a1edb-103">ICertificate2:: Export (método)</span><span class="sxs-lookup"><span data-stu-id="a1edb-103">ICertificate2::Export method</span></span>

<span data-ttu-id="a1edb-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a1edb-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="a1edb-105">En su lugar, use la [**clase X509Certificate2**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="a1edb-105">Instead, use the [**X509Certificate2 Class**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="a1edb-106">El método **Export** copia un certificado en una cadena codificada.</span><span class="sxs-lookup"><span data-stu-id="a1edb-106">The **Export** method copies a certificate to an encoded string.</span></span> <span data-ttu-id="a1edb-107">La cadena codificada puede escribirse en un archivo o importarse en un nuevo objeto de [**certificado**](certificate.md) .</span><span class="sxs-lookup"><span data-stu-id="a1edb-107">The encoded string can be written to a file or imported into a new [**Certificate**](certificate.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1edb-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a1edb-108">Syntax</span></span>


```VB
Certificate.Export( _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="a1edb-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a1edb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1edb-110">*EncodingType* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="a1edb-110">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a1edb-111">Valor de la enumeración de [**\_ \_ tipo de codificación CAPICOM**](capicom-encoding-type.md) que especifica el tipo de codificación de la operación de exportación.</span><span class="sxs-lookup"><span data-stu-id="a1edb-111">A value of the [**CAPICOM\_ENCODING\_TYPE**](capicom-encoding-type.md) enumeration that specifies the encoding type for the export operation.</span></span> <span data-ttu-id="a1edb-112">El valor predeterminado es **CAPICOM \_ encode \_ Base64**.</span><span class="sxs-lookup"><span data-stu-id="a1edb-112">The default value is **CAPICOM\_ENCODE\_BASE64**.</span></span> <span data-ttu-id="a1edb-113">En la siguiente tabla se muestran los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="a1edb-113">The following table shows the possible values.</span></span>



| <span data-ttu-id="a1edb-114">Valor</span><span class="sxs-lookup"><span data-stu-id="a1edb-114">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="a1edb-115">Significado</span><span class="sxs-lookup"><span data-stu-id="a1edb-115">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="a1edb-116"><dt>**CAPICOM \_ codificar \_ any**</dt></span><span class="sxs-lookup"><span data-stu-id="a1edb-116"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="a1edb-117">Este tipo de codificación solo se utiliza cuando los datos de entrada tienen un tipo de codificación desconocido.</span><span class="sxs-lookup"><span data-stu-id="a1edb-117">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="a1edb-118">Si este valor se usa para especificar el tipo de codificación de la salida, \_ se usará CAPICOM encode \_ Base64 en su lugar.</span><span class="sxs-lookup"><span data-stu-id="a1edb-118">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="a1edb-119">Introducido en CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="a1edb-119">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="a1edb-120"><dt>**CAPICOM, codificación \_ \_ Base64**</dt></span><span class="sxs-lookup"><span data-stu-id="a1edb-120"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="a1edb-121">Los datos se guardan como una cadena codificada en Base64.</span><span class="sxs-lookup"><span data-stu-id="a1edb-121">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="a1edb-122"><dt>**\_código binario de codificación de CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a1edb-122"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="a1edb-123">Los datos se guardan como una secuencia binaria pura.</span><span class="sxs-lookup"><span data-stu-id="a1edb-123">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1edb-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a1edb-124">Return value</span></span>

<span data-ttu-id="a1edb-125">Cadena que contiene el certificado exportado en el formato de codificación especificado.</span><span class="sxs-lookup"><span data-stu-id="a1edb-125">A string that contains the exported certificate in the specified encoding form.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1edb-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1edb-126">Requirements</span></span>



| <span data-ttu-id="a1edb-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1edb-127">Requirement</span></span> | <span data-ttu-id="a1edb-128">Value</span><span class="sxs-lookup"><span data-stu-id="a1edb-128">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1edb-129">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="a1edb-129">End of client support</span></span><br/> | <span data-ttu-id="a1edb-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a1edb-130">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="a1edb-131">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="a1edb-131">End of server support</span></span><br/> | <span data-ttu-id="a1edb-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a1edb-132">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="a1edb-133">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="a1edb-133">Redistributable</span></span><br/>       | <span data-ttu-id="a1edb-134">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="a1edb-134">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="a1edb-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a1edb-135">DLL</span></span><br/>                   | <dl> <span data-ttu-id="a1edb-136"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1edb-136"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1edb-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1edb-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1edb-138">Objetos de criptografía</span><span class="sxs-lookup"><span data-stu-id="a1edb-138">Cryptography Objects</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="a1edb-139">**Certificado**</span><span class="sxs-lookup"><span data-stu-id="a1edb-139">**Certificate**</span></span>](certificate.md)
</dt> </dl>

 

 
