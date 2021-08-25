---
description: Recupera un valor booleano que indica si la restricción de longitud de ruta de acceso está presente.
ms.assetid: 25840a62-13d1-4b54-9b09-64f77a465e06
title: BasicConstraints.IsPathLenConstraintPresent, propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints.IsPathLenConstraintPresent
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c6faf267508476f423efaff6b012a25114eca25e7bc21c51c51b9a3e66dde802
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879735"
---
# <a name="basicconstraintsispathlenconstraintpresent-property"></a>BasicConstraints.IsPathLenConstraintPresent, propiedad

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista, Windows XP. En su lugar, use la clase [**X509BasicConstraintsExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/previous-versions/windows/)\]

La **propiedad IsPathLenConstraintPresent** recupera un valor booleano que indica si la restricción de longitud de ruta de acceso está presente.

## <a name="syntax"></a>Syntax


```VB
BasicConstraints.IsPathLenConstraintPresent As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si **es True**, la restricción de longitud de ruta de acceso está presente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
