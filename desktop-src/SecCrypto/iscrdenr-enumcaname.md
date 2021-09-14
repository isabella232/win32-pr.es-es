---
description: Enumera el nombre de las entidades de certificación (CA) para un nombre de plantilla de certificado determinado.
ms.assetid: 82cc3346-a8b9-4abd-933a-c212a37a373e
title: Método ISCrdEnr::enumCAName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.enumCAName
- SCrdEnr.enumCAName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: c23df2f74cdf3791f1280e38cbff8ddd48f924b8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170982"
---
# <a name="iscrdenrenumcaname-method"></a>Método ISCrdEnr::enumCAName

El **método enumCAName** enumera el nombre de las entidades de certificación [*(CA)*](../secgloss/c-gly.md) para un nombre de plantilla de certificado determinado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT enumCAName(
  [in]  DWORD     dwIndex,
  [in]  DWORD     dwFlags,
  [in]  BSTR     bstrCertTemplateName,
  [out] BSTR *pbstrCAName
);
```


```VB

SCrdEnr.enumCAName( _
  ByVal dwIndex, _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName, _
  ByRef pbstrCAName _
)
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwIndex* \[ En\]
</dt> <dd>

Índice de base cero para la secuencia de enumeración.

</dd> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Valor que determina si el nombre hace referencia al nombre de la entidad de certificación o al nombre del equipo de la entidad de certificación. Si este valor es SCARD ENROLL CA MACHINE NAME (definido como 0x01), el nombre hace referencia al nombre \_ del equipo de la entidad de \_ \_ \_ certificación. De lo contrario, el nombre hace referencia al nombre de la entidad de certificación.

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

[**ISCrdEnr::getCACount**](iscrdenr-getcacount.md)
</dt> <dt>

[**ISCrdEnr::getCAName**](iscrdenr-getcaname.md)
</dt> <dt>

[**ISCrdEnr::setCAName**](iscrdenr-setcaname.md)
</dt> </dl>

 

 
