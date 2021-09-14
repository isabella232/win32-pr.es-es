---
description: El instalador puede aumentar la resistencia de la aplicación mediante la reinstalación automática de los componentes dañados.
ms.assetid: aa565e34-f89d-4d26-945d-67b439586523
title: Buscar una característica o componente rotos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8398d084a543ee4c9491242faa287c60d83a5f7e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069645"
---
# <a name="searching-for-a-broken-feature-or-component"></a>Buscar una característica o componente rotos

El instalador puede aumentar la resistencia [de la aplicación](resiliency.md) mediante la reinstalación automática de los componentes dañados. En concreto, el instalador vuelve a instalar un componente o una característica si encuentra que falta el archivo o la clave del Registro especificados en la columna KeyPath de la [tabla Component.](component-table.md)

Si keyPath del componente de una característica está dañado en el origen o si se produce un error en cómo se crea KeyPath en la base de datos, el instalador puede intentar abrir un paquete de instalación y volver a instalar la característica cada vez que se activa el acceso directo de la característica.

Para determinar la causa de los intentos repetidos de reinstalar una característica o aplicación, compruebe en el registro de eventos dos entradas como las siguientes.

``` syntax
Detection of product 'MyProduct', feature 'MyFeature' failed during
 request for component 'MyComponent'
Detection of product 'MyProduct', feature 'MyFeature', component
 'MyComponent' failed
```

El primer mensaje indica qué componente del paquete del producto se estaba instalando. Este es el componente al que se hace referencia en la columna \_ Componente de la tabla de [métodos abreviados](shortcut-table.md).

El segundo mensaje indica qué componente está generando errores de detección. Este es el componente con keyPath que falta o está dañado y que desencadena la reinstalación.

 

 



