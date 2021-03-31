---
description: Recupera el nombre del usuario en cuyo nombre está diseñada la inscripción de certificados.
ms.assetid: 7bd71944-f7dd-4c92-a71c-ecc5c0afd5b2
title: 'ISCrdEnr:: getUserName (método)'
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
ms.openlocfilehash: 51f551a704f3a98b932e646c95810f928e73bac7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361300"
---
# <a name="iscrdenrgetusername-method"></a>ISCrdEnr:: getUserName (método)

El método **getUserName** recupera el nombre del usuario en cuyo nombre está dirigida la inscripción del certificado.

Antes de llamar a este método, debe especificar el nombre de usuario en una llamada a [**ISCrdEnr:: selectUserName**](iscrdenr-selectusername.md) o [**ISCrdEnr:: setUserName**](iscrdenr-setusername.md).

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

*dwFlags* \[ de\]
</dt> <dd>

Este valor debe ser cero (0), \_ nombre de UPN de inscripción PPAC \_ \_ o \_ \_ \_ nombre compatible con el SAM de inscripción \_ .

Si este valor es PPAC \_ ENROLL \_ UPN \_ Name, **GetUserName** devuelve el nombre principal universal (UPN) del usuario, como " someone@example.com ".

Si este valor es PPAC \_ inscribir \_ \_ el nombre compatible con Sam \_ , el método devuelve el nombre del administrador de acceso de seguridad (SAM) del usuario con el formato "dominio \\ usuario".

Si este valor es cero, el método devuelve el nombre UPN del usuario, si existe. Si el usuario no tiene un nombre UPN, el método devuelve el nombre del SAM del usuario.

</dd> <dt>

*pbstrUserName* \[ enuncia\]
</dt> <dd>

Puntero a una cadena que devuelve el nombre del usuario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="c"></a>C++

Si el método se ejecuta correctamente, el método devuelve S \_ correcto.

Si se produce un error en el método, devuelve un valor **HRESULT** que indica el error. Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).

### <a name="vb"></a>VB

Cadena que representa el nombre del usuario.

## <a name="remarks"></a>Observaciones

Puede especificar el nombre del usuario al que se emite la [*tarjeta inteligente*](../secgloss/s-gly.md) llamando a [**ISCrdEnr:: setUserName**](iscrdenr-setusername.md) o [**ISCrdEnr:: selectUserName**](iscrdenr-selectusername.md). Una vez que se ha especificado un nombre de usuario, su valor se puede recuperar llamando a **getUserName**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCrdEnr se define como 753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISCrdEnr**](iscrdenr.md)
</dt> <dt>

[**ISCrdEnr:: resetuser**](iscrdenr-resetuser.md)
</dt> <dt>

[**ISCrdEnr::selectUserName**](iscrdenr-selectusername.md)
</dt> <dt>

[**ISCrdEnr::setUserName**](iscrdenr-setusername.md)
</dt> </dl>

 

 
