---
description: Marca de tiempo el sujeto especificado y permite establecer marcas de tiempo en varias firmas.
ms.assetid: A290ED4F-8803-4EAA-8CE1-68879F7F754A
title: SignerTimeStampEx3 función)
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
ms.openlocfilehash: 538b92160ddbbb9ca9515a65575fdea67990de5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153732"
---
# <a name="signertimestampex3-function"></a>SignerTimeStampEx3 función)

El tiempo de la función **SignerTimeStampEx3** marca el sujeto especificado y permite establecer marcas de tiempo en varias firmas.

> [!Note]  
> Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación. Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.

 

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

*dwFlags* \[ de\]
</dt> <dd>

Marca que especifica el tipo de marca de tiempo que se va a generar. Este parámetro puede ser uno de los valores siguientes. Los valores son mutuamente excluyentes.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Value</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl> <dt><strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong></dt> </dl></td>
<td>Especifica una marca de tiempo de Authenticode.<br/>
<blockquote>
[!Note]<br />
Authenticode ya no es el tipo preferido de marca de tiempo. La compatibilidad con las marcas de tiempo de Authenticode puede quitarse en el futuro. En su lugar, se recomienda usar RFC 3161.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl> <dt><strong>SIGNER_TIMESTAMP_RFC3161</strong></dt> </dl></td>
<td>Especifica una marca de tiempo compatible con RFC 3161.<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*dwIndex* \[ de\]
</dt> <dd>

Especifica el número de secuencia de la firma a la que se agregará la marca de tiempo. Si este valor es cero (0), la firma externa será con marca de tiempo.

</dd> <dt>

*pSubjectInfo* \[ de\]
</dt> <dd>

Dirección de una estructura de [**\_ \_ información de asunto del firmante**](signer-subject-info.md) que representa el sujeto de marca de tiempo.

</dd> <dt>

*pwszHttpTimeStamp* \[ de\]
</dt> <dd>

Dirección de una cadena Unicode terminada en null que contiene la dirección URL de un servidor de marca de tiempo.

</dd> <dt>

*pszAlgorithmOid* \[ de\]
</dt> <dd>

Algoritmo hash que se va a usar para realizar las marcas de tiempo compatibles con RFC 3161. Este parámetro se omite para las marcas de tiempo de Authenticode.

</dd> <dt>

*psRequest* \[ en, opcional\]
</dt> <dd>

Opcional. Dirección de una estructura [**de \_ atributos de cifrado**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) que contiene atributos adicionales que se agregan a la solicitud de marca de tiempo.

Este parámetro es opcional y puede ser **null** si no se incluye.

</dd> <dt>

*pSipData* \[ en, opcional\]
</dt> <dd>

Opcional. Valor de 32 bits que se pasa como datos adicionales a las funciones del [*paquete de interfaz de asunto*](../secgloss/s-gly.md) (SIP). El proveedor SIP define el formato y el contenido de este parámetro.

Este parámetro es opcional y puede ser **null** si no se incluye.

</dd> <dt>

*ppSignerContext* \[ enuncia\]
</dt> <dd>

Opcional. Dirección de un puntero a la estructura de [**\_ contexto del firmante**](signer-context.md) que contiene el BLOB firmado. Cuando haya terminado de usar la estructura de **\_ contexto del firmante** , libere la llamada a la función [**SignerFreeSignerContext**](signerfreesignercontext.md) .

</dd> <dt>

*pCryptoPolicy* \[ en, opcional\]
</dt> <dd>

Si está presente, es un puntero a un [**certificado de \_ \_ firma segura \_ para**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_strong_sign_para) la estructura que contiene los parámetros utilizados para comprobar las signaturas seguras. La marca de tiempo debe pasar esta directiva de cifrado.

</dd> <dt>

*Van* 
</dt> <dd>

Reservado. Este valor debe ser **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, la función devuelve S \_ OK.

Si se produce un error en la función, devuelve un valor **HRESULT** que indica el error. Los códigos de error posibles devueltos por esta función incluyen, entre otros, lo siguiente. Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Código devuelto</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <dt><strong>E_INVALIDARG</strong></dt> </dl></td>
<td>Este error se puede devolver en las condiciones siguientes:<br/>
<ul>
<li>Debe establecer <strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong> o <strong>SIGNER_TIMESTAMP_RFC3161</strong> para el parámetro <em>dwFlags</em> .</li>
<li>El parámetro <em>Reserved</em> debe ser <strong>null</strong>.</li>
<li>Si establece la marca <strong>SIGNER_TIMESTAMP_AUTHENTICODE</strong> en el parámetro <em>dwFlags</em> , debe establecer el parámetro <em>dwIndex</em> en cero.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                 |
| Archivo DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SignerTimeStamp**](signertimestamp.md)
</dt> <dt>

[**SignerTimeStampEx**](signertimestampex.md)
</dt> <dt>

[**SignerTimeStampEx2**](signertimestampex2.md)
</dt> </dl>

 

 
