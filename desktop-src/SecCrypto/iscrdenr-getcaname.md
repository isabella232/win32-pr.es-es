---
description: Recupera el nombre de la entidad de certificación (CA) especificada para una plantilla de certificado determinada.
ms.assetid: e921710a-7c74-4fda-91e1-fbad45889984
title: 'ISCrdEnr:: getCAName (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCAName
- SCrdEnr.getCAName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: b62b0a7e871a29ff0a8edd28eb8cd5e18e97c1a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278803"
---
# <a name="iscrdenrgetcaname-method"></a>ISCrdEnr:: getCAName (método)

El método **getCAName** recupera el nombre de la entidad de [*certificación*](../secgloss/c-gly.md) (CA) especificada para una plantilla de certificado determinada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT getCAName(
  [in]  DWORD     dwFlags,
  [in]  BSTR     bstrCertTemplateName,
  [out] BSTR *pbstrCAName
);
```


```VB

SCrdEnr.getCAName( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName, _
  ByRef pbstrCAName _
)
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Un valor que determina si el nombre hace referencia al nombre de la entidad de certificación o al nombre del equipo de la CA. Si este valor es PPAC \_ ENROLL \_ CA nombre del \_ equipo \_ (definido como 0x01), el nombre hace referencia al nombre del equipo de la CA; de lo contrario, el nombre hace referencia al nombre de la CA.

</dd> <dt>

*bstrCertTemplateName* \[ de\]
</dt> <dd>

Nombre de la plantilla de certificado.

</dd> <dt>

*pbstrCAName* \[ enuncia\]
</dt> <dd>

Puntero a una cadena que devuelve el nombre de la entidad de certificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="c"></a>C++

Si el método se ejecuta correctamente, el método devuelve S \_ correcto.

Si se produce un error en el método, devuelve un valor **HRESULT** que indica el error. Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).

### <a name="vb"></a>VB

Cadena que representa el nombre de la entidad de certificación.

## <a name="remarks"></a>Observaciones

El nombre predeterminado de la entidad de certificación es el nombre de la lista de entidades de certificación disponibles.

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

[**ISCrdEnr::enumCAName**](iscrdenr-enumcaname.md)
</dt> <dt>

[**ISCrdEnr::getCACount**](iscrdenr-getcacount.md)
</dt> <dt>

[**ISCrdEnr::setCAName**](iscrdenr-setcaname.md)
</dt> </dl>

 

 
