---
description: Signos y hora marca el archivo especificado, lo que permite varias firmas anidadas.
ms.assetid: 216EFFCF-CD23-484A-ADBF-94B5AD52289F
title: SignerSignEx2 función)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278424"
---
# <a name="signersignex2-function"></a>SignerSignEx2 función)

La función **SignerSignEx2** firma y marca la hora del archivo especificado, lo que permite varias firmas anidadas.

> [!Note]  
> Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación. Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.

 

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

*dwFlags* \[ de\]
</dt> <dd>

Modifica el comportamiento de esta función.

Si el archivo que se va a firmar es un archivo ejecutable portable (PE), puede ser cero o una combinación de uno o varios de los valores siguientes.



| Value                                                                                                                                                                                                                                                                                    | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SPC_EXC_PE_PAGE_HASHES_FLAG"></span><span id="spc_exc_pe_page_hashes_flag"></span><dl> <dt>**SPC \_ \_Marca de \_ \_ hash \_ de página del PE de EXC**</dt> <dt>0x10</dt> </dl>                    | Excluya los hash de página al crear datos indirectos de SIP para el archivo PE. Esta marca tiene prioridad sobre la marca de **marca de hash de página de SPC \_ Inc \_ PE \_ \_ \_** .<br/> Si no se especifica la marca **hash de página de PE de SPC \_ EXC \_ \_ \_ \_** o la marca hash de **Página de SPC \_ Inc Inc \_ \_ \_ \_** , se usa el valor establecido con la función [**WintrustSetDefaultIncludePEPageHashes**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) para esta configuración. El valor predeterminado para esta opción es excluir los valores hash de página al crear datos indirectos SIP para archivos PE.<br/> Este valor se define en el archivo de encabezado Mssip. h.<br/> **Windows Server 2003 y Windows XP:** Este valor no se admite.<br/> |
| <span id="SPC_INC_PE_IMPORT_ADDR_TABLE_FLAG"></span><span id="spc_inc_pe_import_addr_table_flag"></span><dl> <dt>**SPC \_ El \_ marcador de la tabla de direcciones de importación PE de \_ \_ \_ \_ PE**</dt> es <dt>0x20</dt> </dl> | Este valor no se admite.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SPC_INC_PE_DEBUG_INFO_FLAG"></span><span id="spc_inc_pe_debug_info_flag"></span><dl> <dt>**SPC \_ \_Marca de \_ \_ información de \_ depuración PE de PE**</dt> <dt>0x40</dt> </dl>                       | Este valor no se admite.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SPC_INC_PE_RESOURCES_FLAG"></span><span id="spc_inc_pe_resources_flag"></span><dl> <dt>**SPC \_ \_Indicador de \_ recursos \_ de PE de PE**</dt> <dt>0x80</dt> </dl>                           | Este valor no se admite.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="SPC_INC_PE_PAGE_HASHES_FLAG"></span><span id="spc_inc_pe_page_hashes_flag"></span><dl> <dt>**SPC \_ \_Marca de \_ \_ hash \_ de página de PE de PE**</dt> <dt>0x100</dt> </dl>                   | Incluir hashes de página al crear datos indirectos de SIP para el archivo PE.<br/> **Windows Server 2003 y Windows XP:** Este valor no se admite.<br/> Este valor se define en el archivo de encabezado Mssip. h.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="SIG_APPEND"></span><span id="sig_append"></span><dl> <dt>**SIG \_ ANEXAr**</dt> <dt>0x1000</dt> </dl>                                                                         | La firma se anidará. Si establece esta marca antes de que se agregue cualquier firma, la firma generada se agregará como la firma externa. Si no establece esta marca, la firma generada reemplaza la firma externa y elimina todas las firmas internas.<br/>                                                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> <dt>

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

Puntero a una estructura de [**\_ \_ información del proveedor de firmante**](signer-provider-info.md) que especifica el proveedor de [*servicios criptográficos*](../secgloss/c-gly.md) (CSP) y la información de clave privada que se usa para crear la firma digital.

Si el valor de este parámetro es **null**, el parámetro *pSignerCert* debe especificar un certificado asociado a un CSP.

</dd> <dt>

*dwTimestampFlags* \[ en, opcional\]
</dt> <dd>

Marcas que se pasarán a [**SignerTimeStampEx3**](signertimestampex3.md) si el parámetro *PwszHttpTimeStamp* no es **null**. Puede ser uno de los valores siguientes.



| Value                                                                                                                                                                                                          | Significado                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl> <dt>**marca de tiempo del firmante \_ \_ AUTHENTICODE**</dt> </dl> | Valor predeterminado. Especifica una marca de tiempo de Authenticode.<br/> |
| <span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl> <dt>**Marca de tiempo del firmante \_ \_ RFC3161**</dt> </dl>                | Especifica una marca de tiempo RFC 3161.<br/>                    |



 

Este parámetro se omite si el parámetro *pwszHttpTimeStamp* es **null**.

</dd> <dt>

*pszTimestampAlgorithmOid* \[ en, opcional\]
</dt> <dd>

Identificador de objeto del algoritmo que se va a usar para crear una marca de tiempo RFC 3161. Este parámetro se omite para las marcas de tiempo de Authenticode.

</dd> <dt>

*pwszHttpTimeStamp* \[ en, opcional\]
</dt> <dd>

Dirección URL del servidor de marca de tiempo.

</dd> <dt>

*psRequest* \[ en, opcional\]
</dt> <dd>

Puntero a una matriz de estructuras de [**\_ atributo de cifrado**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attribute) que se agregan a una solicitud de firma. Este parámetro se omite si el parámetro *pwszHttpTimeStamp* no contiene un valor válido o es **null**.

</dd> <dt>

*pSipData* \[ en, opcional\]
</dt> <dd>

Valor de 32 bits que se pasa como datos adicionales a las funciones de SIP. El proveedor SIP define el formato y el contenido de este.

</dd> <dt>

*ppSignerContext* \[ enuncia\]
</dt> <dd>

Dirección de un puntero a la estructura de [**\_ contexto del firmante**](signer-context.md) que contiene el [*BLOB*](../secgloss/b-gly.md)firmado. Cuando haya terminado de usar la estructura de **\_ contexto del firmante** , libere la estructura del **\_ contexto del firmante** llamando a la función [**SignerFreeSignerContext**](signerfreesignercontext.md) .

</dd> <dt>

*pCryptoPolicy* \[ en, opcional\]
</dt> <dd>

Si está presente, es un puntero a un [**certificado de \_ \_ firma segura \_ para**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_strong_sign_para) la estructura que contiene los parámetros utilizados para comprobar las signaturas seguras. Si un certificado o su cadena no pasa, el archivo no se modifica de ninguna manera. Si se pasa una dirección URL para especificar una autoridad de marca de tiempo (TSA), esta Directiva también se aplica a la marca de tiempo.

</dd> <dt>

*Van* 
</dt> <dd>

Reservado. Este valor debe ser **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, la función devuelve S \_ OK.

Si se produce un error en la función, devuelve un valor **HRESULT** que indica el error. Los códigos de error posibles devueltos por esta función incluyen, entre otros, lo siguiente. Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).



| Código devuelto                                                                                  | Descripción                                                                                                                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Si establece el parámetro *dwTimestampFlags* en la marca de tiempo de **firma \_ \_ AUTHENTICODE**, no puede establecer el parámetro *dwFlags* en **SIG \_ Append**.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SignerSign**](signersign.md)
</dt> <dt>

[**SignerSignEx**](signersignex.md)
</dt> <dt>

[**SignerFreeSignerContext**](signerfreesignercontext.md)
</dt> </dl>

 

 
