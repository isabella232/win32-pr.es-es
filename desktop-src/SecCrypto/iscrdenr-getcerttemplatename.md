---
description: Recupera el nombre de la plantilla de certificado.
ms.assetid: 26fd758a-b348-4efb-841b-c8f2ab88efea
title: Método ISCrdEnr::getCertTemplateName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCertTemplateName
- SCrdEnr.getCertTemplateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 4eee84140e0a23b8a0dd5d26099ca61b868a90fa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127270956"
---
# <a name="iscrdenrgetcerttemplatename-method"></a>Método ISCrdEnr::getCertTemplateName

El **método getCertTemplateName** recupera el nombre de la plantilla de certificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT getCertTemplateName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrCertTemplateName
);
```


```VB

SCrdEnr.getCertTemplateName( _
  ByVal dwFlags, _
  ByRef pbstrCertTemplateName _
)
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Valor que determina si se devuelve el nombre real o el nombre para mostrar de la plantilla de certificado. Si *dwFlags tiene* el valor SCARD ENROLL CERT TEMPLATE DISPLAY NAME, se recupera el nombre para mostrar de la plantilla de certificado; de lo contrario, se muestra el nombre real de \_ la plantilla de \_ \_ \_ \_ certificado.

</dd> <dt>

*pbstrCertTemplateName* \[ out\]
</dt> <dd>

Puntero a una cadena que devuelve el nombre de la plantilla de certificado que se usará en la solicitud [*de certificado.*](../secgloss/c-gly.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="c"></a>C++

Si el método se realiza correctamente, el método devuelve S \_ OK.

Si se produce un error en el método , devuelve un **valor HRESULT** que indica el error. Para obtener una lista de códigos de error comunes, vea [Common HRESULT Values](common-hresult-values.md).

### <a name="vb"></a>VB

Cadena que representa el nombre de la plantilla de certificado que se usará en la solicitud [*de certificado*](../secgloss/c-gly.md).

## <a name="remarks"></a>Observaciones

Si no establece el nombre de la plantilla de certificado llamando a [**ISCrdEnr::setCertTemplateName**](iscrdenr-setcerttemplatename.md), el nombre tiene como valor predeterminado el nombre de la lista de plantillas de certificado disponibles.

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

[**ISCrdEnr::setCertTemplateName**](iscrdenr-setcerttemplatename.md)
</dt> </dl>

 

 
