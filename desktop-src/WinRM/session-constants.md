---
title: Constantes de sesión
description: Las constantes de sesión en la \_ \_ enumeración WSManSessionFlags especifican la autenticación y otra información para las llamadas a WSMan. createSession o IWSMan createSession que se conectan a un equipo remoto.
ms.assetid: 5df52696-ac2c-42b7-8b0f-99a27b58575b
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8417289a218203dbdaee288ff03096d894f4bd4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714127"
---
# <a name="session-constants"></a><span data-ttu-id="2d96a-103">Constantes de sesión</span><span class="sxs-lookup"><span data-stu-id="2d96a-103">Session Constants</span></span>

<span data-ttu-id="2d96a-104">Las constantes de sesión en la enumeración **\_ \_ WSManSessionFlags** especifican la autenticación y otra información para las llamadas [**WSMan. createSession**](wsman-createsession.md) o [**IWSMan:: createSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) que se conectan a un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="2d96a-104">The session constants in the **\_\_WSManSessionFlags** enumeration specify authentication and other information for [**WSMan.CreateSession**](wsman-createsession.md) or [**IWSMan::CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) calls that connect to a remote computer.</span></span> <span data-ttu-id="2d96a-105">Estas constantes también están estrechamente relacionadas con los modificadores de la herramienta de línea de comandos de **WinRM** .</span><span class="sxs-lookup"><span data-stu-id="2d96a-105">These constants are also closely related to **Winrm** command-line tool switches.</span></span>

## <a name="using-session-constants"></a><span data-ttu-id="2d96a-106">Usar constantes de sesión</span><span class="sxs-lookup"><span data-stu-id="2d96a-106">Using Session Constants</span></span>

<span data-ttu-id="2d96a-107">Puede establecer las marcas de sesión para la llamada a [**WSMan. createSession**](wsman-createsession.md) de dos maneras diferentes.</span><span class="sxs-lookup"><span data-stu-id="2d96a-107">You can set the Session flags for the call to [**WSMan.CreateSession**](wsman-createsession.md) in two different ways.</span></span> <span data-ttu-id="2d96a-108">Una es más corta y más sencilla.</span><span class="sxs-lookup"><span data-stu-id="2d96a-108">One is shorter and simpler.</span></span> <span data-ttu-id="2d96a-109">La forma más larga, como se muestra en el ejemplo siguiente, es ubicar el valor de la marca que desea usar y crear una constante en el script con ese valor.</span><span class="sxs-lookup"><span data-stu-id="2d96a-109">The longer way, as is shown in the following example, is to locate the value of the flag you want to use and create a constant in your script with that value.</span></span> <span data-ttu-id="2d96a-110">A continuación, la constante se usa para establecer el valor del parámetro *iFlags* .</span><span class="sxs-lookup"><span data-stu-id="2d96a-110">Then the constant is used to set the value of the *iFlags* parameter.</span></span>

``` syntax
Const SessionFlagUseNegotiate = 131072
Const SessionFlagCredUserNamePassword = 4096
iFlags = SessionFlagUseNegotiate Or SessionFlagCredUserNamePassword
```

<span data-ttu-id="2d96a-111">La manera recomendada, como se muestra en el ejemplo siguiente, es usar el método de objeto [**WSMan**](wsman.md) asociado a la marca.</span><span class="sxs-lookup"><span data-stu-id="2d96a-111">The recommended way, as shown in the following example, is to use the [**WSMan**](wsman.md) object method associated with the flag.</span></span>

``` syntax
iFlags = Wsman.SessionFlagUseNegotiate Or Wsman.SessionFlagCredUserNamePassword
```

<dl> <dt>

<span data-ttu-id="2d96a-112"><span id="Authentication_Constants"></span><span id="authentication_constants"></span><span id="AUTHENTICATION_CONSTANTS"></span>[**Constantes de autenticación**](authentication-constants.md)</span><span class="sxs-lookup"><span data-stu-id="2d96a-112"><span id="Authentication_Constants"></span><span id="authentication_constants"></span><span id="AUTHENTICATION_CONSTANTS"></span>[**Authentication Constants**](authentication-constants.md)</span></span>
</dt> <dd>

<span data-ttu-id="2d96a-113">Especifique el método de autenticación y cómo administrar los servidores de certificados.</span><span class="sxs-lookup"><span data-stu-id="2d96a-113">Specify the authentication method and how to handle certificate servers.</span></span>

</dd> <dt>

<span data-ttu-id="2d96a-114"><span id="Other_Session_Constants"></span><span id="other_session_constants"></span><span id="OTHER_SESSION_CONSTANTS"></span>[**Otras constantes de sesión**](other-session-constants.md)</span><span class="sxs-lookup"><span data-stu-id="2d96a-114"><span id="Other_Session_Constants"></span><span id="other_session_constants"></span><span id="OTHER_SESSION_CONSTANTS"></span>[**Other Session Constants**](other-session-constants.md)</span></span>
</dt> <dd>

<span data-ttu-id="2d96a-115">Especifique la codificación, el cifrado y el puerto de nombre de entidad de seguridad de servicio.</span><span class="sxs-lookup"><span data-stu-id="2d96a-115">Specify the encoding, encryption, and service principal name port.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="2d96a-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2d96a-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d96a-117">Constantes y enumeraciones de WinRM</span><span class="sxs-lookup"><span data-stu-id="2d96a-117">WinRM Constants and Enumerations</span></span>](winrm-constants-and-enumerations.md)
</dt> <dt>

[<span data-ttu-id="2d96a-118">**WSMan. CreateSession**</span><span class="sxs-lookup"><span data-stu-id="2d96a-118">**WSMan.CreateSession**</span></span>](wsman-createsession.md)
</dt> <dt>

[<span data-ttu-id="2d96a-119">Autenticación para conexiones remotas</span><span class="sxs-lookup"><span data-stu-id="2d96a-119">Authentication for Remote Connections</span></span>](authentication-for-remote-connections.md)
</dt> </dl>

 

 




