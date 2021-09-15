---
description: Consulta de propiedades disponibles
ms.assetid: 9acf10cd-19a8-4542-8078-3e4ee275d4d5
title: Consulta de propiedades disponibles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22238e04404d2b88efa81ce98d0b0fb0e09d245f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127566813"
---
# <a name="querying-for-available-properties"></a>Consulta de propiedades disponibles

Si está escribiendo una herramienta de administración de uso general, lo más probable es que tenga que escribir rutinas para establecer las propiedades en generalidad completa. Para ello, hay una instalación que le permite consultar dinámicamente las propiedades que están disponibles para los elementos de cualquier colección determinada.

La [**colección PropertyInfo**](propertyinfo.md) está disponible en cualquier colección que pueda contener. La **colección PropertyInfo** contiene un elemento para cada propiedad disponible. Puede enumerar a través de estos elementos para determinar si una propiedad determinada está disponible.

Puede obtener la colección [**PropertyInfo**](propertyinfo.md) de cualquier colección que esté manteniendo mediante el método [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) en el objeto [**COMAdminCatalogCollection,**](comadmincatalogcollection.md) dejando el segundo parámetro en blanco, donde normalmente especificaría la propiedad Key de un elemento primario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Obtener y establecer propiedades](getting-and-setting-properties.md)
</dt> <dt>

[Interdependencias entre propiedades](interdependencies-between-properties.md)
</dt> <dt>

[Guardar o descartar cambios](saving-or-discarding-changes.md)
</dt> </dl>

 

 



