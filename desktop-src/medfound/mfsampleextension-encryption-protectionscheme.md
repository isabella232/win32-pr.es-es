---
description: Especifica el esquema de protección para las muestras cifradas.
ms.assetid: 04E9F908-C61C-43DC-8CF5-9A629FCDD82C
title: MFSampleExtension_Encryption_ProtectionScheme atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a9db7d00d67b0e9806167ea574d10c3dca5f199293c03f5e055d60430c2dd75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119603185"
---
# <a name="mfsampleextension_encryption_protectionscheme-attribute"></a>MfSampleExtension \_ Encryption \_ ProtectionScheme attribute

Especifica el esquema de protección para las muestras cifradas.

## <a name="data-type"></a>Tipo de datos

**UINT32**

## <a name="remarks"></a>Comentarios

El valor de este atributo es un miembro de la [**enumeración MFSampleEncryptionProtectionScheme.**](/windows/win32/api/mfapi/ne-mfapi-mfsampleencryptionprotectionscheme) En los casos en los que el origen de medios se **\_** basa en MP4, el valor se establece en función del valor del campo de tipo de esquema dentro del cuadro de tipo de esquema (''falta') en el encabezado MP4 ('moov' o 'moof').

Si **\_** el campo de tipo de esquema de un archivo basado en MP4, o secuencia, se establece en "cenc" o "cbc1", el atributo **MFSampleExtension \_ Encryption \_ ProtectionScheme** debe establecerse en PROTECTION **SCHEME \_ \_ AES \_ CTR** o **PROTECTION SCHEME \_ \_ CBC**, respectivamente, y no se debe establecer ningún valor para [MFSampleExtension \_ Encryption \_ CryptByteBlock](mfsampleextension-encryption-cryptbyteblock.md) y [MFSampleExtension \_ Encryption \_ SkipByteBlock.](mfsampleextension-encryption-skipbyteblock.md)

Si **\_** el campo de tipo de esquema de un archivo basado en MP4, o secuencia, se establece en "cens" o "cbcs", el atributo **MFSampleExtension \_ Encryption \_ ProtectionScheme** debe establecerse en PROTECTION **SCHEME \_ \_ AES \_ CTR** o **PROTECTION SCHEME \_ \_ CBC**, respectivamente, y [MFSampleExtension \_ Encryption \_ CryptByteBlock](mfsampleextension-encryption-cryptbyteblock.md) y [MFSampleExtension \_ Encryption \_ SkipByteBlock](mfsampleextension-encryption-skipbyteblock.md) deben establecerse con los valores del cuadro "tenc".

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo establecer los atributos **MFSampleExtension \_ Encryption \_ ProtectionScheme** y **MFSampleExtension \_ Encryption \_ CryptByteBlock** y **MFSampleExtension \_ Encryption \_ SkipByteBlock** asociados.


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



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, versión 1709 \[ solo aplicaciones de escritorio\]<br/>                          |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                          |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



 

 
