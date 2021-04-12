---
title: Registro de aplicaciones COM
description: Registro de aplicaciones COM
ms.assetid: 64ab5b42-2fdb-4d06-bd58-fd76f27f7da4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e115c4a8445e701809a7f418e0ce4ef72226eb0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357555"
---
# <a name="registering-com-applications"></a>Registro de aplicaciones COM

El registro es una base de datos del sistema que contiene información acerca de la configuración del hardware y el software del sistema, así como sobre los usuarios del sistema. Cualquier programa basado en Windows puede agregar información al registro y leer información del registro. Los clientes buscan en el registro los componentes interesantes que se van a usar.

El registro mantiene información acerca de todos los objetos COM instalados en el sistema. Cada vez que una aplicación crea una instancia de un componente COM, se consulta el registro para resolver el CLSID o ProgID del componente en el directorio del archivo DLL o EXE del servidor que lo contiene. Después de determinar el servidor del componente, Windows carga el servidor en el espacio de proceso de la aplicación cliente (componentes en proceso) o inicia el servidor en su propio espacio de proceso (servidores locales y remotos). El servidor crea una instancia del componente y devuelve al cliente una referencia a una de las interfaces del componente.

Para obtener más información sobre el registro de Windows, vea los temas siguientes:

-   [Jerarquía del registro](registry-hierarchy.md)
-   [Clases y servidores](classes-and-servers.md)
-   [Clasificar componentes](classifying-components.md)
-   [Usar OleView](using-oleview.md)
-   [Registrar componentes](registering-components.md)
-   [Comprobando registro](checking-registration.md)
-   [Tipos de usuarios desconocidos](unknown-user-types.md)
-   [Claves del registro COM](com-registry-keys.md)

 

 




