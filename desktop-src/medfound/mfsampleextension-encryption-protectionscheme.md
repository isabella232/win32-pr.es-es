---
description: Especifica el esquema de protección para los ejemplos cifrados.
ms.assetid: 04E9F908-C61C-43DC-8CF5-9A629FCDD82C
title: MFSampleExtension_Encryption_ProtectionScheme atributo (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de298eb310e1258274a4ce24d49e9b53def38cde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155968"
---
# <a name="mfsampleextension_encryption_protectionscheme-attribute"></a><span data-ttu-id="53839-103">MFSampleExtension \_ Encryption \_ ProtectionScheme Attribute</span><span class="sxs-lookup"><span data-stu-id="53839-103">MFSampleExtension\_Encryption\_ProtectionScheme attribute</span></span>

<span data-ttu-id="53839-104">Especifica el esquema de protección para los ejemplos cifrados.</span><span class="sxs-lookup"><span data-stu-id="53839-104">Specifies the protection scheme for encrypted samples.</span></span>

## <a name="data-type"></a><span data-ttu-id="53839-105">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="53839-105">Data type</span></span>

<span data-ttu-id="53839-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="53839-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="53839-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="53839-107">Remarks</span></span>

<span data-ttu-id="53839-108">El valor de este atributo es un miembro de la enumeración [**MFSampleEncryptionProtectionScheme**](/windows/win32/api/mfapi/ne-mfapi-mfsampleencryptionprotectionscheme) .</span><span class="sxs-lookup"><span data-stu-id="53839-108">The value of this attribute is a member of the [**MFSampleEncryptionProtectionScheme**](/windows/win32/api/mfapi/ne-mfapi-mfsampleencryptionprotectionscheme) enumeration.</span></span> <span data-ttu-id="53839-109">En los casos en los que el origen multimedia está basado en MP4, el valor se establece en función del valor del campo **\_ tipo de esquema** en el cuadro tipo de esquema (' SCHM ') en el encabezado MP4 (' Moov ' o ' moof ').</span><span class="sxs-lookup"><span data-stu-id="53839-109">In cases where the media source is MP4-based, the value is set based off the value of the **scheme\_type** field within the scheme type box (‘schm’) in the MP4 header (‘moov’ or ‘moof’).</span></span>

<span data-ttu-id="53839-110">Si el campo de **\_ tipo de esquema** de un archivo basado en MP4, o secuencia, se establece en ' Cenc ' o ' cbc1 ', el atributo **MFSampleExtension \_ Encryption \_ ProtectionScheme** debe establecerse en el **esquema de protección \_ \_ AES \_ CTR** o en el **esquema de protección \_ \_ CBC**, respectivamente, y no se debe establecer ningún valor para [MFSampleExtension \_ Encryption \_ CryptByteBlock](mfsampleextension-encryption-cryptbyteblock.md) y [MFSampleExtension \_ Encryption \_ SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md).</span><span class="sxs-lookup"><span data-stu-id="53839-110">If the **scheme\_type** field in an MP4-based file, or stream, is set to ‘cenc’ or ‘cbc1’, then the **MFSampleExtension\_Encryption\_ProtectionScheme** attribute should be set to **PROTECTION\_SCHEME\_AES\_CTR** or **PROTECTION\_SCHEME\_CBC**, respectively, and no values should be set for [MFSampleExtension\_Encryption\_CryptByteBlock](mfsampleextension-encryption-cryptbyteblock.md) and [MFSampleExtension\_Encryption\_SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md).</span></span>

<span data-ttu-id="53839-111">Si el campo de **\_ tipo de esquema** de un archivo basado en MP4, o secuencia, se establece en ' Cens ' o ' CBCS ', el atributo **MFSampleExtension \_ Encryption \_ ProtectionScheme** debe establecerse en el **esquema de protección de \_ \_ AES \_ CTR** o en el **esquema de protección \_ \_ CBC**, respectivamente, y [MFSampleExtension \_ Encryption \_ CryptByteBlock](mfsampleextension-encryption-cryptbyteblock.md) y [MFSampleExtension \_ Encryption \_ SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md) se deben establecer con los valores del cuadro ' tenc '.</span><span class="sxs-lookup"><span data-stu-id="53839-111">If the **scheme\_type** field in an MP4-based file, or stream, is set to ‘cens’ or ‘cbcs’, then the **MFSampleExtension\_Encryption\_ProtectionScheme** attribute should be set to **PROTECTION\_SCHEME\_AES\_CTR** or **PROTECTION\_SCHEME\_CBC**, respectively, and [MFSampleExtension\_Encryption\_CryptByteBlock](mfsampleextension-encryption-cryptbyteblock.md) and [MFSampleExtension\_Encryption\_SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md) must be set using the values in the ‘tenc’ box.</span></span>

## <a name="examples"></a><span data-ttu-id="53839-112">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="53839-112">Examples</span></span>

<span data-ttu-id="53839-113">En el ejemplo siguiente se muestra cómo establecer **el \_ \_ ProtectionScheme de cifrado MFSampleExtension** y los atributos asociados de cifrado **MFSampleExtension \_ \_ CryptByteBlock** y **MFSampleExtension \_ Encryption \_ SkipByteBlock** .</span><span class="sxs-lookup"><span data-stu-id="53839-113">The following example shows how to set the **MFSampleExtension\_Encryption\_ProtectionScheme** and the associated **MFSampleExtension\_Encryption\_CryptByteBlock** and **MFSampleExtension\_Encryption\_SkipByteBlock** attributes.</span></span>


```C++
HRESULT AddEncryptionAttributes(_In_ IMFSample* pSample, _In_ bool fIsEncrypted)
{
      HRESULT hr = S_OK;

      if (fIsEncrypted)
    {
        //Set Encryption Protection Scheme
        hr = pSample->UINT32(MFSampleExtension_Encryption_ProtectionScheme,
            SAMPLE_ENCRYPTION_PROTECTION_SCHEME_AES_CBC);
            if (FAILED(hr))
                return hr;

        //Set the Initialization Vector (IV)
  //(spSampleEncryptionData is omitted from this example for simplicity.) 
        hr = pSample->SetBlob(MFSampleExtension_Encryption_SampleID, 
            (BYTE*)(spSampleEncryptionData->m_pInitializationVector),
            spSampleEncryptionData->m_bIVSize);
            if (FAILED(hr))
                return hr;

        //Set crypt and skip byte blocks for pattern encryption
        hr = pSample->SetUINT32(MFSampleExtension_Encryption_CryptByteBlock, 1);
            if (FAILED(hr))
                return hr;

        hr = pSample->SetUINT32(MFSampleExtension_Encryption_SkipByteBlock, 9);
            if (FAILED(hr))
                return hr;
    }
      return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="53839-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53839-114">Requirements</span></span>



| <span data-ttu-id="53839-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="53839-115">Requirement</span></span> | <span data-ttu-id="53839-116">Value</span><span class="sxs-lookup"><span data-stu-id="53839-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="53839-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53839-117">Minimum supported client</span></span><br/> | <span data-ttu-id="53839-118">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="53839-118">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="53839-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="53839-119">Minimum supported server</span></span><br/> | <span data-ttu-id="53839-120">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="53839-120">None supported</span></span><br/>                                                          |
| <span data-ttu-id="53839-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="53839-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="53839-122"><dt>Mfidl. h</dt></span><span class="sxs-lookup"><span data-stu-id="53839-122"><dt>Mfidl.h</dt></span></span> </dl> |



 

 
