---
description: Marca de tiempo el asunto especificado. Esta función admite la marca de tiempo Authenticode. Para realizar la marca de tiempo de infraestructura de clave pública X.509 (RFC 3161), use la función SignerTimeStampEx2.
ms.assetid: fb2c149b-dba2-4879-be97-831037e1110b
title: Función SignerTimeStamp
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStamp
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: c4c57f231f70477a76b4d4f6156354ebc847a715
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127270876"
---
# <a name="signertimestamp-function"></a>Función SignerTimeStamp

La **función SignerTimeStamp** marca el asunto especificado. Esta función admite la marca de tiempo Authenticode. Para realizar la marca de tiempo de infraestructura de clave pública X.509 (RFC 3161), use la [**función SignerTimeStampEx2.**](signertimestampex2.md)

> [!Note]  
> Esta función no tiene ningún archivo de encabezado asociado ni biblioteca de importación. Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.

 

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI SignerTimeStamp(
  _In_     SIGNER_SUBJECT_INFO *pSubjectInfo,
  _In_     LPCWSTR             pwszHttpTimeStamp,
  _In_opt_ PCRYPT_ATTRIBUTES   psRequest,
  _In_opt_ LPVOID              pSipData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSubjectInfo* \[ En\]
</dt> <dd>

Dirección de una estructura [**SIGNER \_ SUBJECT \_ INFO**](signer-subject-info.md) que representa el sujeto al que se va a marcar la hora.

</dd> <dt>

*pwszHttpTimeStamp* \[ En\]
</dt> <dd>

Dirección de una cadena Unicode terminada en NULL que contiene la dirección URL de un servidor de marca de tiempo.

</dd> <dt>

*psRequest* \[ in, opcional\]
</dt> <dd>

Dirección de una estructura [**CRYPT \_ ATTRIBUTES que**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) contiene atributos adicionales que se agregan a la solicitud de marca de tiempo.

Este parámetro es opcional y puede ser **NULL** si no se incluye.

</dd> <dt>

*pSipData* \[ in, opcional\]
</dt> <dd>

Valor de 32 bits que se pasa como datos adicionales a las funciones de SIP. El proveedor DE SIP define el formato y el contenido de este.

Este parámetro es opcional y puede ser **NULL** si no se incluye.

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



 

 
