---
description: La \_ tabla ForceCodepage es una tabla especial que se usa para cambiar la página de códigos de un paquete de instalación. Puede determinar o establecer la página de códigos exportando o importando un archivo de archivo de texto denominado \_ ForceCodepage.idt.
ms.assetid: d95c205f-a800-4a63-a712-6f06675e4a8a
title: _ForceCodepage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 132843fa092409b26811afd6a4c1f3e7cf0544f7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159306"
---
# <a name="_forcecodepage"></a>\_ForceCodepage

La \_ tabla ForceCodepage es una tabla especial que se usa para cambiar la página de códigos de un paquete de instalación. Puede determinar o establecer la página de códigos exportando o importando un archivo de archivo de [texto](text-archive-files.md) denominado \_ ForceCodepage.idt.

El formato de la tabla ForceCodepage es de 2 líneas en blanco seguidas de una tercera línea \_ que indica la página de códigos numérica. Por ejemplo, un archivo .idt de la tabla ForceCodepage para una base de datos \_ japonesa tendría el siguiente aspecto. En este caso, la página de códigos numérica es 932.

``` syntax
<- this line blank
<- this line blank
932 _ForceCodepage
```

Para obtener más información sobre cómo usar ForceCodepage para obtener o establecer la página de códigos de una base de \_ datos, vea los temas siguientes.

-   [Control de páginas de códigos (Windows instalador)](code-page-handling-windows-installer-.md)
-   [Determinar la página de códigos de una base de datos de instalación](determining-an-installation-database-s-code-page.md)
-   [Establecer la página de códigos de una base de datos](setting-the-code-page-of-a-database.md)

La \_ tabla ForceCodepage es una pseudo tabla especial que se usa para cambiar la página de códigos de un paquete de instalación. El uso de la tabla ForceCodepage establece incondicionalmente la base de datos en la página de códigos sin realizar ninguna validación sobre si los datos actualmente en la base de datos se pueden traducir a la \_ nueva página de códigos. Siempre se recomienda cambiar la página de códigos de una base de datos con una base de datos de idioma neutro.

 

 



