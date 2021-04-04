---
description: Los recursos compartidos DDE son un recurso de equipo.
ms.assetid: 98d24300-52cc-4f0d-b74f-c58b823ac5f3
title: Recursos compartidos DDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 012c219897187c9e68b5b9e662b93678b77974c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910209"
---
# <a name="dde-shares"></a><span data-ttu-id="60ce5-103">Recursos compartidos DDE</span><span class="sxs-lookup"><span data-stu-id="60ce5-103">DDE Shares</span></span>

<span data-ttu-id="60ce5-104">\[Ya no se admite DDE de red.</span><span class="sxs-lookup"><span data-stu-id="60ce5-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="60ce5-105">Nddeapi.dll está presente en Windows Vista, pero todas las llamadas de función devuelven NDDE \_ no \_ implementado.\]</span><span class="sxs-lookup"><span data-stu-id="60ce5-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="60ce5-106">Los recursos compartidos DDE son un recurso de equipo.</span><span class="sxs-lookup"><span data-stu-id="60ce5-106">DDE shares are a machine resource.</span></span> <span data-ttu-id="60ce5-107">Son similares a los recursos compartidos de archivos porque se utilizan para controlar el acceso a un recurso.</span><span class="sxs-lookup"><span data-stu-id="60ce5-107">They are similar to file shares because they are used to control access to a resource.</span></span> <span data-ttu-id="60ce5-108">Con recursos compartidos de archivos, el recurso es un archivo.</span><span class="sxs-lookup"><span data-stu-id="60ce5-108">With file shares, the resource is a file.</span></span> <span data-ttu-id="60ce5-109">Con los recursos compartidos DDE, el recurso cambia de forma dinámica los datos.</span><span class="sxs-lookup"><span data-stu-id="60ce5-109">With DDE shares, the resource is dynamically exchanged data.</span></span> <span data-ttu-id="60ce5-110">El tipo de datos intercambiados viene determinado por la aplicación de servidor que proporciona los datos y la aplicación cliente que solicita los datos.</span><span class="sxs-lookup"><span data-stu-id="60ce5-110">The type of data exchanged is determined by the server application that supplies the data and the client application that requests the data.</span></span>

<span data-ttu-id="60ce5-111">El servidor llama a la función [**NDdeShareAdd**](nddeshareadd.md) para crear el recurso compartido DDE, que se almacena en el administrador de bases de datos de recursos compartidos DDE (DSDM).</span><span class="sxs-lookup"><span data-stu-id="60ce5-111">The server calls the [**NDdeShareAdd**](nddeshareadd.md) function to create the DDE share, which is stored in the DDE share database manager (DSDM).</span></span>

<span data-ttu-id="60ce5-112">El cliente inicia la conversación DDE conectándose al recurso compartido DDE.</span><span class="sxs-lookup"><span data-stu-id="60ce5-112">The client starts the DDE conversation by connecting to the DDE share.</span></span> <span data-ttu-id="60ce5-113">El cliente debe llamar a la función [**DdeInitialize**](/windows/win32/api/ddeml/nf-ddeml-ddeinitializea) para inicializar ddeml y llamar a la función [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) para conectarse al recurso compartido DDE.</span><span class="sxs-lookup"><span data-stu-id="60ce5-113">The client must call the [**DdeInitialize**](/windows/win32/api/ddeml/nf-ddeml-ddeinitializea) function to initialize DDEML and call the [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) function to connect to the DDE share.</span></span> <span data-ttu-id="60ce5-114">En la llamada a **DdeConnect** , el cliente especifica el nombre del servicio como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="60ce5-114">In the **DdeConnect** call, the client specifies the service name as follows:</span></span>

<span data-ttu-id="60ce5-115">\\\\*Nombre del equipo* \\ NDDE $</span><span class="sxs-lookup"><span data-stu-id="60ce5-115">\\\\*ComputerName*\\NDDE$</span></span>

<span data-ttu-id="60ce5-116">donde *ComputerName* es el nombre del equipo que ejecuta la aplicación de servidor.</span><span class="sxs-lookup"><span data-stu-id="60ce5-116">where *ComputerName* is the name of the computer running the server application.</span></span> <span data-ttu-id="60ce5-117">NDDE $ indica que el tema proporcionado a [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) es el nombre del recurso compartido DDE en el equipo remoto denominado *NombreDeEquipo*.</span><span class="sxs-lookup"><span data-stu-id="60ce5-117">The NDDE$ indicates that the topic provided to [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) is the DDE share name on the remote computer named *ComputerName*.</span></span>

<span data-ttu-id="60ce5-118">Hay tres tipos de recursos compartidos DDE: antiguo, estilo nuevo y estático.</span><span class="sxs-lookup"><span data-stu-id="60ce5-118">There are three types of DDE shares: old style, new style, and static.</span></span> <span data-ttu-id="60ce5-119">Es habitual solo admitir el tipo estático.</span><span class="sxs-lookup"><span data-stu-id="60ce5-119">It is typical to support only the static type.</span></span> <span data-ttu-id="60ce5-120">Los nombres de los recursos compartidos estáticos usan la Convención siguiente: *ShareName*$.</span><span class="sxs-lookup"><span data-stu-id="60ce5-120">The names of static shares use the following convention: *ShareName*$.</span></span>

 

 
