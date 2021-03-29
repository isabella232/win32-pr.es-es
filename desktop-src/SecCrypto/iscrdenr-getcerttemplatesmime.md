---
description: Se usa para determinar si una plantilla de certificado contiene el uso de la \_ clave de \_ protección del correo electrónico szOID PKIX KP \_ \_ .
ms.assetid: 1f0512e0-68b6-4b79-84bd-614babb4151d
title: 'ISCrdEnr:: getCertTemplateSMIME (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCertTemplateSMIME
- SCrdEnr.getCertTemplateSMIME
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 4ed66af6a8a91855fbfc5a972a8bf00358314663
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912017"
---
# <a name="iscrdenrgetcerttemplatesmime-method"></a>ISCrdEnr:: getCertTemplateSMIME (método)

El método **getCertTemplateSMIME** se usa para determinar si una plantilla de certificado contiene el \_ uso de claves de protección de correo electrónico de szOID PKIX \_ PK \_ \_ .

Si el uso de esta clave forma parte de la plantilla de certificado, la plantilla de certificado admite operaciones de [*extensiones seguras multipropósito de correo Internet*](../secgloss/s-gly.md) (S/MIME).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT getCertTemplateSMIME(
  [in]  BSTR      bstrCertTemplateName,
  [out] DWORD *pdwCertTemplateSMIME
);
```


```VB

SCrdEnr.getCertTemplateSMIME( _
  ByVal bstrCertTemplateName, _
  ByRef pdwCertTemplateSMIME _
)
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrCertTemplateName* \[ de\]
</dt> <dd>

Nombre del certificado que se consulta para el uso de la clave S/MIME.

</dd> <dt>

*pdwCertTemplateSMIME* \[ enuncia\]
</dt> <dd>

Un puntero a un **DWORD** que devuelve un valor de uno si *bstrCertTemplateName* admite S/MIME; en caso contrario, devuelve cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="c"></a>C++

Si el método se ejecuta correctamente, el método devuelve S \_ correcto.

Si se produce un error en el método, devuelve un valor **HRESULT** que indica el error. Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).

### <a name="vb"></a>VB

Valor **Long** de uno si *bstrCertTemplateName* admite S/MIME; de lo contrario, es cero.

## <a name="remarks"></a>Observaciones

La constante para la \_ \_ protección de correo electrónico szOID PKIX KP \_ \_ se define en Wincrypt. h.

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

[**ISCrdEnr:: ENROLL**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))
</dt> </dl>

 

 
