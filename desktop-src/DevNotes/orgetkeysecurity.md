---
description: Recupera una copia del descriptor de seguridad que protege la clave del registro abierta especificada en un subárbol del registro sin conexión.
ms.assetid: 676d5be5-d9d8-48c6-848a-917d1a0474c6
title: Función ORGetKeySecurity (Offreg. h)
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
ms.openlocfilehash: 13594493af2e7992471d13dce30f0a848501c4bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649981"
---
# <a name="orgetkeysecurity-function"></a>ORGetKeySecurity función)

Recupera una copia del descriptor de seguridad que protege la clave del registro abierta especificada en un subárbol del registro sin conexión.

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

*Identificador* \[ de de\]
</dt> <dd>

Identificador de una clave del registro abierta en un subárbol del registro sin conexión.

</dd> <dt>

*SecurityInformation* \[ de\]
</dt> <dd>

Valor [de \_ información de seguridad](../secauthz/security-information.md) que indica la información de seguridad solicitada.

</dd> <dt>

*pSecurityDescriptor* \[ out, opcional\]
</dt> <dd>

Un puntero a un búfer que recibe una copia del descriptor de seguridad solicitado. Este parámetro puede ser **NULL**.

</dd> <dt>

*lpcbSecurityDescriptor* \[ in, out\]
</dt> <dd>

Puntero a una variable que especifica el tamaño, en bytes, del búfer al que apunta el parámetro *pSecurityDescriptor* . Cuando la función devuelve, la variable contiene el número de bytes escritos en el búfer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, la función devuelve el ERROR \_ Success.

Si se produce un error en la función, devuelve un código de error distinto de cero definido en Winerror. h. Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la \_ \_ marca de formato mensaje de \_ sistema para obtener una descripción genérica del error.

Si el búfer especificado por el parámetro *pSecurityDescriptor* es demasiado pequeño, la función devuelve un error de \_ búfer insuficiente \_ y el parámetro *lpcbSecurityDescriptor* contiene el número de bytes necesarios para el descriptor de seguridad solicitado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|---------------------------------------------------------------------------------------|
| Redistribuible<br/> | Windows offline Registry Library versión 1,0 o posterior<br/>                      |
| Encabezado<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| Archivo DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ORDeleteKey**](ordeletekey.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> <dt>

[**ORSetKeySecurity**](orsetkeysecurity.md)
</dt> <dt>

[información de seguridad \_](../secauthz/security-information.md)
</dt> </dl>

 

 
