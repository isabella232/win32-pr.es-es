---
description: Marca de tiempo el asunto especificado y, opcionalmente, devuelve un puntero a una \_ estructura de contexto del firmante que contiene un puntero a un BLOB. Esta función se puede usar para realizar la infraestructura de clave pública X. 509, RFC 3161&\# 8211; de acuerdo con las marcas de tiempo.
ms.assetid: fb82545b-c00f-44eb-96f4-aa27a125c8d9
title: SignerTimeStampEx2 función)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668325"
---
# <a name="signertimestampex2-function"></a>SignerTimeStampEx2 función)

El tiempo de la función **SignerTimeStampEx2** marca el asunto especificado y, opcionalmente, devuelve un puntero a una estructura de [**\_ contexto del firmante**](signer-context.md) que contiene un puntero a un [*BLOB*](../secgloss/b-gly.md). Esta función se puede usar para realizar la infraestructura de clave pública X. 509, que es compatible con RFC 3161 y las marcas de tiempo.

> [!Note]  
> Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación. Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.

 

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

*dwFlags* \[ de\]
</dt> <dd>

Valor que especifica el tipo de marca de tiempo que se va a generar. Este parámetro puede ser uno de los valores siguientes. Los valores son mutuamente excluyentes.



| Value                                                                                                                                                                                                          | Significado                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="SIGNER_TIMESTAMP_AUTHENTICODE"></span><span id="signer_timestamp_authenticode"></span><dl> <dt>**marca de tiempo del firmante \_ \_ AUTHENTICODE**</dt> </dl> | Especifica una marca de tiempo de Authenticode.<br/>       |
| <span id="SIGNER_TIMESTAMP_RFC3161"></span><span id="signer_timestamp_rfc3161"></span><dl> <dt>**Marca de tiempo del firmante \_ \_ RFC3161**</dt> </dl>                | Especifica una marca de tiempo compatible con RFC 3161.<br/> |



 

</dd> <dt>

*pSubjectInfo* \[ de\]
</dt> <dd>

Dirección de una estructura de [**\_ \_ información de asunto del firmante**](signer-subject-info.md) que representa el sujeto de marca de tiempo.

</dd> <dt>

*pwszHttpTimeStamp* \[ de\]
</dt> <dd>

Dirección de una cadena Unicode terminada en null que contiene la dirección URL de un servidor de marca de tiempo.

</dd> <dt>

*dwAlgId* \[ de\]
</dt> <dd>

Especifica un algoritmo hash que se utilizará para realizar las marcas de tiempo compatibles con RFC 3161. Este parámetro se omite para las marcas de tiempo de Authenticode.

</dd> <dt>

*psRequest* \[ de\]
</dt> <dd>

Opcional. Dirección de una estructura [**de \_ atributos de cifrado**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) que contiene atributos adicionales que se agregan a la solicitud de marca de tiempo.

Este parámetro es opcional y puede ser **null** si no se incluye.

</dd> <dt>

*pSipData* \[ de\]
</dt> <dd>

Opcional. Valor de 32 bits que se pasa como datos adicionales a las funciones del [*paquete de interfaz de asunto*](../secgloss/s-gly.md) (SIP). El proveedor SIP define el formato y el contenido de este parámetro.

Este parámetro es opcional y puede ser **null** si no se incluye.

</dd> <dt>

*ppSignerContext* \[ enuncia\]
</dt> <dd>

Opcional. Dirección de un puntero a la estructura de [**\_ contexto del firmante**](signer-context.md) que contiene el BLOB firmado. Cuando haya terminado de usar la estructura de **\_ contexto del firmante** , libere la llamada a la función [**SignerFreeSignerContext**](signerfreesignercontext.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, la función devuelve S \_ OK.

Si se produce un error en la función, devuelve un valor **HRESULT** que indica el error. Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                 |
| Archivo DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SignerTimeStamp**](signertimestamp.md)
</dt> <dt>

[**SignerTimeStampEx**](signertimestampex.md)
</dt> </dl>

 

 
