---
description: Una directiva de autorización central (CAP) recopila las reglas de autorización específicas (CAPR) en una sola directiva.
ms.assetid: E3E43D9F-6826-468A-86E9-AC8F9A381FD4
title: Directivas de autorización central
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0617f6bddb606d3c3fb3e5ccb6692c79c62a60f90de591b6ec3e04988db46f63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117783229"
---
# <a name="central-authorization-policies"></a>Directivas de autorización central

Una directiva de autorización central (CAP) recopila las reglas de autorización específicas (CAPR) en una sola directiva. Para permitir que las reglas de autorización específicas (CAPR) se combinen en la directiva de autorización holística de la organización, se puede hacer referencia a las CAPR juntas y aplicarse a un conjunto de recursos. Para ello, se recopilan varios (por referencia) en un CAP. Una vez definido un CAP, los administradores de recursos pueden distribuirlo para aplicar la directiva de autorización de organizaciones a los recursos.

Un CAP tiene los siguientes atributos:

-   Colección de CAPR: una lista de referencias a objetos CAPR existentes
-   Un identificador (Sid)
-   Descripción
-   Nombre

Durante la evaluación de acceso, se evalúa un CAP para los archivos y carpetas en los que un administrador lo habilita. Durante una [**llamada a AccessCheck,**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) la comprobación cap se combina lógicamente con la comprobación de ACL discrecional. Esto significa que, para obtener acceso a un archivo al que se aplica el CAP, un usuario debe tener acceso tanto según el CAP (sus CAP Asociados) como la ACL discrecional en el archivo.

CAP de ejemplo:

``` syntax
CORPORATE-FINANCE-CAP]
CAPID=S-1-5-3-4-56-45-67-123
Policies=HBI-CAPE;RETENTION-CAPR
```

## <a name="cap-definition"></a>Definición de CAP

Se crea y edita un CAP en Active Directory mediante una nueva experiencia de usuario en ADAC (o PowerShell) que permite al administrador crear un CAP y especificar un conjunto de CAPR que lo conste.

 

 
