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
ms.openlocfilehash: 6de5d1108ab09c9658af307d6a67c5a94a5dc35514720a221540de263f516c9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119960294"
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

Valor que determina si el nombre hace referencia al nombre de la entidad de certificación o al nombre del equipo de la entidad de certificación. Si este valor es SCARD ENROLL CA MACHINE NAME (definido como 0x01), el nombre hace referencia al nombre del equipo de la entidad de certificación; de lo contrario, el nombre hace referencia al nombre de \_ \_ la entidad de \_ \_ certificación.

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

Si se produce un error en el método , devuelve un **valor HRESULT** que indica el error. Para obtener una lista de códigos de error comunes, vea [Common HRESULT Values](common-hresult-values.md).

### <a name="vb"></a>VB

Cadena que representa el nombre de la CA.

## <a name="remarks"></a>Comentarios

El nombre de ca predeterminado es el nombre de la lista disponible de CA.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Archivo DLL<br/>                      | <dl> <dt>Scrdenrl.dll</dt> </dl> |
| IID<br/>                      | IID ISCrdEnr se define como \_ 753988a1-1357-436d-9cf5-f089bdd67d64<br/>             |



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

 

 
