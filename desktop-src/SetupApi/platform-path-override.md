---
description: Invalidación de la ruta de la plataforma
ms.assetid: f430fd9a-f865-4cdb-b0ea-4e6d79913308
title: Invalidación de la ruta de la plataforma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a9a6ae6795b444c44db91d90ecd93efd19ea9dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669879"
---
# <a name="platform-path-override"></a>Invalidación de la ruta de la plataforma

La función [**SetupSetPlatformPathOverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea) se usa para establecer una invalidación de la ruta de acceso de la plataforma para un equipo de destino cuando se trabaja con archivos INF de un equipo diferente. Como tal, puede hacer referencia a una plataforma distinta de la que se está ejecutando actualmente. Para tratar con orígenes multimedia, puede hacer referencia a plataformas que ya no se admiten, como Alpha, MIPS y PPC. Quita la invalidación de la ruta de acceso de la plataforma si no se especifica ninguno.

Una vez que se establece una invalidación de la ruta de acceso de la plataforma mediante una llamada a [**SetupSetPlatformPathOverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea), cualquier función de instalación que pone en cola las operaciones de copia de archivos examinará el componente final de la ruta de acceso de origen. Si el componente final coincide con el nombre de la plataforma del usuario, la función de instalación lo reemplazará por la cadena de invalidación establecida por **SetupSetPlatformPathOverride**.

Por ejemplo, al instalar controladores de impresora en un servidor MIPS, es posible que desee instalar controladores para todas las plataformas compatibles. Poner en cola los archivos normalmente instalaría los archivos especificados en las secciones dependientes de MIPS del archivo INF, con rutas de acceso de origen como \\ \\ \\ MIPS de origen raíz \\ . Para instalar los archivos de una segunda plataforma, debe llamar a [**SetupSetPlatformPathOverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea) con la *invalidación* que indica la plataforma de reemplazo. Si la ubicación indicada por *override* contiene el valor de cadena "Alpha", las operaciones de copia de archivos enviadas a la cola con una ruta de acceso de origen de \\ \\ \\ MIPS de origen raíz \\ tendrían la ruta de origen cambiada a \\ \\ alfa de origen raíz \\ \\ . Este proceso se repetiría para cada plataforma de interés.

 

 



