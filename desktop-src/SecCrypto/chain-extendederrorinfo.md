---
description: Devuelve una cadena que contiene información de error adicional sobre la entrada indizada.
ms.assetid: 4f0d5289-c414-4e2b-b612-be8ce1d98b12
title: IChain2::ExtendedErrorInfo (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Chain.ExtendedErrorInfo
- IChain2.ExtendedErrorInfo
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: f8a7840d0f54ea7e93ad9998d5e8772a2ae411f2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250328"
---
# <a name="ichain2extendederrorinfo-method"></a>IChain2::ExtendedErrorInfo (método)

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use [**la clase X509Chain**](/dotnet/api/system.security.cryptography.x509certificates.x509chain?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

El **método ExtendedErrorInfo** devuelve una cadena que contiene información de error adicional sobre la entrada indizada.

Este método se introdujo en CAPICOM 2.0.

## <a name="syntax"></a>Sintaxis


```VB
Chain.ExtendedErrorInfo( _
  [ ByVal Index ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Índice* \[ en, opcional\]
</dt> <dd>

Long **que** representa el índice de la entrada. El valor predeterminado es 1, que devuelve información de error para el certificado final de la cadena. **Certificates.Count** devuelve información sobre el certificado raíz de la cadena. 0 devuelve información de error extendida para toda la cadena.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Cadena que contiene la información de error extendida.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Cadena**](chain.md)
</dt> </dl>

 

 
