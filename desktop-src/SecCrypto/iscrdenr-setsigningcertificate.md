---
description: Especifica un certificado de firma (también conocido como certificado de agente de inscripción).
ms.assetid: db2437a9-46f6-48c3-9630-82ec556df645
title: 'ISCrdEnr:: setSigningCertificate (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setSigningCertificate
- SCrdEnr.setSigningCertificate
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: dd00ba19872cb0ba2b21981c79e8f7be03aa4937
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669890"
---
# <a name="iscrdenrsetsigningcertificate-method"></a>ISCrdEnr:: setSigningCertificate (método)

El método **setSigningCertificate** especifica un certificado de firma (también conocido como *certificado de agente de inscripción*).

Antes de inscribirse en nombre de los usuarios, debe seleccionar o establecer un certificado de firma. La [*clave privada*](../secgloss/p-gly.md) asociada a este certificado de firma se usa para firmar una \# solicitud PKCS 7. El archivo PKCS \# 7, a su vez, contiene la solicitud PKCS 10 del usuario \# (que está firmada con la clave privada del usuario).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT setSigningCertificate(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName
);
```


```VB

SCrdEnr.setSigningCertificate( _
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

Nombre de la plantilla de certificado para el certificado de firma. Puede usar el valor "EnrollmentAgent" Si ha obtenido un certificado EnrollmentAgent.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

### <a name="vb"></a>VB

Si el método se ejecuta correctamente, el método devuelve S \_ correcto.

Si se produce un error en el método, devuelve un valor **HRESULT** que indica el error. Para obtener una lista de los códigos de error comunes, vea [Valores HRESULT comunes](common-hresult-values.md).

## <a name="remarks"></a>Observaciones

Antes de inscribirse en nombre de un usuario, primero debe obtener un certificado de firma. Puede obtener un certificado de firma mediante el complemento MMC del administrador de certificados. El método **setSigningCertificate** no obtiene el certificado de firma, pero informa al control de inscripción de tarjetas inteligentes que ha obtenido previamente el certificado de firma que se va a usar. El método **setSigningCertificate** busca el certificado de firma más reciente correspondiente a la plantilla de certificado especificada por *bstrCertTemplateName* en el almacén "My" del llamador.

Una alternativa a **setSigningCertificate** es **ISCrdEnr:: setSigningCertificate**.

Después de establecer un certificado de firma, su nombre se puede recuperar llamando a [**ISCrdEnr:: getSigningCertificateName**](iscrdenr-getsigningcertificatename.md).

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

 

 
