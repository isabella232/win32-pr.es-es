---
description: Recupera el nombre de la plantilla de certificado.
ms.assetid: 26fd758a-b348-4efb-841b-c8f2ab88efea
title: 'ISCrdEnr:: getCertTemplateName (método)'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278801"
---
# <a name="iscrdenrgetcerttemplatename-method"></a>ISCrdEnr:: getCertTemplateName (método)

El método **getCertTemplateName** recupera el nombre de la plantilla de certificado.

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

*dwFlags* \[ de\]
</dt> <dd>

Valor que determina si se devuelve el nombre real o el nombre para mostrar de la plantilla de certificado. Si *dwFlags* tiene el valor PPAC inscribir el nombre para mostrar de la plantilla de certificado \_ \_ \_ \_ \_ , se recupera el nombre para mostrar de la plantilla de certificado; de lo contrario, se muestra el nombre real de la plantilla de certificado.

</dd> <dt>

*pbstrCertTemplateName* \[ enuncia\]
</dt> <dd>

Un puntero a una cadena que devuelve el nombre de la plantilla de certificado que se utilizará en la [*solicitud de certificado*](../secgloss/c-gly.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="c"></a>C++

Si el método se ejecuta correctamente, el método devuelve S \_ correcto.

Si se produce un error en el método, devuelve un valor **HRESULT** que indica el error. Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).

### <a name="vb"></a>VB

Cadena que representa el nombre de la plantilla de certificado que se utilizará en la [*solicitud de certificado*](../secgloss/c-gly.md).

## <a name="remarks"></a>Observaciones

Si no establece el nombre de la plantilla de certificado mediante una llamada a [**ISCrdEnr:: setCertTemplateName**](iscrdenr-setcerttemplatename.md), el nombre tiene como valor predeterminado el nombre en la lista de plantillas de certificado disponibles.

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

[**ISCrdEnr::setCertTemplateName**](iscrdenr-setcerttemplatename.md)
</dt> </dl>

 

 
