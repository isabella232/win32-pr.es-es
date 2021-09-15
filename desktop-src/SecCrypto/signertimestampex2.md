---
description: Marca de tiempo el asunto especificado y, opcionalmente, devuelve un puntero a una estructura SIGNER CONTEXT que \_ contiene un puntero a un BLOB. Esta función se puede usar para realizar marcas de tiempo X.509 Public Key Infrastructure, RFC 3161&\# 8211;compliant.
ms.assetid: fb82545b-c00f-44eb-96f4-aa27a125c8d9
title: Función SignerTimeStampEx2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStampEx2
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 07dc9162c9cb8832e93e2518c7208d235d878875
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127270839"
---
# <a name="signertimestampex2-function"></a>Función SignerTimeStampEx2

La **función SignerTimeStampEx2** marca el asunto especificado y, opcionalmente, devuelve un puntero a una estructura [**SIGNER \_ CONTEXT**](signer-context.md) que contiene un puntero a [*un blob*](../secgloss/b-gly.md). Esta función se puede usar para realizar marcas de tiempo de infraestructura de clave pública X.509 compatible con RFC 3161.

> [!Note]  
> Esta función no tiene ningún archivo de encabezado asociado ni biblioteca de importación. Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI SignerTimeStampEx2(
  _Reserved_ DWORD               dwFlags,
  _In_       SIGNER_SUBJECT_INFO *pSubjectInfo,
  _In_       LPCWSTR             pwszHttpTimeStamp,
  _In_       ALG_ID              dwAlgId,
  _In_       PCRYPT_ATTRIBUTES   psRequest,
  _In_       LPVOID              pSipData,
  _Out_      SIGNER_CONTEXT      **ppSignerContext 
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Valor que especifica el tipo de marca de tiempo que se generará. Este parámetro puede ser uno de los valores siguientes. Los valores son mutuamente excluyentes.



| Value                                                                                                                                                                                                          | Significado                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl> <dt>**SIGNER \_ TIMESTAMP \_ AUTHENTICODE**</dt> </dl> | Especifica una marca de tiempo Authenticode.<br/>       |
| <span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl> <dt>**MARCA DE \_ TIEMPO DEL \_ FIRMANTE RFC3161**</dt> </dl>                | Especifica una marca de tiempo compatible con RFC 3161.<br/> |



 

</dd> <dt>

*pSubjectInfo* \[ En\]
</dt> <dd>

Dirección de una estructura [**SIGNER \_ SUBJECT \_ INFO**](signer-subject-info.md) que representa el sujeto al que se va a marcar la hora.

</dd> <dt>

*pwszHttpTimeStamp* \[ En\]
</dt> <dd>

Dirección de una cadena Unicode terminada en NULL que contiene la dirección URL de un servidor de marca de tiempo.

</dd> <dt>

*dwAlgId* \[ En\]
</dt> <dd>

Especifica un algoritmo hash que se usará para realizar marcas de tiempo compatibles con RFC 3161. Este parámetro se omite para las marcas de tiempo authenticode.

</dd> <dt>

*psRequest* \[ En\]
</dt> <dd>

Opcional. Dirección de una estructura [**CRYPT \_ ATTRIBUTES que**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) contiene atributos adicionales que se agregan a la solicitud de marca de tiempo.

Este parámetro es opcional y puede ser **NULL** si no se incluye.

</dd> <dt>

*pSipData* \[ En\]
</dt> <dd>

Opcional. Valor de 32 bits que se pasa como datos adicionales a las funciones del paquete de [*interfaz de*](../secgloss/s-gly.md) sujeto (SIP). El proveedor DE SIP define el formato y el contenido de este parámetro.

Este parámetro es opcional y puede ser **NULL** si no se incluye.

</dd> <dt>

*ppSignerContext* \[ out\]
</dt> <dd>

Opcional. Dirección de un puntero a la estructura [**SIGNER \_ CONTEXT**](signer-context.md) que contiene el BLOB firmado. Cuando haya terminado de usar la estructura **SIGNER \_ CONTEXT,** descálala mediante una llamada a la [**función SignerFreeSignerContext.**](signerfreesignercontext.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, la función devuelve S \_ OK.

Si se produce un error en la función, devuelve un **valor HRESULT** que indica el error. Para obtener una lista de códigos de error comunes, vea [Common HRESULT Values](common-hresult-values.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio solo\]<br/>                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                 |
| Archivo DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**SignerTimeStamp**](signertimestamp.md)
</dt> <dt>

[**SignerTimeStampEx**](signertimestampex.md)
</dt> </dl>

 

 
