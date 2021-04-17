---
description: Un administrador puede obligar a una aplicación cliente a usar siempre la misma copia de un servidor que no sea COM en un paquete existente&\# 8212; sin que afecte a otras aplicaciones&\# 8212; especificando una relación de componentes aislados entre el servidor y el cliente.
ms.assetid: e10d7942-b13c-46a3-a8ca-cb7bc021c76b
title: Convertir un componente que no sea COM en un paquete existente privado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d87a74a4f9fe7c3770100f78dd0fcd154772943
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677466"
---
# <a name="make-a-non-com-component-in-an-existing-package-private"></a><span data-ttu-id="cd723-103">Convertir un componente que no sea COM en un paquete existente privado</span><span class="sxs-lookup"><span data-stu-id="cd723-103">Make a non-COM Component in an Existing Package Private</span></span>

<span data-ttu-id="cd723-104">Un administrador puede obligar a una aplicación cliente a usar siempre la misma copia de un servidor que no sea COM en un paquete existente, sin que afecte a otras aplicaciones, mediante la especificación de una relación de [componentes aislados](isolated-components.md) entre el servidor y el cliente.</span><span class="sxs-lookup"><span data-stu-id="cd723-104">An administrator can force a client application to always use the same copy of a non-COM server in an existing package—without affecting other applications—by specifying an [isolated components](isolated-components.md) relationship between the server and client.</span></span> <span data-ttu-id="cd723-105">Esto instala una copia privada del componente de servidor en una ubicación utilizada exclusivamente por la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="cd723-105">This installs a private copy of the server component to a location used exclusively by the client application.</span></span> <span data-ttu-id="cd723-106">El administrador debe usar transformaciones o una herramienta de creación de paquetes para realizar lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="cd723-106">The administrator needs to use transforms or a package authoring tool to do the following:</span></span>

-   <span data-ttu-id="cd723-107">Coloque el archivo DLL del servidor y el cliente. exe en componentes independientes.</span><span class="sxs-lookup"><span data-stu-id="cd723-107">Put the server DLL and the .exe client in separate components.</span></span>
-   <span data-ttu-id="cd723-108">Escriba un registro en la [tabla IsolatedComponent](isolatedcomponent-table.md) con el componente de cliente en la \_ columna compartida componente y la aplicación cliente en la \_ columna aplicación de componentes.</span><span class="sxs-lookup"><span data-stu-id="cd723-108">Enter a record in the [IsolatedComponent table](isolatedcomponent-table.md) with the client component in the Component\_Shared column and the client application in the Component\_Application column.</span></span> <span data-ttu-id="cd723-109">Incluya la [acción IsolateComponents](isolatecomponents-action.md) en las tablas de secuencia.</span><span class="sxs-lookup"><span data-stu-id="cd723-109">Include the [IsolateComponents action](isolatecomponents-action.md) in the sequence tables.</span></span>
-   <span data-ttu-id="cd723-110">Establezca el bit **msidbComponentAttributesSharedDllRefCount** en el registro de la [tabla de componentes](component-table.md) para el componente \_ Shared.</span><span class="sxs-lookup"><span data-stu-id="cd723-110">Set the **msidbComponentAttributesSharedDllRefCount** bit in the [Component table](component-table.md) record for Component\_Shared.</span></span> <span data-ttu-id="cd723-111">El instalador requiere este recuento global en la ubicación compartida para proteger los archivos compartidos y el registro en los casos en los que se comparte con otras tecnologías de instalación.</span><span class="sxs-lookup"><span data-stu-id="cd723-111">The installer requires this global refcount on the shared location to protect the shared files and registration in cases where there is sharing with other installation technologies.</span></span>

 

 



