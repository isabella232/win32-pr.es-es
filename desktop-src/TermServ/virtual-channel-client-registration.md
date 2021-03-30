---
title: Registro de cliente de canal virtual
description: Debe almacenar el nombre del archivo DLL de cliente en el registro.
ms.assetid: bf84b2f4-55c2-45fd-bba7-8ff3efe4b1fd
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcd7ecf128f125f6f25202bf683f8aa55ae4f257
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792070"
---
# <a name="virtual-channel-client-registration"></a><span data-ttu-id="be63a-103">Registro de cliente de canal virtual</span><span class="sxs-lookup"><span data-stu-id="be63a-103">Virtual Channel Client Registration</span></span>

<span data-ttu-id="be63a-104">Debe almacenar el nombre del archivo DLL de cliente en el registro.</span><span class="sxs-lookup"><span data-stu-id="be63a-104">You must store the name of the client DLL in the registry.</span></span>

<span data-ttu-id="be63a-105">En el registro, agregue una subclave a una de las siguientes ubicaciones:</span><span class="sxs-lookup"><span data-stu-id="be63a-105">In the registry, add a subkey to one of the following locations:</span></span>

<span data-ttu-id="be63a-106">**HKEY \_ Software de \_ usuario actual** \\  \\  \\  \\  \\ **Complementos** predeterminados de cliente de Microsoft Terminal Server</span><span class="sxs-lookup"><span data-stu-id="be63a-106">**HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Terminal Server Client**\\**Default**\\**Addins**</span></span>

<span data-ttu-id="be63a-107">**HKEY \_ Software de \_ usuario actual** \\  \\  \\  \\  \\ **Complementos** de conexión de cliente de Microsoft Terminal Server</span><span class="sxs-lookup"><span data-stu-id="be63a-107">**HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Terminal Server Client**\\**connection**\\**Addins**</span></span>

> [!Note]  
> <span data-ttu-id="be63a-108">En la ruta de acceso del registro, *Connection* representa el nombre de una conexión en el administrador de conexiones.</span><span class="sxs-lookup"><span data-stu-id="be63a-108">In the registry path, *connection* represents the name of a connection in Connection Manager.</span></span>

 

<span data-ttu-id="be63a-109">Las entradas de la clave **\\ \\ AddIns predeterminada** se aplican a todas las conexiones.</span><span class="sxs-lookup"><span data-stu-id="be63a-109">Entries under the **\\Default\\Addins** key apply to all connections.</span></span> <span data-ttu-id="be63a-110">Las entradas de la clave **\\  \\ AddIns de conexión** solo se aplican a la conexión identificada por la *conexión*.</span><span class="sxs-lookup"><span data-stu-id="be63a-110">Entries under the **\\***connection***\\Addins** key apply only to the connection identified by *connection*.</span></span> <span data-ttu-id="be63a-111">Las conexiones se pueden crear y administrar mediante el administrador de conexiones.</span><span class="sxs-lookup"><span data-stu-id="be63a-111">Connections can be created and managed by using Connection Manager.</span></span>

<span data-ttu-id="be63a-112">A la subclave se le puede asignar cualquier nombre.</span><span class="sxs-lookup"><span data-stu-id="be63a-112">The subkey can be given any name.</span></span> <span data-ttu-id="be63a-113">Debe contener un valor de **reg \_ SZ** o **reg \_ Expand \_ SZ** y puede contener opcionalmente un valor de **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="be63a-113">It must contain a **REG\_SZ** or **REG\_EXPAND\_SZ** value and may optionally contain a **REG\_DWORD** value.</span></span> <span data-ttu-id="be63a-114">La sintaxis de los valores de **reg \_ SZ** o **reg \_ Expand \_** es como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="be63a-114">The syntax of the **REG\_SZ** or **REG\_EXPAND\_SZ** value is as follows.</span></span>

``` syntax
Name = DLLname
```

<span data-ttu-id="be63a-115">Si **Name** es un valor de **reg \_ Expandable \_** , puede contener variables de entorno no expandidas que se expandan en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="be63a-115">If **Name** is a **REG\_EXPAND\_SZ** value, it can contain unexpanded environment variables that are expanded at runtime.</span></span>

<span data-ttu-id="be63a-116">El valor de *DLLname* puede ser una ruta de acceso completa.</span><span class="sxs-lookup"><span data-stu-id="be63a-116">The value of *DLLname* can be a fully qualified path.</span></span> <span data-ttu-id="be63a-117">Si *DLLname* no contiene una ruta de acceso, se usa la estrategia de búsqueda dll estándar.</span><span class="sxs-lookup"><span data-stu-id="be63a-117">If *DLLname* does not contain a path, the standard DLL search strategy is used.</span></span> <span data-ttu-id="be63a-118">Para obtener más información, vea la sección Comentarios para [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya).</span><span class="sxs-lookup"><span data-stu-id="be63a-118">For more information, see the Remarks section for [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya).</span></span>

 

 