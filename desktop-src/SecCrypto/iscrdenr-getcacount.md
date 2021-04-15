---
description: Devuelve el número de entidades de certificación (CA) que están dispuestos a emitir un certificado basado en la plantilla de certificado especificada.
ms.assetid: 377121a8-3895-4308-a803-4a62580c6de0
title: 'ISCrdEnr:: getCACount (método)'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669659"
---
# <a name="iscrdenrgetcacount-method"></a>ISCrdEnr:: getCACount (método)

El método **getCACount** devuelve el número de [*entidades de certificación*](../secgloss/c-gly.md) (CA) que están dispuestos a emitir un certificado basado en la plantilla de certificado especificada.

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

*bstrCertTemplateName* \[ de\]
</dt> <dd>

Cadena que representa el nombre de la plantilla de certificado.

</dd> <dt>

*pdwCACount* \[ enuncia\]
</dt> <dd>

Un puntero a un **valor Long** que devuelve el número de entidades de certificación disponibles que emitirá un certificado para la plantilla de certificado especificada en *bstrCertTemplateName*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="c"></a>C++

Si el método se ejecuta correctamente, el método devuelve S \_ correcto.

Si se produce un error en el método, devuelve un valor **HRESULT** que indica el error. Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).

### <a name="vb"></a>VB

Un valor **Long** que representa el número de entidades de certificación disponibles que emitirá un certificado para la plantilla de certificado especificada en *bstrCertTemplateName*.

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

[**ISCrdEnr::getCAName**](iscrdenr-getcaname.md)
</dt> </dl>

 

 
