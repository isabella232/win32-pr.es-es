---
description: Devuelve el objeto EKU utilizado para generar el objeto de cadena.
ms.assetid: d02f1614-6a4f-4c60-b406-ce174a99e9a5
title: CertificateStatus. EKU, método
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
ms.openlocfilehash: d386251c6d7f674d3850de275559bcb87ea6d61e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670432"
---
# <a name="certificatestatuseku-method"></a>CertificateStatus. EKU, método

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**estructura X509ChainStatus**](/dotnet/api/system.security.cryptography.x509certificates.x509chainstatus?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

El método **EKU** devuelve el objeto [**EKU**](eku.md) usado para generar el objeto de [**cadena**](chain.md) .

## <a name="syntax"></a>Sintaxis


```VB
CertificateStatus.EKU()
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método devuelve un objeto [**EKU**](eku.md) que indica la configuración de uso mejorado de clave del [*certificado*](../secgloss/c-gly.md). La configuración de EKU establece el uso válido de un certificado. Solo se puede establecer un objeto **EKU** para cada certificado.

## <a name="remarks"></a>Observaciones

El método [**CertificateStatus. ApplicationPolicies**](certificatestatus-applicationpolicies.md) proporciona la misma funcionalidad que este método, pero permite especificar muchas configuraciones en lugar de solo una. Si la colección [**OID**](oids.md) devuelta por el método **ApplicationPolicies** contiene uno o más objetos [**OID**](oid.md) , se omite el objeto [**EKU**](eku.md) devuelto por este método. Use el método **ApplicationPolicies** en lugar de este método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CertificateStatus**](certificatestatus.md)
</dt> <dt>

[**Objetos de criptografía**](cryptography-objects.md)
</dt> <dt>

[**EKU**](eku.md)
</dt> </dl>

 

 
