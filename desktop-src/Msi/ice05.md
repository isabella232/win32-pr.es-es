---
description: 'ICE05 valida que determinadas tablas contienen entradas necesarias. Esto incluye, pero no está restringido a, la comprobación de la tabla de propiedades para las propiedades requeridas: ProductName, ProductLanguage, ProductVersion, ProductCode y manufacturer.'
ms.assetid: 90b35758-c9d9-4104-a352-f0b17b04b571
title: ICE05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e9710a81eca3da7ac947afb90a1d6788c0ddd74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652822"
---
# <a name="ice05"></a>ICE05

ICE05 valida que determinadas tablas contienen entradas necesarias. Esto incluye, pero no está restringido a, la comprobación de la [tabla](property-table.md) de propiedades para las propiedades requeridas: [**ProductName**](productname.md), [**ProductLanguage**](productlanguage.md), [**ProductVersion**](productversion.md), [**ProductCode**](productcode.md)y [**manufacturer**](manufacturer.md).

## <a name="result"></a>Resultado

ICE05 publica un error si falta una entrada necesaria.

## <a name="example"></a>Ejemplo

En el ejemplo que se muestra, ICE05 notificaría que la entrada: ' ProductVersion ' es necesaria en la tabla ' property '.

[Tabla de propiedades](property-table.md) (parcial)



| Propiedad                           | Value     |
|------------------------------------|-----------|
| [**ProductName**](productname.md) | Biocida |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



