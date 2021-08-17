---
description: Devuelve el objeto EKU usado para compilar el objeto Chain.
ms.assetid: d02f1614-6a4f-4c60-b406-ce174a99e9a5
title: Método CertificateStatus.EKU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertificateStatus.EKU
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 63ddc2cd793c786cff1f7c5bb983cdba525fb52f940723f826ab4b44b89bf1ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770310"
---
# <a name="certificatestatuseku-method"></a>Método CertificateStatus.EKU

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use [**la estructura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

El **método EKU** devuelve el [**objeto EKU**](eku.md) usado para compilar el [**objeto Chain.**](chain.md)

## <a name="syntax"></a>Sintaxis


```VB
CertificateStatus.EKU()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método devuelve un [**objeto EKU**](eku.md) que indica la configuración de uso de clave extendida del [*certificado*](../secgloss/c-gly.md). La configuración de EKU establece el uso válido de un certificado. Solo se puede establecer un único objeto **EKU** para cada certificado.

## <a name="remarks"></a>Comentarios

El [**método CertificateStatus.ApplicationPolicies**](certificatestatus-applicationpolicies.md) proporciona la misma funcionalidad que este método, pero permite especificar muchos valores en lugar de solo uno. Si la [**colección de OID**](oids.md) devuelta por el método **ApplicationPolicies** contiene uno o varios objetos [**OID,**](oid.md) se omite el objeto [**EKU**](eku.md) devuelto por este método. Use el **método ApplicationPolicies** en lugar de este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CertificateStatus**](certificatestatus.md)
</dt> <dt>

[**Objetos de criptografía**](cryptography-objects.md)
</dt> <dt>

[**EKU**](eku.md)
</dt> </dl>

 

 
