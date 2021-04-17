---
description: Especifica el nombre de la plantilla de certificado.
ms.assetid: 15d22130-e614-4505-94e8-83c2efbf6d87
title: 'ISCrdEnr:: setCertTemplateName (método)'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687596"
---
# <a name="iscrdenrsetcerttemplatename-method"></a>ISCrdEnr:: setCertTemplateName (método)

El método **setCertTemplateName** especifica el nombre de la plantilla de certificado.

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

*dwFlags* \[ de\]
</dt> <dd>

Valor que determina si se está configurando el nombre real o el nombre para mostrar de la plantilla de certificado. Si *dwFlags* tiene el valor de la \_ \_ \_ plantilla de certificado \_ \_ de inscripción, se establece el nombre para mostrar de la plantilla de certificado. De lo contrario, se establece el nombre real de la plantilla de certificado.

</dd> <dt>

*bstrCertTemplateName* \[ de\]
</dt> <dd>

Nombre de la plantilla de certificado que se utilizará en la solicitud de certificado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="vb"></a>VB

Si el método se ejecuta correctamente, el método devuelve S \_ correcto.

Si se produce un error en el método, devuelve un valor **HRESULT** que indica el error. Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).

## <a name="remarks"></a>Observaciones

Si no establece el nombre de la plantilla de certificado mediante una llamada a **ISCrdEnr:: setCertTemplateName**, el nombre tiene como valor predeterminado el nombre en la lista de plantillas de certificado disponibles.

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

[**ISCrdEnr::getCertTemplateName**](iscrdenr-getcerttemplatename.md)
</dt> </dl>

 

 




