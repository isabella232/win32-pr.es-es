---
description: ICE52 comprueba si hay propiedades privadas en la tabla AppSearch. Consulte Acerca de las propiedades.
ms.assetid: 18d1489e-666a-488d-ae12-5dbe60885a2e
title: ICE52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b96f514f38e44a802b092acff53ac14f10c5e5d32c03888b7d45540443d34be3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044045"
---
# <a name="ice52"></a>ICE52

ICE52 comprueba si hay propiedades privadas en la [tabla AppSearch](appsearch-table.md). Vea [Acerca de las propiedades](about-properties.md).

Al usar Windows 2000, todas las propiedades establecidas en la columna Propiedad de la tabla AppSearch deben ser propiedades públicas.

## <a name="result"></a>Resultado

ICE52 envía una advertencia si hay una propiedad privada en la tabla AppSearch.

## <a name="example"></a>Ejemplo

ICE52 publica la siguiente advertencia para el ejemplo mostrado.

``` syntax
Property 'Property2' in AppSearch row 'Property2'.'Signature2' 
    is not public. It should be all uppercase.
```

[Tabla de AppSearch](appsearch-table.md)



| Propiedad  | Firma  |
|-----------|------------|
| PROPERTY1 | Signature1 |
| Property2 | Signature2 |



 

Para corregir este cambio de advertencia en la propiedad pública personalizada: PROPERTY2.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



