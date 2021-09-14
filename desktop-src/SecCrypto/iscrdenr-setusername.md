---
description: Especifica el nombre del usuario en cuyo nombre está prevista la inscripción del certificado.
ms.assetid: e088af63-5064-4b1b-976f-047f52e56af8
title: Método ISCrdEnr::setUserName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setUserName
- SCrdEnr.setUserName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: cc2d3157e41fc7ffd9fc0bf7f607de137559e751
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170946"
---
# <a name="iscrdenrsetusername-method"></a>Método ISCrdEnr::setUserName

El **método setUserName** especifica el nombre del usuario en cuyo nombre está prevista la inscripción de certificados.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT setUserName(
  [in] DWORD dwFlags,
  [in] BSTR bstrUserName
);
```


```VB

SCrdEnr.setUserName( _
  ByVal dwFlags, _
  ByVal bstrUserName _
)
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Este valor debe ser SCARD \_ ENROLL \_ UPN NAME (definido como 1) o \_ SCARD ENROLL SAM \_ COMPATIBLE \_ NAME \_ \_ (definido como 2).

Establezca este valor en SCARD ENROLL UPN NAME si el nombre especificado en \_ \_ \_ *bstrUserName* es el nombre principal universal del usuario, como " someone@example.com ". El nombre de UPN del usuario debe corresponder a un nombre de administrador de acceso de seguridad (SAM) existente.

Establezca este valor en SCARD ENROLL SAM COMPATIBLE NAME si el nombre especificado en bstrUserName es el nombre SAM del usuario con el formato \_ \_ \_ \_ "DOMAIN  \\ USER".

</dd> <dt>

*bstrUserName* \[ En\]
</dt> <dd>

Nombre del usuario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="vb"></a>VB

Si el método se realiza correctamente, el método devuelve S \_ OK.

Si se produce un error en el método , devuelve un **valor HRESULT** que indica el error. Para obtener una lista de códigos de error comunes, vea [Common HRESULT Values](common-hresult-values.md).

## <a name="remarks"></a>Observaciones

Llame a este método para especificar el nombre de usuario al que se va a emitir la [*tarjeta inteligente*](../secgloss/s-gly.md). Una alternativa a **setUserName** [**es ISCrdEnr::selectUserName.**](iscrdenr-selectusername.md)

Una vez especificado un nombre de usuario, su valor se puede recuperar llamando a [**getUserName**](iscrdenr-getusername.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID ISCrdEnr se define como \_ 753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ISCrdEnr**](iscrdenr.md)
</dt> <dt>

[**ISCrdEnr::getUserName**](iscrdenr-getusername.md)
</dt> <dt>

[**ISCrdEnr::resetUser**](iscrdenr-resetuser.md)
</dt> <dt>

[**ISCrdEnr::selectUserName**](iscrdenr-selectusername.md)
</dt> </dl>

 

 
