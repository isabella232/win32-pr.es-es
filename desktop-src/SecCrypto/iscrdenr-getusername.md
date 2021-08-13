---
description: Recupera el nombre del usuario en cuyo nombre está prevista la inscripción del certificado.
ms.assetid: 7bd71944-f7dd-4c92-a71c-ecc5c0afd5b2
title: Método ISCrdEnr::getUserName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getUserName
- SCrdEnr.getUserName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: b61dd43980049355621c2ee4085634303c55e0f9dac79db839602d07c7d61f94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119409454"
---
# <a name="iscrdenrgetusername-method"></a>Método ISCrdEnr::getUserName

El **método getUserName** recupera el nombre del usuario en cuyo nombre está prevista la inscripción del certificado.

Antes de llamar a este método, debe especificar el nombre de usuario en una llamada a [**ISCrdEnr::selectUserName**](iscrdenr-selectusername.md) o [**ISCrdEnr::setUserName**](iscrdenr-setusername.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT getUserName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrUserName
);
```


```VB

SCrdEnr.getUserName( _
  ByVal dwFlags, _
  ByRef pbstrUserName _
)
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Este valor debe ser cero (0), SCARD ENROLL UPN NAME o \_ \_ \_ SCARD \_ ENROLL SAM \_ COMPATIBLE \_ \_ NAME.

Si este valor es SCARD ENROLL UPN NAME, getUserName devuelve el nombre \_ \_ principal universal \_ (UPN) del usuario, como "  someone@example.com ".

Si este valor es SCARD ENROLL SAM COMPATIBLE NAME, el método devuelve el nombre del administrador de acceso de seguridad (SAM) del usuario con el formato \_ \_ \_ \_ "USUARIO \\ DE DOMINIO".

Si este valor es cero, el método devuelve el nombre UPN del usuario si existe. Si el usuario no tiene un nombre UPN, el método devuelve el nombre SAM del usuario.

</dd> <dt>

*pbstrUserName* \[ out\]
</dt> <dd>

Puntero a una cadena que devuelve el nombre del usuario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="c"></a>C++

Si el método se realiza correctamente, el método devuelve S \_ OK.

Si se produce un error en el método, devuelve un **valor HRESULT** que indica el error. Para obtener una lista de códigos de error comunes, vea [Common HRESULT Values](common-hresult-values.md).

### <a name="vb"></a>VB

Cadena que representa el nombre del usuario.

## <a name="remarks"></a>Comentarios

Puede especificar el nombre del usuario [](../secgloss/s-gly.md) al que se emite la tarjeta inteligente llamando a [**ISCrdEnr::setUserName**](iscrdenr-setusername.md) o [**ISCrdEnr::selectUserName**](iscrdenr-selectusername.md). Una vez especificado un nombre de usuario, su valor se puede recuperar llamando a **getUserName**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID ISCrdEnr se define como \_ 753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ISCrdEnr**](iscrdenr.md)
</dt> <dt>

[**ISCrdEnr::resetUser**](iscrdenr-resetuser.md)
</dt> <dt>

[**ISCrdEnr::selectUserName**](iscrdenr-selectusername.md)
</dt> <dt>

[**ISCrdEnr::setUserName**](iscrdenr-setusername.md)
</dt> </dl>

 

 
