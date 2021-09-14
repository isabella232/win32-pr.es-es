---
description: Especifica el nombre de la plantilla de certificado.
ms.assetid: 15d22130-e614-4505-94e8-83c2efbf6d87
title: Método ISCrdEnr::setCertTemplateName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setCertTemplateName
- SCrdEnr.setCertTemplateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 53ba18626a7d2bb703ed4d11953fb4872cf9257c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170950"
---
# <a name="iscrdenrsetcerttemplatename-method"></a>Método ISCrdEnr::setCertTemplateName

El **método setCertTemplateName** especifica el nombre de la plantilla de certificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT setCertTemplateName(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName
);
```


```VB

SCrdEnr.setCertTemplateName( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName _
)
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Valor que determina si se establece el nombre real o el nombre para mostrar de la plantilla de certificado. Si *dwFlags tiene* el valor SCARD ENROLL CERT TEMPLATE DISPLAY NAME, se establece el nombre para mostrar de la \_ plantilla de \_ \_ \_ \_ certificado. De lo contrario, se establece el nombre real de la plantilla de certificado.

</dd> <dt>

*bstrCertTemplateName* \[ En\]
</dt> <dd>

Nombre de la plantilla de certificado que se usará en la solicitud de certificado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="vb"></a>VB

Si el método se realiza correctamente, el método devuelve S \_ OK.

Si se produce un error en el método , devuelve un **valor HRESULT** que indica el error. Para obtener una lista de códigos de error comunes, vea [Common HRESULT Values](common-hresult-values.md).

## <a name="remarks"></a>Observaciones

Si no establece el nombre de la plantilla de certificado llamando a **ISCrdEnr::setCertTemplateName**, el nombre tiene como valor predeterminado el nombre de la lista de plantillas de certificado disponibles.

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

[**ISCrdEnr::getCertTemplateName**](iscrdenr-getcerttemplatename.md)
</dt> </dl>

 

 




