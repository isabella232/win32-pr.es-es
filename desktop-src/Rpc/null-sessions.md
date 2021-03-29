---
title: Sesiones nulas
description: A veces, una llamada que llega a la sesión nula puede aparecer como una llamada autenticada.
ms.assetid: 5d113d20-c7af-4fb3-ba17-d0715671f290
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68fe0542d86dd2e6b903a08834293d6cc2f09828
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486991"
---
# <a name="null-sessions"></a><span data-ttu-id="fd370-103">Sesiones nulas</span><span class="sxs-lookup"><span data-stu-id="fd370-103">Null Sessions</span></span>

<span data-ttu-id="fd370-104">A veces, una llamada que llega a la sesión nula puede aparecer como una llamada autenticada.</span><span class="sxs-lookup"><span data-stu-id="fd370-104">Sometimes a call arriving on the null session can appear like an authenticated call.</span></span> <span data-ttu-id="fd370-105">Concretamente, al llamar a la función [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) se devuelve el nivel de autenticación y el proveedor de seguridad utilizados para la llamada.</span><span class="sxs-lookup"><span data-stu-id="fd370-105">Specifically, calling the [**RpcBindingInqAuthClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient) function returns the authentication level and security provider used for the call.</span></span> <span data-ttu-id="fd370-106">Esta operación no significa que la llamada no estuviera en una sesión nula.</span><span class="sxs-lookup"><span data-stu-id="fd370-106">This operation does not mean the call was not on a null session.</span></span> <span data-ttu-id="fd370-107">Los dos problemas son ortogonales.</span><span class="sxs-lookup"><span data-stu-id="fd370-107">The two issues are orthogonal.</span></span> <span data-ttu-id="fd370-108">En Microsoft Windows 2000, una llamada a procedimiento remoto puede intentar suplantar a un llamador y comprobar los permisos después de la suplantación.</span><span class="sxs-lookup"><span data-stu-id="fd370-108">On Microsoft Windows 2000, a remote procedure call can attempt to impersonate a caller and check the permissions after impersonation.</span></span> <span data-ttu-id="fd370-109">En Microsoft Windows XP, es más rápido llamar a la función [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) y comprobar la marca **NullSession** .</span><span class="sxs-lookup"><span data-stu-id="fd370-109">On Microsoft Windows XP, it is faster to call the [**RpcServerInqCallAttributes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcserverinqcallattributesa) function and check for the **NullSession** flag.</span></span>

<span data-ttu-id="fd370-110">Existe otra diferencia importante entre Windows 2000 y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fd370-110">Another relevant difference exists between Windows 2000 and Windows XP.</span></span> <span data-ttu-id="fd370-111">Si solo \_ \_ se especifica la marca RPC si se permite la opción permitir \_ \_ solo protección, las llamadas en la sesión nula pasan en Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="fd370-111">If only the RPC\_IF\_ALLOW\_SECURE\_ONLY flag is specified, calls on the null session go through in Windows 2000.</span></span> <span data-ttu-id="fd370-112">En Windows XP, con el ajuste general de la configuración de seguridad predeterminada, cuando se especifica esta marca, se rechazan las llamadas en la sesión nula con acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="fd370-112">In Windows XP, with the general tightening of default security settings, when this flag is specified, calls on the null session are rejected with access denied.</span></span> <span data-ttu-id="fd370-113">Sin embargo, incluso con el \_ uso de la marca RPC si \_ permitir \_ \_ solo protección, RPC no garantiza el nivel de privilegios del usuario que realiza la llamada.</span><span class="sxs-lookup"><span data-stu-id="fd370-113">However, even with the RPC\_IF\_ALLOW\_SECURE\_ONLY flag, RPC does not guarantee the privilege level of the calling user.</span></span> <span data-ttu-id="fd370-114">Todas las comprobaciones de RPC son que el usuario tiene credenciales válidas.</span><span class="sxs-lookup"><span data-stu-id="fd370-114">All RPC checks is that the user has valid credentials.</span></span> <span data-ttu-id="fd370-115">Es posible que el usuario que realiza la llamada esté usando la cuenta invitado u otras cuentas con pocos privilegios.</span><span class="sxs-lookup"><span data-stu-id="fd370-115">It is possible that the calling user is using the guest account or other low privileged accounts.</span></span> <span data-ttu-id="fd370-116">Asegúrese de que el servidor no asuma un privilegio alto una vez que \_ \_ se use RPC si permitir \_ \_ solo protección.</span><span class="sxs-lookup"><span data-stu-id="fd370-116">Make sure the server does not assume high privilege once RPC\_IF\_ALLOW\_SECURE\_ONLY is used.</span></span>

 

 




