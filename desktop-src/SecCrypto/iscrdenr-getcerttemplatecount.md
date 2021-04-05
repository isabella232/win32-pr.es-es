---
description: Recupera el número de plantillas de certificado.
ms.assetid: f56e6e72-1562-4c53-b0da-b4bc69511559
title: 'ISCrdEnr:: getCertTemplateCount (método)'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912826"
---
# <a name="iscrdenrgetcerttemplatecount-method"></a>ISCrdEnr:: getCertTemplateCount (método)

El método **getCertTemplateCount** recupera el número de plantillas de certificado.

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

*dwFlags* \[ de\]
</dt> <dd>

Un valor que determina si la plantilla es para certificados de usuario o de equipo. Si este valor es \_ \_ la plantilla de certificado de usuario SCard ENROLL \_ \_ (definida como 1), el recuento devuelto será para las plantillas de certificado de usuario. Si este valor es PPAC \_ inscribir \_ \_ la plantilla de certificado de la máquina \_ (definida como 2), el recuento devuelto será para las plantillas de certificado de equipo.

</dd> <dt>

*pdwCertTemplateCount* \[ enuncia\]
</dt> <dd>

Un puntero a un **Long** que devuelve el número de plantillas de certificado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="c"></a>C++

Si el método se ejecuta correctamente, el método devuelve S \_ correcto.

Si se produce un error en el método, devuelve un valor **HRESULT** que indica el error. Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).

### <a name="vb"></a>VB

Un valor de **tipo Long** que representa el número de plantillas de certificado.

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

[**ISCrdEnr::enumCertTemplateName**](iscrdenr-enumcerttemplatename.md)
</dt> </dl>

 

 




