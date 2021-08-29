---
description: El instalador establece las propiedades con el orden de precedencia siguiente. Un valor de propiedad de esta lista puede invalidar un valor que viene después de él y se reemplaza por un valor que aparece delante de él en la lista.
ms.assetid: ba9240fe-2e5a-43f5-8cdf-59dd6348092b
title: Orden de prioridad de propiedad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b243180b356b081e3d14515d72c2ed1313ba6fa1f2fd81356b329c2edcd83598
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942822"
---
# <a name="order-of-property-precedence"></a>Orden de prioridad de propiedad

El instalador establece las propiedades con el orden de precedencia siguiente. Un valor de propiedad de esta lista puede invalidar un valor que viene después de él y se reemplaza por un valor que aparece delante de él en la lista.

1.  Propiedades especificadas por el entorno operativo.
2.  [Propiedades públicas establecidas](public-properties.md) en la línea de comandos.
3.  Propiedades públicas enumeradas por el [**conjunto de propiedades AdminProperties**](adminproperties.md) durante [una instalación administrativa.](administrative-installation.md)
4.  Propiedades públicas o privadas establecidas durante la aplicación de una [*transformación*](t-gly.md).
5.  Propiedad pública o privada que se establece mediante la creación de la [tabla Property](property-table.md) del .msi archivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de las propiedades](about-properties.md)
</dt> </dl>

 

 



