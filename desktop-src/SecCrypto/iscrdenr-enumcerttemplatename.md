---
description: Enumera los nombres de las plantillas de certificado.
ms.assetid: 4741eb0d-b8e0-468c-8a00-9ccacb52a9a7
title: 'ISCrdEnr:: enumCertTemplateName (método)'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669660"
---
# <a name="iscrdenrenumcerttemplatename-method"></a>ISCrdEnr:: enumCertTemplateName (método)

El método **enumCertTemplateName** enumera los nombres de las plantillas de certificado.

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

*dwIndex* \[ de\]
</dt> <dd>

Índice de base cero de la secuencia de enumeración.

</dd> <dt>

*dwFlags* \[ de\]
</dt> <dd>

Un valor que determina si la plantilla de certificado enumerada se aplica a los certificados de usuario o de equipo. Si este valor es una plantilla de certificado de \_ usuario de inscripción PPAC \_ \_ \_ (definida como 1), la enumeración se aplica a las plantillas de certificado de usuario. Si este valor es PPAC inscribir la plantilla de certificado de la \_ \_ máquina \_ \_ (definida como 2), la enumeración se aplica a las plantillas de certificado de equipo.

</dd> <dt>

*pbstrCertTemplateName* \[ enuncia\]
</dt> <dd>

Puntero a una cadena que devuelve el nombre de la plantilla de certificado enumerada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="c"></a>C++

Si el método se ejecuta correctamente, el método devuelve S \_ correcto.

Si se produce un error en el método, devuelve un valor **HRESULT** que indica el error. Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).

### <a name="vb"></a>VB

Cadena que contiene el nombre de la plantilla de certificado enumerada.

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

[**ISCrdEnr::getCertTemplateCount**](iscrdenr-getcerttemplatecount.md)
</dt> <dt>

[**ISCrdEnr::getCertTemplateName**](iscrdenr-getcerttemplatename.md)
</dt> <dt>

[**ISCrdEnr::setCertTemplateName**](iscrdenr-setcerttemplatename.md)
</dt> </dl>

 

 




