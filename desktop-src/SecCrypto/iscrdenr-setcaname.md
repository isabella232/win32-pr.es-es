---
description: Especifica el nombre de la entidad de certificación (CA).
ms.assetid: 224c2a51-8a25-4b66-b86b-c87531475145
title: 'ISCrdEnr:: setCAName (método)'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668330"
---
# <a name="iscrdenrsetcaname-method"></a>ISCrdEnr:: setCAName (método)

El método **setCAName** especifica el nombre de la [*entidad de certificación*](../secgloss/c-gly.md) (CA).

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

*dwFlags* \[ de\]
</dt> <dd>

Valor que especifica si el nombre hace referencia al nombre de la entidad de certificación o al nombre del equipo de la CA. Si este valor es PPAC \_ ENROLL \_ CA nombre del \_ equipo \_ (definido como 0x01), el nombre hace referencia al nombre del equipo de la entidad de certificación. De lo contrario, el nombre hace referencia al nombre de la entidad de certificación.

</dd> <dt>

*bstrCertTemplateName* \[ de\]
</dt> <dd>

Nombre de la plantilla de certificado.

</dd> <dt>

*bstrCAName* \[ de\]
</dt> <dd>

Nombre de la entidad de certificación que se usará con la plantilla de certificado especificada por *bstrCertTemplateName*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="vb"></a>VB

El valor devuelto es **HRESULT**. Un valor de S \_ OK indica que la llamada se realizó correctamente.

## <a name="remarks"></a>Observaciones

Utilice este método para especificar una CA para una plantilla de certificado.

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

 

 
