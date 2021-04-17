---
description: .
ms.assetid: 25d07e42-b5eb-4f72-b4b1-0ebb881644ba
title: Protección de recursos de Windows adicionales en las claves del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb048a45324e52c9b9319f52f95b64361b95bbfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697786"
---
# <a name="additional-windows-resource-protection-on-registry-keys"></a><span data-ttu-id="9d53c-103">Protección de recursos de Windows adicionales en las claves del registro</span><span class="sxs-lookup"><span data-stu-id="9d53c-103">Additional Windows Resource Protection on Registry Keys</span></span>

## <a name="platform"></a><span data-ttu-id="9d53c-104">Plataforma</span><span class="sxs-lookup"><span data-stu-id="9d53c-104">Platform</span></span>

<span data-ttu-id="9d53c-105">**Clientes** : Windows 7</span><span class="sxs-lookup"><span data-stu-id="9d53c-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="9d53c-106">**Servidores** : Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9d53c-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="9d53c-107">Impacto en las características</span><span class="sxs-lookup"><span data-stu-id="9d53c-107">Feature Impact</span></span>

<span data-ttu-id="9d53c-108">**Gravedad** : medio</span><span class="sxs-lookup"><span data-stu-id="9d53c-108">**Severity** - Medium</span></span>  
<span data-ttu-id="9d53c-109">**Frecuencia** : baja</span><span class="sxs-lookup"><span data-stu-id="9d53c-109">**Frequency** - Low</span></span>  


## <a name="description"></a><span data-ttu-id="9d53c-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="9d53c-110">Description</span></span>

<span data-ttu-id="9d53c-111">Los recursos adicionales del sistema han agregado la configuración de Protección de recursos de Windows (WRP) en Windows 7, con lo que se convierte en una configuración de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9d53c-111">Additional system resources have added Windows Resource Protection (WRP) settings in Windows 7, making them read-only settings.</span></span> <span data-ttu-id="9d53c-112">La gran mayoría de los recursos que recibieron protección adicional son claves de servidor COM del sistema, aunque algunas características han agregado protección de recursos de destino.</span><span class="sxs-lookup"><span data-stu-id="9d53c-112">The vast majority of resources that received added protection are system COM server keys, although some features have added targeted resource protection.</span></span> <span data-ttu-id="9d53c-113">Microsoft ha cambiado estos recursos con el fin de proteger el sistema y otras aplicaciones del modo de interrupción y para proporcionar una plataforma coherente y estable en la que las aplicaciones puedan ejecutarse de forma confiable.</span><span class="sxs-lookup"><span data-stu-id="9d53c-113">Microsoft changed these resources in order to protect the system and other applications from breaking each other and to provide a consistent, stable platform upon which applications can reliably run.</span></span> <span data-ttu-id="9d53c-114">En el pasado, las aplicaciones podían proporcionar archivos personalizados y utilizar el registro COM sin protección para cambiar el sistema.</span><span class="sxs-lookup"><span data-stu-id="9d53c-114">In the past, applications could provide custom files and use the unprotected COM registration to change the system.</span></span> <span data-ttu-id="9d53c-115">En el caso de las aplicaciones anteriores, esto puede degradar los tiempos de ejecución del sistema o cambiar la interfaz en la que otras aplicaciones necesitan funcionar correctamente.</span><span class="sxs-lookup"><span data-stu-id="9d53c-115">In the case of older applications, this can downgrade system runtimes or change the interface upon which other applications needed to work properly.</span></span> <span data-ttu-id="9d53c-116">En el peor de los casos, estas instalaciones podrían producir un error o una degradación del sistema a lo largo del tiempo.</span><span class="sxs-lookup"><span data-stu-id="9d53c-116">In the worst case, such installations could cause system failure or degradation over time.</span></span> <span data-ttu-id="9d53c-117">Para proporcionar una mejor experiencia y una plataforma de aplicaciones más estable, bloqueamos estos registros para que solo las actualizaciones de Microsoft pudieran cambiar componentes del sistema.</span><span class="sxs-lookup"><span data-stu-id="9d53c-117">To provide a better experience and a more stable application platform, we locked down these registrations so that only Microsoft updates could change system components.</span></span>

<span data-ttu-id="9d53c-118">Dado que la mayoría de los recursos cambiados son claves COM utilizadas por el sistema, este cambio no afectará a la mayoría de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="9d53c-118">Since most resources changed are COM keys used by the system, this change will not affect the majority of applications.</span></span> <span data-ttu-id="9d53c-119">Aunque esperamos que la mayoría de las aplicaciones tengan una mejor experiencia en Windows 7 como resultado de estos cambios, un pequeño subconjunto de aplicaciones puede verse afectado negativamente.</span><span class="sxs-lookup"><span data-stu-id="9d53c-119">While we expect most applications to have a better experience on Windows 7 as a result of these changes, a small subset of applications may be negatively affected.</span></span> <span data-ttu-id="9d53c-120">Los niveles de compatibilidad de aplicaciones del sistema resolverán automáticamente los problemas de instalación al indicar siempre a la aplicación que se ha cambiado correctamente la configuración, incluso si se ha producido un error debido a que se trata de un recurso protegido.</span><span class="sxs-lookup"><span data-stu-id="9d53c-120">The system's application compatibility layers will automatically resolve setup problems by always telling the application that it succeeded in changing a setting, even if it failed due to it being a protected resource.</span></span> <span data-ttu-id="9d53c-121">Esto evita que se interrumpan las configuraciones de la aplicación, pero puede causar problemas si es necesario cambiar la configuración para que la aplicación funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="9d53c-121">This prevents application setups from breaking but may cause problems if the setting needed to be changed in order for the application to function properly.</span></span>

## <a name="manifestation"></a><span data-ttu-id="9d53c-122">Manifestación</span><span class="sxs-lookup"><span data-stu-id="9d53c-122">Manifestation</span></span>

<span data-ttu-id="9d53c-123">Las aplicaciones pueden haber modificado esta configuración antes de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9d53c-123">Applications may have modified these settings prior to Windows 7.</span></span> <span data-ttu-id="9d53c-124">Tras instalar en Windows 7, las aplicaciones pueden encontrar ciertas características que ya no funcionan porque la configuración no refleja lo que esperaba la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9d53c-124">Upon installing on Windows 7, applications may find certain features no longer work because the settings did not reflect what the application expected.</span></span>

<span data-ttu-id="9d53c-125">Hay dos escenarios en los que las aplicaciones pueden encontrar problemas relacionados con esta protección agregada:</span><span class="sxs-lookup"><span data-stu-id="9d53c-125">There are two scenarios in which applications may encounter problems related to this added protection:</span></span>

-   <span data-ttu-id="9d53c-126">Aplicaciones que pueden haber estado usando la configuración protegida ahora como un almacén de datos o como un punto de extensibilidad poco frecuente o imprevisto</span><span class="sxs-lookup"><span data-stu-id="9d53c-126">Applications that may have been using the now-protected settings as a data store or as a rare or unintended extensibility point</span></span>
-   <span data-ttu-id="9d53c-127">En raras ocasiones, es posible que el mecanismo de detección usado para identificar las configuraciones de la aplicación no reconozca una configuración determinada, por lo que es posible que no se aplique la capa de mitigación de compatibilidad de aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="9d53c-127">In rare cases, the detection mechanism used to identify application setups may not recognize a particular setup and so the application compatibility mitigation layer may not be applied</span></span>

## <a name="mitigation"></a><span data-ttu-id="9d53c-128">Mitigación</span><span class="sxs-lookup"><span data-stu-id="9d53c-128">Mitigation</span></span>

<span data-ttu-id="9d53c-129">El medio principal de mitigación es el nivel de compatibilidad de aplicaciones del sistema, que se aplica automáticamente a las configuraciones de la aplicación cuando se detecta.</span><span class="sxs-lookup"><span data-stu-id="9d53c-129">The primary means of mitigation is the system's application compatibility layer, which is automatically applied to application setups when detected.</span></span> <span data-ttu-id="9d53c-130">También puede aplicarla manualmente a cualquier aplicación mediante la pestaña Compatibilidad en las propiedades de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9d53c-130">You can also manually apply it to any application using the compatibility tab in the application's properties.</span></span>

<span data-ttu-id="9d53c-131">Este nivel resuelve el problema interceptando las operaciones del registro.</span><span class="sxs-lookup"><span data-stu-id="9d53c-131">This layer resolves the problem by intercepting registry operations.</span></span> <span data-ttu-id="9d53c-132">En el caso de que la aplicación estuviera intentando modificar una configuración de solo lectura (WRP), la capa siempre devuelve Success, aunque la configuración no se haya modificado realmente.</span><span class="sxs-lookup"><span data-stu-id="9d53c-132">In the case where the application was attempting to modify a read-only (WRP) setting, the layer always returns success, even though the setting was not really changed.</span></span> <span data-ttu-id="9d53c-133">Para la mayoría de las aplicaciones, esto no provocará problemas.</span><span class="sxs-lookup"><span data-stu-id="9d53c-133">For most applications, this will cause no problems.</span></span> <span data-ttu-id="9d53c-134">Sin embargo, existe la posibilidad de que la aplicación necesite que la configuración haya cambiado para funcionar correctamente, que es el primer escenario descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="9d53c-134">However, there is a possibility that the application needed that setting changed in order to function properly, which is the first scenario described above.</span></span>

## <a name="solution"></a><span data-ttu-id="9d53c-135">Solución</span><span class="sxs-lookup"><span data-stu-id="9d53c-135">Solution</span></span>

<span data-ttu-id="9d53c-136">Para los dos escenarios identificados anteriormente:</span><span class="sxs-lookup"><span data-stu-id="9d53c-136">For the two scenarios identified above:</span></span>

-   <span data-ttu-id="9d53c-137">Si la aplicación requiere la escritura de la clave para poder funcionar o usar el almacén de datos, no hay ninguna solución que no sea cambiar la aplicación para que ya no escriba en esa ubicación.</span><span class="sxs-lookup"><span data-stu-id="9d53c-137">If the application requires the key to be writable in order to function or use the data store, there is no solution other than changing the application so that it no longer writes to that location.</span></span>
-   <span data-ttu-id="9d53c-138">Si el nivel de compatibilidad no se aplicó a una instalación, se debe detectar el error de instalación y se le puede aplicar y volver a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="9d53c-138">If the compatibility layer was not applied to a setup, the setup failure should be detected and offered to be applied and re-run.</span></span> <span data-ttu-id="9d53c-139">Las aplicaciones también se pueden ejecutar en modo de compatibilidad, en cuyo caso siempre se aplica la capa de mitigación.</span><span class="sxs-lookup"><span data-stu-id="9d53c-139">Applications can also run in compatibility mode, in which case the mitigation layer is always applied.</span></span>

## <a name="compatibility-tests"></a><span data-ttu-id="9d53c-140">Pruebas de compatibilidad</span><span class="sxs-lookup"><span data-stu-id="9d53c-140">Compatibility Tests</span></span>

<span data-ttu-id="9d53c-141">Cómo detectar si una aplicación tenía una mitigación de WRP aplicada a ella:</span><span class="sxs-lookup"><span data-stu-id="9d53c-141">How to detect if an application had WRP mitigation applied to it:</span></span>

-   <span data-ttu-id="9d53c-142">Windows Installer es consciente de WRP; omite de forma automática y silenciosa los intentos de escribir o modificar un recurso protegido.</span><span class="sxs-lookup"><span data-stu-id="9d53c-142">Windows Installer is aware of WRP; it automatically and silently ignores attempts to write or modify a protected resource.</span></span> <span data-ttu-id="9d53c-143">Si la aplicación se instaló con Windows Installer y se ha habilitado el registro, se registrará una advertencia para cada operación de escritura de clave del registro que se haya omitido debido a que se trata de un recurso protegido por WRP.</span><span class="sxs-lookup"><span data-stu-id="9d53c-143">If the application was installed with Windows Installer and logging was enabled, then a warning will be logged for each registry key write operation that was ignored due to its being a WRP-protected resource.</span></span>
-   <span data-ttu-id="9d53c-144">La API de WRP incorpora SfCIsKeyProtected, que puede consultar si una clave del registro está protegida por WRP en el sistema actual.</span><span class="sxs-lookup"><span data-stu-id="9d53c-144">The WRP API incorporates SfCIsKeyProtected, which can query if a registry key is WRP-protected on the current system.</span></span> <span data-ttu-id="9d53c-145">Vea la entrada de WRP en MSDN en los vínculos siguientes para obtener información adicional sobre el uso de esta API.</span><span class="sxs-lookup"><span data-stu-id="9d53c-145">See the WRP entry in MSDN in the links below for additional information on using this API.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="9d53c-146">Vínculos a otros recursos</span><span class="sxs-lookup"><span data-stu-id="9d53c-146">Links to Other Resources</span></span>

<dl>

[<span data-ttu-id="9d53c-147">Protección de recursos de Windows</span><span class="sxs-lookup"><span data-stu-id="9d53c-147">Windows Resource Protection</span></span>](/windows/desktop/Wfp/windows-resource-protection-portal)  
</dl>

 

 
