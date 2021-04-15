---
description: Especifica el nombre del usuario en cuyo nombre se ha diseñado la inscripción de certificados.
ms.assetid: e088af63-5064-4b1b-976f-047f52e56af8
title: 'ISCrdEnr:: setUserName (método)'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688674"
---
# <a name="iscrdenrsetusername-method"></a>ISCrdEnr:: setUserName (método)

El método **setUserName** especifica el nombre del usuario en cuyo nombre se ha diseñado la inscripción de certificados.

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

*dwFlags* \[ de\]
</dt> <dd>

Este valor debe ser el \_ \_ \_ nombre de UPN de inscripción PPAC (definido como 1) o \_ \_ \_ el nombre compatible con el SAM de inscripción de Sam \_ (definido como 2).

Establezca este valor en PPACd \_ ENROLL \_ UPN \_ Name, si el nombre especificado en *bstrUserName* es el nombre de la entidad de seguridad universal del usuario, por ejemplo, " someone@example.com ". El nombre de UPN del usuario debe corresponder a un nombre de administrador de acceso de seguridad (SAM) existente.

Establezca este valor en el \_ \_ nombre compatible con el SAM de inscripción \_ \_ , si el nombre especificado en *BSTRUSERNAME* es el nombre del SAM del usuario con el formato "usuario del dominio \\ ".

</dd> <dt>

*bstrUserName* \[ de\]
</dt> <dd>

Nombre del usuario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="vb"></a>VB

Si el método se ejecuta correctamente, el método devuelve S \_ correcto.

Si se produce un error en el método, devuelve un valor **HRESULT** que indica el error. Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).

## <a name="remarks"></a>Observaciones

Llame a este método para especificar el nombre de usuario para el que se va a emitir la [*tarjeta inteligente*](../secgloss/s-gly.md). Una alternativa a **setUserName** es [**ISCrdEnr:: selectUserName**](iscrdenr-selectusername.md).

Una vez que se ha especificado un nombre de usuario, su valor se puede recuperar llamando a [**getUserName**](iscrdenr-getusername.md).

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

[**ISCrdEnr:: getUserName**](iscrdenr-getusername.md)
</dt> <dt>

[**ISCrdEnr:: resetuser**](iscrdenr-resetuser.md)
</dt> <dt>

[**ISCrdEnr::selectUserName**](iscrdenr-selectusername.md)
</dt> </dl>

 

 
