---
description: Firma y marca de tiempo el archivo especificado, lo que permite varias firmas anidadas.
ms.assetid: 216EFFCF-CD23-484A-ADBF-94B5AD52289F
title: Función SignerSignEx2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerSignEx2
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: a03d326969ce1f447dc82708792bd3761e02a823
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127270879"
---
# <a name="signersignex2-function"></a>Función SignerSignEx2

La **función SignerSignEx2** firma y marca de tiempo el archivo especificado, lo que permite varias firmas anidadas.

> [!Note]  
> Esta función no tiene ningún archivo de encabezado asociado ni biblioteca de importación. Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI SignerSignEx2(
  _In_       DWORD                  dwFlags,
  _In_       SIGNER_SUBJECT_INFO    *pSubjectInfo,
  _In_       SIGNER_CERT            *pSignerCert,
  _In_       SIGNER_SIGNATURE_INFO  *pSignatureInfo,
  _In_opt_   SIGNER_PROVIDER_INFO   *pProviderInfo,
  _In_opt_   DWORD                  dwTimestampFlags,
  _In_opt_   PCSTR                  pszTimestampAlgorithmOid,
  _In_opt_   PCWSTR                 pwszHttpTimeStamp,
  _In_opt_   PCRYPT_ATTRIBUTES      psRequest,
  _In_opt_   PVOID                  pSipData,
  _Out_      SIGNER_CONTEXT         **ppSignerContext,
  _In_opt_   PCERT_STRONG_SIGN_PARA pCryptoPolicy,
  _Reserved_ PVOID                  pReserved
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Modifica el comportamiento de esta función.

Si el archivo que se va a firmar es un archivo ejecutable portátil (PE), puede ser cero o una combinación de uno o varios de los valores siguientes.



| Value                                                                                                                                                                                                                                                                                    | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SPC_EXC_PE_PAGE_HASHES_FLAG"></span><span id="spc_exc_pe_page_hashes_flag"></span><dl> <dt>**SPC \_ MARCA DE HASH DE PÁGINA DE EXC \_ PE \_ \_ \_ 0x10**</dt> <dt></dt> </dl>                    | Excluya los hashes de página al crear datos indirectos de SIP para el archivo PE. Esta marca tiene prioridad sobre la marca **SPC \_ INC PE PAGE \_ \_ \_ HASHES \_ FLAG.**<br/> Si no se especifica la marca **\_ SPC EXC \_ PE PAGE \_ \_ HASHES \_ FLAG** o **SPC INC PAGE \_ \_ \_ \_ HASHES \_ FLAG,** el valor establecido con la función [**WintrustSetDefaultIncludePEPageHashes**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) se usa para esta configuración. El valor predeterminado de esta configuración es excluir los hashes de página al crear datos indirectos de SIP para archivos PE.<br/> Este valor se define en el archivo de encabezado Mssip.h.<br/> **Windows Server 2003 y Windows XP:** Este valor no se admite.<br/> |
| <span id="SPC_INC_PE_IMPORT_ADDR_TABLE_FLAG"></span><span id="spc_inc_pe_import_addr_table_flag"></span><dl> <dt>**SPC \_ INC \_ PE \_ IMPORT \_ ADDR TABLE \_ \_ FLAG**</dt> <dt>0x20</dt> </dl> | Este valor no se admite.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SPC_INC_PE_DEBUG_INFO_FLAG"></span><span id="spc_inc_pe_debug_info_flag"></span><dl> <dt>**SPC \_ MARCA \_ DE INFORMACIÓN DE \_ \_ DEPURACIÓN DE \_ INC PE**</dt> <dt>0x40</dt> </dl>                       | Este valor no se admite.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SPC_INC_PE_RESOURCES_FLAG"></span><span id="spc_inc_pe_resources_flag"></span><dl> <dt>**SPC \_ MARCA \_ DE RECURSOS \_ DE \_ INC PE**</dt> <dt>0x80</dt> </dl>                           | Este valor no se admite.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SPC_INC_PE_PAGE_HASHES_FLAG"></span><span id="spc_inc_pe_page_hashes_flag"></span><dl> <dt>**SPC \_ MARCA \_ DE HASH DE PÁGINA INC PE \_ \_ \_ 0x100**</dt> <dt></dt> </dl>                   | Incluir hashes de página al crear datos indirectos de SIP para el archivo PE.<br/> **Windows Server 2003 y Windows XP:** Este valor no se admite.<br/> Este valor se define en el archivo de encabezado Mssip.h.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SIG_APPEND"></span><span id="sig_append"></span><dl> <dt>**SIG \_ Append**</dt> <dt>0x1000</dt> </dl>                                                                         | La firma se anidará. Si establece esta marca antes de agregar cualquier firma, la firma generada se agregará como firma externa. Si no establece esta marca, la firma generada reemplaza la firma externa, eliminando todas las firmas internas.<br/>                                                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> <dt>

*pSubjectInfo* \[ En\]
</dt> <dd>

Puntero a una [**estructura SIGNER \_ SUBJECT \_ INFO**](signer-subject-info.md) que especifica el sujeto al que se firmará.

</dd> <dt>

*pSignerCert* \[ En\]
</dt> <dd>

Puntero a una [**estructura \_ SIGNER CERT**](signer-cert.md) que especifica el certificado que se usará para crear la firma digital.

</dd> <dt>

*pSignatureInfo* \[ En\]
</dt> <dd>

Puntero a una estructura [**SIGNER \_ SIGNATURE \_ INFO**](signer-signature-info.md) que contiene información sobre la firma digital.

</dd> <dt>

*pProviderInfo* \[ in, opcional\]
</dt> <dd>

Puntero a una [**estructura SIGNER \_ PROVIDER \_ INFO**](signer-provider-info.md) que especifica el proveedor de servicios criptográficos [*(CSP)*](../secgloss/c-gly.md) y la información de clave privada que se usa para crear la firma digital.

Si el valor de este parámetro es **NULL,** el *parámetro pSignerCert* debe especificar un certificado asociado a un CSP.

</dd> <dt>

*dwTimestampFlags* \[ in, opcional\]
</dt> <dd>

Marcas que se pasarán a [**SignerTimeStampEx3**](signertimestampex3.md) si el *parámetro pwszHttpTimeStamp* no es **NULL.** Puede ser uno de los siguientes valores.



| Value                                                                                                                                                                                                          | Significado                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl> <dt>**SIGNER \_ TIMESTAMP \_ AUTHENTICODE**</dt> </dl> | Valor predeterminado. Especifica una marca de tiempo Authenticode.<br/> |
| <span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl> <dt>**MARCA DE \_ TIEMPO DEL \_ FIRMANTE RFC3161**</dt> </dl>                | Especifica una marca de tiempo RFC 3161.<br/>                    |



 

Este parámetro se omite si el *parámetro pwszHttpTimeStamp* es **NULL.**

</dd> <dt>

*pszTimestampAlgorithmOid* \[ in, opcional\]
</dt> <dd>

Identificador de objeto del algoritmo que se va a usar para crear una marca de tiempo RFC 3161. Este parámetro se omite para las marcas de tiempo authenticode.

</dd> <dt>

*pwszHttpTimeStamp* \[ in, opcional\]
</dt> <dd>

Dirección URL del servidor de marca de tiempo.

</dd> <dt>

*psRequest* \[ in, opcional\]
</dt> <dd>

Puntero a una matriz de [**estructuras CRYPT \_ ATTRIBUTE**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) que se agregan a una solicitud de firma. Este parámetro se omite si el *parámetro pwszHttpTimeStamp* no contiene un valor válido o es **NULL.**

</dd> <dt>

*pSipData* \[ in, opcional\]
</dt> <dd>

Valor de 32 bits que se pasa como datos adicionales a las funciones de SIP. El proveedor DE SIP define el formato y el contenido de este.

</dd> <dt>

*ppSignerContext* \[ out\]
</dt> <dd>

Dirección de un puntero a la estructura [**SIGNER \_ CONTEXT**](signer-context.md) que contiene el [*blob firmado.*](../secgloss/b-gly.md) Cuando haya terminado de usar la estructura **SIGNER \_ CONTEXT,** libera la estructura **SIGNER \_ CONTEXT** mediante una llamada a la [**función SignerFreeSignerContext.**](signerfreesignercontext.md)

</dd> <dt>

*pCryptoPolicy* \[ in, opcional\]
</dt> <dd>

Si está presente, puntero a una estructura [**CERT \_ STRONG SIGN \_ \_ PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_strong_sign_para) que contiene los parámetros usados para comprobar si hay firmas seguras. Si no se pasa un certificado o su cadena, el archivo no se modifica de ninguna manera. Si se pasa una dirección URL para especificar una entidad de marca de tiempo (TSA), esta directiva también se aplica a la marca de tiempo.

</dd> <dt>

*Conservado* 
</dt> <dd>

Reservado. Este valor debe ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, la función devuelve S \_ OK.

Si se produce un error en la función, devuelve un **valor HRESULT** que indica el error. Entre los posibles códigos de error devueltos por esta función se incluyen, entre otros, los siguientes. Para obtener una lista de códigos de error comunes, vea [Common HRESULT Values](common-hresult-values.md).



| Código devuelto                                                                                  | Descripción                                                                                                                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Si establece el parámetro *dwTimestampFlags* en **SIGNER \_ TIMESTAMP \_ AUTHENTICODE**, no puede establecer el parámetro *dwFlags* en **SIG \_ APPEND**.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SignerSign**](signersign.md)
</dt> <dt>

[**SignerSignEx**](signersignex.md)
</dt> <dt>

[**SignerFreeSignerContext**](signerfreesignercontext.md)
</dt> </dl>

 

 
