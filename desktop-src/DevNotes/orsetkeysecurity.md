---
description: Establece la seguridad de una clave del registro abierta en un subárbol del registro sin conexión.
ms.assetid: 002866bb-1532-41ad-a4db-a32d6e1c0a6a
title: Función ORSetKeySecurity (Offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSetKeySecurity
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: ff63a7d896964f486b5fcb168c08513f8d5703be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670379"
---
# <a name="orsetkeysecurity-function"></a>ORSetKeySecurity función)

Establece la seguridad de una clave del registro abierta en un subárbol del registro sin conexión.

## <a name="syntax"></a>Sintaxis


```C++
DWORD ORSetKeySecurity(
  _In_ ORHKEY               Handle,
  _In_ SECURITY_INFORMATION SecurityInformation,
  _In_ PSECURITY_DESCRIPTOR pSecurityDescriptor
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

Marcas de bits que indican el tipo de información de seguridad que se va a establecer. Este parámetro puede ser una combinación de las marcas de bits de [ \_ información de seguridad](../secauthz/security-information.md) .

</dd> <dt>

*pSecurityDescriptor* \[ de\]
</dt> <dd>

Puntero a una estructura [de \_ descriptores de seguridad](/windows/win32/api/winnt/ns-winnt-security_descriptor) que especifica los atributos de seguridad que se van a establecer para la clave especificada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, la función devuelve el ERROR \_ Success.

Si se produce un error en la función, devuelve un código de error distinto de cero definido en Winerror. h. Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la \_ \_ marca de formato mensaje de \_ sistema para obtener una descripción genérica del error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|---------------------------------------------------------------------------------------|
| Redistribuible<br/> | Windows offline Registry Library versión 1,0 o posterior<br/>                      |
| Encabezado<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| Archivo DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ORCloseKey**](orclosekey.md)
</dt> <dt>

[**ORDeleteKey**](ordeletekey.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> <dt>

[**ORGetKeySecurity**](orgetkeysecurity.md)
</dt> <dt>

[descriptor de seguridad \_](/windows/win32/api/winnt/ns-winnt-security_descriptor)
</dt> <dt>

[información de seguridad \_](../secauthz/security-information.md)
</dt> </dl>

 

 
