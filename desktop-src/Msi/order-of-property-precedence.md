---
description: El instalador establece las propiedades mediante el orden de prioridad siguiente. Un valor de propiedad de esta lista puede invalidar un valor que se encuentra después de él y que se ha reemplazado por un valor que está delante de él en la lista.
ms.assetid: ba9240fe-2e5a-43f5-8cdf-59dd6348092b
title: Orden de prioridad de propiedad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90c114594b9a825a3847db37f5b98dc990211d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678469"
---
# <a name="order-of-property-precedence"></a>Orden de prioridad de propiedad

El instalador establece las propiedades mediante el orden de prioridad siguiente. Un valor de propiedad de esta lista puede invalidar un valor que se encuentra después de él y que se ha reemplazado por un valor que está delante de él en la lista.

1.  Propiedades especificadas por el entorno operativo.
2.  [Propiedades públicas](public-properties.md) establecidas en la línea de comandos.
3.  Propiedades públicas enumeradas por [**AdminProperties**](adminproperties.md) propertyset durante una [instalación administrativa](administrative-installation.md) .
4.  Propiedades públicas o privadas establecidas durante la aplicación de una [*transformación*](t-gly.md).
5.  Propiedad pública o privada que se establece mediante la creación de la [tabla de propiedades](property-table.md) del archivo. msi.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de las propiedades](about-properties.md)
</dt> </dl>

 

 



