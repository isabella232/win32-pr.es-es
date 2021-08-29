---
description: Establece la seguridad de una clave del Registro abierta en un subárbol del Registro sin conexión.
ms.assetid: 002866bb-1532-41ad-a4db-a32d6e1c0a6a
title: Función ORSetKeySecurity (Offreg.h)
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
ms.openlocfilehash: 933bc37e8bc4a79191d781fa5981e8633939757482d6156a7a08f7da6a36cff2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758435"
---
# <a name="orsetkeysecurity-function"></a>Función ORSetKeySecurity

Establece la seguridad de una clave del Registro abierta en un subárbol del Registro sin conexión.

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

*Identificador* \[ En\]
</dt> <dd>

Identificador de una clave del Registro abierta en un subárbol del Registro sin conexión.

</dd> <dt>

*SecurityInformation* \[ En\]
</dt> <dd>

Marcas de bits que indican el tipo de información de seguridad que se debe establecer. Este parámetro puede ser una combinación de las marcas de bits [ \_ SECURITY INFORMATION.](../secauthz/security-information.md)

</dd> <dt>

*pSecurityDescriptor* \[ En\]
</dt> <dd>

Puntero a una estructura [ \_ DESCRIPTOR DE SEGURIDAD](/windows/win32/api/winnt/ns-winnt-security_descriptor) que especifica los atributos de seguridad que se establecerán para la clave especificada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, la función devuelve ERROR \_ SUCCESS.

Si se produce un error en la función, devuelve un código de error distinto de cero definido en Winerror.h. Puede usar la función [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) con la marca FORMAT \_ MESSAGE FROM SYSTEM para obtener una descripción genérica del \_ \_ error.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|---------------------------------------------------------------------------------------|
| Redistribuible<br/> | Windows Biblioteca del Registro sin conexión versión 1.0 o posterior<br/>                      |
| Header<br/>          | <dl> <dt>Offreg.h</dt> </dl>   |
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

[DESCRIPTOR \_ DE SEGURIDAD](/windows/win32/api/winnt/ns-winnt-security_descriptor)
</dt> <dt>

[INFORMACIÓN DE \_ SEGURIDAD](../secauthz/security-information.md)
</dt> </dl>

 

 
