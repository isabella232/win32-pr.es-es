---
title: Usuario especificado
description: Usuario especificado
ms.assetid: ec7684fb-a9f1-4ef2-a7d4-07caf24b6023
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acce63aa502a8966cd0eb53c90dcca3c4454e80b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704610"
---
# <a name="specified-user"></a><span data-ttu-id="75648-103">Usuario especificado</span><span class="sxs-lookup"><span data-stu-id="75648-103">Specified User</span></span>

<span data-ttu-id="75648-104">Especificar un usuario determinado (y la contraseña del usuario) es la identidad preferida para los servidores COM.</span><span class="sxs-lookup"><span data-stu-id="75648-104">Specifying a particular user (and the user's password) is the preferred identity for COM servers.</span></span> <span data-ttu-id="75648-105">La razón por la que se prefiere esta identidad es que no se tiene que registrar ninguna en el equipo en el que se ejecuta el servidor y que cada cliente se comunica con la misma instancia del servidor si el servidor registra su generador de clases como multiuso.</span><span class="sxs-lookup"><span data-stu-id="75648-105">The reason this identity is preferred is that no one has to be logged on the machine where the server is running for the server to run, and every client talks to the same instance of the server if the server registers its class factory as multi-use.</span></span> <span data-ttu-id="75648-106">Si el servidor tiene una GUI, no debe elegir esta identidad; Si lo hace, el usuario no podrá ver la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="75648-106">If the server has a GUI, you should not choose this identity; if you do, the user will not be able to see the user interface.</span></span>

<span data-ttu-id="75648-107">Este tipo de servidor tiene un token principal y puede tener acceso a recursos remotos en los que un servidor que tenga la identidad de inicio-usuario podría no ser capaz de hacerlo.</span><span class="sxs-lookup"><span data-stu-id="75648-107">This type of server has a primary token and can access remote resources where a server that has the launching-user identity might not be able to.</span></span> <span data-ttu-id="75648-108">Para obtener más información sobre la suplantación y los tokens de acceso, vea [niveles de suplantación](impersonation-levels.md) y [ocultación](cloaking.md).</span><span class="sxs-lookup"><span data-stu-id="75648-108">For more information about impersonation and access tokens, see [Impersonation Levels](impersonation-levels.md) and [Cloaking](cloaking.md).</span></span>

<span data-ttu-id="75648-109">Ejecutar como cuenta de usuario fijo es más seguro que la identidad de usuario interactiva, ya que solo alguien que tenga la contraseña de usuario específica puede asignar esta identidad a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="75648-109">Running as a fixed user account is more secure than the interactive user identity because this identity can be assigned to the application only by someone who has the specific user's password.</span></span>

## <a name="related-topics"></a><span data-ttu-id="75648-110">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="75648-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75648-111">Identidad de la aplicación</span><span class="sxs-lookup"><span data-stu-id="75648-111">Application Identity</span></span>](application-identity.md)
</dt> <dt>

[<span data-ttu-id="75648-112">Usuario interactivo</span><span class="sxs-lookup"><span data-stu-id="75648-112">Interactive User</span></span>](interactive-user.md)
</dt> <dt>

[<span data-ttu-id="75648-113">Iniciando usuario</span><span class="sxs-lookup"><span data-stu-id="75648-113">Launching User</span></span>](launching-user.md)
</dt> <dt>

[<span data-ttu-id="75648-114">Identidad de servicio</span><span class="sxs-lookup"><span data-stu-id="75648-114">Service Identity</span></span>](service-identity.md)
</dt> </dl>

 

 




