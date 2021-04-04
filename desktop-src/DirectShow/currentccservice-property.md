---
description: La propiedad CurrentCCService establece o recupera el servicio de subtítulos (CC) actual.
ms.assetid: 094cf812-3122-4d5f-af8a-afd1c2264a2b
title: Propiedad CurrentCCService
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb5c1ddf243b0ec943be1f22930a8802d28d1bda
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906696"
---
# <a name="currentccservice-property"></a>Propiedad CurrentCCService

> [!Note]  
> Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003. En versiones posteriores podría modificarse o no estar disponible.

 

La `CurrentCCService` propiedad establece o recupera el servicio de subtítulos (CC) actual.

``` syntax
[ iService = ] MSWebDVD.CurrentCCService
```

## <a name="return-value"></a>Valor devuelto

Devuelve un valor entero que indica el tipo de servicio de subtítulos (CC) habilitado.

## <a name="remarks"></a>Observaciones

Los valores posibles de esta propiedad son:



| Value | Descripción                                                          |
|-------|----------------------------------------------------------------------|
| 0x0   | No hay ningún servicio actual. Este es el valor predeterminado.                       |
| 0x1   | Título real, primer campo. Servicio predeterminado.                       |
| 0x2   | Subtítulos para el segundo campo del idioma secundario. Por lo general, no se usa. |



 

Esta propiedad es de lectura y escritura.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**CCActive**](ccactive-property.md)
</dt> </dl>

 

 



