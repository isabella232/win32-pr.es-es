---
description: Monitor de red usa tres tipos de objetos binarios grandes (BLOB) para seleccionar y conectar tarjetas de interfaz de red (NIC), capturar datos y manipular datos de NPP.
ms.assetid: f7cbceb1-1a85-4a05-8420-90b32c9c9b61
title: Tipos de BLOB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029c375c446d53074cc0c9797dfa2992b2b2d933
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279140"
---
# <a name="blob-types"></a><span data-ttu-id="f9178-103">Tipos de BLOB</span><span class="sxs-lookup"><span data-stu-id="f9178-103">BLOB Types</span></span>

<span data-ttu-id="f9178-104">Monitor de red usa tres tipos de objetos binarios grandes (BLOB) para seleccionar y conectar tarjetas de interfaz de red (NIC), capturar datos y manipular datos de NPP.</span><span class="sxs-lookup"><span data-stu-id="f9178-104">Network Monitor uses three types of binary large objects (BLOBs) to select and connect network interface cards (NICs), capture data, and manipulate NPP data.</span></span>

## <a name="npp-blob"></a><span data-ttu-id="f9178-105">BLOB DE NPP</span><span class="sxs-lookup"><span data-stu-id="f9178-105">NPP BLOB</span></span>

<span data-ttu-id="f9178-106">Las aplicaciones usan blobs NPP para conectarse a una NIC específica a través de un NPP.</span><span class="sxs-lookup"><span data-stu-id="f9178-106">Applications use NPP BLOBs to connect to a specific NIC through an NPP.</span></span> <span data-ttu-id="f9178-107">(La aplicación realiza la conexión con una llamada a **CreateNPPInterface** y los datos de ubicación en el BLOB de NPP). Una aplicación también puede almacenar sus datos de configuración en el BLOB NPP para configurar NPP.</span><span class="sxs-lookup"><span data-stu-id="f9178-107">(The application makes the connection with a call to **CreateNPPInterface** and location data in the NPP BLOB.) An application can also store its configuration data in the NPP BLOB to configure the NPP.</span></span> <span data-ttu-id="f9178-108">Además, no es necesario que una aplicación que guarde su BLOB NPP pase por el buscador para volver a usar ese BLOB.</span><span class="sxs-lookup"><span data-stu-id="f9178-108">Also, an application that saves its NPP BLOB is not required to go through the Finder to reuse that BLOB.</span></span>

## <a name="filter-blob"></a><span data-ttu-id="f9178-109">Filtrar BLOB</span><span class="sxs-lookup"><span data-stu-id="f9178-109">Filter BLOB</span></span>

<span data-ttu-id="f9178-110">Un BLOB en filtro contiene criterios definidos por la aplicación que puede usar para seleccionar un NPP y una NIC.</span><span class="sxs-lookup"><span data-stu-id="f9178-110">A filter BLOB contains application-defined criteria that you can use to select an NPP and a NIC.</span></span> <span data-ttu-id="f9178-111">Por ejemplo, una aplicación puede solicitar una NIC específica, solo tarjetas Ethernet o tarjetas que admiten una velocidad de captura de fotogramas específica.</span><span class="sxs-lookup"><span data-stu-id="f9178-111">For example, an application can request a specific NIC, only Ethernet cards, or cards that support a specific frame capture rate.</span></span>

## <a name="special-blob"></a><span data-ttu-id="f9178-112">BLOB especial</span><span class="sxs-lookup"><span data-stu-id="f9178-112">Special BLOB</span></span>

<span data-ttu-id="f9178-113">Cuando un NPP requiere datos adicionales para poder devolver un BLOB NPP a una aplicación, el NPP usa un BLOB especial.</span><span class="sxs-lookup"><span data-stu-id="f9178-113">When an NPP requires additional data before it can return an NPP BLOB to an application, the NPP uses a special BLOB.</span></span> <span data-ttu-id="f9178-114">La mayoría de las veces, la aplicación no necesitará ni usará blobs especiales, por lo que no se devuelven a una aplicación a menos que se establezca una marca específica en una llamada de función.</span><span class="sxs-lookup"><span data-stu-id="f9178-114">Most often, the application will not need or use special BLOBs so they are not returned to an application unless a specific flag is set in one function call.</span></span> <span data-ttu-id="f9178-115">Por ejemplo, un NPP remoto usa un BLOB especial porque se requiere un nombre de ruta de acceso para realizar una conexión.</span><span class="sxs-lookup"><span data-stu-id="f9178-115">For example, a remote NPP uses a special BLOB because a path name is required to make a connection.</span></span> <span data-ttu-id="f9178-116">Una aplicación que recibe un BLOB especial de NPP remoto podría agregar la cadena y volver a llamar al buscador para obtener una tabla de BLOBs NPP.</span><span class="sxs-lookup"><span data-stu-id="f9178-116">An application that receives a remote NPP special BLOB could add the string and call back into the Finder to get an NPP BLOB table.</span></span> <span data-ttu-id="f9178-117">Para obtener más información, consulte [entradas de BLOB especiales](special-blob-entries.md).</span><span class="sxs-lookup"><span data-stu-id="f9178-117">For more information, see [Special BLOB Entries](special-blob-entries.md).</span></span>

 

 



