---
description: Recupera el número de plantillas de certificado.
ms.assetid: f56e6e72-1562-4c53-b0da-b4bc69511559
title: Método ISCrdEnr::getCertTemplateCount
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCertTemplateCount
- SCrdEnr.getCertTemplateCount
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 86a78f03929bc6cdcfc7b611944b81c59a1c9fc9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127270964"
---
# <a name="iscrdenrgetcerttemplatecount-method"></a>Método ISCrdEnr::getCertTemplateCount

El **método getCertTemplateCount** recupera el número de plantillas de certificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT getCertTemplateCount(
  [in]  DWORD     dwFlags,
  [out] LONG *pdwCertTemplateCount
);
```


```VB

SCrdEnr.getCertTemplateCount( _
  ByVal dwFlags, _
  ByRef pdwCertTemplateCount _
)
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Valor que determina si la plantilla es para certificados de usuario o equipo. Si este valor es SCARD ENROLL USER CERT TEMPLATE (definido como \_ \_ 1), el recuento devuelto será para \_ las plantillas de certificado de \_ usuario. Si este valor es SCARD ENROLL MACHINE CERT TEMPLATE (definido como \_ \_ 2), el recuento devuelto será para \_ las plantillas de certificado de \_ equipo.

</dd> <dt>

*pdwCertTemplateCount* \[ out\]
</dt> <dd>

Puntero a **long** que devuelve el número de plantillas de certificado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="c"></a>C++

Si el método se realiza correctamente, el método devuelve S \_ OK.

Si se produce un error en el método, devuelve un **valor HRESULT** que indica el error. Para obtener una lista de códigos de error comunes, vea [Common HRESULT Values](common-hresult-values.md).

### <a name="vb"></a>VB

Valor **Long** que representa el número de plantillas de certificado.

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

[**ISCrdEnr::enumCertTemplateName**](iscrdenr-enumcerttemplatename.md)
</dt> </dl>

 

 




