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
# <a name="updating-application-components"></a><span data-ttu-id="5c20b-103">Actualización de componentes de la aplicación</span><span class="sxs-lookup"><span data-stu-id="5c20b-103">Updating Application Components</span></span>

<span data-ttu-id="5c20b-104">Los ensamblados privados en paralelo se pueden usar para crear componentes que se pueden actualizar fácilmente sin actualizar también la aplicación de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="5c20b-104">Side-by-side private assemblies can be used to create components that can be easily updated without also updating the hosting application.</span></span> <span data-ttu-id="5c20b-105">Esto permite que un servicio de actualización Instale los componentes actualizados de la aplicación, reinicie la aplicación y haga que la aplicación use los cambios.</span><span class="sxs-lookup"><span data-stu-id="5c20b-105">This allows an updating service to install the application's updated components, restart the application, and have the application use the changes.</span></span> <span data-ttu-id="5c20b-106">Cuando se usan manifiestos de aplicación, se puede actualizar la funcionalidad de los componentes hospedados por una aplicación sin tener que cambiar el código de la aplicación de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="5c20b-106">When using application manifests, the functionality of components hosted by an application can be updated without having to change the hosting application's code.</span></span>

<span data-ttu-id="5c20b-107">Este método se puede utilizar para actualizar la versión de los recursos de una aplicación.</span><span class="sxs-lookup"><span data-stu-id="5c20b-107">This method can be used to update the version of an application's resources.</span></span> <span data-ttu-id="5c20b-108">Por ejemplo, si una aplicación contiene un ensamblado, el manifiesto de la aplicación puede especificar una dependencia en este ensamblado.</span><span class="sxs-lookup"><span data-stu-id="5c20b-108">For example, if an application contains an assembly, the application's manifest can specify a dependency on this assembly.</span></span> <span data-ttu-id="5c20b-109">La aplicación puede obtener el ensamblado llamando a [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) para buscar y cargar los archivos que requiere.</span><span class="sxs-lookup"><span data-stu-id="5c20b-109">The application can get the assembly by calling [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) to find and load the files it requires.</span></span> <span data-ttu-id="5c20b-110">Un actualizador simplemente tiene que desconectar los bits más recientes para el ensamblado, que puede existir en paralelo con una versión anterior del ensamblado.</span><span class="sxs-lookup"><span data-stu-id="5c20b-110">An updater simply has to bring down the newest bits for the assembly, which can exist side-by-side with an earlier version of the assembly.</span></span>

 

 
