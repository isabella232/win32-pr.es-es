---
title: Autotreatas
description: Establece automáticamente el CLSID para la clave treatAs en el valor especificado.
ms.assetid: 5adf7bc5-a4d6-444d-bd56-0c4e6eee5111
keywords:
- COM de clave del registro autotreatl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa9ff717e17f08e5d37885f3994d03671bddaa9c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418329"
---
# <a name="autotreatas"></a>Autotreatas

Establece automáticamente el CLSID para la clave [**treatAs**](treatas.md) en el valor especificado.

## <a name="registry-entry"></a>Entrada del Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      AutoTreatAs = value
```

## <a name="remarks"></a>Observaciones

Se trata de un valor de **reg \_ SZ** que especifica el identificador de clase.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**CoTreatAsClass**](/windows/desktop/api/Objbase/nf-objbase-cotreatasclass)
</dt> </dl>

 

 




