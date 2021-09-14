---
description: Muestra un cuadro de diálogo Seleccionar certificado, que permite seleccionar un certificado de firma (también conocido como certificado del agente de inscripción).
ms.assetid: b8198f65-4ffb-4dfa-8286-e62ef483ab16
title: Método ISCrdEnr::selectSigningCertificate
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.selectSigningCertificate
- SCrdEnr.selectSigningCertificate
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: a4ef3be0ef16797597f57c12e90736ba50109601
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170973"
---
# <a name="iscrdenrselectsigningcertificate-method"></a>Método ISCrdEnr::selectSigningCertificate

El **método selectSigningCertificate** muestra un cuadro de diálogo Seleccionar certificado, lo que permite seleccionar un certificado de firma (también conocido como certificado del agente de inscripción). 

Antes de inscribirse en nombre de los usuarios, debe seleccionar un certificado de firma. La [*clave privada*](../secgloss/p-gly.md) asociada a este certificado de firma se usa para firmar una solicitud PKCS \# 7. PkCS 7, a su vez, contiene la solicitud \# PKCS 10 del usuario (que está firmada con la clave \# privada del usuario).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT selectSigningCertificate(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName
);
```


```VB

SCrdEnr.selectSigningCertificate( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName _
)
```





## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwFlags* \[ En\]
</dt> <dd>

Reservado para uso futuro. Establezca este valor en cero.

</dd> <dt>

*bstrCertTemplateName* \[ En\]
</dt> <dd>

Cadena que representa el nombre de la plantilla de certificado para el certificado de firma. Puede usar el valor "EnrollmentAgent" si ha obtenido un certificado EnrollmentAgent.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="vb"></a>VB

Si el método se realiza correctamente, el método devuelve **S \_ OK**.

Si se produce un error en el método , devuelve un **valor HRESULT** que indica el error. Para obtener una lista de códigos de error comunes, vea [Common HRESULT Values](common-hresult-values.md).

## <a name="remarks"></a>Observaciones

Antes de inscribirse en nombre de un usuario, primero debe obtener un certificado de firma. Puede obtener un certificado de firma mediante el complemento MMC del Administrador de certificados. El **método selectSigningCertificate** no obtiene el certificado de firma, pero muestra un cuadro de diálogo de certificados de firma obtenidos previamente, lo que le permite elegir qué certificado se usará para firmar las solicitudes de inscripción en nombre.

Una alternativa a **selectSigningCertificate** [**es ISCrdEnr::setSigningCertificate.**](iscrdenr-setsigningcertificate.md)

Una vez seleccionado un certificado de firma, su nombre se puede recuperar llamando a [**ISCrdEnr::getSigningCertificateName**](iscrdenr-getsigningcertificatename.md).

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

[**ISCrdEnr::getSigningCertificateName**](iscrdenr-getsigningcertificatename.md)
</dt> </dl>

 

 
