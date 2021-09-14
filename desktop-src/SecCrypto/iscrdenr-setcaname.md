---
description: Especifica el nombre de la entidad de certificación (CA).
ms.assetid: 224c2a51-8a25-4b66-b86b-c87531475145
title: Método ISCrdEnr::setCAName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setCAName
- SCrdEnr.setCAName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 46dcd9294337c088b9e1b0ab68bddefe4308ed27
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170961"
---
# <a name="iscrdenrsetcaname-method"></a>Método ISCrdEnr::setCAName

El **método setCAName** especifica el nombre de la [*entidad de certificación*](../secgloss/c-gly.md) (CA).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT setCAName(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName,
  [in] BSTR bstrCAName
);
```


```VB

SCrdEnr.setCAName( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName, _
  ByVal bstrCAName _
)
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Valor que especifica si el nombre hace referencia al nombre de la entidad de certificación o al nombre del equipo de la entidad de certificación. Si este valor es SCARD ENROLL CA MACHINE NAME (definido como 0x01), el nombre hace referencia al nombre \_ del equipo de la entidad de \_ \_ \_ certificación. De lo contrario, el nombre hace referencia al nombre de la entidad de certificación.

</dd> <dt>

*bstrCertTemplateName* \[ En\]
</dt> <dd>

Nombre de la plantilla de certificado.

</dd> <dt>

*bstrCAName* \[ En\]
</dt> <dd>

Nombre de ca que se va a usar con la plantilla de certificado especificada *por bstrCertTemplateName*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="vb"></a>VB

El valor devuelto es **un HRESULT.** Un valor de S \_ OK indica que la llamada se ha realizado correctamente.

## <a name="remarks"></a>Observaciones

Use este método para especificar una entidad de certificación para una plantilla de certificado.

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

 

 
