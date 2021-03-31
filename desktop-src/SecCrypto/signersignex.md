---
description: Firma el archivo especificado y devuelve un puntero a los datos firmados.
ms.assetid: 9921ffae-2299-4bf2-b76d-77f7f6afb663
title: SignerSignEx función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerSignEx
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 9944a09459219ccac74f5fafc9424e9f85a01112
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812823"
---
# <a name="signersignex-function"></a>SignerSignEx función)

La función **SignerSignEx** firma el archivo especificado y devuelve un puntero a los datos firmados.

> [!Note]  
> Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación. Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI SignerSignEx(
  _In_     DWORD                 dwFlags,
  _In_     SIGNER_SUBJECT_INFO   *pSubjectInfo,
  _In_     SIGNER_CERT           *pSignerCert,
  _In_     SIGNER_SIGNATURE_INFO *pSignatureInfo,
  _In_opt_ SIGNER_PROVIDER_INFO  *pProviderInfo,
  _In_opt_ LPCWSTR               pwszHttpTimeStamp,
  _In_opt_ PCRYPT_ATTRIBUTES     psRequest,
  _In_opt_ LPVOID                pSipData,
  _Out_    SIGNER_CONTEXT        **ppSignerContext
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Modifica el comportamiento de esta función.

Si el archivo que se va a firmar es un archivo ejecutable portable (PE), puede ser cero o una combinación de uno o varios de los valores siguientes. Estos identificadores se definen en Mssip. h.



| Value                                                                                                                                                                                                                                                                                    | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SPC_EXC_PE_PAGE_HASHES_FLAG"></span><span id="spc_exc_pe_page_hashes_flag"></span><dl> <dt>**SPC \_ \_Marca de \_ \_ hash \_ de página del PE de EXC**</dt> <dt>0x10</dt> </dl>                    | Excluya los hash de página al crear datos indirectos de SIP para el archivo PE. Esta marca tiene prioridad sobre la marca de **marca de hash de página de SPC \_ Inc \_ PE \_ \_ \_** .<br/> Si no se especifica la marca **hash de página de PE de SPC \_ EXC \_ \_ \_ \_** o la marca hash de **Página de SPC \_ Inc Inc \_ \_ \_ \_** , se usa el valor establecido con la función [**WintrustSetDefaultIncludePEPageHashes**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) para esta configuración. El valor predeterminado para esta opción es excluir los valores hash de página al crear datos indirectos SIP para archivos PE.<br/> **Windows Server 2003 y Windows XP:** Este valor no se admite.<br/> |
| <span id="SPC_INC_PE_IMPORT_ADDR_TABLE_FLAG"></span><span id="spc_inc_pe_import_addr_table_flag"></span><dl> <dt>**SPC \_ El \_ marcador de la tabla de direcciones de importación PE de \_ \_ \_ \_ PE**</dt> es <dt>0x20</dt> </dl> | Este valor no se admite.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SPC_INC_PE_DEBUG_INFO_FLAG"></span><span id="spc_inc_pe_debug_info_flag"></span><dl> <dt>**SPC \_ \_Marca de \_ \_ información de \_ depuración PE de PE**</dt> <dt>0x40</dt> </dl>                       | Este valor no se admite.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SPC_INC_PE_RESOURCES_FLAG"></span><span id="spc_inc_pe_resources_flag"></span><dl> <dt>**SPC \_ \_Indicador de \_ recursos \_ de PE de PE**</dt> <dt>0x80</dt> </dl>                           | Este valor no se admite.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SPC_INC_PE_PAGE_HASHES_FLAG"></span><span id="spc_inc_pe_page_hashes_flag"></span><dl> <dt>**SPC \_ \_Marca de \_ \_ hash \_ de página de PE de PE**</dt> <dt>0x100</dt> </dl>                   | Incluir hashes de página al crear datos indirectos de SIP para el archivo PE.<br/> **Windows Server 2003 y Windows XP:** Este valor no se admite.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

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

</dd> <dt>

*ppSignerContext* \[ enuncia\]
</dt> <dd>

Dirección de un puntero a la estructura de [**\_ contexto del firmante**](signer-context.md) que contiene el [*BLOB*](../secgloss/b-gly.md)firmado. Cuando haya terminado de usar la estructura de **\_ contexto del firmante** , libere la estructura del **\_ contexto del firmante** llamando a la función [**SignerFreeSignerContext**](signerfreesignercontext.md) .

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

[**SignerSign**](signersign.md)
</dt> <dt>

[**SignerFreeSignerContext**](signerfreesignercontext.md)
</dt> </dl>

 

 
