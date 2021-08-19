---
description: Recupera un valor booleano que indica si la extensión de restricciones básicas está presente. Esta es la propiedad predeterminada.
ms.assetid: 775b37fc-5015-4096-9e94-608f13a5ed14
title: BasicConstraints.IsPresent, propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints.IsPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 646d7988b24d9ad03e55bb7ee4401875c42f7b779a81e1b80a611aaae18a93a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773027"
---
# <a name="basicconstraintsispresent-property"></a>BasicConstraints.IsPresent, propiedad

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista, Windows XP. En su lugar, use la clase [**X509BasicConstraintsExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/previous-versions/windows/)\]

La **propiedad IsPresent** recupera un valor booleano que indica si la extensión de restricciones básicas está presente. Esta es la propiedad predeterminada.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
BasicConstraints.IsPresent As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si **es true**, la extensión de restricciones básicas está presente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**BasicConstraints**](basicconstraints.md)
</dt> </dl>

 

 
