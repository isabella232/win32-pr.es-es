---
description: El instalador puede aumentar la resistencia de la aplicación reinstalando automáticamente los componentes dañados.
ms.assetid: aa565e34-f89d-4d26-945d-67b439586523
title: Buscar una característica o componente interrumpido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8398d084a543ee4c9491242faa287c60d83a5f7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277367"
---
# <a name="searching-for-a-broken-feature-or-component"></a>Buscar una característica o componente interrumpido

El instalador puede aumentar la [resistencia](resiliency.md) de la aplicación reinstalando automáticamente los componentes dañados. En concreto, el instalador vuelve a instalar un componente o una característica si encuentra que falta el archivo o la clave del registro especificados en la columna de ruta de acceso de la [tabla de componentes](component-table.md) .

Si la ruta de acceso del componente de una característica está dañada en el origen, o si se produce un error en la forma en que se crea la ruta de acceso de la base de datos, es posible que el instalador intente abrir un paquete de instalación y reinstale la característica cada vez que se active el método abreviado de la característica.

Para determinar la causa de los intentos repetidos de reinstalar una característica o aplicación, busque en el registro de eventos dos entradas como la siguiente.

``` syntax
Detection of product 'MyProduct', feature 'MyFeature' failed during
 request for component 'MyComponent'
Detection of product 'MyProduct', feature 'MyFeature', component
 'MyComponent' failed
```

El primer mensaje indica qué componente del paquete del producto se estaba instalando. Este es el componente al que se hace referencia en la \_ columna componente de la [tabla de acceso directo](shortcut-table.md).

El segundo mensaje indica qué componente está detectando errores. Este es el componente con la ruta de la ruta de rutas que falta o está dañada y que desencadena la reinstalación.

 

 



