---
description: 'ICE05 valida que determinadas tablas contienen entradas necesarias. Esto incluye, pero no está restringido, comprobar en la tabla Property las propiedades necesarias: ProductName, ProductLanguage, ProductVersion, ProductCode y Manufacturer.'
ms.assetid: 90b35758-c9d9-4104-a352-f0b17b04b571
title: ICE05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e9710a81eca3da7ac947afb90a1d6788c0ddd74
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074677"
---
# <a name="ice05"></a>ICE05

ICE05 valida que determinadas tablas contienen entradas necesarias. Esto incluye, pero no está restringido a , comprobar en la tabla [Property](property-table.md) las propiedades necesarias: [**ProductName**](productname.md), [**ProductLanguage,**](productlanguage.md) [**ProductVersion**](productversion.md), [**ProductCode**](productcode.md)y [**Manufacturer**](manufacturer.md).

## <a name="result"></a>Resultado

ICE05 envía un error si falta una entrada necesaria.

## <a name="example"></a>Ejemplo

En el ejemplo que se muestra, ICE05 notificaría que se requiere la entrada "ProductVersion" en la tabla "Property".

[Tabla de propiedades](property-table.md) (parcial)



| Propiedad.                           | Value     |
|------------------------------------|-----------|
| [**ProductName**](productname.md) | MyProduct |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



