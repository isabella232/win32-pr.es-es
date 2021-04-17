---
description: Cuando establece un nivel de autenticación para una aplicación, determina el grado de autenticación que se realiza cuando los clientes realizan una llamada a la aplicación.
ms.assetid: a59935de-6b8f-4c0a-8479-e30bc0509698
title: Establecer un nivel de autenticación para una aplicación de servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83450b3f8d1939d08cc3d16a21f438c8da6f8fc1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705319"
---
# <a name="setting-an-authentication-level-for-a-server-application"></a><span data-ttu-id="c4ec9-103">Establecer un nivel de autenticación para una aplicación de servidor</span><span class="sxs-lookup"><span data-stu-id="c4ec9-103">Setting an Authentication Level for a Server Application</span></span>

<span data-ttu-id="c4ec9-104">Cuando establece un nivel de autenticación para una aplicación, determina el grado de autenticación que se realiza cuando los clientes realizan una llamada a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c4ec9-104">When you set an authentication level for an application, you determine what degree of authentication is performed when clients call into the application.</span></span> <span data-ttu-id="c4ec9-105">Los niveles de autenticación más altos proporcionan mayor seguridad e integridad de los datos, aunque normalmente con cierta degradación del rendimiento.</span><span class="sxs-lookup"><span data-stu-id="c4ec9-105">Higher authentication levels provide greater security and data integrity, although usually with some performance degradation.</span></span> <span data-ttu-id="c4ec9-106">Para obtener más información, consulte [autenticación del cliente](client-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="c4ec9-106">For more information, see [Client Authentication](client-authentication.md).</span></span>

<span data-ttu-id="c4ec9-107">**Para seleccionar un nivel de autenticación para una aplicación de servidor**</span><span class="sxs-lookup"><span data-stu-id="c4ec9-107">**To select an authentication level for a server application**</span></span>

1.  <span data-ttu-id="c4ec9-108">Haga clic con el botón secundario en la aplicación COM+ para la que está configurando la autenticación y, a continuación, haga clic en **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="c4ec9-108">Right-click the COM+ application for which you are setting authentication, and then click **Properties**.</span></span>

2.  <span data-ttu-id="c4ec9-109">En el cuadro de diálogo Propiedades de la aplicación, haga clic en la pestaña **seguridad** .</span><span class="sxs-lookup"><span data-stu-id="c4ec9-109">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="c4ec9-110">En el cuadro **nivel de autenticación para llamadas** , seleccione el nivel adecuado.</span><span class="sxs-lookup"><span data-stu-id="c4ec9-110">In the **Authentication level for calls** box, select the appropriate level.</span></span> <span data-ttu-id="c4ec9-111">Los niveles son los siguientes, ordenados de menor a mayor seguridad:</span><span class="sxs-lookup"><span data-stu-id="c4ec9-111">The levels are as follows, ordered from lowest to highest security:</span></span>

    -   <span data-ttu-id="c4ec9-112">**No**.</span><span class="sxs-lookup"><span data-stu-id="c4ec9-112">**None**.</span></span> <span data-ttu-id="c4ec9-113">no se realiza ninguna autenticación.</span><span class="sxs-lookup"><span data-stu-id="c4ec9-113">No authentication occurs.</span></span>
    -   <span data-ttu-id="c4ec9-114">**Conéctese**.</span><span class="sxs-lookup"><span data-stu-id="c4ec9-114">**Connect**.</span></span> <span data-ttu-id="c4ec9-115">Autentica las credenciales solo cuando la conexión está establecida.</span><span class="sxs-lookup"><span data-stu-id="c4ec9-115">Authenticates credentials only when the connection is made.</span></span>
    -   <span data-ttu-id="c4ec9-116">**Llame a**.</span><span class="sxs-lookup"><span data-stu-id="c4ec9-116">**Call**.</span></span> <span data-ttu-id="c4ec9-117">Autentica las credenciales al principio de cada llamada.</span><span class="sxs-lookup"><span data-stu-id="c4ec9-117">Authenticates credentials at the beginning of every call.</span></span>
    -   <span data-ttu-id="c4ec9-118">**Paquete**.</span><span class="sxs-lookup"><span data-stu-id="c4ec9-118">**Packet**.</span></span> <span data-ttu-id="c4ec9-119">Realiza autenticación de las credenciales y comprueba si todos los datos de la llamada se han recibido.</span><span class="sxs-lookup"><span data-stu-id="c4ec9-119">Authenticates credentials and verifies that all call data is received.</span></span> <span data-ttu-id="c4ec9-120">Ésta es la configuración predeterminada para las aplicaciones de servidor COM+.</span><span class="sxs-lookup"><span data-stu-id="c4ec9-120">This is the default setting for COM+ server applications.</span></span>
    -   <span data-ttu-id="c4ec9-121">**Integridad del paquete**.</span><span class="sxs-lookup"><span data-stu-id="c4ec9-121">**Packet Integrity**.</span></span> <span data-ttu-id="c4ec9-122">Realiza la autenticación de las credenciales y comprueba si algún dato de la llamada se ha modificado durante la transmisión.</span><span class="sxs-lookup"><span data-stu-id="c4ec9-122">Authenticates credentials and verifies that no call data has been modified in transit.</span></span>
    -   <span data-ttu-id="c4ec9-123">**Privacidad de paquetes**.</span><span class="sxs-lookup"><span data-stu-id="c4ec9-123">**Packet Privacy**.</span></span> <span data-ttu-id="c4ec9-124">Realiza autenticación de credenciales y cifra el paquete, incluidos los datos y la identidad y firma del remitente.</span><span class="sxs-lookup"><span data-stu-id="c4ec9-124">Authenticates credentials and encrypts the packet, including the data and the sender's identity and signature.</span></span>

4.  <span data-ttu-id="c4ec9-125">Haga clic en **OK**.</span><span class="sxs-lookup"><span data-stu-id="c4ec9-125">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4ec9-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c4ec9-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4ec9-127">Habilitar la autenticación para una aplicación de biblioteca</span><span class="sxs-lookup"><span data-stu-id="c4ec9-127">Enabling Authentication for a Library Application</span></span>](enabling-authentication-for-a-library-application.md)
</dt> </dl>

 

 



