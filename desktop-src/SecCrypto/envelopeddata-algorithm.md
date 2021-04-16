---
description: Recupera el algoritmo de cifrado y la longitud de la clave.
ms.assetid: 13b2a3db-f04b-4436-b64f-f194fc9ddac2
title: EnvelopedData. algorithm (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9d6550be7ac32c08568baa8ef811478de50b27c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649803"
---
# <a name="envelopeddataalgorithm-property"></a>EnvelopedData. algorithm (propiedad)

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**clase EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

La propiedad **algorithm** recupera el algoritmo de cifrado y la longitud de la [*clave*](../secgloss/k-gly.md).

## <a name="syntax"></a>Sintaxis


```VB
EnvelopedData.Algorithm As Algorithm
```



## <a name="property-value"></a>Valor de propiedad

Objeto de [**algoritmo**](algorithm.md) que contiene el algoritmo de cifrado y la longitud de clave.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**EnvelopedData**](envelopeddata.md)
</dt> </dl>

 

 
