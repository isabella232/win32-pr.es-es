---
title: Configuración del proveedor de servicios de nombres del localizador de Microsoft
description: Puede cambiar el proveedor de servicio de nombres especificado editando el archivo de configuración Rpcreg. dat, que contiene los parámetros NSP y la configuración del protocolo RPC. Use un editor de texto para cambiar las entradas NSP.
ms.assetid: b499e40e-d38f-4e51-bbce-41af3ff12a7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14a5334436ce307030048a862f1375a91000b41e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357291"
---
# <a name="configuring-the-microsoft-locator-name-service-provider"></a><span data-ttu-id="0b198-104">Configuración del proveedor de servicios de nombres del localizador de Microsoft</span><span class="sxs-lookup"><span data-stu-id="0b198-104">Configuring the Microsoft Locator Name Service Provider</span></span>

<span data-ttu-id="0b198-105">Puede cambiar el proveedor de servicio de nombres especificado editando el archivo de configuración Rpcreg. dat, que contiene los parámetros NSP y la configuración del protocolo RPC.</span><span class="sxs-lookup"><span data-stu-id="0b198-105">You can change the name service provider you specified by editing the Rpcreg.dat configuration file, which contains the NSP parameters and RPC protocol settings.</span></span> <span data-ttu-id="0b198-106">Use un editor de texto para cambiar las entradas NSP.</span><span class="sxs-lookup"><span data-stu-id="0b198-106">Use a text editor to change NSP entries.</span></span>

<span data-ttu-id="0b198-107">**Para volver a configurar el proveedor de servicios de nombres del localizador de Microsoft**</span><span class="sxs-lookup"><span data-stu-id="0b198-107">**To reconfigure the Microsoft Locator name service provider**</span></span>

1.  <span data-ttu-id="0b198-108">Abra el archivo Rpcreg. dat con un editor de texto.</span><span class="sxs-lookup"><span data-stu-id="0b198-108">Open the Rpcreg.dat file using a text editor.</span></span>

    <span data-ttu-id="0b198-109">Rpcreg. dat está en el directorio raíz a menos que haya especificado una ruta de acceso diferente durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="0b198-109">Rpcreg.dat is in the root directory unless you specified a different path during setup.</span></span>

2.  <span data-ttu-id="0b198-110">Establezca los siguientes valores para las entradas del registro.</span><span class="sxs-lookup"><span data-stu-id="0b198-110">Set the following values for the registry entries.</span></span> 

    | <span data-ttu-id="0b198-111">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="0b198-111">Registry entry</span></span>                                         | <span data-ttu-id="0b198-112">Value</span><span class="sxs-lookup"><span data-stu-id="0b198-112">Value</span></span>                                                                                                                                                 |
    |--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="0b198-113">\\Protocolo Microsoft \\ RPC \\ NameService \\</span><span class="sxs-lookup"><span data-stu-id="0b198-113">Software\\Microsoft\\RPC \\NameService\\Protocol</span></span>       | <span data-ttu-id="0b198-114">La secuencia de protocolos para el protocolo que está usando.</span><span class="sxs-lookup"><span data-stu-id="0b198-114">The protocol sequence for the protocol you are using.</span></span> <span data-ttu-id="0b198-115">El valor predeterminado es **ncacn \_ NP**.</span><span class="sxs-lookup"><span data-stu-id="0b198-115">The default is **ncacn\_np**.</span></span>                                                                   |
    | <span data-ttu-id="0b198-116">Software \\ Microsoft \\ RPC \\ NameService \\ NetworkAddress</span><span class="sxs-lookup"><span data-stu-id="0b198-116">Software\\Microsoft\\RPC\\ NameService\\NetworkAddress</span></span> | <span data-ttu-id="0b198-117">Nombre del equipo que ejecuta el localizador que usan los clientes durante las operaciones de búsqueda de servicio de nombres.</span><span class="sxs-lookup"><span data-stu-id="0b198-117">The name of the computer running Locator that is used by clients during name service lookup operations.</span></span> <span data-ttu-id="0b198-118">El valor predeterminado es el controlador de dominio principal.</span><span class="sxs-lookup"><span data-stu-id="0b198-118">The default is the primary domain controller.</span></span> |
    | <span data-ttu-id="0b198-119">\\Punto de conexión de Microsoft \\ RPC \\ NameService \\ de software</span><span class="sxs-lookup"><span data-stu-id="0b198-119">Software\\Microsoft\\RPC\\ NameService\\Endpoint</span></span>       | <span data-ttu-id="0b198-120">Nombre del punto de conexión utilizado por el servicio de nombres.</span><span class="sxs-lookup"><span data-stu-id="0b198-120">The name of the endpoint used by the name service.</span></span> <span data-ttu-id="0b198-121">El valor predeterminado es el \\ localizador de canalización \\ .</span><span class="sxs-lookup"><span data-stu-id="0b198-121">The default is \\pipe\\locator.</span></span>                                                                    |

    

     

3.  <span data-ttu-id="0b198-122">Guarde y cierre el archivo.</span><span class="sxs-lookup"><span data-stu-id="0b198-122">Save and close the file.</span></span>

 

 




