---
title: Registro de aplicaciones COM
description: Registro de aplicaciones COM
ms.assetid: 64ab5b42-2fdb-4d06-bd58-fd76f27f7da4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e115c4a8445e701809a7f418e0ce4ef72226eb0
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369672"
---
# <a name="registering-com-applications"></a>Registro de aplicaciones COM

El registro es una base de datos del sistema que contiene información sobre la configuración de hardware y software del sistema, así como sobre los usuarios del sistema. Cualquier Windows basado en el registro puede agregar información al registro y leer información del registro. Los clientes buscan en el registro componentes interesantes que usar.

El Registro mantiene información sobre todos los objetos COM instalados en el sistema. Cada vez que una aplicación crea una instancia de un componente COM, se consulta al Registro para resolver el CLSID o ProgID del componente en el nombre de ruta de acceso del archivo DLL o EXE del servidor que lo contiene. Después de determinar el servidor del componente, Windows carga el servidor en el espacio de proceso de la aplicación cliente (componentes en proceso) o inicia el servidor en su propio espacio de proceso (servidores locales y remotos). El servidor crea una instancia del componente y devuelve al cliente una referencia a una de las interfaces del componente.

Para obtener más información sobre el registro Windows, vea los temas siguientes:

-   [Jerarquía del Registro](registry-hierarchy.md)
-   [Clases y servidores](classes-and-servers.md)
-   [Clasificación de componentes](classifying-components.md)
-   [Uso de OleView](using-oleview.md)
-   [Registrar componentes](registering-components.md)
-   [Comprobación del registro](checking-registration.md)
-   [Tipos de usuario desconocidos](unknown-user-types.md)
-   [Claves del Registro COM](com-registry-keys.md)

 

 




