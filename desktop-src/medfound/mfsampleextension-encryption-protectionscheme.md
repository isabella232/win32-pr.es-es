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
# <a name="mfsampleextension_encryption_protectionscheme-attribute"></a>MFSampleExtension \_ Encryption \_ ProtectionScheme Attribute

Especifica el esquema de protección para los ejemplos cifrados.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Observaciones

El valor de este atributo es un miembro de la enumeración [**MFSampleEncryptionProtectionScheme**](/windows/win32/api/mfapi/ne-mfapi-mfsampleencryptionprotectionscheme) . En los casos en los que el origen multimedia está basado en MP4, el valor se establece en función del valor del campo **\_ tipo de esquema** en el cuadro tipo de esquema (' SCHM ') en el encabezado MP4 (' Moov ' o ' moof ').

Si el campo de **\_ tipo de esquema** de un archivo basado en MP4, o secuencia, se establece en ' Cenc ' o ' cbc1 ', el atributo **MFSampleExtension \_ Encryption \_ ProtectionScheme** debe establecerse en el **esquema de protección \_ \_ AES \_ CTR** o en el **esquema de protección \_ \_ CBC**, respectivamente, y no se debe establecer ningún valor para [MFSampleExtension \_ Encryption \_ CryptByteBlock](mfsampleextension-encryption-cryptbyteblock.md) y [MFSampleExtension \_ Encryption \_ SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md).

Si el campo de **\_ tipo de esquema** de un archivo basado en MP4, o secuencia, se establece en ' Cens ' o ' CBCS ', el atributo **MFSampleExtension \_ Encryption \_ ProtectionScheme** debe establecerse en el **esquema de protección de \_ \_ AES \_ CTR** o en el **esquema de protección \_ \_ CBC**, respectivamente, y [MFSampleExtension \_ Encryption \_ CryptByteBlock](mfsampleextension-encryption-cryptbyteblock.md) y [MFSampleExtension \_ Encryption \_ SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md) se deben establecer con los valores del cuadro ' tenc '.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo establecer **el \_ \_ ProtectionScheme de cifrado MFSampleExtension** y los atributos asociados de cifrado **MFSampleExtension \_ \_ CryptByteBlock** y **MFSampleExtension \_ Encryption \_ SkipByteBlock** .


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



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



 

 
