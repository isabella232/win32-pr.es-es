---
description: Los ensamblados privados en paralelo se pueden usar para crear componentes que se pueden actualizar fácilmente sin actualizar también la aplicación de hospedaje.
ms.assetid: 5a45ee79-3ae1-4e9b-a77e-d4209fb23fa8
title: Actualización de componentes de la aplicación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02948355143bc6f08c759ec6c2fe6009399cc6d8ca4b2bbd687e3d206c0e771f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101595"
---
# <a name="updating-application-components"></a>Actualización de componentes de la aplicación

Los ensamblados privados en paralelo se pueden usar para crear componentes que se pueden actualizar fácilmente sin actualizar también la aplicación de hospedaje. Esto permite que un servicio de actualización instale los componentes actualizados de la aplicación, reinicie la aplicación y haga que la aplicación use los cambios. Al usar manifiestos de aplicación, la funcionalidad de los componentes hospedados por una aplicación se puede actualizar sin tener que cambiar el código de la aplicación de hospedaje.

Este método se puede usar para actualizar la versión de los recursos de una aplicación. Por ejemplo, si una aplicación contiene un ensamblado, el manifiesto de la aplicación puede especificar una dependencia en este ensamblado. La aplicación puede obtener el ensamblado llamando a [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) para buscar y cargar los archivos que requiere. Un actualizador simplemente tiene que bajar los bits más nuevos del ensamblado, que pueden existir en paralelo con una versión anterior del ensamblado.

 

 
