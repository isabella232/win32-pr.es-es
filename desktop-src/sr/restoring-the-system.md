---
title: Restaurar el sistema
description: A medida que el equipo se usa a lo largo del tiempo, los puntos de restauración se recopilan en el archivo de datos sin necesidad de administración o intervención requerida por el usuario.
ms.assetid: 9581eff5-44d0-407e-b7cb-d3e13910a936
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4c5ff4aef88ec9eca591ee3c1afb1ad570689a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695318"
---
# <a name="restoring-the-system"></a>Restaurar el sistema

A medida que el equipo se usa a lo largo del tiempo, los puntos de restauración se recopilan en el archivo de datos sin necesidad de administración o intervención requerida por el usuario. Si el usuario necesita restaurar el sistema a un estado anterior, los puntos de restauración disponibles se hacen visibles al usuario a través de la interfaz de usuario de restauración del sistema. El usuario puede elegir cualquiera de estos puntos de restauración. La única manera de tener acceso a este archivo de puntos de restauración es a través de la interfaz de usuario de restauración del sistema y la API de restauración del sistema. Esto se hace para proteger la integridad de los datos y evitar cambios accidentales realizados por el usuario, las aplicaciones u otros agentes.

Para restaurar un sistema, Restaurar sistema deshace los cambios de archivo realizados en los archivos supervisados, recapturando el estado del archivo en el momento del punto de restauración seleccionado. A continuación, reemplaza el registro actual por el que se guardó para el punto de restauración seleccionado.

Para asegurarse de que la aplicación tenga el comportamiento deseado después de una restauración, haga lo siguiente:

-   No almacene información en el registro que impida el acceso de los usuarios a archivos de datos personales o a aplicaciones en Restaurar sistema. De lo contrario, debe proporcionar un mecanismo por el que el usuario pueda descargar y volver a instalar las aplicaciones sin tener que pagarlas de nuevo.
-   Use la [API de restauración del sistema](system-restore-api.md) para crear puntos de restauración significativos en instalación y desinstalación.
-   En Windows XP, los archivos binarios de la aplicación clave que se van a proteger deben usar extensiones coherentes con las utilizadas en Filelist.xml. Para obtener más información, vea [extensiones de nombre de archivo supervisado](monitored-file-extensions.md). Windows 7 y Windows Vista no usan este archivo. No use tipos de extensión supervisados para archivos editables por el usuario. Por ejemplo, si se denomina el archivo de datos personales de un usuario mediante la extensión. ini, el usuario puede perder el trabajo como resultado de una restauración del sistema.

 

 




