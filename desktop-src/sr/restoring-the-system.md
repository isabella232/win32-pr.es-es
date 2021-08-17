---
title: Restaurar el sistema
description: A medida que el equipo se usa con el tiempo, los puntos de restauración se recopilan en el archivo de datos sin necesidad de administración ni intervención por parte del usuario.
ms.assetid: 9581eff5-44d0-407e-b7cb-d3e13910a936
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99d7e54fd12bbb05dacd0c388c1867319189924d761a43d90c6f2a9f718f26e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857525"
---
# <a name="restoring-the-system"></a>Restaurar el sistema

A medida que el equipo se usa con el tiempo, los puntos de restauración se recopilan en el archivo de datos sin necesidad de administración ni intervención por parte del usuario. Si el usuario necesita restaurar el sistema a un estado anterior, los puntos de restauración disponibles se hacen visibles para el usuario a través de la interfaz Restaurar sistema usuario. El usuario puede elegir cualquiera de estos puntos de restauración. La única manera de acceder a este archivo de puntos de restauración es a través de la interfaz Restaurar sistema usuario y la API Restaurar sistema restauración. esto es para proteger la integridad de los datos y evitar cambios accidentales realizados por el usuario, las aplicaciones u otros agentes.

Para restaurar un sistema, Restaurar sistema deshace los cambios realizados en los archivos supervisados, recapturando el estado del archivo en el momento del punto de restauración seleccionado. A continuación, reemplaza el registro actual por el guardado para el punto de restauración seleccionado.

Para asegurarse de que la aplicación tiene el comportamiento deseado después de una restauración, haga lo siguiente:

-   No almacene información en el Registro que impida que el usuario acceda a archivos de datos personales o aplicaciones durante la restauración del sistema. De lo contrario, debe proporcionar un mecanismo por el que el usuario pueda descargar y volver a instalar las aplicaciones sin tener que volver a pagar por ellas.
-   Use la [API Restaurar sistema para](system-restore-api.md) crear puntos de restauración significativos al instalar y desinstalar.
-   En Windows XP, los archivos binarios de aplicación clave que se deben proteger deben usar extensiones coherentes con las que se usan en Filelist.xml. Para obtener más información, [vea Extensiones de nombre de archivo supervisado.](monitored-file-extensions.md) Este archivo no se usa en Windows 7 y Windows Vista. No use tipos de extensión supervisados para archivos editables por el usuario. Por ejemplo, si se llama archivo de datos personales de un usuario mediante la extensión .ini, el usuario puede perder el trabajo como resultado de una restauración del sistema.

 

 




