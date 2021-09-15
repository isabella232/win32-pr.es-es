---
description: Marca de tiempo el asunto especificado y admite la configuración de marcas de tiempo en varias firmas.
ms.assetid: A290ED4F-8803-4EAA-8CE1-68879F7F754A
title: Función SignerTimeStampEx3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStampEx3
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 7eb5c19292b451b1a3d0265da4bb178eafcc6f00
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127270836"
---
# <a name="signertimestampex3-function"></a>Función SignerTimeStampEx3

La **función SignerTimeStampEx3** marca el asunto especificado y admite la configuración de marcas de tiempo en varias firmas.

> [!Note]  
> Esta función no tiene ningún archivo de encabezado asociado ni biblioteca de importación. Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI SignerTimeStampEx3(
  _In_       DWORD                  dwFlags,
  _In_       DWORD                  dwIndex,
  _In_       SIGNER_SUBJECT_INFO    *pSubjectInfo,
  _In_       PCWSTR                 pwszHttpTimeStamp,
  _In_       PCWSTR                 pszAlgorithmOid,
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

Marca que especifica el tipo de marca de tiempo que se generará. Este parámetro puede ser uno de los valores siguientes. Los valores son mutuamente excluyentes.




| Value | Significado | 
|-------|---------|
| <span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl><dt><strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong></dt></dl> | Especifica una marca de tiempo Authenticode.<br /><blockquote>[!Note]<br />Authenticode ya no es el tipo preferido de marca de tiempo. La compatibilidad con marcas de tiempo de Authenticode puede quitarse en el futuro. Se recomienda usar RFC 3161 en su lugar.</blockquote><br /> | 
| <span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl><dt><strong>SIGNER_TIMESTAMP_RFC3161</strong></dt></dl> | Especifica una marca de tiempo compatible con RFC 3161.<br /> | 




 

</dd> <dt>

*dwIndex* \[ En\]
</dt> <dd>

Especifica el número de secuencia de la firma a la que se agregará la marca de tiempo. Si este valor es cero (0), se marcará la marca de tiempo de la firma externa.

</dd> <dt>

*pSubjectInfo* \[ En\]
</dt> <dd>

Dirección de una estructura [**SIGNER \_ SUBJECT \_ INFO**](signer-subject-info.md) que representa el sujeto al que se va a marcar la hora.

</dd> <dt>

*pwszHttpTimeStamp* \[ En\]
</dt> <dd>

Dirección de una cadena Unicode terminada en NULL que contiene la dirección URL de un servidor de marca de tiempo.

</dd> <dt>

*pszAlgorithmOid* \[ En\]
</dt> <dd>

Algoritmo hash que se va a usar para realizar marcas de tiempo compatibles con RFC 3161. Este parámetro se omite para las marcas de tiempo authenticode.

</dd> <dt>

*psRequest* \[ en, opcional\]
</dt> <dd>

Opcional. Dirección de una estructura [**CRYPT \_ ATTRIBUTES que**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) contiene atributos adicionales que se agregan a la solicitud de marca de tiempo.

Este parámetro es opcional y puede ser **NULL** si no se incluye.

</dd> <dt>

*pSipData* \[ en, opcional\]
</dt> <dd>

Opcional. Valor de 32 bits que se pasa como datos adicionales a las funciones del paquete [*de interfaz de sujeto*](../secgloss/s-gly.md) (SIP). El proveedor SIP define el formato y el contenido de este parámetro.

Este parámetro es opcional y puede ser **NULL** si no se incluye.

</dd> <dt>

*ppSignerContext* \[ out\]
</dt> <dd>

Opcional. Dirección de un puntero a la estructura [**SIGNER \_ CONTEXT**](signer-context.md) que contiene el BLOB firmado. Cuando haya terminado de usar la estructura **SIGNER \_ CONTEXT,** desconéctela mediante una llamada a la [**función SignerFreeSignerContext.**](signerfreesignercontext.md)

</dd> <dt>

*pCryptoPolicy* \[ en, opcional\]
</dt> <dd>

Si está presente, puntero a una [**estructura CERT STRONG SIGN \_ \_ \_ PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_strong_sign_para) que contiene los parámetros usados para comprobar si hay firmas seguras. La marca de tiempo debe pasar esta directiva criptográfica.

</dd> <dt>

*Conservado* 
</dt> <dd>

Reservado. Este valor debe ser **NULL.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, la función devuelve S \_ OK.

Si se produce un error en la función, devuelve un **valor HRESULT** que indica el error. Los posibles códigos de error devueltos por esta función incluyen, entre otros, los siguientes. Para obtener una lista de códigos de error comunes, vea [Common HRESULT Values](common-hresult-values.md).




| Código devuelto | Descripción | 
|-------------|-------------|
| <dl><dt><strong>E_INVALIDARG</strong></dt></dl> | Este error se puede devolver para las siguientes condiciones:<br /><ul><li>Debe establecer <strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong> o <strong>SIGNER_TIMESTAMP_RFC3161</strong> para el <em>parámetro dwFlags.</em></li><li>El <em>parámetro pReserved</em> debe ser <strong>NULL.</strong></li><li>Si establece la <strong>marca SIGNER_TIMESTAMP_AUTHENTICODE</strong> en el <em>parámetro dwFlags,</em> debe establecer el <em>parámetro dwIndex</em> en cero.</li></ul> | 




 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                 |
| Archivo DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SignerTimeStamp**](signertimestamp.md)
</dt> <dt>

[**SignerTimeStampEx**](signertimestampex.md)
</dt> <dt>

[**SignerTimeStampEx2**](signertimestampex2.md)
</dt> </dl>

 

 
