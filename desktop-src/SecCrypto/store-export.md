---
description: Copia el contenido de un almacén de certificados abierto en una cadena codificada.
ms.assetid: 00697579-f929-42ed-8e8e-5c970fe4465b
title: Store. Export (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Export
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: dbf4a2912cb62935447daa1589b6829c5a96488e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671404"
---
# <a name="storeexport-method"></a><span data-ttu-id="b4b99-103">Store. Export (método)</span><span class="sxs-lookup"><span data-stu-id="b4b99-103">Store.Export method</span></span>

<span data-ttu-id="b4b99-104">\[El método de **exportación** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos.</span><span class="sxs-lookup"><span data-stu-id="b4b99-104">\[The **Export** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="b4b99-105">En su lugar, use la [**clase X509Store**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="b4b99-105">Instead, use the [**X509Store Class**](/previous-versions/windows/embedded/hh424027(v=msdn.10)) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="b4b99-106">El método **Export** copia el contenido de un [*almacén de certificados*](../secgloss/c-gly.md) abierto en una cadena codificada.</span><span class="sxs-lookup"><span data-stu-id="b4b99-106">The **Export** method copies the contents of an open [*certificate store*](../secgloss/c-gly.md) to an encoded string.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4b99-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b4b99-107">Syntax</span></span>


```VB
Store.Export( _
  [ ByVal SaveAs ], _
  [ ByVal EncodingType ] _
)
```



## <a name="parameters"></a><span data-ttu-id="b4b99-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b4b99-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4b99-109">*Guardar como* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b4b99-109">*SaveAs* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b4b99-110">Un valor de la enumeración de [ \_ \_ Guardar \_ como \_ tipo de almacenamiento de CAPICOM](capicom-store-save-as-type.md) que indica el formato de la operación de exportación.</span><span class="sxs-lookup"><span data-stu-id="b4b99-110">A value of the [CAPICOM\_STORE\_SAVE\_AS\_TYPE](capicom-store-save-as-type.md) enumeration that indicates the format for the export operation.</span></span> <span data-ttu-id="b4b99-111">El valor predeterminado es CAPICOM \_ Store \_ Save \_ como \_ serializado.</span><span class="sxs-lookup"><span data-stu-id="b4b99-111">The default value is CAPICOM\_STORE\_SAVE\_AS\_SERIALIZED.</span></span> <span data-ttu-id="b4b99-112">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="b4b99-112">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="b4b99-113">Valor</span><span class="sxs-lookup"><span data-stu-id="b4b99-113">Value</span></span>                                                                                                                                                                                                                     | <span data-ttu-id="b4b99-114">Significado</span><span class="sxs-lookup"><span data-stu-id="b4b99-114">Meaning</span></span>                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="CAPICOM_STORE_SAVE_AS_SERIALIZED"></span><span id="capicom_store_save_as_serialized"></span><dl> <span data-ttu-id="b4b99-115"><dt>**el \_ almacén \_ de CAPICOM se guardó \_ como \_ serializado**</dt></span><span class="sxs-lookup"><span data-stu-id="b4b99-115"><dt>**CAPICOM\_STORE\_SAVE\_AS\_SERIALIZED**</dt></span></span> </dl> | <span data-ttu-id="b4b99-116">El almacén se guarda en formato serializado.</span><span class="sxs-lookup"><span data-stu-id="b4b99-116">The store is saved in serialized format.</span></span><br/> |
| <span id="CAPICOM_STORE_SAVE_AS_PKCS7"></span><span id="capicom_store_save_as_pkcs7"></span><dl> <span data-ttu-id="b4b99-117"><dt>**El \_ almacén \_ de CAPICOM se guarda \_ como \_ pkcs7**</dt></span><span class="sxs-lookup"><span data-stu-id="b4b99-117"><dt>**CAPICOM\_STORE\_SAVE\_AS\_PKCS7**</dt></span></span> </dl>                | <span data-ttu-id="b4b99-118">El almacén se guarda en \# formato PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="b4b99-118">The store is saved in PKCS \#7 format.</span></span><br/>   |



 

</dd> <dt>

<span data-ttu-id="b4b99-119">*EncodingType* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b4b99-119">*EncodingType* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b4b99-120">Un valor de la enumeración de [ \_ \_ tipo de codificación CAPICOM](capicom-encoding-type.md) que indica el tipo de codificación del almacén exportado.</span><span class="sxs-lookup"><span data-stu-id="b4b99-120">A value of the [CAPICOM\_ENCODING\_TYPE](capicom-encoding-type.md) enumeration that indicates the encoding type of the exported store.</span></span> <span data-ttu-id="b4b99-121">El valor predeterminado es CAPICOM \_ encode \_ Base64.</span><span class="sxs-lookup"><span data-stu-id="b4b99-121">The default value is CAPICOM\_ENCODE\_BASE64.</span></span> <span data-ttu-id="b4b99-122">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="b4b99-122">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="b4b99-123">Valor</span><span class="sxs-lookup"><span data-stu-id="b4b99-123">Value</span></span>                                                                                                                                                                                  | <span data-ttu-id="b4b99-124">Significado</span><span class="sxs-lookup"><span data-stu-id="b4b99-124">Meaning</span></span>                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCODE_ANY"></span><span id="capicom_encode_any"></span><dl> <span data-ttu-id="b4b99-125"><dt>**CAPICOM \_ codificar \_ any**</dt></span><span class="sxs-lookup"><span data-stu-id="b4b99-125"><dt>**CAPICOM\_ENCODE\_ANY**</dt></span></span> </dl>          | <span data-ttu-id="b4b99-126">Este tipo de codificación solo se utiliza cuando los datos de entrada tienen un tipo de codificación desconocido.</span><span class="sxs-lookup"><span data-stu-id="b4b99-126">This encoding type is used only when the input data has an unknown encoding type.</span></span> <span data-ttu-id="b4b99-127">Si este valor se usa para especificar el tipo de codificación de la salida, \_ se usará CAPICOM encode \_ Base64 en su lugar.</span><span class="sxs-lookup"><span data-stu-id="b4b99-127">If this value is used to specify the output's encoding type, CAPICOM\_ENCODE\_BASE64 will be used instead.</span></span> <span data-ttu-id="b4b99-128">Introducido en CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="b4b99-128">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_ENCODE_BASE64"></span><span id="capicom_encode_base64"></span><dl> <span data-ttu-id="b4b99-129"><dt>**CAPICOM, codificación \_ \_ Base64**</dt></span><span class="sxs-lookup"><span data-stu-id="b4b99-129"><dt>**CAPICOM\_ENCODE\_BASE64**</dt></span></span> </dl> | <span data-ttu-id="b4b99-130">Los datos se guardan como una cadena codificada en Base64.</span><span class="sxs-lookup"><span data-stu-id="b4b99-130">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                                                               |
| <span id="CAPICOM_ENCODE_BINARY"></span><span id="capicom_encode_binary"></span><dl> <span data-ttu-id="b4b99-131"><dt>**\_código binario de codificación de CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b4b99-131"><dt>**CAPICOM\_ENCODE\_BINARY**</dt></span></span> </dl> | <span data-ttu-id="b4b99-132">Los datos se guardan como una secuencia binaria pura.</span><span class="sxs-lookup"><span data-stu-id="b4b99-132">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4b99-133">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b4b99-133">Return value</span></span>

<span data-ttu-id="b4b99-134">Este método devuelve una cadena que contiene los certificados del almacén en el formato de codificación especificado.</span><span class="sxs-lookup"><span data-stu-id="b4b99-134">This method returns a string that contains the certificates in the store in the specified encoding form.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4b99-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4b99-135">Requirements</span></span>



| <span data-ttu-id="b4b99-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4b99-136">Requirement</span></span> | <span data-ttu-id="b4b99-137">Value</span><span class="sxs-lookup"><span data-stu-id="b4b99-137">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4b99-138">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="b4b99-138">Redistributable</span></span><br/> | <span data-ttu-id="b4b99-139">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="b4b99-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="b4b99-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b4b99-140">DLL</span></span><br/>             | <dl> <span data-ttu-id="b4b99-141"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4b99-141"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4b99-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="b4b99-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4b99-143">**Store**</span><span class="sxs-lookup"><span data-stu-id="b4b99-143">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="b4b99-144">**Objetos de criptografía**</span><span class="sxs-lookup"><span data-stu-id="b4b99-144">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> </dl>

 

 
