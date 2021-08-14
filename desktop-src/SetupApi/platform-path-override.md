---
description: Invalidación de la ruta de acceso de la plataforma
ms.assetid: f430fd9a-f865-4cdb-b0ea-4e6d79913308
title: Invalidación de la ruta de acceso de la plataforma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c63cc1e6ba4b1cb53c26e380eeab95a96091d5159e8356d8f7067529a6b589d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992625"
---
# <a name="platform-path-override"></a>Invalidación de la ruta de acceso de la plataforma

La [**función SetupSetPlatformPathOverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea) se usa para establecer una invalidación de ruta de acceso de plataforma para una máquina de destino cuando se trabaja con archivos INF desde otro equipo. Por lo tanto, puede hacer referencia a una plataforma diferente de la que se está ejecutando actualmente. Para tratar con orígenes multimedia, puede hacer referencia a plataformas que ya no se admiten, como Alpha, MIPS y PPC. Quita la invalidación de la ruta de acceso de la plataforma si no se especifica ninguno.

Después de establecer una invalidación de ruta de acceso de plataforma mediante una llamada a [**SetupSetPlatformPathOverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea), cualquier función de instalación que pone en cola las operaciones de copia de archivos examinará el componente final de la ruta de acceso de origen. Si el componente final coincide con el nombre de la plataforma del usuario, la función setup lo reemplazará por la cadena de invalidación establecida por **SetupSetPlatformPathOverride**.

Por ejemplo, al instalar controladores de impresora en un servidor MIPS, es posible que quiera instalar controladores para todas las plataformas compatibles. La cola de los archivos normalmente instalaría los archivos especificados en las secciones dependientes de MIPS del archivo INF, con rutas de acceso de origen como los mips de \\ \\ \\ \\ origen raíz. Para instalar los archivos de una segunda plataforma, debe llamar a [**SetupSetPlatformPathOverride**](/windows/desktop/api/Setupapi/nf-setupapi-setupsetplatformpathoverridea) con *Override* que indique la plataforma de reemplazo. Si la ubicación indicada por *Override* contiene el valor de cadena "alpha", las operaciones de copia de archivos enviadas a la cola con una ruta de acceso de origen de mips de origen raíz cambiarían su ruta de acceso de origen a origen \\ \\ raíz \\ \\ \\ \\ \\ \\ alfa. Repetiría este proceso para cada plataforma de interés.

 

 



