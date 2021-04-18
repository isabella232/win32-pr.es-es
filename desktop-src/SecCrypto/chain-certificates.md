---
description: La propiedad Certificates recupera una colección de certificados que representa los certificados de la cadena. Esta es la propiedad predeterminada.
ms.assetid: c3e6953f-35e5-469a-a1aa-e3a4ebe21ac3
title: 'IChain2:: Certificates (propiedad)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IChain2.Certificates
- IChain2.get_Certificates
- IChain.Certificates
- IChain.get_Certificates
- Chain.Certificates
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a166f1d0dfa7f027058be65c3371d5c055cdb7bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670714"
---
# <a name="ichain2certificates-property"></a>IChain2:: Certificates (propiedad)

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**clase X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La propiedad **Certificates** recupera una colección de [**certificados**](certificates.md) que representa los certificados de la cadena. Esta es la propiedad predeterminada.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
Chain.Certificates As Certificates
```



## <a name="property-value"></a>Valor de propiedad

Colección de [**certificados**](certificates.md) que se usa para recuperar información sobre cada certificado de la cadena. El primer certificado de la colección devuelta, **Certificates. Item**(1), es el certificado final de la cadena. El último certificado de la colección, Certificates **. Item**(**Certificates. Count**), es el [*certificado raíz*](../secgloss/r-gly.md) de la cadena.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
