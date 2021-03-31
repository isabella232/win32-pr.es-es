---
title: Desactivación de la seguridad de llamadas
description: 'La seguridad de llamada determina si un cliente tiene permiso para llamar a los métodos de un servidor. Hay dos formas de deshabilitar la seguridad de la llamada: el uso de Dcomcnfg.exe para modificar el registro y el otro requiere llamadas a CoInitializeSecurity.'
ms.assetid: 7ce162d0-20e0-4385-ad9f-472f2c17b060
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a838a9c7936c126a1fedeeafc977f55641b63c5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418475"
---
# <a name="turning-off-call-security"></a><span data-ttu-id="2bf57-104">Desactivación de la seguridad de llamadas</span><span class="sxs-lookup"><span data-stu-id="2bf57-104">Turning Off Call Security</span></span>

<span data-ttu-id="2bf57-105">La seguridad de llamada determina si un cliente tiene permiso para llamar a los métodos de un servidor.</span><span class="sxs-lookup"><span data-stu-id="2bf57-105">Call security determines whether a client has permission to call a server's methods.</span></span> <span data-ttu-id="2bf57-106">Hay dos formas de deshabilitar la seguridad de llamada: una implica el uso de Dcomcnfg.exe para modificar el registro y la otra requiere llamadas a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="2bf57-106">There are two ways to disable call security: One involves using Dcomcnfg.exe to modify the registry, and the other requires calls to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>

-   [<span data-ttu-id="2bf57-107">Desactivar la seguridad de llamadas mediante DCOMCNFG</span><span class="sxs-lookup"><span data-stu-id="2bf57-107">Turning Off Call Security Using DCOMCNFG</span></span>](#turning-off-call-security-using-dcomcnfg)
-   [<span data-ttu-id="2bf57-108">Desactivar la seguridad de llamadas mediante programación</span><span class="sxs-lookup"><span data-stu-id="2bf57-108">Turning Off Call Security Programmatically</span></span>](#turning-off-call-security-programmatically)
-   [<span data-ttu-id="2bf57-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2bf57-109">Related topics</span></span>](#related-topics)

## <a name="turning-off-call-security-using-dcomcnfg"></a><span data-ttu-id="2bf57-110">Desactivar la seguridad de llamadas mediante DCOMCNFG</span><span class="sxs-lookup"><span data-stu-id="2bf57-110">Turning Off Call Security Using DCOMCNFG</span></span>

<span data-ttu-id="2bf57-111">La seguridad de llamadas se puede desactivar más fácilmente mediante Dcomcnfg.exe para modificar el registro.</span><span class="sxs-lookup"><span data-stu-id="2bf57-111">Call security can most easily be turned off by using Dcomcnfg.exe to modify the registry.</span></span> <span data-ttu-id="2bf57-112">Sin embargo, el uso de Dcomcnfg.exe para desactivar la seguridad funcionará solo si el cliente y el servidor no llaman a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="2bf57-112">However, using Dcomcnfg.exe to turn security off will work only if both the client and the server do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="2bf57-113">Esto se debe a que cuando se llama a **CoInitializeSecurity** , DCOM omite la configuración del registro y usa en su lugar los valores proporcionados a **CoInitializeSecurity** .</span><span class="sxs-lookup"><span data-stu-id="2bf57-113">This is because when **CoInitializeSecurity** is called, DCOM ignores the registry settings and uses the values supplied to **CoInitializeSecurity** instead.</span></span>

<span data-ttu-id="2bf57-114">Para desactivar la seguridad con Dcomcnfg.exe, tanto el cliente como el servidor deben establecer sus niveles de autenticación en ninguno.</span><span class="sxs-lookup"><span data-stu-id="2bf57-114">To turn off security with Dcomcnfg.exe, both the client and the server must set their Authentication Levels to None.</span></span> <span data-ttu-id="2bf57-115">Se deben completar los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="2bf57-115">The following steps must be completed:</span></span>

1.  <span data-ttu-id="2bf57-116">Ejecute Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="2bf57-116">Run Dcomcnfg.exe.</span></span>
2.  <span data-ttu-id="2bf57-117">En la página **aplicaciones** , seleccione la aplicación que representa el servidor.</span><span class="sxs-lookup"><span data-stu-id="2bf57-117">On the **Applications** page, select the application that represents the server.</span></span> <span data-ttu-id="2bf57-118">Haga clic en el botón **propiedades** (o haga doble clic en la aplicación seleccionada).</span><span class="sxs-lookup"><span data-stu-id="2bf57-118">Click the **Properties** button (or double-click the selected application).</span></span>
3.  <span data-ttu-id="2bf57-119">Haga clic en la pestaña **General**.</span><span class="sxs-lookup"><span data-stu-id="2bf57-119">Click the **General** tab.</span></span>
4.  <span data-ttu-id="2bf57-120">En el cuadro de lista **nivel de autenticación predeterminado** , seleccione **(ninguno)**.</span><span class="sxs-lookup"><span data-stu-id="2bf57-120">From the **Default Authentication Level** list box, select **(None)**.</span></span>
5.  <span data-ttu-id="2bf57-121">Haga clic en el botón **aplicar** para aplicar los cambios; sin embargo, los cambios no se aplican a las instancias en ejecución de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2bf57-121">Click the **Apply** button to apply changes; however, changes are not applied to any running instances of the application.</span></span>
6.  <span data-ttu-id="2bf57-122">Si el cliente aparece en la lista de la página *aplicaciones* , repita los pasos del 2 al 5 y elija el cliente en lugar del servidor para el paso 2.</span><span class="sxs-lookup"><span data-stu-id="2bf57-122">If the client appears on the list on the *Applications* page, repeat steps 2 through 5, choosing the client instead of the server for step 2.</span></span> <span data-ttu-id="2bf57-123">A continuación, haga clic en el botón **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="2bf57-123">Then click the **OK** button.</span></span> <span data-ttu-id="2bf57-124">Si el cliente no está en la lista, puede realizar una de estas tres acciones:</span><span class="sxs-lookup"><span data-stu-id="2bf57-124">If the client is not on the list, you can do one of the following three things:</span></span>
    -   <span data-ttu-id="2bf57-125">Puede establecer el nivel de autenticación del cliente en ninguno en todo el equipo mediante Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="2bf57-125">You can set the client's Authentication Level to None on a computer-wide basis by using Dcomcnfg.exe.</span></span> <span data-ttu-id="2bf57-126">(Vea la advertencia y el procedimiento que se indica a continuación).</span><span class="sxs-lookup"><span data-stu-id="2bf57-126">(See the warning and the procedure below.)</span></span>
    -   <span data-ttu-id="2bf57-127">Puede establecer el nivel de autenticación del cliente en ninguno mediante programación.</span><span class="sxs-lookup"><span data-stu-id="2bf57-127">You can set the client's authentication level to None programmatically.</span></span>
    -   <span data-ttu-id="2bf57-128">Puede crear una clave [AppID](appid-key.md) para que el cliente indique un nivel de autenticación de ninguno.</span><span class="sxs-lookup"><span data-stu-id="2bf57-128">You can create an [AppID](appid-key.md) key for the client to indicate an authentication level of None.</span></span> <span data-ttu-id="2bf57-129">(Consulte [configuración de Process-Wide seguridad a través del registro](setting-processwide-security-through-the-registry.md)).</span><span class="sxs-lookup"><span data-stu-id="2bf57-129">(See [Setting Process-Wide Security Through the Registry](setting-processwide-security-through-the-registry.md).)</span></span>

<span data-ttu-id="2bf57-130">Para establecer el nivel de autenticación en ninguno en todo el equipo:</span><span class="sxs-lookup"><span data-stu-id="2bf57-130">To set the Authentication Level to None on a computer-wide basis:</span></span>

> [!Note]  
> <span data-ttu-id="2bf57-131">Establecer el nivel de autenticación para todo el equipo en ninguno es extremadamente poco seguro.</span><span class="sxs-lookup"><span data-stu-id="2bf57-131">Setting the computer-wide Authentication Level to None is extremely unsecure.</span></span>

 

1.  <span data-ttu-id="2bf57-132">Ejecute Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="2bf57-132">Run Dcomcnfg.exe.</span></span>
2.  <span data-ttu-id="2bf57-133">Elija la pestaña **propiedades predeterminadas** .</span><span class="sxs-lookup"><span data-stu-id="2bf57-133">Choose the **Default Properties** tab.</span></span>
3.  <span data-ttu-id="2bf57-134">En el cuadro de lista **nivel de autenticación predeterminado** , elija **(ninguno)**.</span><span class="sxs-lookup"><span data-stu-id="2bf57-134">From the **Default Authentication Level** list box, choose **(None)**.</span></span>
4.  <span data-ttu-id="2bf57-135">Haga clic en el botón **Aceptar** .</span><span class="sxs-lookup"><span data-stu-id="2bf57-135">Click the **OK** button.</span></span>

## <a name="turning-off-call-security-programmatically"></a><span data-ttu-id="2bf57-136">Desactivar la seguridad de llamadas mediante programación</span><span class="sxs-lookup"><span data-stu-id="2bf57-136">Turning Off Call Security Programmatically</span></span>

<span data-ttu-id="2bf57-137">Para desactivar la seguridad de llamadas mediante programación, tanto el cliente como el servidor deben llamar a **CoInitializeSecurity**, estableciendo el nivel de autenticación en el parámetro *dwAuthnLevel* en el \_ \_ nivel none de autenticación de RPC C \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2bf57-137">To turn call security off programmatically, both the client and the server must call **CoInitializeSecurity**, setting the authentication level in the *dwAuthnLevel* parameter to RPC\_C\_AUTHN\_LEVEL\_NONE.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2bf57-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2bf57-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2bf57-139">Desactivar la seguridad de activación</span><span class="sxs-lookup"><span data-stu-id="2bf57-139">Turning Off Activation Security</span></span>](turning-off-activation-security.md)
</dt> </dl>

 

 




