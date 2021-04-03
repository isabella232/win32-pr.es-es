---
description: Para obligar a una aplicación cliente a usar siempre la misma copia de un servidor que no sea COM, cree el paquete de instalación de la aplicación para especificar una relación de componentes aislados entre el servidor y el cliente.
ms.assetid: 3ca9cad7-6848-4483-b5e3-2b7bbdefe605
title: Instalar un componente que no es COM en una ubicación privada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52ea4e10e7a08fd008352a36feca537685ee4390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913497"
---
# <a name="installing-a-non-com-component-to-a-private-location"></a><span data-ttu-id="6a716-103">Instalar un componente que no es COM en una ubicación privada</span><span class="sxs-lookup"><span data-stu-id="6a716-103">Installing a non-COM Component to a Private Location</span></span>

<span data-ttu-id="6a716-104">Para obligar a una aplicación cliente a usar siempre la misma copia de un servidor que no sea COM, cree el paquete de instalación de la aplicación para especificar una relación de [componentes aislados](isolated-components.md) entre el servidor y el cliente.</span><span class="sxs-lookup"><span data-stu-id="6a716-104">To force a client application to always use the same copy of a non-COM server, author the application's installation package to specify an [isolated components](isolated-components.md) relationship between the server and client.</span></span> <span data-ttu-id="6a716-105">Esto instala una copia privada del componente de servidor en una ubicación utilizada exclusivamente por la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="6a716-105">This installs a private copy of the server component to a location used exclusively by the client application.</span></span> <span data-ttu-id="6a716-106">Al crear el paquete, realice lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="6a716-106">Do the following when authoring the package:</span></span>

-   <span data-ttu-id="6a716-107">Coloque el archivo DLL del servidor y el cliente. exe en componentes independientes.</span><span class="sxs-lookup"><span data-stu-id="6a716-107">Put the server DLL and the .exe client in separate components.</span></span>
-   <span data-ttu-id="6a716-108">Escriba un registro en la [tabla IsolatedComponent](isolatedcomponent-table.md) con el componente de cliente en la \_ columna compartida componente y la aplicación cliente en la \_ columna aplicación de componentes.</span><span class="sxs-lookup"><span data-stu-id="6a716-108">Enter a record in the [IsolatedComponent table](isolatedcomponent-table.md) with the client component in the Component\_Shared column and the client application in the Component\_Application column.</span></span> <span data-ttu-id="6a716-109">Incluya la [acción IsolateComponents](isolatecomponents-action.md) en las tablas de secuencia.</span><span class="sxs-lookup"><span data-stu-id="6a716-109">Include the [IsolateComponents action](isolatecomponents-action.md) in the sequence tables.</span></span>
-   <span data-ttu-id="6a716-110">Establezca el bit msidbComponentAttributesSharedDllRefCount en el registro de la [tabla de componentes](component-table.md) para el componente \_ Shared.</span><span class="sxs-lookup"><span data-stu-id="6a716-110">Set the msidbComponentAttributesSharedDllRefCount bit in the [Component table](component-table.md) record for Component\_Shared.</span></span> <span data-ttu-id="6a716-111">El instalador requiere este recuento global en la ubicación compartida para proteger los archivos compartidos y el registro en los casos en los que se comparte con otras tecnologías de instalación.</span><span class="sxs-lookup"><span data-stu-id="6a716-111">The installer requires this global refcount on the shared location to protect the shared files and registration in cases where there is sharing with other installation technologies.</span></span>
-   <span data-ttu-id="6a716-112">Evite la creación de una ruta de acceso registrada compartida entre los componentes.</span><span class="sxs-lookup"><span data-stu-id="6a716-112">Avoid authoring a shared registered path across components.</span></span>

 

 



