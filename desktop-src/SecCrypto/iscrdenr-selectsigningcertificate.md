---
description: Muestra un cuadro de diálogo Seleccionar certificado, que permite seleccionar un certificado de firma (también conocido como certificado de agente de inscripción).
ms.assetid: b8198f65-4ffb-4dfa-8286-e62ef483ab16
title: 'ISCrdEnr:: selectSigningCertificate (método)'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912825"
---
# <a name="iscrdenrselectsigningcertificate-method"></a>ISCrdEnr:: selectSigningCertificate (método)

El método **selectSigningCertificate** muestra el cuadro de diálogo **seleccionar certificado** , que permite seleccionar un certificado de firma (también conocido como *certificado de agente de inscripción*).

Antes de inscribirse en nombre de los usuarios, debe seleccionar un certificado de firma. La [*clave privada*](../secgloss/p-gly.md) asociada a este certificado de firma se usa para firmar una \# solicitud PKCS 7. El archivo PKCS \# 7, a su vez, contiene la solicitud PKCS 10 del usuario \# (que está firmada con la clave privada del usuario).

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

*dwFlags* \[ de\]
</dt> <dd>

Reservado para uso futuro. Establezca este valor en cero.

</dd> <dt>

*bstrCertTemplateName* \[ de\]
</dt> <dd>

Cadena que representa el nombre de la plantilla de certificado para el certificado de firma. Puede usar el valor "EnrollmentAgent" Si ha obtenido un certificado EnrollmentAgent.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="vb"></a>VB

Si el método se ejecuta correctamente, el método devuelve **S \_ correcto**.

Si se produce un error en el método, devuelve un valor **HRESULT** que indica el error. Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).

## <a name="remarks"></a>Observaciones

Antes de inscribirse en nombre de un usuario, primero debe obtener un certificado de firma. Puede obtener un certificado de firma mediante el complemento MMC del administrador de certificados. El método **selectSigningCertificate** no obtiene el certificado de firma, pero muestra un cuadro de diálogo de certificados de firma previamente obtenidos, lo que le permite elegir qué certificado se usará para firmar las solicitudes de inscripción en nombre.

Una alternativa a **selectSigningCertificate** es [**ISCrdEnr:: setSigningCertificate**](iscrdenr-setsigningcertificate.md).

Una vez que se selecciona un certificado de firma, su nombre se puede recuperar llamando a [**ISCrdEnr:: getSigningCertificateName**](iscrdenr-getsigningcertificatename.md).

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

[**ISCrdEnr::getSigningCertificateName**](iscrdenr-getsigningcertificatename.md)
</dt> </dl>

 

 
