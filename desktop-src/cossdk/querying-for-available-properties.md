---
description: Consultar las propiedades disponibles
ms.assetid: 9acf10cd-19a8-4542-8078-3e4ee275d4d5
title: Consultar las propiedades disponibles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22238e04404d2b88efa81ce98d0b0fb0e09d245f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153388"
---
# <a name="querying-for-available-properties"></a>Consultar las propiedades disponibles

Si está escribiendo una herramienta de administración de uso general, lo más probable es que tenga que escribir rutinas para establecer las propiedades en general. Para admitir esto, existe una instalación que permite consultar de forma dinámica las propiedades que están disponibles para los elementos de una colección determinada.

La colección [**PropertyInfo**](propertyinfo.md) está disponible en cualquier colección que pueda contener. La colección **PropertyInfo** contiene un elemento para cada propiedad disponible. Puede enumerar estos elementos para determinar si una propiedad determinada está disponible.

Puede obtener la colección [**PropertyInfo**](propertyinfo.md) de cualquier colección que esté conservando mediante el método [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) en el objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , y dejar en blanco el segundo parámetro, donde normalmente se especificaría la propiedad clave de un elemento primario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Obtener y establecer propiedades](getting-and-setting-properties.md)
</dt> <dt>

[Interdependencias entre propiedades](interdependencies-between-properties.md)
</dt> <dt>

[Guardar o descartar cambios](saving-or-discarding-changes.md)
</dt> </dl>

 

 



