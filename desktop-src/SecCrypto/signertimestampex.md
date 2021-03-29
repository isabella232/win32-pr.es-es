---
description: Marca de tiempo el asunto especificado y, opcionalmente, devuelve un puntero a una \_ estructura de contexto del firmante que contiene un puntero a un BLOB.
ms.assetid: f3a910f6-64f8-4cf5-b008-2a16872f9a98
title: SignerTimeStampEx función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStampEx
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: a4562ca84f8b3376a22d00a5e9501947152ed875
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816718"
---
# <a name="signertimestampex-function"></a>SignerTimeStampEx función)

El tiempo de la función **SignerTimeStampEx** marca el asunto especificado y, opcionalmente, devuelve un puntero a una estructura de [**\_ contexto del firmante**](signer-context.md) que contiene un puntero a un [*BLOB*](../secgloss/b-gly.md). Esta función admite la marca de tiempo de Authenticode. Para realizar una marca de tiempo de la infraestructura de clave pública (RFC 3161) de X. 509, utilice la función [**SignerTimeStampEx2**](signertimestampex2.md) .

> [!Note]  
> Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación. Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI SignerTimeStampEx(
  _Reserved_ DWORD               dwFlags,
  _In_       SIGNER_SUBJECT_INFO *pSubjectInfo,
  _In_       LPCWSTR             pwszHttpTimeStamp,
  _In_       PCRYPT_ATTRIBUTES   psRequest,
  _In_       LPVOID              pSipData,
  _Out_      SIGNER_CONTEXT      **ppSignerContext 
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Reservado. Este parámetro debe establecerse en cero.

</dd> <dt>

*pSubjectInfo* \[ de\]
</dt> <dd>

Dirección de una estructura de [**\_ \_ información de asunto del firmante**](signer-subject-info.md) que representa el sujeto de marca de tiempo.

</dd> <dt>

*pwszHttpTimeStamp* \[ de\]
</dt> <dd>

Dirección de una cadena Unicode terminada en null que contiene la dirección URL de un servidor de marca de tiempo.

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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Mssign32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>


</dt> <dt>

[**SignerTimeStamp**](signertimestamp.md)
</dt> </dl>

 

 
