---
description: Devuelve el número de entidades de certificación (CA) que están dispuestos a emitir un certificado en función de la plantilla de certificado especificada.
ms.assetid: 377121a8-3895-4308-a803-4a62580c6de0
title: Método ISCrdEnr::getCACount
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCACount
- SCrdEnr.getCACount
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: eb33f6c7345862dedf6c909054d811ff4da470ee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127270975"
---
# <a name="iscrdenrgetcacount-method"></a>Método ISCrdEnr::getCACount

El **método getCACount** devuelve el número de entidades de certificación [*(CA)*](../secgloss/c-gly.md) que están dispuestos a emitir un certificado en función de la plantilla de certificado especificada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT getCACount(
  [in]  BSTR     bstrCertTemplateName,
  [out] LONG *pdwCACount
);
```


```VB

SCrdEnr.getCACount( _
  ByVal bstrCertTemplateName, _
  ByRef pdwCACount _
)
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrCertTemplateName* \[ En\]
</dt> <dd>

Cadena que representa el nombre de la plantilla de certificado.

</dd> <dt>

*pdwCACount* \[ out\]
</dt> <dd>

Puntero a un **valor LONG** que devuelve el número de CA disponibles que emitirán un certificado para la plantilla de certificado especificada en *bstrCertTemplateName*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="c"></a>C++

Si el método se realiza correctamente, el método devuelve S \_ OK.

Si se produce un error en el método , devuelve un **valor HRESULT** que indica el error. Para obtener una lista de códigos de error comunes, vea [Common HRESULT Values](common-hresult-values.md).

### <a name="vb"></a>VB

Valor **Long** que representa el número de CA disponibles que emitirán un certificado para la plantilla de certificado especificada en *bstrCertTemplateName*.

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

[**ISCrdEnr::getCAName**](iscrdenr-getcaname.md)
</dt> </dl>

 

 
