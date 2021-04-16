---
description: Una directiva de autorización central (CAP) recopila las reglas de autorización específicas (CAPRs) en una única directiva.
ms.assetid: E3E43D9F-6826-468A-86E9-AC8F9A381FD4
title: Directivas de autorización central
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b890236b0dae0f8f8d51254def4e1607cc35894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648243"
---
# <a name="central-authorization-policies"></a>Directivas de autorización central

Una directiva de autorización central (CAP) recopila las reglas de autorización específicas (CAPRs) en una única directiva. Para permitir la combinación de las reglas de autorización específicas (CAPRs) en la Directiva de autorización holística de la organización, se puede hacer referencia a CAPRs y aplicarla a un conjunto de recursos. Para ello, se recopilan varios (por referencia) en un extremo. Una vez definido un extremo, los administradores de recursos pueden distribuirlo para aplicar la Directiva de autorización de la organización a los recursos.

Un extremo tiene los siguientes atributos:

-   Colección de CAPRs: una lista de referencias a objetos CAPR existentes
-   Un identificador (SID)
-   Descripción
-   Nombre

Un extremo se evalúa durante la evaluación del acceso para los archivos y carpetas en los que un administrador lo habilita. Durante una llamada a [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) , la comprobación de Cap se combina lógicamente con la comprobación de la ACL discrecional; Esto significa que, para obtener acceso a un archivo al que se aplica el límite, un usuario debe tener acceso ambos según el CAP (su CAPRs asociado) y la ACL discrecional del archivo.

CAP de ejemplo:

``` syntax
CORPORATE-FINANCE-CAP]
CAPID=S-1-5-3-4-56-45-67-123
Policies=HBI-CAPE;RETENTION-CAPR
```

## <a name="cap-definition"></a>Definición de CAP

Se crea un extremo y se edita en Active Directory mediante una nueva experiencia de usuario en ADAC (o PowerShell) que permite al administrador crear un CAP y especificar un conjunto de CAPRs que componen el límite.

 

 
