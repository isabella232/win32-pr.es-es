---
description: Enumera los nombres de las plantillas de certificado.
ms.assetid: 4741eb0d-b8e0-468c-8a00-9ccacb52a9a7
title: Método ISCrdEnr::enumCertTemplateName
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.enumCertTemplateName
- SCrdEnr.enumCertTemplateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: a0a4850143cac48ef9b9b853f99153d4daeb4366
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170981"
---
# <a name="iscrdenrenumcerttemplatename-method"></a>Método ISCrdEnr::enumCertTemplateName

El **método enumCertTemplateName** enumera los nombres de las plantillas de certificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT enumCertTemplateName(
  [in]  DWORD     dwIndex,
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrCertTemplateName
);
```


```VB

SCrdEnr.enumCertTemplateName( _
  ByVal dwIndex, _
  ByVal dwFlags, _
  ByRef pbstrCertTemplateName _
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

Valor que determina si la plantilla de certificado enumerada se aplica a los certificados de usuario o equipo. Si este valor es SCARD \_ ENROLL USER CERT TEMPLATE \_ \_ (definido como 1), la enumeración se aplica a \_ las plantillas de certificado de usuario. Si este valor es SCARD \_ ENROLL MACHINE CERT TEMPLATE \_ \_ (definido como 2), la enumeración se aplica a \_ las plantillas de certificado de equipo.

</dd> <dt>

*pbstrCertTemplateName* \[ out\]
</dt> <dd>

Puntero a una cadena que devuelve el nombre de la plantilla de certificado enumerada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="c"></a>C++

Si el método se realiza correctamente, el método devuelve S \_ OK.

Si se produce un error en el método, devuelve un **valor HRESULT** que indica el error. Para obtener una lista de códigos de error comunes, vea [Common HRESULT Values](common-hresult-values.md).

### <a name="vb"></a>VB

Cadena que contiene el nombre de la plantilla de certificado enumerada.

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

[**ISCrdEnr::getCertTemplateCount**](iscrdenr-getcerttemplatecount.md)
</dt> <dt>

[**ISCrdEnr::getCertTemplateName**](iscrdenr-getcerttemplatename.md)
</dt> <dt>

[**ISCrdEnr::setCertTemplateName**](iscrdenr-setcerttemplatename.md)
</dt> </dl>

 

 




