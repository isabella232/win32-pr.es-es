---
description: Los ensamblados privados en paralelo se pueden usar para crear componentes que se pueden actualizar fácilmente sin actualizar también la aplicación de hospedaje.
ms.assetid: 5a45ee79-3ae1-4e9b-a77e-d4209fb23fa8
title: Actualización de componentes de la aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba559323c3272db96f0cd106f0fc61624519b770
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001060"
---
# <a name="updating-application-components"></a>Actualización de componentes de la aplicación

Los ensamblados privados en paralelo se pueden usar para crear componentes que se pueden actualizar fácilmente sin actualizar también la aplicación de hospedaje. Esto permite que un servicio de actualización Instale los componentes actualizados de la aplicación, reinicie la aplicación y haga que la aplicación use los cambios. Cuando se usan manifiestos de aplicación, se puede actualizar la funcionalidad de los componentes hospedados por una aplicación sin tener que cambiar el código de la aplicación de hospedaje.

Este método se puede utilizar para actualizar la versión de los recursos de una aplicación. Por ejemplo, si una aplicación contiene un ensamblado, el manifiesto de la aplicación puede especificar una dependencia en este ensamblado. La aplicación puede obtener el ensamblado llamando a [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) para buscar y cargar los archivos que requiere. Un actualizador simplemente tiene que desconectar los bits más recientes para el ensamblado, que puede existir en paralelo con una versión anterior del ensamblado.

 

 
