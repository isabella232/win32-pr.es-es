---
description: El instalador puede aumentar la resistencia de la aplicación reinstalando automáticamente los componentes dañados.
ms.assetid: aa565e34-f89d-4d26-945d-67b439586523
title: Buscar una característica o un componente rotos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fa17fc66fdf0bda0a04df9a5917d4e79671b32f453ead921d4f43f89bbd47dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041245"
---
# <a name="searching-for-a-broken-feature-or-component"></a>Buscar una característica o un componente rotos

El instalador puede aumentar la resistencia [de la aplicación](resiliency.md) reinstalando automáticamente los componentes dañados. En concreto, el instalador reinstala un componente o una característica si encuentra que falta el [](component-table.md) archivo o la clave del Registro especificados en la columna KeyPath de la tabla Component.

Si keyPath del componente de una característica está dañado en el origen o si se produce un error en la forma en que se crea KeyPath en la base de datos, el instalador puede intentar abrir un paquete de instalación y volver a instalar la característica cada vez que se activa el acceso directo de la característica.

Para determinar la causa de los intentos repetidos de reinstalar una característica o aplicación, compruebe en el registro de eventos dos entradas como las siguientes.

``` syntax
Detection of product 'MyProduct', feature 'MyFeature' failed during
 request for component 'MyComponent'
Detection of product 'MyProduct', feature 'MyFeature', component
 'MyComponent' failed
```

El primer mensaje indica qué componente del paquete del producto se estaba instalando. Este es el componente al que se hace referencia en la columna \_ Componente de la tabla Acceso [directo](shortcut-table.md).

El segundo mensaje indica qué componente está generando errores de detección. Este es el componente con keyPath que falta o está dañado que desencadena la reinstalación.

 

 



