---
description: Marca de tiempo el sujeto especificado. Esta función admite la marca de tiempo de Authenticode. Para realizar una marca de tiempo de la infraestructura de clave pública (RFC 3161) de X. 509, utilice la función SignerTimeStampEx2.
ms.assetid: fb2c149b-dba2-4879-be97-831037e1110b
title: SignerTimeStamp función)
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002667"
---
# <a name="signertimestamp-function"></a>SignerTimeStamp función)

El tiempo de la función **SignerTimeStamp** marca el sujeto especificado. Esta función admite la marca de tiempo de Authenticode. Para realizar una marca de tiempo de la infraestructura de clave pública (RFC 3161) de X. 509, utilice la función [**SignerTimeStampEx2**](signertimestampex2.md) .

> [!Note]  
> Esta función no tiene asociado ningún archivo de encabezado ni biblioteca de importación. Para llamar a esta función, debe crear un archivo de encabezado definido por el usuario y usar las funciones [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a Mssign32.dll.

 

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

*pSubjectInfo* \[ de\]
</dt> <dd>

Dirección de una estructura de [**\_ \_ información de asunto del firmante**](signer-subject-info.md) que representa el sujeto de marca de tiempo.

</dd> <dt>

*pwszHttpTimeStamp* \[ de\]
</dt> <dd>

Dirección de una cadena Unicode terminada en null que contiene la dirección URL de un servidor de marca de tiempo.

</dd> <dt>

*psRequest* \[ en, opcional\]
</dt> <dd>

Dirección de una estructura [**de \_ atributos de cifrado**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) que contiene atributos adicionales que se agregan a la solicitud de marca de tiempo.

Este parámetro es opcional y puede ser **null** si no se incluye.

</dd> <dt>

*pSipData* \[ en, opcional\]
</dt> <dd>

Valor de 32 bits que se pasa como datos adicionales a las funciones de SIP. El proveedor SIP define el formato y el contenido de este.

Este parámetro es opcional y puede ser **null** si no se incluye.

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



 

 
