---
description: Firma el archivo especificado.
ms.assetid: 5a59e663-057b-4380-aa14-536030e4051d
title: Función SignerSign
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173105"
---
# <a name="signersign-function"></a>Función SignerSign

La **función SignerSign** firma el archivo especificado.

> [!Note]  
> Esta función no tiene ningún archivo de encabezado asociado ni biblioteca de importación. Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.

 

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

*pSubjectInfo* \[ En\]
</dt> <dd>

Puntero a una estructura [**SIGNER \_ SUBJECT \_ INFO**](signer-subject-info.md) que especifica el firmante.

</dd> <dt>

*pSignerCert* \[ En\]
</dt> <dd>

Puntero a una [**estructura SIGNER \_ CERT**](signer-cert.md) que especifica el certificado que se usará para crear la firma digital.

</dd> <dt>

*pSignatureInfo* \[ En\]
</dt> <dd>

Puntero a una estructura [**SIGNER \_ SIGNATURE \_ INFO**](signer-signature-info.md) que contiene información sobre la firma digital.

</dd> <dt>

*pProviderInfo* \[ in, opcional\]
</dt> <dd>

Puntero a una estructura [**SIGNER \_ PROVIDER \_ INFO**](signer-provider-info.md) que especifica el proveedor de servicios criptográficos [*(CSP)*](../secgloss/c-gly.md) y la [*información*](../secgloss/p-gly.md) de clave privada que se usa para crear la firma digital.

Si el valor de este parámetro es **NULL,** el valor del parámetro *pSignerCert* debe especificar un certificado asociado a un CSP.

</dd> <dt>

*pwszHttpTimeStamp* \[ in, opcional\]
</dt> <dd>

Dirección URL de un servidor de marca de tiempo.

</dd> <dt>

*psRequest* \[ in, opcional\]
</dt> <dd>

Puntero a una matriz de estructuras [**CRYPT \_ ATTRIBUTE**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) que se agregan a una solicitud de firma. Este parámetro se omite si el *parámetro pwszHttpTimeStamp* no contiene un valor válido que no sea **NULL.**

</dd> <dt>

*pSipData* \[ in, opcional\]
</dt> <dd>

Valor de 32 bits que se pasa como datos adicionales a las funciones de SIP. El proveedor DE SIP define el formato y el contenido de este.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, la función devuelve S \_ OK.

Si se produce un error en la función, devuelve un **valor HRESULT** que indica el error. Para obtener una lista de códigos de error comunes, vea [Common HRESULT Values](common-hresult-values.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SignerSignEx**](signersignex.md)
</dt> </dl>

 

 
