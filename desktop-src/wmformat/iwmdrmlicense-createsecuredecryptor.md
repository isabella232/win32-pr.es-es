---
title: Método IWMDRMLicense CreateSecureDecryptor (wmdrmsdk. h)
description: El método CreateSecureDecryptor crea un objeto descifrador seguro. El descifrador seguro difiere del descifrador normal en que descifra el contenido y, a continuación, lo vuelve a cifrar según la configuración especificada en los parámetros de este método.
ms.assetid: f3fe8d47-ec7b-4ba5-b5ae-6262cb455ffc
keywords:
- Método CreateSecureDecryptor formato de Windows Media
- Método CreateSecureDecryptor formato de Windows Media, interfaz IWMDRMLicense
- Interfaz IWMDRMLicense formato de Windows Media, método CreateSecureDecryptor
topic_type:
- apiref
api_name:
- IWMDRMLicense.CreateSecureDecryptor
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ededb4c985e345c1e40563d02c87bfe447b8960f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708168"
---
# <a name="iwmdrmlicensecreatesecuredecryptor-method"></a><span data-ttu-id="681c5-107">IWMDRMLicense:: CreateSecureDecryptor (método)</span><span class="sxs-lookup"><span data-stu-id="681c5-107">IWMDRMLicense::CreateSecureDecryptor method</span></span>

<span data-ttu-id="681c5-108">El método **CreateSecureDecryptor** crea un objeto descifrador seguro.</span><span class="sxs-lookup"><span data-stu-id="681c5-108">The **CreateSecureDecryptor** method creates a secure decryptor object.</span></span> <span data-ttu-id="681c5-109">El descifrador seguro difiere del descifrador normal en que descifra el contenido y, a continuación, lo vuelve a cifrar según la configuración especificada en los parámetros de este método.</span><span class="sxs-lookup"><span data-stu-id="681c5-109">The secure decryptor differs from the normal decryptor in that it decrypts the content and then re-encrypts it according to the settings specified in the parameters of this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="681c5-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="681c5-110">Syntax</span></span>


```C++
HRESULT CreateSecureDecryptor(
  [in]      BYTE          *pbCertificate,
  [in]      DWORD         cbCertificate,
  [in]      DWORD         dwCertificateType,
  [in]      DWORD         dwFlags,
  [out]     BYTE          *pbInitializationVector,
  [in, out] DWORD         *pcbInitializationVector,
  [out]     IWMDRMDecrypt **ppDecryptor
);
```



## <a name="parameters"></a><span data-ttu-id="681c5-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="681c5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="681c5-112">*pbCertificate* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="681c5-112">*pbCertificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="681c5-113">Certificado de la aplicación que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="681c5-113">Certificate of the calling application.</span></span>

</dd> <dt>

<span data-ttu-id="681c5-114">*cbCertificate* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="681c5-114">*cbCertificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="681c5-115">Tamaño del certificado en bytes.</span><span class="sxs-lookup"><span data-stu-id="681c5-115">Size of the certificate in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="681c5-116">*dwCertificateType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="681c5-116">*dwCertificateType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="681c5-117">Tipo del certificado.</span><span class="sxs-lookup"><span data-stu-id="681c5-117">The type of the certificate.</span></span> <span data-ttu-id="681c5-118">Establezca en \_ tipo de certificado WMDRM \_ \_ xml.</span><span class="sxs-lookup"><span data-stu-id="681c5-118">Set to WMDRM\_CERTIFICATE\_TYPE\_XML.</span></span>

</dd> <dt>

<span data-ttu-id="681c5-119">*dwFlags* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="681c5-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="681c5-120">El tipo de protección de sesión que se va a usar para la recodificación.</span><span class="sxs-lookup"><span data-stu-id="681c5-120">The type of session protection to use for re-encoding.</span></span> <span data-ttu-id="681c5-121">Debe establecerse en una de las constantes de la tabla siguiente:</span><span class="sxs-lookup"><span data-stu-id="681c5-121">Must be set to one of the constants in the following table:</span></span>



| <span data-ttu-id="681c5-122">Constante</span><span class="sxs-lookup"><span data-stu-id="681c5-122">Constant</span></span>                     | <span data-ttu-id="681c5-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="681c5-123">Description</span></span>                                                                                                 |
|------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="681c5-124">Tipo de protección de WMDRM \_ \_ \_ RC4</span><span class="sxs-lookup"><span data-stu-id="681c5-124">WMDRM\_PROTECTION\_TYPE\_RC4</span></span> | <span data-ttu-id="681c5-125">Usa el cifrado RC4 para el cifrado de sesión.</span><span class="sxs-lookup"><span data-stu-id="681c5-125">Uses RC4 encryption for session encryption.</span></span> <span data-ttu-id="681c5-126">Esta es la única protección de sesión compatible para esta versión.</span><span class="sxs-lookup"><span data-stu-id="681c5-126">This is the only supported session protection for this version.</span></span> |



 

</dd> <dt>

<span data-ttu-id="681c5-127">*pbInitializationVector* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="681c5-127">*pbInitializationVector* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="681c5-128">Recibe el vector de inicialización.</span><span class="sxs-lookup"><span data-stu-id="681c5-128">Receives the initialization vector.</span></span> <span data-ttu-id="681c5-129">El vector de inicialización es RSA cifrado mediante el esquema de relleno OAEP con la clave pública RSA que se encuentra en el certificado.</span><span class="sxs-lookup"><span data-stu-id="681c5-129">The initialization vector is RSA encrypted using the OAEP padding scheme with the RSA public key found in the certificate.</span></span> <span data-ttu-id="681c5-130">Establezca en **null** para recibir el tamaño de búfer necesario en *pcbInitializationVector*.</span><span class="sxs-lookup"><span data-stu-id="681c5-130">Set to **NULL** to receive the required buffer size in *pcbInitializationVector*.</span></span>

</dd> <dt>

<span data-ttu-id="681c5-131">*pcbInitializationVector* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="681c5-131">*pcbInitializationVector* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="681c5-132">En la entrada, el tamaño del búfer pasado como *pbInitializationVector*.</span><span class="sxs-lookup"><span data-stu-id="681c5-132">On input, the size of the buffer passed as *pbInitializationVector*.</span></span> <span data-ttu-id="681c5-133">En la salida, tamaño de la parte utilizada del búfer.</span><span class="sxs-lookup"><span data-stu-id="681c5-133">On output, the size of the used portion of the buffer.</span></span> <span data-ttu-id="681c5-134">Si pasa **null** para *pbInitializationVector*, este valor se establece en el tamaño de búfer necesario en la salida.</span><span class="sxs-lookup"><span data-stu-id="681c5-134">If you pass **NULL** for *pbInitializationVector*, this value is set to the required buffer size on output.</span></span>

</dd> <dt>

<span data-ttu-id="681c5-135">*ppDecryptor* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="681c5-135">*ppDecryptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="681c5-136">Recibe un puntero a la interfaz [**IWMDRMDecrypt**](iwmdrmdecrypt.md) del objeto recién creado.</span><span class="sxs-lookup"><span data-stu-id="681c5-136">Receives a pointer to the [**IWMDRMDecrypt**](iwmdrmdecrypt.md) interface of the newly created object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="681c5-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="681c5-137">Return value</span></span>

<span data-ttu-id="681c5-138">El método devuelve un **valor HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="681c5-138">The method returns an **HRESULT**.</span></span> <span data-ttu-id="681c5-139">Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.</span><span class="sxs-lookup"><span data-stu-id="681c5-139">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="681c5-140">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="681c5-140">Return code</span></span>                                                                          | <span data-ttu-id="681c5-141">Descripción</span><span class="sxs-lookup"><span data-stu-id="681c5-141">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="681c5-142"><dt>**S \_ correcto**</dt></span><span class="sxs-lookup"><span data-stu-id="681c5-142"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="681c5-143">El método se ha llevado a cabo de forma correcta.</span><span class="sxs-lookup"><span data-stu-id="681c5-143">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="681c5-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="681c5-144">Remarks</span></span>

<span data-ttu-id="681c5-145">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="681c5-145">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="681c5-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="681c5-146">Requirements</span></span>



| <span data-ttu-id="681c5-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="681c5-147">Requirement</span></span> | <span data-ttu-id="681c5-148">Value</span><span class="sxs-lookup"><span data-stu-id="681c5-148">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="681c5-149">Encabezado</span><span class="sxs-lookup"><span data-stu-id="681c5-149">Header</span></span><br/> | <dl> <span data-ttu-id="681c5-150"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="681c5-150"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="681c5-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="681c5-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="681c5-152">**Interfaz IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="681c5-152">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





