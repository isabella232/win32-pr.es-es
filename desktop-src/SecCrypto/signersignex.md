---
description: Firma el archivo especificado y devuelve un puntero a los datos firmados.
ms.assetid: 9921ffae-2299-4bf2-b76d-77f7f6afb663
title: Función SignerSignEx
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
ms.openlocfilehash: 0b880cc02053d5a90089cffc721b057c6fce9f34b8be6517c12ef59fef9e0ed4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118898328"
---
# <a name="signersignex-function"></a>Función SignerSignEx

La **función SignerSignEx** firma el archivo especificado y devuelve un puntero a los datos firmados.

> [!Note]  
> Esta función no tiene ningún archivo de encabezado asociado ni biblioteca de importación. Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.

 

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

*dwFlags* \[ En\]
</dt> <dd>

Modifica el comportamiento de esta función.

Si el archivo que se va a firmar es un archivo ejecutable portátil (PE), puede ser cero o una combinación de uno o varios de los valores siguientes. Estos identificadores se definen en Mssip.h.



| Valor                                                                                                                                                                                                                                                                                    | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SPC_EXC_PE_PAGE_HASHES_FLAG"></span><span id="spc_exc_pe_page_hashes_flag"></span><dl> <dt>**SPC \_ MARCA DE HASH DE PÁGINA DE EXC \_ PE \_ \_ \_ 0x10**</dt> <dt></dt> </dl>                    | Excluya los hashes de página al crear datos indirectos de SIP para el archivo PE. Esta marca tiene prioridad sobre la marca **SPC \_ INC PE PAGE \_ \_ \_ HASHES \_ FLAG.**<br/> Si no se especifica la marca **\_ SPC EXC \_ PE PAGE \_ \_ HASHES \_ FLAG** o **SPC INC PAGE \_ \_ \_ \_ HASHES \_ FLAG,** el valor establecido con la función [**WintrustSetDefaultIncludePEPageHashes**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) se usa para esta configuración. El valor predeterminado de esta configuración es excluir los hashes de página al crear datos indirectos de SIP para archivos PE.<br/> **Windows Server 2003 y Windows XP:** Este valor no se admite.<br/> |
| <span id="SPC_INC_PE_IMPORT_ADDR_TABLE_FLAG"></span><span id="spc_inc_pe_import_addr_table_flag"></span><dl> <dt>**SPC \_ INC \_ PE \_ IMPORT \_ ADDR TABLE \_ \_ FLAG**</dt> <dt>0x20</dt> </dl> | Este valor no se admite.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SPC_INC_PE_DEBUG_INFO_FLAG"></span><span id="spc_inc_pe_debug_info_flag"></span><dl> <dt>**SPC \_ MARCA \_ DE INFORMACIÓN DE \_ \_ DEPURACIÓN DE \_ INC PE**</dt> <dt>0x40</dt> </dl>                       | Este valor no se admite.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SPC_INC_PE_RESOURCES_FLAG"></span><span id="spc_inc_pe_resources_flag"></span><dl> <dt>**SPC \_ MARCA \_ DE RECURSOS \_ DE \_ INC PE**</dt> <dt>0x80</dt> </dl>                           | Este valor no se admite.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="SPC_INC_PE_PAGE_HASHES_FLAG"></span><span id="spc_inc_pe_page_hashes_flag"></span><dl> <dt>**SPC \_ MARCA DE HASH DE PÁGINA DE INC \_ PE \_ \_ \_ 0x100**</dt> <dt></dt> </dl>                   | Incluir hashes de página al crear datos indirectos de SIP para el archivo PE.<br/> **Windows Server 2003 y Windows XP:** Este valor no se admite.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

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

Puntero a una estructura [**SIGNER \_ PROVIDER \_ INFO**](signer-provider-info.md) que especifica el proveedor de servicios criptográficos [*(CSP)*](../secgloss/c-gly.md) y la información de clave privada que se usa para crear la firma digital.

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

</dd> <dt>

*ppSignerContext* \[ out\]
</dt> <dd>

Dirección de un puntero a la estructura [**SIGNER \_ CONTEXT**](signer-context.md) que contiene el [*blob firmado.*](../secgloss/b-gly.md) Cuando haya terminado de usar la estructura **SIGNER \_ CONTEXT,** libera la estructura **SIGNER \_ CONTEXT** llamando a la [**función SignerFreeSignerContext.**](signerfreesignercontext.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, la función devuelve S \_ OK.

Si se produce un error en la función, devuelve un **valor HRESULT** que indica el error. Para obtener una lista de códigos de error comunes, vea [Common HRESULT Values](common-hresult-values.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SignerSign**](signersign.md)
</dt> <dt>

[**SignerFreeSignerContext**](signerfreesignercontext.md)
</dt> </dl>

 

 
