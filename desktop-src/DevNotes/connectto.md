---
description: HKLM \\ software \\ Microsoft \\ MSSQLSERVER \\ Client.
ms.assetid: d6eb774b-d7ae-4f51-9947-90fb176e9acf
title: ConnectTo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 581b1f77fc90bca467e90a3c3b7f407b8ba6d33d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080169"
---
# <a name="connectto"></a><span data-ttu-id="9aacd-103">ConnectTo</span><span class="sxs-lookup"><span data-stu-id="9aacd-103">ConnectTo</span></span>

<span data-ttu-id="9aacd-104">**HKLM \\ software \\ Microsoft \\ MSSQLSERVER \\ Client**</span><span class="sxs-lookup"><span data-stu-id="9aacd-104">**HKLM\\SOFTWARE\\Microsoft\\MSSQLServer\\Client**</span></span>

## <a name="description"></a><span data-ttu-id="9aacd-105">Descripción</span><span class="sxs-lookup"><span data-stu-id="9aacd-105">Description</span></span>

<span data-ttu-id="9aacd-106">La subclave **ConnectTo** almacena información de conexión para los clientes basados en Windows que se conectan a las instancias del motor de base de datos de Microsoft SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9aacd-106">The **ConnectTo** subkey stores connection information for Windows-based clients that connect to instances of the Microsoft SQL Server database engine.</span></span> <span data-ttu-id="9aacd-107">Las entradas del registro de esta subclave son del tipo de datos REG \_ SZ y sus valores especifican la Net-Library que se va a usar para conectarse a la instancia, así como cualquier parámetro específico de la red.</span><span class="sxs-lookup"><span data-stu-id="9aacd-107">Registry entries in this subkey are of data type REG\_SZ, and their values specify the Net-Library to use for connecting to the instance, as well as any network-specific parameters.</span></span>

<span data-ttu-id="9aacd-108">El proveedor de OLE DB lee la información de conexión almacenada en esta subclave para SQL Server, el controlador ODBC de SQL Server o la SQL Server DB-Library biblioteca de vínculos dinámicos (DLL).</span><span class="sxs-lookup"><span data-stu-id="9aacd-108">The connection information stored in this subkey is read by the OLE DB Provider for SQL Server, the SQL Server ODBC driver, or the SQL Server DB-Library dynamic-link library (DLL).</span></span>

## <a name="change-method"></a><span data-ttu-id="9aacd-109">Cambiar método</span><span class="sxs-lookup"><span data-stu-id="9aacd-109">Change Method</span></span>

<span data-ttu-id="9aacd-110">No debe modificar las entradas de esta subclave mediante el editor del registro.</span><span class="sxs-lookup"><span data-stu-id="9aacd-110">You should not modify entries in this subkey by using the registry editor.</span></span> <span data-ttu-id="9aacd-111">Use la herramienta de red de cliente de SQL Server para configurar el nombre del servidor y la información de conexión.</span><span class="sxs-lookup"><span data-stu-id="9aacd-111">Use the SQL Server Client Network Utility to configure server name and connection information.</span></span> <span data-ttu-id="9aacd-112">Consulte SQL Server ayuda de la herramienta de red de cliente para obtener más instrucciones.</span><span class="sxs-lookup"><span data-stu-id="9aacd-112">See SQL Server Client Network Utility Help for further instructions.</span></span>

## <a name="notes"></a><span data-ttu-id="9aacd-113">Notas</span><span class="sxs-lookup"><span data-stu-id="9aacd-113">Notes</span></span>

-   <span data-ttu-id="9aacd-114">El proveedor de OLE DB usa la subclave **ConnectTo** para SQL Server, el controlador ODBC de SQL Server y el archivo DLL de DB-Library SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9aacd-114">The **ConnectTo** subkey is used by the OLE DB Provider for SQL Server, the SQL Server ODBC Driver, and the SQL Server DB-Library DLL.</span></span> <span data-ttu-id="9aacd-115">Las entradas de esta subclave identifican a qué Net-Library estos componentes de la interfaz de programación de aplicaciones (API) de acceso a datos llaman.</span><span class="sxs-lookup"><span data-stu-id="9aacd-115">Entries in this subkey identify which Net-Library these data access application programming interface (API) components call.</span></span>
-   <span data-ttu-id="9aacd-116">Net-Libraries son componentes SQL Server que protegen los componentes de la API de acceso a datos de los detalles del uso de diferentes métodos de comunicación entre procesos (IPC) para comunicarse con una instancia del motor de base de datos de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9aacd-116">Net-Libraries are SQL Server components that shield the data access API components from the details of using different Interprocess Communication (IPC) methods to communicate with an instancess of the SQL Server database engine.</span></span>
-   <span data-ttu-id="9aacd-117">La actualización incorrecta de la subclave **ConnectTo** podría impedir que las aplicaciones se conecten correctamente a una instancia del motor de base de datos de SQL Server.</span><span class="sxs-lookup"><span data-stu-id="9aacd-117">Improperly updating the **ConnectTo** subkey might prevent applications from successfully connecting to an instance of the SQL Server database engine.</span></span>

 

 



