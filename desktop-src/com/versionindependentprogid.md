---
title: VersionIndependentProgID
description: Asocia un ProgID a un CLSID. Este valor se usa para determinar la versión más reciente de una aplicación de objeto.
ms.assetid: 5d188db9-ea4f-47fe-882f-a6caa7e86a25
keywords:
- VersionIndependentProgID, clave del Registro COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fe1defaa52df5251d6c021655d6e84c90677e2a2d57f0bfb67f925e0ffa5bc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118549725"
---
# <a name="versionindependentprogid"></a>VersionIndependentProgID

Asocia un ProgID a un CLSID. Este valor se usa para determinar la versión más reciente de una aplicación de objeto.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      VersionIndependentProgID = Program.Component
```

## <a name="remarks"></a>Observaciones

Se trata de **un valor \_ SZ reg** que especifica la versión más reciente de la aplicación de objeto.

El ProgID independiente de la versión se almacena y mantiene únicamente mediante código de aplicación. Cuando se le da el ProgID independiente de la versión, la función [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) devuelve el CLSID de la versión actual.

Puede usar [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) y [**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) para convertir entre estas dos representaciones.

 

 




