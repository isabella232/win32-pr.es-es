---
description: Recupera el nombre de la entidad de certificación (CA) especificada para una plantilla de certificado determinada.
ms.assetid: e921710a-7c74-4fda-91e1-fbad45889984
title: Método ISCrdEnr::getCAName
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127270967"
---
# <a name="iscrdenrgetcaname-method"></a>Método ISCrdEnr::getCAName

El **método getCAName** recupera el nombre de la entidad de certificación [*(CA)*](../secgloss/c-gly.md) especificada para una plantilla de certificado determinada.

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

*dwFlags* \[ En\]
</dt> <dd>

Valor que determina si el nombre hace referencia al nombre de la entidad de certificación o al nombre del equipo de la entidad de certificación. Si este valor es SCARD ENROLL CA MACHINE NAME (definido como 0x01), el nombre hace referencia al nombre del equipo de la entidad de certificación; de lo contrario, el nombre hace referencia al nombre \_ \_ de la \_ \_ ca.

</dd> <dt>

*bstrCertTemplateName* \[ En\]
</dt> <dd>

Nombre de la plantilla de certificado.

</dd> <dt>

*pbstrCAName* \[ out\]
</dt> <dd>

Puntero a una cadena que devuelve el nombre de la entidad de certificación.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="c"></a>C++

Si el método se realiza correctamente, el método devuelve S \_ OK.

Si se produce un error en el método, devuelve un **valor HRESULT** que indica el error. Para obtener una lista de códigos de error comunes, vea [Common HRESULT Values](common-hresult-values.md).

### <a name="vb"></a>VB

Cadena que representa el nombre de la entidad de certificación.

## <a name="remarks"></a>Observaciones

El nombre de entidad de certificación predeterminado es el nombre de la lista de CA disponibles.

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

[**ISCrdEnr::enumCAName**](iscrdenr-enumcaname.md)
</dt> <dt>

[**ISCrdEnr::getCACount**](iscrdenr-getcacount.md)
</dt> <dt>

[**ISCrdEnr::setCAName**](iscrdenr-setcaname.md)
</dt> </dl>

 

 
