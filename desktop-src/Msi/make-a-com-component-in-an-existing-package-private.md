---
description: Un administrador puede obligar a una aplicación cliente COM a usar siempre la misma copia de un servidor COM en un paquete existente&\# 8212; sin afectar a otras aplicaciones&\# 8212; especificando una relación de componentes aislados entre el servidor com y el cliente.
ms.assetid: 814eca94-2bb5-4aff-8de3-473da71d4400
title: Convertir un componente COM en un paquete existente privado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4935d20c5034af81a52c18d35454553b04cfb97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678253"
---
# <a name="make-a-com-component-in-an-existing-package-private"></a><span data-ttu-id="252ba-103">Convertir un componente COM en un paquete existente privado</span><span class="sxs-lookup"><span data-stu-id="252ba-103">Make a COM Component in an Existing Package Private</span></span>

<span data-ttu-id="252ba-104">Un administrador puede obligar a una aplicación cliente COM a usar siempre la misma copia de un servidor COM en un paquete existente, sin que afecte a otras aplicaciones, mediante la especificación de una relación de [componentes aislados](isolated-components.md) entre el cliente y el servidor com.</span><span class="sxs-lookup"><span data-stu-id="252ba-104">An administrator can force a COM-client application to always use the same copy of a COM-server in an existing package—without affecting other applications—by specifying an [isolated components](isolated-components.md) relationship between the COM server and client.</span></span> <span data-ttu-id="252ba-105">De este modo se instala una copia privada del componente COM-Server en una ubicación utilizada exclusivamente por la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="252ba-105">This installs a private copy of the COM-server component to a location used exclusively by the client application.</span></span> <span data-ttu-id="252ba-106">El administrador debe usar transformaciones o una herramienta de creación de paquetes para realizar lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="252ba-106">The administrator needs to use transforms or a package authoring tool to do the following:</span></span>

-   <span data-ttu-id="252ba-107">Coloque el archivo DLL del servidor COM y el cliente. exe en componentes independientes.</span><span class="sxs-lookup"><span data-stu-id="252ba-107">Put the COM server DLL and the .exe client in separate components.</span></span>
-   <span data-ttu-id="252ba-108">Escriba un registro en la [tabla IsolatedComponent](isolatedcomponent-table.md) con el componente de cliente com en la \_ columna compartida componente y la aplicación cliente en la \_ columna aplicación de componentes.</span><span class="sxs-lookup"><span data-stu-id="252ba-108">Enter a record in the [IsolatedComponent table](isolatedcomponent-table.md) with the COM-client component in the Component\_Shared column and the client application in the Component\_Application column.</span></span> <span data-ttu-id="252ba-109">Incluya la [acción IsolateComponents](isolatecomponents-action.md) en las tablas de secuencia.</span><span class="sxs-lookup"><span data-stu-id="252ba-109">Include the [IsolateComponents action](isolatecomponents-action.md) in the sequence tables.</span></span>
-   <span data-ttu-id="252ba-110">Establezca el bit **msidbComponentAttributesSharedDllRefCount** en el registro de la [tabla de componentes](component-table.md) para el componente \_ Shared.</span><span class="sxs-lookup"><span data-stu-id="252ba-110">Set the **msidbComponentAttributesSharedDllRefCount** bit in the [Component table](component-table.md) record for Component\_Shared.</span></span> <span data-ttu-id="252ba-111">El instalador requiere este recuento global en la ubicación compartida para proteger los archivos compartidos y el registro en los casos en los que se comparte con otras tecnologías de instalación.</span><span class="sxs-lookup"><span data-stu-id="252ba-111">The installer requires this global refcount on the shared location to protect the shared files and registration in cases where there is sharing with other installation technologies.</span></span>

 

 



