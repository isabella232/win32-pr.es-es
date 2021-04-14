---
description: Especificar el protocolo de autenticación
ms.assetid: 2f469332-6b3e-475a-9ec6-782e1e445672
title: Especificar el protocolo de autenticación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9bb2ec20df1ec398f32f3a1ee17334c10d9735
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496319"
---
# <a name="specifying-the-authentication-protocol"></a><span data-ttu-id="9c137-103">Especificar el protocolo de autenticación</span><span class="sxs-lookup"><span data-stu-id="9c137-103">Specifying the Authentication Protocol</span></span>

<span data-ttu-id="9c137-104">En función de los requisitos de seguridad de su sitio, puede solicitar que el servicio de componentes en cola Compruebe siempre la identidad de un cliente, nunca para comprobar la identidad de un cliente o comprobar la identidad de un cliente solo si el componente está configurado para requerir la autenticación incluso cuando no se tiene acceso a ella a través de una cola.</span><span class="sxs-lookup"><span data-stu-id="9c137-104">Depending on the security requirements at your site, you can require the queued components service always to verify a client's identity, never to verify a client's identity, or to verify a client's identity only if the component is configured to require authentication even when not accessed through a queue.</span></span>

> [!Note]  
> <span data-ttu-id="9c137-105">Para usar un componente en cola en el modo de grupo de trabajo, el nivel de autenticación debe estar establecido en ninguno.</span><span class="sxs-lookup"><span data-stu-id="9c137-105">In order to use a queued component in workgroup mode, the authentication level must be set to none.</span></span>

 

## <a name="component-services-administrative-tool"></a><span data-ttu-id="9c137-106">Herramienta administrativa Servicios de componentes</span><span class="sxs-lookup"><span data-stu-id="9c137-106">Component Services Administrative Tool</span></span>

<span data-ttu-id="9c137-107">Para especificar el protocolo de autenticación, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="9c137-107">To specify the authentication protocol, use the following steps:</span></span>

1.  <span data-ttu-id="9c137-108">En el árbol de consola de la herramienta administrativa Servicios de componentes, en **servicios de componentes**, abra la carpeta **aplicaciones com+** asociada con el equipo que desea administrar.</span><span class="sxs-lookup"><span data-stu-id="9c137-108">In the console tree of the Component Services administrative tool, under **Component Services**, open the **COM+ Applications** folder associated with the computer you wish to manage.</span></span>

2.  <span data-ttu-id="9c137-109">Haga clic con el botón secundario en la aplicación en cola para la que desea especificar el protocolo de autenticación y, a continuación, haga clic en **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="9c137-109">Right-click the queued application for which you want to specify the authentication protocol, and then click **Properties**.</span></span>

3.  <span data-ttu-id="9c137-110">Seleccione la pestaña **puesta en cola** en el cuadro de diálogo Propiedades.</span><span class="sxs-lookup"><span data-stu-id="9c137-110">Select the **Queuing** tab in the properties dialog.</span></span>

4.  <span data-ttu-id="9c137-111">En **autenticación de mensajes de MSMQ**, seleccione el botón de radio asociado al Protocolo de autenticación que desea implementar.</span><span class="sxs-lookup"><span data-stu-id="9c137-111">Under **MSMQ Message Authentication**, select the radio button associated with the authentication protocol you want to implement.</span></span>

5.  <span data-ttu-id="9c137-112">Haga clic en **OK**.</span><span class="sxs-lookup"><span data-stu-id="9c137-112">Click **OK**.</span></span>

## <a name="visual-basic"></a><span data-ttu-id="9c137-113">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="9c137-113">Visual Basic</span></span>

<span data-ttu-id="9c137-114">Use el parámetro *AuthLevel* al activar la aplicación en cola como se describe en el [moniker](using-the-queue-moniker.md)de la cola.</span><span class="sxs-lookup"><span data-stu-id="9c137-114">Use the *AuthLevel* parameter when activating the queued application as described in the [Using the Queue Moniker](using-the-queue-moniker.md).</span></span>

## <a name="cc"></a><span data-ttu-id="9c137-115">C/C++</span><span class="sxs-lookup"><span data-stu-id="9c137-115">C/C++</span></span>

<span data-ttu-id="9c137-116">Use el parámetro *AuthLevel* al activar la aplicación en cola como se describe en el [moniker](using-the-queue-moniker.md)de la cola.</span><span class="sxs-lookup"><span data-stu-id="9c137-116">Use the *AuthLevel* parameter when activating the queued application as described in the [Using the Queue Moniker](using-the-queue-moniker.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c137-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9c137-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c137-118">Seguridad de componentes en cola</span><span class="sxs-lookup"><span data-stu-id="9c137-118">Queued Components Security</span></span>](queued-components-security.md)
</dt> <dt>

[<span data-ttu-id="9c137-119">Limitaciones de seguridad en el modo de grupo de trabajo</span><span class="sxs-lookup"><span data-stu-id="9c137-119">Security Limitations in Workgroup Mode</span></span>](security-limitations-in-workgroup-mode.md)
</dt> </dl>

 

 



