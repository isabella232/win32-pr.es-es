---
description: ICEM10 comprueba que un módulo de combinación contiene solo las propiedades permitidas en la tabla de propiedades.
ms.assetid: 9ac7a724-ea0e-4caa-bb4f-846bfb802037
title: ICEM10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80263e5033ec14bd669c5d046c7f3842d58e332f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074469"
---
# <a name="icem10"></a>ICEM10

ICEM10 comprueba que un módulo de combinación contiene solo las propiedades permitidas en la [tabla de propiedades](property-table.md). No se permiten las siguientes propiedades específicas del producto en la tabla de propiedades:

-   [**Propiedad ProductLanguage**](productlanguage.md)
-   [**Propiedad ProductCode**](productcode.md)
-   [**Propiedad ProductVersion**](productversion.md)
-   [**Propiedad ProductName**](productname.md)
-   [**Propiedad Fabricante**](manufacturer.md)

## <a name="result"></a>Resultado

ICEM10 publica un error cuando un módulo de combinación contiene una propiedad que no se permite en la [tabla de propiedades](property-table.md).

## <a name="example"></a>Ejemplo

ICEM10 publica los siguientes mensajes de error para un módulo que contiene las entradas de base de datos mostradas.

``` syntax
The property 'ProductLanguage' is not allowed in a merge module.

The property 'Manufacturer' is not allowed in a merge module.
```

En la tabla siguiente se muestra una tabla [de propiedades parcial](property-table.md).



| Propiedad                                   | Valores    |
|--------------------------------------------|-----------|
| Color                                      | Rojo       |
| [**Fabricante**](manufacturer.md)       | Microsoft |
| [**ProductLanguage**](productlanguage.md) | 3082      |



 

En el procedimiento siguiente se muestra cómo corregir errores.

**Para corregir los errores**

1.  Quite la propiedad [**' Fabricante**](manufacturer.md)' de la tabla [de propiedades](property-table.md).
2.  Quite la propiedad [**' ProductLanguage**](productlanguage.md)' de la [tabla de propiedades](property-table.md).

## <a name="table-used-during-execution"></a>Tabla usada durante la ejecución

La [tabla de propiedades](property-table.md) se usa durante la ejecución.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE del módulo de mezcla](merge-module-ice-reference.md)
</dt> </dl>

 

 



