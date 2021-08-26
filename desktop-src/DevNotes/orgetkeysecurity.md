---
description: Recupera una copia del descriptor de seguridad que protege la clave del Registro abierta especificada en un subárbol del Registro sin conexión.
ms.assetid: 676d5be5-d9d8-48c6-848a-917d1a0474c6
title: Función ORGetKeySecurity (Offreg.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetKeySecurity
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 786321db22c513e7698fcd1661d173ccb5fdf76f1b09d9dd3e739ddf3fb2ca47
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984165"
---
# <a name="orgetkeysecurity-function"></a>Función ORGetKeySecurity

Recupera una copia del descriptor de seguridad que protege la clave del Registro abierta especificada en un subárbol del Registro sin conexión.

## <a name="syntax"></a>Sintaxis


```C++
DWORD ORGetKeySecurity(
  _In_      ORHKEY               Handle,
  _In_      SECURITY_INFORMATION SecurityInformation,
  _Out_opt_ PSECURITY_DESCRIPTOR pSecurityDescriptor,
  _Inout_   PDWORD               lpcbSecurityDescriptor
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Identificador* \[ En\]
</dt> <dd>

Identificador de una clave del Registro abierta en un subárbol del Registro sin conexión.

</dd> <dt>

*SecurityInformation* \[ En\]
</dt> <dd>

Valor [DE \_ INFORMACIÓN DE](../secauthz/security-information.md) SEGURIDAD que indica la información de seguridad solicitada.

</dd> <dt>

*pSecurityDescriptor* \[ out, opcional\]
</dt> <dd>

Puntero a un búfer que recibe una copia del descriptor de seguridad solicitado. Este parámetro puede ser **NULL**.

</dd> <dt>

*lpcbSecurityDescriptor* \[ in, out\]
</dt> <dd>

Puntero a una variable que especifica el tamaño, en bytes, del búfer al que apunta el *parámetro pSecurityDescriptor.* Cuando la función devuelve un resultado, la variable contiene el número de bytes escritos en el búfer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, la función devuelve ERROR \_ SUCCESS.

Si se produce un error en la función, devuelve un código de error distinto de cero definido en Winerror.h. Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la marca FORMAT \_ MESSAGE FROM SYSTEM para obtener una descripción genérica del \_ \_ error.

Si el búfer especificado por el parámetro *pSecurityDescriptor* es demasiado pequeño, la función devuelve ERROR INSUFFICIENT BUFFER y el parámetro \_ \_ *lpcbSecurityDescriptor* contiene el número de bytes necesarios para el descriptor de seguridad solicitado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|---------------------------------------------------------------------------------------|
| Redistribuible<br/> | Windows Biblioteca del Registro sin conexión versión 1.0 o posterior<br/>                      |
| Header<br/>          | <dl> <dt>Offreg.h</dt> </dl>   |
| Archivo DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ORDeleteKey**](ordeletekey.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> <dt>

[**ORSetKeySecurity**](orsetkeysecurity.md)
</dt> <dt>

[INFORMACIÓN DE \_ SEGURIDAD](../secauthz/security-information.md)
</dt> </dl>

 

 
