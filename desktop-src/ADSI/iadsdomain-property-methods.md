---
title: Métodos de propiedad IADsDomain (Iads.h)
description: Los métodos de interfaz IADsDomain leen y escriben las propiedades descritas en este tema. Para obtener más información, vea Métodos de propiedad de interfaz.
ms.assetid: ff2c4cbc-a8d5-4db5-85d4-da3367f27fa0
ms.tgt_platform: multiple
keywords:
- ADSI de métodos de propiedad IADsDomain
topic_type:
- apiref
api_name:
- IADsDomain Property Methods
- IADsDomain.AutoUnlockInterval
- IADsDomain.get_AutoUnlockInterval
- IADsDomain.put_AutoUnlockInterval
- IADsDomain.IsWorkgroup
- IADsDomain.get_IsWorkgroup
- IADsDomain.LockoutObservationInterval
- IADsDomain.get_LockoutObservationInterval
- IADsDomain.put_LockoutObservationInterval
- IADsDomain.MinPasswordAge
- IADsDomain.get_MinPasswordAge
- IADsDomain.put_MinPasswordAge
- IADsDomain.MinPasswordLength
- IADsDomain.get_MinPasswordLength
- IADsDomain.put_MinPasswordLength
- IADsDomain.MaxBadPasswordsAllowed
- IADsDomain.get_MaxBadPasswordsAllowed
- IADsDomain.put_MaxBadPasswordsAllowed
- IADsDomain.MaxPasswordAge
- IADsDomain.get_MaxPasswordAge
- IADsDomain.put_MaxPasswordAge
- IADsDomain.PasswordAttributes
- IADsDomain.get_PasswordAttributes
- IADsDomain.put_PasswordAttributes
- IADsDomain.PasswordHistoryLength
- IADsDomain.get_PasswordHistoryLength
- IADsDomain.put_PasswordHistoryLength
api_location:
- Activeds.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90769faec8bc5e05f1aa590dd3211125665a4b07228b920e622fc5b33754e322
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082499"
---
# <a name="iadsdomain-property-methods"></a>Métodos de propiedad IADsDomain

Los [**métodos de interfaz IADsDomain**](/windows/desktop/api/Iads/nn-iads-iadsdomain) leen y escriben las propiedades descritas en este tema. Para obtener más información, vea [Métodos de propiedad de interfaz](interface-property-methods.md).

## <a name="properties"></a>Propiedades

<dl> <dt>

**AutoUnlockInterval**
</dt> <dd> <dl>

Indica el tiempo mínimo que debe transcurrir antes de que la cuenta se vuelva a habilitar automáticamente.

<dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Tipo de datos de scripting: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_AutoUnlockInterval(
  [out] LONG* plAutoUnlockInterval
);
HRESULT put_AutoUnlockInterval(
  [in] LONG lAutoUnlockInterval
);
```


</dt> </dl> </dd> <dt>

**IsWorkgroup**
</dt> <dd> <dl>

Esta propiedad ya no se implementa.

<dt>

Tipo de acceso: solo lectura
</dt> <dt>

Tipo de datos de scripting: **VARIANT \_ BOOL**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_IsWorkgroup(
  [out] VARIANT_BOOL* retval
);
```


</dt> </dl> </dd> <dt>

**LockoutObservationInterval**
</dt> <dd> <dl>

Indica el período de tiempo durante el cual se supervisa y acumula el número de contraseñas incorrectas antes de determinar si la cuenta debe bloquearse. Por ejemplo, si el número de intentos de contraseña incorrecta en una cuenta supera el umbral (se permiten contraseñas incorrectas máximas) durante el período de tiempo especificado (intervalo de observación de bloqueo), la cuenta se bloqueará estableciendo la propiedad adecuada en el conjunto de propiedades Parámetro de inicio de sesión.

<dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Tipo de datos de scripting: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_LockoutObservationInterval(
  [out] LONG* plLockoutObservationInterval
);
HRESULT put_LockoutObservationInterval(
  [in] LONG lLockoutObservationInterval
);
```


</dt> </dl> </dd> <dt>

**MaxBadPasswordsAllowed**
</dt> <dd> <dl>

Indica el número máximo de inicios de sesión con contraseña incorrecta permitidos antes de un bloqueo de cuenta.

<dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Tipo de datos de scripting: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxBadPasswordsAllowed(
  [out] LONG* plMaxBadPasswordsAllowed
);
HRESULT put_MaxBadPasswordsAllowed(
  [in] LONG lMaxBadPasswordsAllowed
);
```


</dt> </dl> </dd> <dt>

**MaxPasswordAge**
</dt> <dd> <dl>

Indica el intervalo de tiempo máximo, en segundos, después del cual el usuario debe cambiar la contraseña.

<dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Tipo de datos de scripting: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MaxPasswordAge(
  [out] LONG* plMaxPasswordAge
);
RESULT put_MaxPasswordAge(
  [in] LONG lMaxPasswordAge
);
```


</dt> </dl> </dd> <dt>

**MinPasswordAge**
</dt> <dd> <dl>

Indica el intervalo de tiempo mínimo, en segundos, antes de que se pueda cambiar la contraseña.

<dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Tipo de datos de scripting: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MinPasswordAge(
  [out] LONG* plMinPasswordAge
);
HRESULT put_MinPasswordAge(
  [in] LONG lMinPasswordAge
);
```


</dt> </dl> </dd> <dt>

**MinPasswordLength**
</dt> <dd> <dl>

Indica el número mínimo de caracteres que se deben usar para una contraseña.

<dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Tipo de datos de scripting: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_MinPasswordLength(
  [out] LONG* plMinPasswordLength
);
HRESULT put_MinPasswordLength(
  [in] LONG lMinPasswordLength
);
```


</dt> </dl> </dd> <dt>

**PasswordAttributes**
</dt> <dd> <dl>

Indica restricciones en las contraseñas, tal como se define en la siguiente lista de atributos y valores.

> [!Note]  
> Para PASSWORD ATTR COMPLEX, la contraseña debe incluir al menos un signo de \_ \_ puntuación o un carácter no imprimible.

 

<dt>

<span id="PASSWORD_ATTR_NONE"></span><span id="password_attr_none"></span>

**PASSWORD \_ ATTR \_ NONE** (0x00000000)


</dt> <dd></dd> <dt>

<span id="PASSWORD_ATTR_MIXED_CASE"></span><span id="password_attr_mixed_case"></span>

**PASSWORD \_ ATTR \_ MIXED \_ CASE** (0x00000001)


</dt> <dd></dd> <dt>

<span id="PASSWORD_ATTR_COMPLEX"></span><span id="password_attr_complex"></span>

**PASSWORD \_ ATTR \_ COMPLEX** (0x00000002)


</dt> <dd></dd> </dl> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Tipo de datos de scripting: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PasswordAttributes(
  [out] LONG* plPasswordAttributes
);
HRESULT put_PasswordAttributes(
  [in] LONG lPasswordAttributes
);
```


</dt> </dl> </dd> <dt>

**PasswordHistoryLength**
</dt> <dd> <dl>

Indica el número de contraseñas anteriores guardadas en la lista de historial. El usuario no puede reutilizar una contraseña en la lista de historial.

<dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Tipo de datos de scripting: **LONG**
</dt> <dt>



``` syntax
// C++ method syntax
HRESULT get_PasswordHistoryLength(
  [out] LONG* plPasswordHistoryLength
);
HRESULT put_PasswordHistoryLength(
  [in] LONG lPasswordHistoryLength
);
```


</dt> </dl> </dd> </dl>

 

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se muestra el valor **de la propiedad PasswordHistoryLength.**


```VB
Dim dom As IADsDomain
On Error Resume Next

Set dom = GetObject("WinNT://myDomain")

debug.print "PasswordHistoryLength" & dom.PasswordHistoryLength
```



En el ejemplo de código siguiente se muestra el valor **de la propiedad PasswordHistoryLength.**


```C++
LPWSTR adsPath = L"WinNT://myDomain";
LONG nPasswordHistoryLength = 0;

// Bind to the domain object.
hr = ADsGetObject(adsPath,IID_IADsDomain,(void**)&pDomain);
if(FAILED(hr)) {goto Cleanup;}

hr = pDomain->get_PasswordHistoryLength(&nPasswordHistoryLength);
if(FAILED(hr)) {goto Cleanup;}
printf("Password history length: %d",nPasswordHistoryLength);

Cleanup:
    if(pDomain) pDomain->Release();
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Iads.h</dt> </dl>       |
| Archivo DLL<br/>                      | <dl> <dt>Activeds.dll</dt> </dl> |
| IID<br/>                      | IID \_ IADsDomain se define como 00E4C220-FD16-11CE-ABC4-02608C9E7553<br/>           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IADsDomain**](/windows/desktop/api/Iads/nn-iads-iadsdomain)
</dt> <dt>

[Métodos de propiedad de interfaz](interface-property-methods.md)
</dt> </dl>

 

 





