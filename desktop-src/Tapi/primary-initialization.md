---
description: Una aplicación TAPI debe llamar a una operación de inicialización, que solicita una serie de acciones de TAPI y los proveedores de servicios que configuran el entorno de comunicación de la aplicación.
ms.assetid: 10df0fb4-08d6-4ba0-85f7-108cc4e237c1
title: Inicialización principal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bcf37eecdee18861732dd27a4b134face9a17d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688145"
---
# <a name="primary-initialization"></a><span data-ttu-id="565d8-103">Inicialización principal</span><span class="sxs-lookup"><span data-stu-id="565d8-103">Primary Initialization</span></span>

<span data-ttu-id="565d8-104">Una aplicación TAPI debe llamar a una operación de inicialización, que solicita una serie de acciones de TAPI y los proveedores de servicios que configuran el entorno de comunicación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="565d8-104">A TAPI application must call an initialization operation, which prompts a series of actions from TAPI and the service providers that set up the communication environment for the application.</span></span>

-   <span data-ttu-id="565d8-105">La inicialización es sincrónica y no devuelve ningún resultado hasta que se completa o se produce un error en la operación.</span><span class="sxs-lookup"><span data-stu-id="565d8-105">Initialization is synchronous and does not return until the operation is complete or has failed.</span></span>
-   <span data-ttu-id="565d8-106">Si TAPISRV no se está ejecutando, TAPI lo inicia.</span><span class="sxs-lookup"><span data-stu-id="565d8-106">If TAPISRV is not already running, TAPI starts it.</span></span>
-   <span data-ttu-id="565d8-107">TAPI configura una conexión al proceso TAPISRV.</span><span class="sxs-lookup"><span data-stu-id="565d8-107">TAPI sets up a connection to the TAPISRV process.</span></span>
-   <span data-ttu-id="565d8-108">TAPISVR carga los proveedores de servicios especificados en el registro y les solicita que inicialicen los dispositivos que admiten.</span><span class="sxs-lookup"><span data-stu-id="565d8-108">TAPISVR loads the service providers specified in the registry and prompts them to initialize the devices they support.</span></span>

<span data-ttu-id="565d8-109">**TAPI 2. x:** Las aplicaciones realizan la inicialización mediante una llamada a [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa).</span><span class="sxs-lookup"><span data-stu-id="565d8-109">**TAPI 2.x:** Applications perform initialization by calling [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa).</span></span>

<span data-ttu-id="565d8-110">**TAPI 3. x:** Las aplicaciones llaman a [**ITTAPI:: Initialize**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-initialize).</span><span class="sxs-lookup"><span data-stu-id="565d8-110">**TAPI 3.x:** Applications call [**ITTAPI::Initialize**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-initialize).</span></span>

 

 
