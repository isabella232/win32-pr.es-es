---
description: Recupera un valor booleano que indica si la extensión de restricción básica está marcada como crítica.
ms.assetid: 4e84ea58-397b-491c-bdab-b5b4d46e070e
title: BasicConstraints.IsCritical, propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints.IsCritical
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3918a89719195e6c8672a0dab13c62af3e866f8fd5695df20f0126f7831f369c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773037"
---
# <a name="basicconstraintsiscritical-property"></a>BasicConstraints.IsCritical, propiedad

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista, Windows XP. En su lugar, use la clase [**X509BasicConstraintsExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/previous-versions/windows/)\]

La **propiedad IsCritical** recupera un valor booleano que indica si la extensión de restricción básica está marcada como crítica.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
BasicConstraints.IsCritical As Boolean
```



## <a name="property-value"></a>Valor de propiedad

Si **es true,** la extensión de restricción básica se marca como crítica.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
