---
description: Se usa para determinar si una plantilla de certificado contiene el uso de clave szOID \_ PKIX \_ KP EMAIL \_ \_ PROTECTION.
ms.assetid: 1f0512e0-68b6-4b79-84bd-614babb4151d
title: Método ISCrdEnr::getCertTemplateSMIME
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
ms.openlocfilehash: 8da8c9c3202c0955a001a63e77f85858fc6237d7476c0fc5222ae8f85e94a7c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119515965"
---
# <a name="iscrdenrgetcerttemplatesmime-method"></a>Método ISCrdEnr::getCertTemplateSMIME

El **método getCertTemplateSMIME** se usa para determinar si una plantilla de certificado contiene el uso de clave szOID \_ PKIX KP EMAIL \_ \_ \_ PROTECTION.

Si este uso de clave forma parte de la plantilla de certificado, la plantilla de certificado admite operaciones de extensiones de correo electrónico de Internet (S/MIME) [*seguras*](../secgloss/s-gly.md) o multipropósito.

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

*bstrCertTemplateName* \[ En\]
</dt> <dd>

Nombre del certificado que se consulta para el uso de la clave S/MIME.

</dd> <dt>

*pdwCertTemplateSMIME* \[ out\]
</dt> <dd>

Puntero a un **DWORD que** devuelve un valor de uno si *bstrCertTemplateName* admite S/MIME; de lo contrario, devuelve cero.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="c"></a>C++

Si el método se realiza correctamente, el método devuelve S \_ OK.

Si se produce un error en el método , devuelve un **valor HRESULT** que indica el error. Para obtener una lista de códigos de error comunes, vea [Common HRESULT Values](common-hresult-values.md).

### <a name="vb"></a>VB

**Valor** largo de uno si *bstrCertTemplateName admite* S/MIME; de lo contrario, cero.

## <a name="remarks"></a>Comentarios

La constante de szOID \_ PKIX \_ KP EMAIL PROTECTION se define en \_ \_ Wincrypt.h.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID ISCrdEnr se define como \_ 753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISCrdEnr**](iscrdenr.md)
</dt> <dt>

[**ISCrdEnr::enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))
</dt> </dl>

 

 
