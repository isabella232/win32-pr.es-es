---
description: Firma el archivo especificado.
ms.assetid: 5a59e663-057b-4380-aa14-536030e4051d
title: SignerSign función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerSign
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 9aa8ecc15e38c4a502b363898d5845cba5b0e47e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687908"
---
# <a name="signersign-function"></a>SignerSign función)

La función **SignerSign** firma el archivo especificado.

> [!Note]  
> Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación. Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI SignerSign(
  _In_     SIGNER_SUBJECT_INFO   *pSubjectInfo,
  _In_     SIGNER_CERT           *pSignerCert,
  _In_     SIGNER_SIGNATURE_INFO *pSignatureInfo,
  _In_opt_ SIGNER_PROVIDER_INFO  *pProviderInfo,
  _In_opt_ LPCWSTR               pwszHttpTimeStamp,
  _In_opt_ PCRYPT_ATTRIBUTES     psRequest,
  _In_opt_ LPVOID                pSipData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSubjectInfo* \[ de\]
</dt> <dd>

Puntero a una estructura de [**\_ \_ información de asunto del firmante**](signer-subject-info.md) que especifica el sujeto que se va a firmar.

</dd> <dt>

*pSignerCert* \[ de\]
</dt> <dd>

Puntero a una estructura de [**\_ certificado de firmante**](signer-cert.md) que especifica el certificado que se va a utilizar para crear la firma digital.

</dd> <dt>

*pSignatureInfo* \[ de\]
</dt> <dd>

Puntero a una estructura de [**\_ \_ información de firma de firmante**](signer-signature-info.md) que contiene información sobre la firma digital.

</dd> <dt>

*pProviderInfo* \[ en, opcional\]
</dt> <dd>

Puntero a una estructura de [**\_ \_ información del proveedor de firmante**](signer-provider-info.md) que especifica el proveedor de [*servicios criptográficos*](../secgloss/c-gly.md) (CSP) y la información de [*clave privada*](../secgloss/p-gly.md) que se usa para crear la firma digital.

Si el valor de este parámetro es **null**, el valor del parámetro *pSignerCert* debe especificar un certificado asociado a un CSP.

</dd> <dt>

*pwszHttpTimeStamp* \[ en, opcional\]
</dt> <dd>

Dirección URL de un servidor de marca de tiempo.

</dd> <dt>

*psRequest* \[ en, opcional\]
</dt> <dd>

Puntero a una matriz de estructuras [**de \_ atributo de cifrado**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) que se agregan a una solicitud de firma. Este parámetro se omite si el parámetro *pwszHttpTimeStamp* no contiene un valor válido que no sea **null**.

</dd> <dt>

*pSipData* \[ en, opcional\]
</dt> <dd>

Valor de 32 bits que se pasa como datos adicionales a las funciones de SIP. El proveedor SIP define el formato y el contenido de este.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, la función devuelve S \_ OK.

Si se produce un error en la función, devuelve un valor **HRESULT** que indica el error. Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SignerSignEx**](signersignex.md)
</dt> </dl>

 

 
