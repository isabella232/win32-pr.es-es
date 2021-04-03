---
description: Para obligar a una aplicación cliente COM a usar siempre la misma copia de un servidor COM, cree el paquete de instalación de la aplicación para especificar una relación de componentes aislados entre el cliente y el servidor COM.
ms.assetid: 387c1c4d-16f5-4f46-b868-c2be7cb3f942
title: Instalar un componente COM en una ubicación privada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838b3f40c513fd0998402893543e88526e4a6d07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908307"
---
# <a name="installing-a-com-component-to-a-private-location"></a><span data-ttu-id="5b3e9-103">Instalar un componente COM en una ubicación privada</span><span class="sxs-lookup"><span data-stu-id="5b3e9-103">Installing a COM Component to a Private Location</span></span>

<span data-ttu-id="5b3e9-104">Para obligar a una aplicación cliente COM a usar siempre la misma copia de un servidor COM, cree el paquete de instalación de la aplicación para especificar una relación de [componentes aislados](isolated-components.md) entre el cliente y el servidor com.</span><span class="sxs-lookup"><span data-stu-id="5b3e9-104">To force a COM-client application to always use the same copy of a COM-server, author the application's installation package to specify an [isolated components](isolated-components.md) relationship between the COM server and client.</span></span> <span data-ttu-id="5b3e9-105">De este modo se instala una copia privada del componente COM-Server en una ubicación utilizada exclusivamente por la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="5b3e9-105">This installs a private copy of the COM-server component to a location used exclusively by the client application.</span></span> <span data-ttu-id="5b3e9-106">Al crear el paquete, realice lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="5b3e9-106">Do the following when authoring the package:</span></span>

-   <span data-ttu-id="5b3e9-107">Coloque el archivo DLL del servidor COM y el cliente. exe en componentes independientes.</span><span class="sxs-lookup"><span data-stu-id="5b3e9-107">Put the COM server DLL and the .exe client in separate components.</span></span>
-   <span data-ttu-id="5b3e9-108">Escriba un registro en la [tabla IsolatedComponent](isolatedcomponent-table.md) con el componente de cliente com en la \_ columna compartida componente y la aplicación cliente en la \_ columna aplicación de componentes.</span><span class="sxs-lookup"><span data-stu-id="5b3e9-108">Enter a record in the [IsolatedComponent table](isolatedcomponent-table.md) with the COM-client component in the Component\_Shared column and the client application in the Component\_Application column.</span></span> <span data-ttu-id="5b3e9-109">Incluya la [acción IsolateComponents](isolatecomponents-action.md) en las tablas de secuencia.</span><span class="sxs-lookup"><span data-stu-id="5b3e9-109">Include the [IsolateComponents action](isolatecomponents-action.md) in the sequence tables.</span></span>
-   <span data-ttu-id="5b3e9-110">Establezca el bit msidbComponentAttributesSharedDllRefCount en el registro de la [tabla de componentes](component-table.md) para el componente \_ Shared.</span><span class="sxs-lookup"><span data-stu-id="5b3e9-110">Set the msidbComponentAttributesSharedDllRefCount bit in the [Component table](component-table.md) record for Component\_Shared.</span></span> <span data-ttu-id="5b3e9-111">El instalador requiere este recuento global en la ubicación compartida para proteger los archivos compartidos y el registro en los casos en los que se comparte con otras tecnologías de instalación.</span><span class="sxs-lookup"><span data-stu-id="5b3e9-111">The installer requires this global refcount on the shared location to protect the shared files and registration in cases where there is sharing with other installation technologies.</span></span>

 

 



