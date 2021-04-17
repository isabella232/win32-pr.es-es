---
description: La \_ tabla ForceCodepage es una tabla especial que se usa para cambiar la página de códigos de un paquete de instalación. Puede determinar o establecer la página de códigos exportando o importando un archivo de almacenamiento de texto denominado \_ ForceCodepage. IDT.
ms.assetid: d95c205f-a800-4a63-a712-6f06675e4a8a
title: _ForceCodepage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 132843fa092409b26811afd6a4c1f3e7cf0544f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667082"
---
# <a name="_forcecodepage"></a>\_ForceCodepage

La \_ tabla ForceCodepage es una tabla especial que se usa para cambiar la página de códigos de un paquete de instalación. Puede determinar o establecer la página de códigos exportando o importando un [archivo de almacenamiento de texto](text-archive-files.md) denominado \_ ForceCodepage. IDT.

El formato de la \_ tabla ForceCodepage es 2 líneas en blanco seguidas de una tercera línea que indica la página de códigos numérica. Por ejemplo, un \_ archivo Table. IDT de ForceCodepage para una base de datos japonesa tendría el siguiente aspecto. En este caso, la página de códigos numérica es 932.

``` syntax
<- this line blank
<- this line blank
932 _ForceCodepage
```

Para obtener más información sobre cómo usar \_ ForceCodepage para obtener o establecer la página de códigos de una base de datos, vea los temas siguientes.

-   [Control de páginas de códigos (Windows Installer)](code-page-handling-windows-installer-.md)
-   [Determinar la página de códigos de una base de datos de instalación](determining-an-installation-database-s-code-page.md)
-   [Establecer la página de códigos de una base de datos](setting-the-code-page-of-a-database.md)

La \_ tabla ForceCodepage es una pseudo tabla especial que se usa para cambiar la página de códigos de un paquete de instalación. El uso de la \_ tabla ForceCodepage establece incondicionalmente la base de datos en la página de códigos sin realizar ninguna validación en cuanto a si los datos que se encuentran actualmente en la base de datos se pueden traducir en la nueva página de códigos. Siempre se recomienda que el cambio de la página de códigos de una base de datos comience con una base de datos independiente del lenguaje.

 

 



