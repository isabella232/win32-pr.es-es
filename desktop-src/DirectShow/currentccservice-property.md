---
description: La propiedad CurrentCCService establece o recupera el servicio de subtítulos actual.
ms.assetid: 094cf812-3122-4d5f-af8a-afd1c2264a2b
title: Propiedad CurrentCCService
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d836e852d1a144abb5422f71d0127eb9c37b8f333dce0723db2c2b3b1889ec50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075965"
---
# <a name="currentccservice-property"></a>Propiedad CurrentCCService

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `CurrentCCService` propiedad establece o recupera el servicio de subtítulos actual.

``` syntax
[ iService = ] MSWebDVD.CurrentCCService
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero que indica el tipo de servicio de subtítulos habilitado.

## <a name="remarks"></a>Comentarios

Los valores posibles de esta propiedad son:



| Valor | Descripción                                                          |
|-------|----------------------------------------------------------------------|
| 0x0   | No hay ningún servicio actual. Este es el valor predeterminado.                       |
| 0x1   | Subtítulos verdaderos, primer campo. Servicio predeterminado.                       |
| 0x2   | Subtítulos para el idioma secundario, segundo campo. Por lo general, no se usa. |



 

Esta propiedad es de lectura y escritura.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**CCActive**](ccactive-property.md)
</dt> </dl>

 

 



