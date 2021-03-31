---
title: Pruebas de validación para las tiendas en línea del tipo de incorporación 2
description: En este tema se describen las pruebas que Microsoft realizará para validar la tienda en línea de tipo 2. Microsoft requiere que ejecute estas pruebas antes de enviar una versión candidata para lanzamiento. La tienda en línea debe superar correctamente estas pruebas para que se publiquen.
ms.assetid: 1da51772-9711-4913-b05d-830fabe49da2
keywords:
- Windows Media Player tiendas en línea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beefd0945f9d1a9ae61e61f8be74beada1695baf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418753"
---
# <a name="validation-tests-for-on-boarding-type-2-online-stores"></a><span data-ttu-id="6dbcd-106">Pruebas de validación para las tiendas en línea del tipo de incorporación 2</span><span class="sxs-lookup"><span data-stu-id="6dbcd-106">Validation Tests for On-boarding Type 2 Online Stores</span></span>

<span data-ttu-id="6dbcd-107">En este tema se describen las pruebas que Microsoft realizará para validar la tienda en línea de tipo 2.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-107">This topic describes tests that Microsoft will perform to validate your Type 2 online store.</span></span> <span data-ttu-id="6dbcd-108">Microsoft requiere que ejecute estas pruebas antes de enviar una versión candidata para lanzamiento.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-108">Microsoft requires that you run these tests before you submit a release candidate.</span></span> <span data-ttu-id="6dbcd-109">La tienda en línea debe superar correctamente estas pruebas para que se publiquen.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-109">Your online store must successfully pass these tests to be published.</span></span>

> [!Note]  
> <span data-ttu-id="6dbcd-110">Si su almacén es de tipo 1 en lugar de tipo 2, puede usar este tema como guía para comprender el ámbito de las pruebas de certificación que se trata para los almacenes de tipo 1.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-110">If your store is Type 1 rather than Type 2, you can use this topic as a guideline to understand the scope of the certification testing that is covered for Type 1 stores.</span></span> <span data-ttu-id="6dbcd-111">Para obtener el conjunto completo de pruebas para los almacenes de tipo 1, póngase en contacto con [soporte técnico de Microsoft](https://support.microsoft.com/ph/7763#tab0).</span><span class="sxs-lookup"><span data-stu-id="6dbcd-111">For the complete set of tests for Type 1 stores, contact [Microsoft Support](https://support.microsoft.com/ph/7763#tab0).</span></span>

 

<span data-ttu-id="6dbcd-112">En este tema se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-112">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="6dbcd-113">Lista de comprobación de prueba</span><span class="sxs-lookup"><span data-stu-id="6dbcd-113">Test Checklist</span></span>](#test-checklist)
    -   [<span data-ttu-id="6dbcd-114">Preparación de prueba superada</span><span class="sxs-lookup"><span data-stu-id="6dbcd-114">Test Pass Preparation</span></span>](#test-pass-preparation)
-   [<span data-ttu-id="6dbcd-115">Entorno de prueba</span><span class="sxs-lookup"><span data-stu-id="6dbcd-115">Test Environment</span></span>](#test-environment)
-   [<span data-ttu-id="6dbcd-116">Instalación y configuración</span><span class="sxs-lookup"><span data-stu-id="6dbcd-116">Configuration and Setup</span></span>](#configuration-and-setup)
    -   [<span data-ttu-id="6dbcd-117">Configuración de una máquina de pruebas</span><span class="sxs-lookup"><span data-stu-id="6dbcd-117">Setting Up a Test Machine</span></span>](#setting-up-a-test-machine)
    -   [<span data-ttu-id="6dbcd-118">Configuración de un almacén</span><span class="sxs-lookup"><span data-stu-id="6dbcd-118">Setting Up a Store</span></span>](#setting-up-a-store)
    -   [<span data-ttu-id="6dbcd-119">Creación de una cuenta</span><span class="sxs-lookup"><span data-stu-id="6dbcd-119">Creating an Account</span></span>](#creating-an-account)
    -   [<span data-ttu-id="6dbcd-120">Configuración del almacenamiento en caché de credenciales</span><span class="sxs-lookup"><span data-stu-id="6dbcd-120">Setting Up Credential Caching</span></span>](#setting-up-credential-caching)
-   [<span data-ttu-id="6dbcd-121">Adquisición de contenido</span><span class="sxs-lookup"><span data-stu-id="6dbcd-121">Content Acquisition</span></span>](#content-acquisition)
    -   [<span data-ttu-id="6dbcd-122">Contenido de streaming</span><span class="sxs-lookup"><span data-stu-id="6dbcd-122">Streaming Content</span></span>](#streaming-content)
    -   [<span data-ttu-id="6dbcd-123">Obtener contenido</span><span class="sxs-lookup"><span data-stu-id="6dbcd-123">Obtaining Content</span></span>](#obtaining-content)
    -   [<span data-ttu-id="6dbcd-124">Grabar contenido</span><span class="sxs-lookup"><span data-stu-id="6dbcd-124">Burning Content</span></span>](#burning-content)
    -   [<span data-ttu-id="6dbcd-125">Transferir contenido</span><span class="sxs-lookup"><span data-stu-id="6dbcd-125">Transferring Content</span></span>](#transferring-content)
-   [<span data-ttu-id="6dbcd-126">Almacenar características</span><span class="sxs-lookup"><span data-stu-id="6dbcd-126">Store Features</span></span>](#store-features)
    -   [<span data-ttu-id="6dbcd-127">Administrar una cuenta</span><span class="sxs-lookup"><span data-stu-id="6dbcd-127">Managing an Account</span></span>](#managing-an-account)
    -   [<span data-ttu-id="6dbcd-128">Administrar el centro de información</span><span class="sxs-lookup"><span data-stu-id="6dbcd-128">Managing the Info Center</span></span>](#managing-the-info-center)
-   [<span data-ttu-id="6dbcd-129">Interacción de la tienda</span><span class="sxs-lookup"><span data-stu-id="6dbcd-129">Store Interaction</span></span>](#store-interaction)
    -   [<span data-ttu-id="6dbcd-130">Producir en el almacén activo</span><span class="sxs-lookup"><span data-stu-id="6dbcd-130">Yielding to the Active Store</span></span>](#yielding-to-the-active-store)
    -   [<span data-ttu-id="6dbcd-131">Impedir que el almacén probado tome el control en el almacén activo</span><span class="sxs-lookup"><span data-stu-id="6dbcd-131">Preventing the Tested Store From Taking Over the Active Store</span></span>](#preventing-the-tested-store-from-taking-over-the-active-store)
    -   [<span data-ttu-id="6dbcd-132">Acceso a un almacén en modo de High-Contrast</span><span class="sxs-lookup"><span data-stu-id="6dbcd-132">Accessing a Store in High-Contrast Mode</span></span>](#accessing-a-store-in-high-contrast-mode)
    -   [<span data-ttu-id="6dbcd-133">Protección de un almacén</span><span class="sxs-lookup"><span data-stu-id="6dbcd-133">Securing a Store</span></span>](#securing-a-store)

## <a name="test-checklist"></a><span data-ttu-id="6dbcd-134">Lista de comprobación de prueba</span><span class="sxs-lookup"><span data-stu-id="6dbcd-134">Test Checklist</span></span>

<span data-ttu-id="6dbcd-135">Use la lista de comprobación de la siguiente tabla para validar la tienda en línea de tipo 2 que desea incorporar a la placa.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-135">Use the checklist in the following table to validate your Type 2 online store that you wish to bring on board.</span></span>



<span data-ttu-id="6dbcd-136">Prueba</span><span class="sxs-lookup"><span data-stu-id="6dbcd-136">Test</span></span>

<span data-ttu-id="6dbcd-137">Windows XP</span><span class="sxs-lookup"><span data-stu-id="6dbcd-137">Windows XP</span></span>

<span data-ttu-id="6dbcd-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6dbcd-138">Windows Vista</span></span>

<span data-ttu-id="6dbcd-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="6dbcd-139">Windows 7</span></span>

<span data-ttu-id="6dbcd-140">Resultado (Pass/Fail/no aplicable)</span><span class="sxs-lookup"><span data-stu-id="6dbcd-140">Result (pass/fail/not applicable)</span></span>

<span data-ttu-id="6dbcd-141">32</span><span class="sxs-lookup"><span data-stu-id="6dbcd-141">32</span></span>

<span data-ttu-id="6dbcd-142">64</span><span class="sxs-lookup"><span data-stu-id="6dbcd-142">64</span></span>

<span data-ttu-id="6dbcd-143">32</span><span class="sxs-lookup"><span data-stu-id="6dbcd-143">32</span></span>

<span data-ttu-id="6dbcd-144">64</span><span class="sxs-lookup"><span data-stu-id="6dbcd-144">64</span></span>

<span data-ttu-id="6dbcd-145">32</span><span class="sxs-lookup"><span data-stu-id="6dbcd-145">32</span></span>

<span data-ttu-id="6dbcd-146">64</span><span class="sxs-lookup"><span data-stu-id="6dbcd-146">64</span></span>

1. <span data-ttu-id="6dbcd-147">Compruebe que el software se instala.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-147">Verify that software installs.</span></span>

2. <span data-ttu-id="6dbcd-148">Compruebe que se desinstala el software.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-148">Verify that software uninstalls.</span></span>

3. <span data-ttu-id="6dbcd-149">Compruebe que el software no se ejecuta en la bandeja.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-149">Verify that software does not run in the tray.</span></span>

4. <span data-ttu-id="6dbcd-150">Compruebe que funciona la pestaña almacén.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-150">Verify that the store tab operates.</span></span>

5. <span data-ttu-id="6dbcd-151">Compruebe que el almacén tiene una opción para crear una cuenta nueva.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-151">Verify that the store has an option to create a new account.</span></span>

6. <span data-ttu-id="6dbcd-152">Compruebe que la cuenta creada puede iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-152">Verify that the created account can sign in.</span></span>

7. <span data-ttu-id="6dbcd-153">Compruebe que el almacén tiene una opción para guardar la información de usuario.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-153">Verify that the store has an option to save user information.</span></span>

8. <span data-ttu-id="6dbcd-154">Compruebe que el almacenamiento en caché de credenciales está presente y en funcionamiento.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-154">Verify that credential caching is present and working.</span></span>

9. <span data-ttu-id="6dbcd-155">Compruebe que al usuario se le piden las credenciales si no están almacenadas en caché.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-155">Verify that the user is prompted for credentials if they are not cached.</span></span>

10. <span data-ttu-id="6dbcd-156">Compruebe que todos los tipos disponibles de flujo de contenido.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-156">Verify that all available types of content stream.</span></span>

11. <span data-ttu-id="6dbcd-157">Compruebe que el contenido se reproduce en Microsoft Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-157">Verify that content plays in Microsoft Windows Media Player.</span></span>

12. <span data-ttu-id="6dbcd-158">Compruebe que el precio calculado es correcto.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-158">Verify that a calculated price is correct.</span></span>

13. <span data-ttu-id="6dbcd-159">Compruebe que el contenido adquirido se descarga en la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-159">Verify that purchased content is downloaded to the library.</span></span>

14. <span data-ttu-id="6dbcd-160">Compruebe que se han descargado los metadatos de la compra.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-160">Verify that metadata is downloaded for the purchase.</span></span>

15. <span data-ttu-id="6dbcd-161">Compruebe que los derechos de uso de medios sean correctos para la compra.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-161">Verify that media usage rights are correct for the purchase.</span></span>

16. <span data-ttu-id="6dbcd-162">Compruebe que el contenido adquirido puede reproducirse.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-162">Verify that the purchased content can play.</span></span>

17. <span data-ttu-id="6dbcd-163">Compruebe que al hacer  clic en **el botón comprar o comprar,** se cambia a la tienda.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-163">Verify that clicking the **Buy** or **Shop** button switches to the store.</span></span>

18. <span data-ttu-id="6dbcd-164">Compruebe que se ha descargado el contenido adquirido.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-164">Verify that purchased content downloaded.</span></span>

19. <span data-ttu-id="6dbcd-165">Compruebe que se puede grabar el contenido adquirido.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-165">Verify that purchased content can be burned.</span></span>

20. <span data-ttu-id="6dbcd-166">Compruebe que se reduce el número de grabaciones.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-166">Verify that the burn count is decremented.</span></span>

21. <span data-ttu-id="6dbcd-167">Compruebe que el contenido se puede transferir a otro equipo.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-167">Verify that content can be transferred to another computer.</span></span>

22. <span data-ttu-id="6dbcd-168">Compruebe que el contenido se transfiere a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-168">Verify that content transfers to a device.</span></span>

23. <span data-ttu-id="6dbcd-169">Compruebe que se reduce el número de sincronizaciones.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-169">Verify that the sync count is decremented.</span></span>

24. <span data-ttu-id="6dbcd-170">Compruebe que el historial de compras realiza un seguimiento de las compras anteriores.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-170">Verify that the purchase history tracks prior purchases.</span></span>

25. <span data-ttu-id="6dbcd-171">Compruebe que se puede restaurar una compra anterior.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-171">Verify that a prior purchase can be restored.</span></span>

26. <span data-ttu-id="6dbcd-172">Compruebe la funcionalidad de un almacén para administrar varios equipos.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-172">Verify a store's functionality to manage multiple computers.</span></span>

27. <span data-ttu-id="6dbcd-173">Compruebe que el centro de información está desactivado de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-173">Verify that the Info Center is off by default.</span></span>

28. <span data-ttu-id="6dbcd-174">Compruebe que el centro de información tiene información multimedia en el área de reproducción en curso.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-174">Verify that the Info Center has media information in the now-playing area.</span></span>

29. <span data-ttu-id="6dbcd-175">Compruebe que los vínculos naveguen a la tienda.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-175">Verify that links navigate to the store.</span></span>

30. <span data-ttu-id="6dbcd-176">Compruebe que el almacén probado produce el almacén activo.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-176">Verify that the tested store yields to the active store.</span></span>

31. <span data-ttu-id="6dbcd-177">Compruebe que el almacén probado no asuma el almacén actual.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-177">Verify that the tested store does not take over the current store.</span></span>

32. <span data-ttu-id="6dbcd-178">Compruebe que el almacén es accesible en el modo de alto contraste.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-178">Verify that the store is accessible in high-contrast mode.</span></span>

33. <span data-ttu-id="6dbcd-179">Compruebe que el almacén es seguro.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-179">Verify that the store is secure.</span></span>



 

### <a name="test-pass-preparation"></a><span data-ttu-id="6dbcd-180">Preparación de prueba superada</span><span class="sxs-lookup"><span data-stu-id="6dbcd-180">Test Pass Preparation</span></span>

<span data-ttu-id="6dbcd-181">Antes de ejecutar una prueba superada, debe asegurarse de que el almacén y las cuentas de prueba están listos para las pruebas.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-181">Before you run a test pass, you should ensure that the store and the test accounts are ready for testing.</span></span> <span data-ttu-id="6dbcd-182">Debe determinar la siguiente información antes de que se inicie el paso.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-182">You should determine the following information before the pass starts.</span></span> <span data-ttu-id="6dbcd-183">Si puede determinar la información de algunos días antes de que se supere la prueba, el paso se ejecutará de forma más eficaz.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-183">If you can determine the information some days in advance of the test pass, the pass will run more efficiently.</span></span>

-   <span data-ttu-id="6dbcd-184">Determine la siguiente información acerca de las cuentas de prueba suministradas por el almacén:</span><span class="sxs-lookup"><span data-stu-id="6dbcd-184">Determine the following information about test accounts that are supplied by the store:</span></span>
    -   <span data-ttu-id="6dbcd-185">Las cuentas y las contraseñas funcionan para permitir que un usuario inicie sesión</span><span class="sxs-lookup"><span data-stu-id="6dbcd-185">Accounts and passwords work to allow a user to sign in</span></span>
    -   <span data-ttu-id="6dbcd-186">Las cuentas se financian correctamente y de forma adecuada para cada tipo de modo de negocio que ofrece la tienda</span><span class="sxs-lookup"><span data-stu-id="6dbcd-186">Accounts are correctly and adequately funded for each type of business mode the store offers</span></span>
    -   <span data-ttu-id="6dbcd-187">Las cuentas son válidas para todas las configuraciones regionales que se van a probar o existen cuentas para cada configuración regional si las cuentas no pueden cruzar configuraciones regionales.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-187">Accounts are valid for all locales to be tested, or accounts exist for each locale if accounts cannot cross locales</span></span>
-   <span data-ttu-id="6dbcd-188">Determine las configuraciones regionales que se van a probar.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-188">Determine which locales to test.</span></span>
-   <span data-ttu-id="6dbcd-189">Determine los idiomas que se van a probar.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-189">Determine which languages to test.</span></span>
-   <span data-ttu-id="6dbcd-190">Determine la siguiente información sobre el entorno de prueba:</span><span class="sxs-lookup"><span data-stu-id="6dbcd-190">Determine the following information about the test environment:</span></span>

    -   <span data-ttu-id="6dbcd-191">Tiendas en directo que funcionan con Windows XP, Windows Vista y Windows 7</span><span class="sxs-lookup"><span data-stu-id="6dbcd-191">Live stores that work with Windows XP, Windows Vista, and Windows 7</span></span>
    -   <span data-ttu-id="6dbcd-192">El almacén no activo que se va a probar</span><span class="sxs-lookup"><span data-stu-id="6dbcd-192">The non-live store to test</span></span>
    -   <span data-ttu-id="6dbcd-193">Compruebe que el almacén no activo que se va a probar es visible en todas las versiones del sistema operativo y en todas las versiones de la plataforma Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-193">Verify that the non-live store to test is visible in all versions of the operating system and all versions of the Windows Media Player platform.</span></span>

-   <span data-ttu-id="6dbcd-194">Determine la siguiente información sobre el almacén que se va a probar:</span><span class="sxs-lookup"><span data-stu-id="6dbcd-194">Determine the following information about the store to test:</span></span>

    -   <span data-ttu-id="6dbcd-195">Nombre de almacén</span><span class="sxs-lookup"><span data-stu-id="6dbcd-195">Store name</span></span>
    -   <span data-ttu-id="6dbcd-196">Etiqueta y gráficos del logotipo de la pestaña del almacén esperado</span><span class="sxs-lookup"><span data-stu-id="6dbcd-196">Expected store tab logo graphics and label</span></span>
    -   <span data-ttu-id="6dbcd-197">¿Está el almacén activo para todas las versiones de sistema operativo?</span><span class="sxs-lookup"><span data-stu-id="6dbcd-197">Is the store live for all operating system versions?</span></span>
    -   <span data-ttu-id="6dbcd-198">¿Se trata de una nueva versión del almacén en pruebas?</span><span class="sxs-lookup"><span data-stu-id="6dbcd-198">Is this is a new version of the store under test?</span></span>
    -   <span data-ttu-id="6dbcd-199">¿El almacén en prueba es de tipo 1 o de tipo 2?</span><span class="sxs-lookup"><span data-stu-id="6dbcd-199">Is the store under test a Type 1 or Type 2 store?</span></span>
    -   <span data-ttu-id="6dbcd-200">¿Ha cambiado el tipo de almacén?</span><span class="sxs-lookup"><span data-stu-id="6dbcd-200">Has the store type changed?</span></span>

-   <span data-ttu-id="6dbcd-201">Determine en qué versiones y plataformas de sistema operativo planea probar la tienda.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-201">Determine on which operating system versions and platforms you plan to test the store.</span></span>
-   <span data-ttu-id="6dbcd-202">Determine que el instalador y el complemento funcionan en todas las plataformas y versiones de sistema operativo que se van a probar.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-202">Determine that the installer and plug-in works on all operating system versions and platforms to be tested.</span></span>
-   <span data-ttu-id="6dbcd-203">Determine si es necesario un documento de navegación.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-203">Determine if a navigation document is required.</span></span>
-   <span data-ttu-id="6dbcd-204">Determine la siguiente información sobre los medios que ofrece el almacén:</span><span class="sxs-lookup"><span data-stu-id="6dbcd-204">Determine the following information about the media that the store offers:</span></span>

    -   <span data-ttu-id="6dbcd-205">Formatos</span><span class="sxs-lookup"><span data-stu-id="6dbcd-205">Formats</span></span>
    -   <span data-ttu-id="6dbcd-206">¿Se requiere software de propiedad?</span><span class="sxs-lookup"><span data-stu-id="6dbcd-206">Is any proprietary software required?</span></span>
    -   <span data-ttu-id="6dbcd-207">¿Debe probar todos los tipos de medios o solo un subconjunto de tipos de medios?</span><span class="sxs-lookup"><span data-stu-id="6dbcd-207">Must you test all media types, or only a subset of media types?</span></span>

-   <span data-ttu-id="6dbcd-208">Determine la siguiente información sobre los derechos de uso de medios:</span><span class="sxs-lookup"><span data-stu-id="6dbcd-208">Determine the following information about media usage rights:</span></span>

    -   <span data-ttu-id="6dbcd-209">¿Los medios de almacenamiento tienen protección de contenido?</span><span class="sxs-lookup"><span data-stu-id="6dbcd-209">Does the store media have content protection?</span></span>
    -   <span data-ttu-id="6dbcd-210">Si es así, determine el tipo de protección de contenido que tienen los medios.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-210">If so, determine the type of content protection that the media have.</span></span>
    -   <span data-ttu-id="6dbcd-211">Si es así, determine el comportamiento protegido esperado.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-211">If so, determine the expected protected behavior.</span></span>
    -   <span data-ttu-id="6dbcd-212">¿Los derechos de uso de medios incluyen el uso compartido de equipos a equipos?</span><span class="sxs-lookup"><span data-stu-id="6dbcd-212">Do the media usage rights include computer-to-computer sharing?</span></span>
    -   <span data-ttu-id="6dbcd-213">Derechos de sincronización</span><span class="sxs-lookup"><span data-stu-id="6dbcd-213">The sync rights</span></span>
    -   <span data-ttu-id="6dbcd-214">Los derechos de grabación</span><span class="sxs-lookup"><span data-stu-id="6dbcd-214">The burn rights</span></span>
    -   <span data-ttu-id="6dbcd-215">Los derechos de reproducción</span><span class="sxs-lookup"><span data-stu-id="6dbcd-215">The play rights</span></span>
    -   <span data-ttu-id="6dbcd-216">Fechas de expiración, si las hay.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-216">The expiration dates, if any</span></span>

-   <span data-ttu-id="6dbcd-217">Determine si dispone de medios suficientes (un catálogo suficientemente grande) para proporcionar un ejemplo significativo.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-217">Determine if you have sufficient media (a large enough catalog) to provide a meaningful sample.</span></span>
-   <span data-ttu-id="6dbcd-218">Determine cuál es el paso de la fase: RC 0, cumplimiento, etc.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-218">Determine what the stage pass is: RC 0, compliance, and so on.</span></span>
-   <span data-ttu-id="6dbcd-219">Determine si la prueba superada es un tipo determinado: regresión, humo, etc.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-219">Determine if the test pass is a certain type: regression, smoke, and so on.</span></span>

## <a name="test-environment"></a><span data-ttu-id="6dbcd-220">Entorno de prueba</span><span class="sxs-lookup"><span data-stu-id="6dbcd-220">Test Environment</span></span>

<span data-ttu-id="6dbcd-221">Debe realizar pruebas en las siguientes configuraciones:</span><span class="sxs-lookup"><span data-stu-id="6dbcd-221">You must conduct testing on the following configurations:</span></span>

-   <span data-ttu-id="6dbcd-222">Sistemas operativos de Microsoft Windows Media Player 11 en Windows XP con Service Pack 3 (SP3) 32 y 64 bits</span><span class="sxs-lookup"><span data-stu-id="6dbcd-222">Microsoft Windows Media Player 11 on Windows XP with Service Pack 3 (SP3) 32-bit and 64-bit operating systems</span></span>
-   <span data-ttu-id="6dbcd-223">Sistemas operativos Windows Media Player 11 en Windows Vista 32 y 64 bits (Windows Media Player de 32 bits)</span><span class="sxs-lookup"><span data-stu-id="6dbcd-223">Windows Media Player 11 on Windows Vista 32-bit and 64-bit (32-bit Windows Media Player) operating systems</span></span>
-   <span data-ttu-id="6dbcd-224">Sistemas operativos de Microsoft Windows Media Player 12 en Windows 7 32 y de 64 bits (Windows Media Player de 32 bits)</span><span class="sxs-lookup"><span data-stu-id="6dbcd-224">Microsoft Windows Media Player 12 on Windows 7 32-bit and 64-bit (32-bit Windows Media Player) operating systems</span></span>

<span data-ttu-id="6dbcd-225">Aunque debe realizar pruebas en todas las plataformas y versiones de sistema operativo enumeradas, las versiones de 32 bits de Windows Vista y Windows 7 son las versiones de sistema operativo de destino prioritario.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-225">Although you must perform testing on all the operating system versions and platforms listed, 32-bit versions of Windows Vista and Windows 7 are the priority targeted operating system versions.</span></span> <span data-ttu-id="6dbcd-226">Debe probar la instalación de cualquier software en todas las plataformas.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-226">You must test the installation of any software on all platforms.</span></span>

<span data-ttu-id="6dbcd-227">Las capturas de pantalla de este tema usan un almacén ficticio, Proseware, para demostrar el uso de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-227">Screen shots in this topic use a fictitious store, Proseware, to demonstrate the usage of the user interface.</span></span>

## <a name="configuration-and-setup"></a><span data-ttu-id="6dbcd-228">Instalación y configuración</span><span class="sxs-lookup"><span data-stu-id="6dbcd-228">Configuration and Setup</span></span>

<span data-ttu-id="6dbcd-229">En las secciones siguientes se describe cómo configurar y configurar las pruebas de validación en una tienda en línea de tipo 2.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-229">The following sections describe how to configure and set up validation testing to on-board a Type 2 online store.</span></span>

### <a name="setting-up-a-test-machine"></a><span data-ttu-id="6dbcd-230">Configuración de una máquina de pruebas</span><span class="sxs-lookup"><span data-stu-id="6dbcd-230">Setting Up a Test Machine</span></span>

<span data-ttu-id="6dbcd-231">Realice los pasos siguientes para configurar un equipo de pruebas:</span><span class="sxs-lookup"><span data-stu-id="6dbcd-231">Perform the following steps to set up a test machine:</span></span>

1.  <span data-ttu-id="6dbcd-232">Señale el equipo de prueba a los servidores de prueba de contenido agregando una clave del registro específica del almacén.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-232">Point the test computer to content test servers by adding a store-specific registry key.</span></span>
2.  <span data-ttu-id="6dbcd-233">Establezca los valores del cuadro de diálogo Configuración **regional y de idioma** en la configuración regional y de idioma adecuada.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-233">Set values in the **Regional and Language Options** dialog box to the proper language and locale settings.</span></span> <span data-ttu-id="6dbcd-234">Para establecer el idioma, seleccione la pestaña **formatos** y, a continuación, seleccione el idioma en el cuadro combinado **formato actual** .</span><span class="sxs-lookup"><span data-stu-id="6dbcd-234">To set the language, select the **Formats** tab and then select the language from the **Current format** combo box.</span></span> <span data-ttu-id="6dbcd-235">Para establecer la región, seleccione la pestaña **Ubicación** y, a continuación, seleccione la región en el cuadro combinado **ubicación actual** .</span><span class="sxs-lookup"><span data-stu-id="6dbcd-235">To set the region, select the **Location** tab and then select the region from the **Current location** combo box.</span></span> <span data-ttu-id="6dbcd-236">Además, en el caso de los almacenes que requieran la instalación de un complemento o un software personalizado específico del almacén, es posible que deba cambiar la configuración regional del sistema al idioma de la configuración regional del almacén para facilitar la instalación.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-236">Additionally, for stores that require installation of a plug-in or store-specific custom software, you might need to change the system locale to the language of the store's locale to facilitate installation.</span></span> <span data-ttu-id="6dbcd-237">El instalador de software debe ser compatible con caracteres de byte único y doble y debe ejecutarse en cualquier configuración regional.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-237">The software installer must support both single and double byte characters and must run on any locale.</span></span> <span data-ttu-id="6dbcd-238">Debe probar la configuración regional nativa.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-238">You must test in the native locale.</span></span> <span data-ttu-id="6dbcd-239">Para establecer la configuración regional nativa, abra el cuadro de diálogo **región e idioma** , seleccione la pestaña **administrativo** y, a continuación, haga clic en el botón **Cambiar configuración regional del sistema** como se muestra en la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-239">To set the native locale, open the **Region and Language** dialog box, select the **Administrative** tab, and then click the **Change system locale** button as shown in the following screen shot.</span></span> <span data-ttu-id="6dbcd-240">Al hacer clic en este botón, se muestra el cuadro **de diálogo Configuración de región e idioma** .</span><span class="sxs-lookup"><span data-stu-id="6dbcd-240">Clicking this button displays the **Region and Language Settings** dialog box.</span></span> <span data-ttu-id="6dbcd-241">El cuadro combinado actual de la **configuración regional del sistema** de ese cuadro de diálogo cambia la configuración regional del sistema.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-241">The **Current system locale** combo box in that dialog box changes the system locale.</span></span>

    <span data-ttu-id="6dbcd-242">En las siguientes capturas de pantalla se muestran las pestañas en las que puede establecer la región y el idioma:</span><span class="sxs-lookup"><span data-stu-id="6dbcd-242">The following screen shots show the tabs on which you can set region and language:</span></span>

    ![captura de pantalla del cuadro de diálogo Opciones regionales y de idioma](images/reg-lang-opt.png)

    ![captura de pantalla que muestra cómo cambiar la configuración regional actual del sistema](images/reg-lang-settings.png)

3.  <span data-ttu-id="6dbcd-245">Desactive la vista del centro de información de un almacén estableciendo Windows Media Player para reproducir una visualización.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-245">Turn off the view of a store's Info Center by setting Windows Media Player to play a visualization.</span></span> <span data-ttu-id="6dbcd-246">La diferencia principal entre las plataformas es que en Windows Media Player 11, para empezar, haga clic en **reproducción** en curso, mientras que en Windows Media Player 12, haga clic con el botón secundario en la ventana principal.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-246">The main difference between the platforms is that in Windows Media Player 11, you start by clicking **Now Playing**, whereas in Windows Media Player 12, you start by right-clicking the main window.</span></span>

    <span data-ttu-id="6dbcd-247">En la captura de pantalla siguiente se muestra la secuencia de opciones de menú que reproduce una visualización en Windows Media Player 11:</span><span class="sxs-lookup"><span data-stu-id="6dbcd-247">The following screen shot shows the sequence of menu options that plays a visualization in Windows Media Player 11:</span></span>

    ![captura de pantalla que muestra cómo reproducir una visualización en el reproductor de Windows Media 11](images/wmp11-visual.png)

    <span data-ttu-id="6dbcd-249">En la captura de pantalla siguiente se muestra la secuencia de opciones de menú que reproduce una visualización en Windows Media Player 12:</span><span class="sxs-lookup"><span data-stu-id="6dbcd-249">The following screen shot shows the sequence of menu options that plays a visualization in Windows Media Player 12:</span></span>

    ![captura de pantalla que muestra cómo reproducir una visualización en el reproductor de Windows Media 12](images/wmp12-visual.png)

### <a name="setting-up-a-store"></a><span data-ttu-id="6dbcd-251">Configuración de un almacén</span><span class="sxs-lookup"><span data-stu-id="6dbcd-251">Setting Up a Store</span></span>

<span data-ttu-id="6dbcd-252">En primer lugar, realice los pasos siguientes para configurar un almacén y, a continuación, siga los pasos iniciales para comprobar la configuración del almacén:</span><span class="sxs-lookup"><span data-stu-id="6dbcd-252">First perform the following steps to set up a store, and then perform the steps that follow the initial steps to verify the store setup:</span></span>

1.  <span data-ttu-id="6dbcd-253">Inicie Windows Media Player y espere unos segundos para adquirir el archivo de AllServices.xml más reciente.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-253">Launch Windows Media Player and wait several seconds to acquire the latest AllServices.xml file.</span></span>
2.  <span data-ttu-id="6dbcd-254">En Windows XP y Windows Vista, para seleccionar una tienda en línea, primero haga clic en la pestaña que se divide entre la vista de la guía multimedia y la vista de tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-254">For Windows XP and Windows Vista, to select an online store, first click the tab that splits between the Media Guide view and the Online Stores view.</span></span> <span data-ttu-id="6dbcd-255">A continuación, en el menú, haga clic en **examinar todas las tiendas en línea** y seleccione la tienda haciendo clic en su icono en la lista de tiendas.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-255">Then, from the menu click **Browse all Online Stores**, and select the store by clicking its icon in the list of stores.</span></span> <span data-ttu-id="6dbcd-256">En Windows 7, haga clic en el botón del panel de navegación biblioteca que se divide entre el botón **guía multimedia** y el botón **tiendas en línea** .</span><span class="sxs-lookup"><span data-stu-id="6dbcd-256">For Windows 7, click the button in the library-navigation pane that splits between the **Media Guide** button and the **Online Stores** button.</span></span> <span data-ttu-id="6dbcd-257">A continuación, en el menú, haga clic en **examinar todas las tiendas en línea** y seleccione la tienda haciendo clic en su icono en la lista de tiendas.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-257">Then, from the menu click **Browse all online stores**, and select the store by clicking its icon in the list of stores.</span></span>

    <span data-ttu-id="6dbcd-258">En la captura de pantalla siguiente se muestra cómo seleccionar una tienda en línea en Windows Media Player 11:</span><span class="sxs-lookup"><span data-stu-id="6dbcd-258">The following screen shot shows how to select an online store in Windows Media Player 11:</span></span>

    ![captura de pantalla que muestra cómo seleccionar una tienda en línea en el reproductor de Windows Media 11](images/wmp11-set-store.png)

    <span data-ttu-id="6dbcd-260">En la captura de pantalla siguiente se muestra cómo seleccionar una tienda en línea en Windows Media Player 12:</span><span class="sxs-lookup"><span data-stu-id="6dbcd-260">The following screen shot shows how to select an Online Store in Windows Media Player 12:</span></span>

    ![captura de pantalla que muestra cómo seleccionar una tienda en línea en el reproductor de Windows Media 12](images/wmp12-set-store.png)

3.  <span data-ttu-id="6dbcd-262">Siga las instrucciones de la tienda para instalar cualquier software adicional que sea necesario para usar el almacén.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-262">Follow instructions from the store to install any additional software that is needed to use the store.</span></span>

<span data-ttu-id="6dbcd-263">**Para comprobar la configuración del almacén**</span><span class="sxs-lookup"><span data-stu-id="6dbcd-263">**To verify store setup**</span></span>

1.  <span data-ttu-id="6dbcd-264">Compruebe que el software se instala.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-264">Verify that the software installs.</span></span>

    <span data-ttu-id="6dbcd-265">Compruebe que el complemento OCX o cualquier otro software de la tienda se descargue e instale sin errores.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-265">Verify that the OCX plug-in or any other software from the store downloads and installs without error.</span></span>

2.  <span data-ttu-id="6dbcd-266">Compruebe que el software se desinstala.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-266">Verify that the software uninstalls.</span></span>

    <span data-ttu-id="6dbcd-267">Compruebe que en el panel de control, en el elemento **programas y características** , aparece el software que instala el almacén en la lista **desinstalar o cambiar un programa** , y compruebe que puede desinstalarlo de esta lista sin errores.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-267">Verify that in Control Panel, in the **Programs and Features** item, the software that the store installs appears in the **Uninstall or change a program** list, and verify that you can uninstall it from this list without error.</span></span>

3.  <span data-ttu-id="6dbcd-268">Compruebe que el software no se ejecuta en la bandeja del sistema.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-268">Verify that software does not run in the system tray.</span></span>

    <span data-ttu-id="6dbcd-269">Compruebe que ningún software del almacén agrega iconos al área de notificación del programa (en la barra de tareas situada a la izquierda del reloj) antes del consentimiento del cliente para descargar el software de la tienda.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-269">Verify that none of the software from the store adds icons to the program notification area (on the Taskbar to the left of the clock) prior to customer consent to download store software.</span></span>

    <span data-ttu-id="6dbcd-270">La experiencia de tienda básica no debe requerir la instalación de software adicional.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-270">The basic store experience should not require installation of additional software.</span></span> <span data-ttu-id="6dbcd-271">Debe haber disponible una experiencia multimedia básica, como la transmisión por secuencias de multimedia.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-271">A basic media experience, such as streaming media, should be available.</span></span> <span data-ttu-id="6dbcd-272">Algunos almacenes instalan software adicional, como los administradores de descargas para una experiencia multimedia Premier. Estos almacenes pueden tener iconos en la bandeja del sistema si los iconos representan aplicaciones independientes de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-272">Some stores install additional software such as download managers for a premier media experience; these stores can have icons in the system tray if the icons represent applications that are separate from Windows Media Player.</span></span>

4.  <span data-ttu-id="6dbcd-273">Compruebe que funciona la pestaña almacén.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-273">Verify that the store tab operates.</span></span>

    <span data-ttu-id="6dbcd-274">Compruebe que la pestaña almacén cambia para indicar el almacén seleccionado.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-274">Verify that the store tab changes to indicate the selected store.</span></span>

    <span data-ttu-id="6dbcd-275">En Windows XP y Windows Vista con Windows Media Player 11, compruebe que el nombre del almacén y el icono están visibles en el fondo de Windows Media Player 11 oscuro.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-275">For Windows XP and Windows Vista with Windows Media Player 11, verify that the store name and icon are visible against the dark Windows Media Player 11 background.</span></span>

    <span data-ttu-id="6dbcd-276">En Windows 7 con Windows Media Player 12, compruebe que el nombre del almacén y el icono están visibles en el panel de navegación biblioteca, en el menú contextual del selector de servicio.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-276">For Windows 7 with Windows Media Player 12, verify the store name and icon are visible in the library-navigation pane, in the service-selector context menu.</span></span>

    <span data-ttu-id="6dbcd-277">Compruebe que la tienda aparece en la parte superior de la lista de selección de almacén en el menú.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-277">Verify that the store is listed at the top of the store selector list in the menu.</span></span>

    > [!Note]  
    > <span data-ttu-id="6dbcd-278">No habrá ninguna opción de **menú Agregar servicio actual a** si el almacén de tipo 2 es el almacén destacado (predeterminado) para la región.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-278">There will be no **Add current service to menu** option if the Type 2 store is the featured (default) store for the region.</span></span>

     

    <span data-ttu-id="6dbcd-279">En la captura de pantalla siguiente se muestra el menú que aparece al hacer clic en la pestaña en la esquina superior derecha de Windows Media Player 11:</span><span class="sxs-lookup"><span data-stu-id="6dbcd-279">The following screen shot shows the menu that appears when you click the tab at the top right corner of Windows Media Player 11:</span></span>

    ![captura de pantalla que muestra la pestaña de almacenamiento en el reproductor de Windows Media 11](images/wmp11-verify-store.png)

    <span data-ttu-id="6dbcd-281">En la captura de pantalla siguiente se muestra el menú que aparece al hacer clic en el botón de expansión situado en la esquina inferior izquierda de Windows Media Player 12:</span><span class="sxs-lookup"><span data-stu-id="6dbcd-281">The following screen shot shows the menu that appears when you click the split button at the lower left corner of Windows Media Player 12:</span></span>

    ![captura de pantalla que muestra la pestaña de almacenamiento en el reproductor de Windows Media 12](images/wmp12-verify-store.png)

### <a name="creating-an-account"></a><span data-ttu-id="6dbcd-283">Creación de una cuenta</span><span class="sxs-lookup"><span data-stu-id="6dbcd-283">Creating an Account</span></span>

<span data-ttu-id="6dbcd-284">**Para comprobar la configuración de la cuenta**</span><span class="sxs-lookup"><span data-stu-id="6dbcd-284">**To verify account setup**</span></span>

1.  <span data-ttu-id="6dbcd-285">Compruebe que la tienda tiene una opción para crear una cuenta nueva y, a continuación, siga las instrucciones de la tienda para crear una cuenta nueva.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-285">Verify that the store has an option to create a new account, and then follow the store instructions to create a new account.</span></span>

    <span data-ttu-id="6dbcd-286">En la siguiente captura de pantalla se resalta un botón **crear nueva cuenta** , como podría aparecer en Windows Media Player 11:</span><span class="sxs-lookup"><span data-stu-id="6dbcd-286">The following screen shot highlights a **Create New Account** button as it might appear in Windows Media Player 11:</span></span>

    ![captura de pantalla que muestra cómo comprobar la configuración de la cuenta del reproductor de Windows Media 11](images/wmp11-verify-account.png)

    <span data-ttu-id="6dbcd-288">En la siguiente captura de pantalla se resalta un botón **crear nueva cuenta** , como podría aparecer en Windows Media Player 12:</span><span class="sxs-lookup"><span data-stu-id="6dbcd-288">The following screen shot highlights a **Create New Account** button as it might appear in Windows Media Player 12:</span></span>

    ![captura de pantalla que muestra cómo comprobar la configuración de la cuenta del reproductor de Windows Media 12](images/wmp12-verify-account.png)

2.  <span data-ttu-id="6dbcd-290">Compruebe que puede iniciar sesión en la cuenta que ha creado.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-290">Verify that you can sign in to the account that you created.</span></span>

### <a name="setting-up-credential-caching"></a><span data-ttu-id="6dbcd-291">Configuración del almacenamiento en caché de credenciales</span><span class="sxs-lookup"><span data-stu-id="6dbcd-291">Setting Up Credential Caching</span></span>

<span data-ttu-id="6dbcd-292">En primer lugar, realice los pasos siguientes para configurar el almacenamiento en caché de las credenciales y, a continuación, siga los pasos iniciales para comprobar la configuración del almacenamiento en caché de credenciales:</span><span class="sxs-lookup"><span data-stu-id="6dbcd-292">First perform the following steps to set up credential caching, and then perform the steps that follow the initial steps to verify the credential-caching setup:</span></span>

1.  <span data-ttu-id="6dbcd-293">En la página de inicio de sesión, escriba las credenciales y seleccione la opción para guardar la información de usuario.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-293">At the sign-in page, enter credentials and select the option to save user information.</span></span>
2.  <span data-ttu-id="6dbcd-294">Compruebe que la página de inicio de sesión tiene una casilla que permite al usuario almacenar en caché las credenciales.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-294">Verify that the sign-in page has a check box that allows the user to cache credentials.</span></span>
3.  <span data-ttu-id="6dbcd-295">El almacenamiento en caché opcional de credenciales es un punto de seguridad importante.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-295">Optional credential caching is an important security point.</span></span> <span data-ttu-id="6dbcd-296">El almacenamiento en caché automático de credenciales puede exponer información de identificación personal de los usuarios que inician sesión en un equipo público o compartido.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-296">Automatic credential caching can expose personally identifiable information of users who sign into a shared or public computer.</span></span> <span data-ttu-id="6dbcd-297">Debe proteger la información del cliente ofreciendo una casilla que representa el almacenamiento en caché opcional.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-297">You should protect customer information by offering a check box that renders the caching optional.</span></span>

<span data-ttu-id="6dbcd-298">**Para comprobar el almacenamiento en caché de credenciales**</span><span class="sxs-lookup"><span data-stu-id="6dbcd-298">**To verify credential caching**</span></span>

1.  <span data-ttu-id="6dbcd-299">Compruebe que la tienda tiene una casilla para la opción **guardar mi información de usuario** .</span><span class="sxs-lookup"><span data-stu-id="6dbcd-299">Verify that the store has a check box for a **Save my user information** option.</span></span>

    1.  <span data-ttu-id="6dbcd-300">Cierre Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-300">Close Windows Media Player.</span></span>
    2.  <span data-ttu-id="6dbcd-301">Vuelva a abrir Windows Media Player e intente descargar el contenido.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-301">Reopen Windows Media Player and attempt to download some content.</span></span>

2.  <span data-ttu-id="6dbcd-302">Compruebe que el almacenamiento en caché de credenciales está presente y en funcionamiento.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-302">Verify that credential caching is present and working.</span></span>

    1.  <span data-ttu-id="6dbcd-303">Cierre la sesión del almacén.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-303">Sign out of the store.</span></span>
    2.  <span data-ttu-id="6dbcd-304">Cierre Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-304">Close Windows Media Player.</span></span>
    3.  <span data-ttu-id="6dbcd-305">Vuelva a abrir Windows Media Player e intente descargar el contenido.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-305">Reopen Windows Media Player and attempt to download some content.</span></span>

3.  <span data-ttu-id="6dbcd-306">Compruebe que al usuario se le piden las credenciales si no están almacenadas en caché.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-306">Verify that the user is prompted for credentials if they are not cached.</span></span>

    <span data-ttu-id="6dbcd-307">Después de cerrar la sesión y tratar de usar el almacén, se le pedirán las credenciales al cliente.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-307">After signing out and then trying to use the store, the customer should be prompted for credentials.</span></span>

## <a name="content-acquisition"></a><span data-ttu-id="6dbcd-308">Adquisición de contenido</span><span class="sxs-lookup"><span data-stu-id="6dbcd-308">Content Acquisition</span></span>

<span data-ttu-id="6dbcd-309">En esta sección se describen las distintas formas de adquirir contenido y de comprobar que se ha adquirido dicho contenido.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-309">This section describes the various ways to acquire content and how to verify that that content was acquired.</span></span>

### <a name="streaming-content"></a><span data-ttu-id="6dbcd-310">Contenido de streaming</span><span class="sxs-lookup"><span data-stu-id="6dbcd-310">Streaming Content</span></span>

<span data-ttu-id="6dbcd-311">Transmita todos los tipos de contenido disponibles desde el almacén.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-311">Stream all available types of content from the store.</span></span> <span data-ttu-id="6dbcd-312">Por ejemplo, transmisión por secuencias de radio, vídeo, audio y versiones preliminares.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-312">For example, stream radio, video, audio, and previews content.</span></span>

<span data-ttu-id="6dbcd-313">**Para comprobar el contenido de streaming**</span><span class="sxs-lookup"><span data-stu-id="6dbcd-313">**To verify streaming content**</span></span>

1.  <span data-ttu-id="6dbcd-314">Compruebe que todos los tipos disponibles de flujo de contenido.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-314">Verify that all available types of content stream.</span></span>

2.  <span data-ttu-id="6dbcd-315">Compruebe que el contenido se reproduce en Windows Media Player y no en otro reproductor o control.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-315">Verify that content plays in Windows Media Player and not some other player or control.</span></span>

### <a name="obtaining-content"></a><span data-ttu-id="6dbcd-316">Obtener contenido</span><span class="sxs-lookup"><span data-stu-id="6dbcd-316">Obtaining Content</span></span>

<span data-ttu-id="6dbcd-317">En primer lugar, realice los pasos siguientes para adquirir contenido y, a continuación, siga los pasos que se indican a continuación para comprobar la compra y comprobar que el contenido se ha descargado:</span><span class="sxs-lookup"><span data-stu-id="6dbcd-317">First perform the following steps to purchase content, and then perform the steps that follow the initial steps to verify the purchase and verify that the content downloaded:</span></span>

1.  <span data-ttu-id="6dbcd-318">Inicie Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-318">Launch Windows Media Player.</span></span>
2.  <span data-ttu-id="6dbcd-319">Inicie sesión en la cuenta de prueba.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-319">Sign in to the test account.</span></span>
3.  <span data-ttu-id="6dbcd-320">Navegue hasta el contenido que desea comprar.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-320">Navigate to the content to purchase.</span></span>
4.  <span data-ttu-id="6dbcd-321">Siga el procedimiento específico del almacén para comprar contenido.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-321">Follow the store-specific procedure to purchase content.</span></span>

<span data-ttu-id="6dbcd-322">**Para comprobar el contenido comprado y descargado**</span><span class="sxs-lookup"><span data-stu-id="6dbcd-322">**To verify purchased and downloaded content**</span></span>

1.  <span data-ttu-id="6dbcd-323">Compruebe que el precio calculado es correcto.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-323">Verify that the calculated price is correct.</span></span>

    <span data-ttu-id="6dbcd-324">Compruebe que el precio es correcto, especialmente cuando compra varios fragmentos de contenido a la vez, y compruebe que la información de saldo de la cuenta se ha actualizado correctamente después de la compra.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-324">Verify that the price is correct, especially when purchasing multiple pieces of content at once, and verify that any account balance information is updated correctly after purchase.</span></span> <span data-ttu-id="6dbcd-325">Algunos contenidos se pueden adquirir como pistas únicas y solo como álbumes.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-325">Some content can be purchased as single tracks and some as albums only.</span></span> <span data-ttu-id="6dbcd-326">Compruebe que el precio del álbum no sea mayor que la suma de las pistas individuales.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-326">Verify that the album price is not larger than the sum of the individual tracks.</span></span>

2.  <span data-ttu-id="6dbcd-327">Compruebe que el contenido adquirido se descarga en la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-327">Verify that the purchased content downloads to the library.</span></span>

    <span data-ttu-id="6dbcd-328">Una vez finalizada la descarga, navegue hasta el contenido descargado en la biblioteca de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-328">When the download completes, navigate to the downloaded content in the Windows Media Player library.</span></span> <span data-ttu-id="6dbcd-329">El contenido descargado se encuentra en la biblioteca del usuario actual.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-329">The downloaded content is located in the current user's library.</span></span>

    -   <span data-ttu-id="6dbcd-330">En Windows XP y Windows Vista con Windows Media Player 11, el contenido descargado aparece en el panel de navegación de la biblioteca, en dinámica de **biblioteca** y, a continuación, en **canciones**.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-330">For Windows XP and Windows Vista with Windows Media Player 11, downloaded content appears in the library navigation pane, under **Library** pivot, and then under **Songs**.</span></span>
    -   <span data-ttu-id="6dbcd-331">En el caso de Windows 7 con Windows Media Player 12, el contenido que se descarga en la biblioteca de Media Player de Windows aparece en el panel de navegación de Windows Media Player bajo **música**.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-331">For Windows 7 with Windows Media Player 12, content that is downloaded to the Windows Media Player library appears in the Windows Media Player navigation pane under **Music**.</span></span>

3.  <span data-ttu-id="6dbcd-332">Compruebe que las descargas de metadatos para la compra.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-332">Verify that metadata downloads for the purchase.</span></span>

    <span data-ttu-id="6dbcd-333">Asegúrese de que las siguientes columnas aparecen en la biblioteca de Media Player de Windows (agréguelas si no):</span><span class="sxs-lookup"><span data-stu-id="6dbcd-333">Ensure that the following columns appear in the Windows Media Player library (add them if not):</span></span>

    -   <span data-ttu-id="6dbcd-334">Intérprete del álbum</span><span class="sxs-lookup"><span data-stu-id="6dbcd-334">Album Artist</span></span>
    -   <span data-ttu-id="6dbcd-335">Title</span><span class="sxs-lookup"><span data-stu-id="6dbcd-335">Title</span></span>
    -   <span data-ttu-id="6dbcd-336">Título del álbum</span><span class="sxs-lookup"><span data-stu-id="6dbcd-336">Album Title</span></span>
    -   <span data-ttu-id="6dbcd-337">Proveedor de contenido</span><span class="sxs-lookup"><span data-stu-id="6dbcd-337">Content Provider</span></span>
    -   <span data-ttu-id="6dbcd-338">Género</span><span class="sxs-lookup"><span data-stu-id="6dbcd-338">Genre</span></span>

    <span data-ttu-id="6dbcd-339">Se deben rellenar las columnas anteriores.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-339">The preceding columns must be populated.</span></span> <span data-ttu-id="6dbcd-340">El contenido debe tener carátulas de álbum.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-340">Content should have album art.</span></span> <span data-ttu-id="6dbcd-341">Sin embargo, no es necesario carátulas de álbum para pasar las pruebas de validación.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-341">However, album art is not required to pass validation testing.</span></span>

4.  <span data-ttu-id="6dbcd-342">Compruebe que los derechos de uso de medios sean correctos para la compra.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-342">Verify that media usage rights are correct for the purchase.</span></span>

    <span data-ttu-id="6dbcd-343">Para cada pista descargada, haga clic con el botón secundario en la pista y seleccione **propiedades** y, a continuación, seleccione la ficha **derechos de uso de medios** .</span><span class="sxs-lookup"><span data-stu-id="6dbcd-343">For each downloaded track, right-click the track and select **Properties**, and then select the **Media Usage Rights** tab.</span></span>

    <span data-ttu-id="6dbcd-344">El almacén puede optar por proteger su contenido con derechos de uso de medios o puede optar por no proteger el contenido.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-344">The store can choose to protect its content with media usage rights, or can choose to not protect the content.</span></span> <span data-ttu-id="6dbcd-345">La pestaña **derechos de uso de medios** refleja ese estado en la lista de restricciones o indicando que el contenido no está protegido.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-345">The **Media Usage Rights** tab reflects that status either by listing the restrictions, or by stating that the content is not protected.</span></span> <span data-ttu-id="6dbcd-346">El almacén debe comunicar su plan más actual para los derechos de uso de medios.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-346">The store must communicate its most current plan for media usage rights.</span></span> <span data-ttu-id="6dbcd-347">Debe comprobar los resultados reales en relación con este comportamiento esperado.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-347">You must verify actual results against this expected behavior.</span></span>

    <span data-ttu-id="6dbcd-348">Las licencias de los derechos multimedia deben entregarse previamente.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-348">Media rights licenses must be pre-delivered.</span></span> <span data-ttu-id="6dbcd-349">El cliente no debe ser necesario para reproducir el contenido o pasar por algún otro proceso para obtener la licencia.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-349">The customer must not be required to play the content or go through some other process to get the license.</span></span> <span data-ttu-id="6dbcd-350">Debe comparar los derechos de uso de medios específicos con lo que el almacén ha comunicado al cliente según corresponda.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-350">You must compare the specific media usage rights to what the store has communicated to the customer as appropriate.</span></span> <span data-ttu-id="6dbcd-351">Los derechos deben transferirse al menos a otros dos equipos.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-351">Rights must be transferable to at least two other computers.</span></span> <span data-ttu-id="6dbcd-352">Los clientes deben poder grabar y sincronizar sus medios.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-352">Customers must be able to burn and synchronize their media.</span></span>

    <span data-ttu-id="6dbcd-353">En la captura de pantalla siguiente se muestran los derechos de uso de medios de un archivo protegido:</span><span class="sxs-lookup"><span data-stu-id="6dbcd-353">The following screen shot shows the media usage rights of a protected file:</span></span>

    ![captura de pantalla que muestra los derechos de uso de medios para un archivo protegido](images/media-rights-protected.png)

    <span data-ttu-id="6dbcd-355">Si el contenido no está protegido, la ficha **derechos de uso de medios** indica este hecho.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-355">If the content is not protected, the **Media Usage Rights** tab indicates this fact.</span></span>

    <span data-ttu-id="6dbcd-356">En la captura de pantalla siguiente se muestran los derechos de uso de medios de un archivo sin protección:</span><span class="sxs-lookup"><span data-stu-id="6dbcd-356">The following screen shot shows the media usage rights of an unprotected file:</span></span>

    ![captura de pantalla que muestra los derechos de uso de medios para un archivo no protegido](images/media-rights-not-protected.png)

5.  <span data-ttu-id="6dbcd-358">Compruebe que el contenido adquirido se reproduzca.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-358">Verify that the purchased content plays.</span></span>

    <span data-ttu-id="6dbcd-359">Compruebe que el contenido descargado se reproduce en Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-359">Verify that downloaded content plays in Windows Media Player.</span></span>

    <span data-ttu-id="6dbcd-360">Reproducir cualquier contenido adquirido en la tienda y que resida en la biblioteca local, o bien transmitir una vista previa.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-360">Play any content that was purchased from the store and that resides in the local library, or stream a preview.</span></span>

    <span data-ttu-id="6dbcd-361">Realice los pasos siguientes para adquirir contenido en Windows XP y Windows Vista con Windows Media Player 11:</span><span class="sxs-lookup"><span data-stu-id="6dbcd-361">Perform the following steps to purchase content in Windows XP and Windows Vista with Windows Media Player 11:</span></span>

    1.  <span data-ttu-id="6dbcd-362">Haga clic en la pestaña **reproducción en curso** .</span><span class="sxs-lookup"><span data-stu-id="6dbcd-362">Click the **Now Playing** tab.</span></span>
    2.  <span data-ttu-id="6dbcd-363">En el panel lista, coloque el puntero del mouse para desplazarse sobre las carátulas de álbum con el fin de mostrar el vínculo **comprar** .</span><span class="sxs-lookup"><span data-stu-id="6dbcd-363">In the list pane, position the mouse pointer to hover over album art in order to show the **Buy** link.</span></span>
    3.  <span data-ttu-id="6dbcd-364">Haga clic en **comprar**.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-364">Click **Buy**.</span></span>

    <span data-ttu-id="6dbcd-365">En la captura de pantalla siguiente se muestra la ubicación del vínculo **Buy** en Windows Media Player 11:</span><span class="sxs-lookup"><span data-stu-id="6dbcd-365">The following screen shot shows the location of the **Buy** link in Windows Media Player 11:</span></span>

    ![captura de pantalla que muestra cómo comprar contenido en el reproductor de Windows Media 11](images/wmp11-verify-buy-play.png)

    <span data-ttu-id="6dbcd-367">Realice los pasos siguientes para comprar contenido en Windows 7 con Windows Media Player 12:</span><span class="sxs-lookup"><span data-stu-id="6dbcd-367">Perform the following steps to purchase content in Windows 7 with Windows Media Player 12:</span></span>

    1.  <span data-ttu-id="6dbcd-368">En el modo de biblioteca, haga clic en la pestaña **reproducir** .</span><span class="sxs-lookup"><span data-stu-id="6dbcd-368">In library mode, click the **Play** tab.</span></span>
    2.  <span data-ttu-id="6dbcd-369">En la lista de reproducción, en la carátula del álbum, haga clic en **tienda**</span><span class="sxs-lookup"><span data-stu-id="6dbcd-369">In the playlist, under the album art, click **Shop**</span></span>

    <span data-ttu-id="6dbcd-370">En la captura de pantalla siguiente se muestra cómo comprar contenido en Windows Media Player 12:</span><span class="sxs-lookup"><span data-stu-id="6dbcd-370">The following screen shot shows how to buy content in Windows Media Player 12:</span></span>

    ![captura de pantalla que muestra cómo comprar contenido en el reproductor de Windows Media 12](images/wmp12-verify-buy-play.png)

6.  <span data-ttu-id="6dbcd-372">Compruebe que al hacer clic en **comprar o comprar** cambia a **la tienda.**</span><span class="sxs-lookup"><span data-stu-id="6dbcd-372">Verify that clicking **Buy** or **Shop** switches to the store.</span></span>

    <span data-ttu-id="6dbcd-373">La Media Player de Windows debe cambiar a la tienda en la vista biblioteca y cargar la experiencia de compra de la tienda.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-373">The Windows Media Player should switch to the store in library view and load the purchasing experience of the store.</span></span>

    <span data-ttu-id="6dbcd-374">Después, debe continuar con la compra de la pista.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-374">You must then continue to purchase the track.</span></span>

7.  <span data-ttu-id="6dbcd-375">Compruebe que **después de hacer** clic en comprar o **comprar** , el contenido se descarga.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-375">Verify that after clicking **Buy** or **Shop**, the content downloads.</span></span>

    <span data-ttu-id="6dbcd-376">Compruebe que los derechos de uso de medios sean adecuados para el contenido adquirido y sus metadatos, y compruebe que el seguimiento se reproduce.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-376">Verify that the media usage rights are appropriate for the purchased content and its metadata, and verify that the track plays.</span></span> <span data-ttu-id="6dbcd-377">En general, este método de compra debe tener los mismos resultados que otros métodos.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-377">In general, this method of purchase should have the same results as other methods.</span></span>

### <a name="burning-content"></a><span data-ttu-id="6dbcd-378">Grabar contenido</span><span class="sxs-lookup"><span data-stu-id="6dbcd-378">Burning Content</span></span>

<span data-ttu-id="6dbcd-379">En primer lugar, realice los pasos siguientes para grabar contenido adquirido (Copie el contenido adquirido en un CD o DVD grabable) y, a continuación, siga los pasos que se indican a continuación para comprobar que el contenido se grabe:</span><span class="sxs-lookup"><span data-stu-id="6dbcd-379">First perform the following steps to burn purchased content (copy purchased content to a writeable CD or DVD), and then perform the steps that follow the initial steps to verify that the content burns:</span></span>

> [!Note]  
> <span data-ttu-id="6dbcd-380">Antes de grabar una pista comprada, tenga en cuenta su número de grabaciones para que pueda comprobar más adelante si el recuento disminuye después de grabar la pista.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-380">Before you burn a purchased track, note its burn count so you can later verify whether the count decrements after you burn the track.</span></span>

 

1.  <span data-ttu-id="6dbcd-381">Haga clic en la pestaña **grabar** .</span><span class="sxs-lookup"><span data-stu-id="6dbcd-381">Click the **Burn** tab</span></span>
2.  <span data-ttu-id="6dbcd-382">Arrastre pistas compradas a la **lista de grabación**.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-382">Drag purchased tracks to the **Burn List**.</span></span>
3.  <span data-ttu-id="6dbcd-383">Haga clic en el botón **iniciar grabación** .</span><span class="sxs-lookup"><span data-stu-id="6dbcd-383">Click the **Start Burn** button.</span></span>

<span data-ttu-id="6dbcd-384">En la captura de pantalla siguiente se muestra la **lista de grabación** en el lado derecho de la pantalla y el botón **iniciar grabación** debajo de la **lista de grabación** en Windows Media Player 11:</span><span class="sxs-lookup"><span data-stu-id="6dbcd-384">The following screen shot shows the **Burn List** on the right side of the screen and the **Start Burn** button below the **Burn List** in Windows Media Player 11:</span></span>

![captura de pantalla que muestra cómo grabar contenido en el reproductor de Windows Media 11](images/wmp11-verify-burn.png)

<span data-ttu-id="6dbcd-386">En la captura de pantalla siguiente se muestra cómo aparece la lista de grabación en Windows Media Player 12 después de arrastrar una pista a la lista de grabación y se muestra el botón **iniciar grabación** en la parte superior de la pestaña **grabar** :</span><span class="sxs-lookup"><span data-stu-id="6dbcd-386">The following screen shot shows how the burn list appears in Windows Media Player 12 after you drag a track to the burn list, and it shows the **Start Burn** button at the top of the **Burn** tab:</span></span>

![captura de pantalla que muestra cómo grabar contenido en el reproductor de Windows Media 12](images/wmp12-verify-burn.png)

<span data-ttu-id="6dbcd-388">**Para comprobar que se puede grabar el contenido adquirido**</span><span class="sxs-lookup"><span data-stu-id="6dbcd-388">**To verify that purchased content can be burned**</span></span>

1.  <span data-ttu-id="6dbcd-389">Compruebe que el contenido adquirido se grabe reproduciendo el CD o DVD una vez finalizada la grabación.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-389">Verify that the purchased content burns by playing the CD or DVD after burning completes.</span></span>

2.  <span data-ttu-id="6dbcd-390">Compruebe que se reduce el número de grabaciones.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-390">Verify that the burn count is decremented.</span></span>

    <span data-ttu-id="6dbcd-391">Vaya a la biblioteca y abra los derechos de uso de medios para una pista comprada que se grabó.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-391">Navigate to the library and open the media usage rights for a purchased track that was burned.</span></span>

    <span data-ttu-id="6dbcd-392">Si el número de veces que se puede grabar una pista es limitado, compruebe que este número disminuye después de grabar la pista.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-392">If the number of times a track can be burned is limited, verify that this number decreases after the track is burned.</span></span>

### <a name="transferring-content"></a><span data-ttu-id="6dbcd-393">Transferir contenido</span><span class="sxs-lookup"><span data-stu-id="6dbcd-393">Transferring Content</span></span>

<span data-ttu-id="6dbcd-394">Transferir contenido a otro equipo.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-394">Transfer content to another computer.</span></span>

<span data-ttu-id="6dbcd-395">**Para comprobar que el contenido adquirido se puede transferir a otro equipo**</span><span class="sxs-lookup"><span data-stu-id="6dbcd-395">**To verify that purchased content can be transferred to another computer**</span></span>

-   <span data-ttu-id="6dbcd-396">Si el almacén permite transferir contenido a otro equipo, transfiera el contenido a dos equipos como mínimo.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-396">If the store allows transferring content to another computer, transfer the content to at least two computers.</span></span>

<span data-ttu-id="6dbcd-397">En primer lugar, realice los pasos siguientes para sincronizar con un dispositivo y transferir el contenido adquirido a ese dispositivo y, a continuación, siga los pasos que se indican a continuación para comprobar que el contenido se transfiere:</span><span class="sxs-lookup"><span data-stu-id="6dbcd-397">First perform the following steps to sync to a device and transfer purchased content to that device, and then perform the steps that follow the initial steps to verify that the content is transferred:</span></span>

> [!Note]  
> <span data-ttu-id="6dbcd-398">Antes de transferir una pista comprada, tenga en cuenta su número de sincronizaciones para que pueda comprobar más adelante si el recuento disminuye después de transferir la pista.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-398">Before you transfer a purchased track, note its sync count so you can later verify whether the count decrements after you transfer the track.</span></span>

 

1.  <span data-ttu-id="6dbcd-399">Conectar un dispositivo con un reloj seguro.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-399">Connect a device with a secure clock.</span></span> <span data-ttu-id="6dbcd-400">Algunos ejemplos son los dispositivos que usan DRM de Windows Media para dispositivos portátiles, como un centro multimedia portátil como iRiver H10, Creative Zen, etc.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-400">Examples include devices that use Windows Media DRM for Portable Devices, such as a Portable Media Center like the iRiver H10, the Creative Zen, and so on.</span></span>
2.  <span data-ttu-id="6dbcd-401">En Windows Media Player, haga clic en la pestaña **sincronizar** .</span><span class="sxs-lookup"><span data-stu-id="6dbcd-401">In Windows Media Player, click the **Sync** tab.</span></span>
3.  <span data-ttu-id="6dbcd-402">Arrastre el contenido de la biblioteca al área **lista de sincronización** de la pestaña **sincronizar** .</span><span class="sxs-lookup"><span data-stu-id="6dbcd-402">Drag content from the library to the **Sync list** area on the **Sync** tab.</span></span>
4.  <span data-ttu-id="6dbcd-403">Haga clic en el botón **Iniciar sincronización** .</span><span class="sxs-lookup"><span data-stu-id="6dbcd-403">Click the **Start Sync** button.</span></span>

<span data-ttu-id="6dbcd-404">En la captura de pantalla siguiente se muestra el seguimiento 1 en el área de **lista de sincronización** y se muestra el botón **Iniciar sincronización** en Windows Media Player 11:</span><span class="sxs-lookup"><span data-stu-id="6dbcd-404">The following screen shot shows Track 1 in the **Sync list** area and shows the **Start Sync** button in Windows Media Player 11:</span></span>

![captura de pantalla que muestra cómo transferir contenido en el reproductor de Windows Media 11](images/wmp11-verify-transfer.png)

<span data-ttu-id="6dbcd-406">En la captura de pantalla siguiente se muestra el seguimiento 1 en el área de **lista de sincronización** y se muestra el botón **Iniciar sincronización** en Windows Media Player 12:</span><span class="sxs-lookup"><span data-stu-id="6dbcd-406">The following screen shot shows Track 1 in the **Sync list** area and shows the **Start Sync** button in Windows Media Player 12:</span></span>

![captura de pantalla que muestra cómo transferir contenido en el reproductor de Windows Media 12](images/wmp12-verify-transfer.png)

<span data-ttu-id="6dbcd-408">**Para comprobar que el contenido adquirido se puede transferir a otro dispositivo**</span><span class="sxs-lookup"><span data-stu-id="6dbcd-408">**To verify that purchased content can be transferred to another device**</span></span>

1.  <span data-ttu-id="6dbcd-409">Compruebe que el contenido adquirido se transfiere al dispositivo reproduciendo el contenido en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-409">Verify that the purchased content is transferred to the device by playing the content on the device.</span></span> <span data-ttu-id="6dbcd-410">El contenido transferido también debe tener los metadatos adecuados.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-410">The transferred content must also have appropriate metadata.</span></span>

2.  <span data-ttu-id="6dbcd-411">Compruebe que se reduce el número de sincronizaciones.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-411">Verify that the sync count is decremented.</span></span>

    <span data-ttu-id="6dbcd-412">Navegue a la biblioteca y abra los derechos de uso de medios para una pista transferida.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-412">Navigate to the library and open the media usage rights for a transferred track.</span></span>

    <span data-ttu-id="6dbcd-413">Si el número de veces que se puede sincronizar una pista es limitado, compruebe que este número se reduce cuando se transfiere la pista.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-413">If the number of times a track can sync is limited, verify that this number decreases when the track is transferred.</span></span>

## <a name="store-features"></a><span data-ttu-id="6dbcd-414">Almacenar características</span><span class="sxs-lookup"><span data-stu-id="6dbcd-414">Store Features</span></span>

<span data-ttu-id="6dbcd-415">En las secciones siguientes se describe cómo probar varias características de una tienda en línea incorporada.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-415">The following sections describe how to test various features of an on-boarded online store.</span></span>

### <a name="managing-an-account"></a><span data-ttu-id="6dbcd-416">Administrar una cuenta</span><span class="sxs-lookup"><span data-stu-id="6dbcd-416">Managing an Account</span></span>

<span data-ttu-id="6dbcd-417">Inicie sesión con una cuenta que haya realizado algunas compras y abra el historial de compras.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-417">Sign in with an account that has made some purchases and open the purchase history.</span></span>

<span data-ttu-id="6dbcd-418">**Para comprobar el historial de compras**</span><span class="sxs-lookup"><span data-stu-id="6dbcd-418">**To verify purchase history**</span></span>

-   <span data-ttu-id="6dbcd-419">Compruebe que el historial de compras realiza un seguimiento de las compras anteriores.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-419">Verify that the purchase history tracks prior purchases.</span></span>

<span data-ttu-id="6dbcd-420">Si el tipo de almacén o cuenta es compatible con esta característica, intente restaurar una compra eliminada.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-420">If the store or account type supports this feature, attempt to restore a deleted purchase.</span></span>

<span data-ttu-id="6dbcd-421">**Para comprobar que las compras anteriores se pueden readquirir**</span><span class="sxs-lookup"><span data-stu-id="6dbcd-421">**To verify that prior purchases can be reacquired**</span></span>

-   <span data-ttu-id="6dbcd-422">Compruebe que se puede restaurar una compra anterior.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-422">Verify that a prior purchase can be restored.</span></span>

<span data-ttu-id="6dbcd-423">Si el almacén admite el uso de varios equipos con la cuenta, compruebe las funciones que proporciona esta característica.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-423">If the store supports using multiple computers with the account, verify any functionality that this feature provides.</span></span>

<span data-ttu-id="6dbcd-424">**Para comprobar la administración de varios equipos con una sola cuenta**</span><span class="sxs-lookup"><span data-stu-id="6dbcd-424">**To verify multiple computer management with a single account**</span></span>

-   <span data-ttu-id="6dbcd-425">Compruebe la funcionalidad del almacén para administrar varios equipos.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-425">Verify the store's functionality to manage multiple computers.</span></span>

### <a name="managing-a-store-specific-account"></a><span data-ttu-id="6dbcd-426">Administración de una cuenta de Store-Specific</span><span class="sxs-lookup"><span data-stu-id="6dbcd-426">Managing a Store-Specific Account</span></span>

<span data-ttu-id="6dbcd-427">Es posible que el almacén no tenga tipos de cuenta, restricciones o contenido típicos.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-427">The store might not have typical account types, restrictions, or content.</span></span> <span data-ttu-id="6dbcd-428">Por ejemplo, un almacén que alquila el vídeo de streaming necesitará alguna interfaz de usuario para mostrar los alquileres activos y la interfaz de usuario se debe probar.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-428">For example, a store that rents streaming video would need some user interface to display active rentals and that user interface would need to be tested.</span></span>

> [!Note]  
> <span data-ttu-id="6dbcd-429">Aunque Microsoft no puede certificar la funcionalidad de la cuenta específica del almacén, para garantizar una buena experiencia del cliente, debe probar esa funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-429">Although Microsoft cannot certify store-specific account functionality, to ensure a good customer experience, you should test that functionality.</span></span>

 

### <a name="managing-the-info-center"></a><span data-ttu-id="6dbcd-430">Administrar el centro de información</span><span class="sxs-lookup"><span data-stu-id="6dbcd-430">Managing the Info Center</span></span>

<span data-ttu-id="6dbcd-431">En primer lugar, realice los pasos siguientes para preparar la prueba del estado predeterminado y, a continuación, realice el siguiente paso que sigue los pasos iniciales para comprobar que el centro de información está desactivado de forma predeterminada:</span><span class="sxs-lookup"><span data-stu-id="6dbcd-431">First perform the following steps to prepare for testing the default state, and then perform the next step that follows the initial steps to verify that the Info Center is off by default:</span></span>

1.  <span data-ttu-id="6dbcd-432">Reproducir contenido de la tienda.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-432">Play some content from the store.</span></span>
2.  <span data-ttu-id="6dbcd-433">Cambiar al modo de reproducción en curso.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-433">Switch to Now Playing mode.</span></span> <span data-ttu-id="6dbcd-434">En Windows XP o Windows Vista con Windows Media Player 11, haga clic en la pestaña **reproducción en curso** . En Windows 7 con Windows Media Player 12, haga clic en el botón **cambiar a reproducción en curso** en la esquina inferior derecha.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-434">In Windows XP or Windows Vista with Windows Media Player 11, click the **Now Playing** tab. In Windows 7 with Windows Media Player 12, click the **Switch to Now Playing** button at the lower right corner.</span></span>

<span data-ttu-id="6dbcd-435">**Para comprobar que el centro de información está desactivado de forma predeterminada**</span><span class="sxs-lookup"><span data-stu-id="6dbcd-435">**To verify that the Info Center is off by default**</span></span>

-   <span data-ttu-id="6dbcd-436">Compruebe que el centro de información está desactivado de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-436">Verify that the Info Center is off by default.</span></span>

<span data-ttu-id="6dbcd-437">Si el almacén ofrece una vista de centro de información, reproduzca parte del contenido del almacén y mientras se reproduce el contenido, cambie al modo de reproducción en curso y Active info Center.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-437">If the store offers an Info Center view, play some content from the store, and while the content is playing, switch to Now Playing mode and turn Info Center on.</span></span>

<span data-ttu-id="6dbcd-438">En Windows XP o Windows Vista con Windows Media Player 11, haga clic con el botón derecho en la ventana de reproducción en curso y, a continuación, en el menú contextual, seleccione **info Center View**.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-438">In Windows XP or Windows Vista with Windows Media Player 11, right-click the now-playing window, and then from the context menu select **Info Center View**.</span></span>

<span data-ttu-id="6dbcd-439">En la captura de pantalla siguiente se muestra el menú contextual en Windows Media Player 11:</span><span class="sxs-lookup"><span data-stu-id="6dbcd-439">The following screen shot shows the context menu in Windows Media Player 11:</span></span>

![captura de pantalla que muestra cómo obtener acceso al centro de información de un almacén en el reproductor de Windows Media 11](images/wmp11-info-center.png)

<span data-ttu-id="6dbcd-441">En Windows 7 con Windows Media Player 12, haga clic con el botón derecho en la ventana de reproducción en curso, seleccione **visualizaciones** en el menú contextual y, a continuación, haga clic en **info Center View**.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-441">In Windows 7 with Windows Media Player 12, right-click the now-playing window, on the context menu select **Visualizations**, and then click **Info Center View**.</span></span>

<span data-ttu-id="6dbcd-442">En la captura de pantalla siguiente se muestra el menú contextual de Windows Media Player 12:</span><span class="sxs-lookup"><span data-stu-id="6dbcd-442">The following screen shot shows the context menu in Windows Media Player 12:</span></span>

![captura de pantalla que muestra cómo obtener acceso al centro de información de un almacén en el reproductor de Windows Media 12](images/wmp12-info-center.png)

<span data-ttu-id="6dbcd-444">**Para comprobar que el centro de información es funcional**</span><span class="sxs-lookup"><span data-stu-id="6dbcd-444">**To verify that the Info Center is functional**</span></span>

-   <span data-ttu-id="6dbcd-445">Compruebe que el centro de información muestra información multimedia en el área de reproducción en curso.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-445">Verify that the Info Center shows media information in the now-playing area.</span></span> <span data-ttu-id="6dbcd-446">En la captura de pantalla siguiente se muestra un ejemplo de la información multimedia:</span><span class="sxs-lookup"><span data-stu-id="6dbcd-446">The following screen shot shows an example of such media information:</span></span>

    ![captura de pantalla que muestra la funcionalidad del centro de información de un almacén](images/media-information.png)

<span data-ttu-id="6dbcd-448">Si aparecen vínculos de compra u otros vínculos en la página, haga clic en los vínculos.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-448">If any buy links or other links appear on the page, click the links.</span></span>

<span data-ttu-id="6dbcd-449">**Para comprobar los vínculos en la vista de centro de información**</span><span class="sxs-lookup"><span data-stu-id="6dbcd-449">**To verify links in the Info Center view**</span></span>

-   <span data-ttu-id="6dbcd-450">Compruebe que los vínculos muestran el almacén.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-450">Verify that the links show the store.</span></span>

    <span data-ttu-id="6dbcd-451">El Media Player de Windows debe cambiar al almacén en su biblioteca.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-451">The Windows Media Player should switch to the store in its library.</span></span>

## <a name="store-interaction"></a><span data-ttu-id="6dbcd-452">Interacción de la tienda</span><span class="sxs-lookup"><span data-stu-id="6dbcd-452">Store Interaction</span></span>

<span data-ttu-id="6dbcd-453">En las secciones siguientes se describe cómo probar la interacción entre los otros almacenes y el almacén que se está probando.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-453">The following sections describe how to test interaction between the other stores and the store that you are testing.</span></span>

### <a name="yielding-to-the-active-store"></a><span data-ttu-id="6dbcd-454">Producir en el almacén activo</span><span class="sxs-lookup"><span data-stu-id="6dbcd-454">Yielding to the Active Store</span></span>

<span data-ttu-id="6dbcd-455">Cambie a un almacén que no sea el almacén que se está probando.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-455">Switch to a store other than the store being tested.</span></span>

<span data-ttu-id="6dbcd-456">**Para comprobar la producción en el almacén activo**</span><span class="sxs-lookup"><span data-stu-id="6dbcd-456">**To verify yielding to the active store**</span></span>

-   <span data-ttu-id="6dbcd-457">Compruebe que el almacén probado produce el almacén activo.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-457">Verify that the tested store yields to the active store.</span></span>

### <a name="preventing-the-tested-store-from-taking-over-the-active-store"></a><span data-ttu-id="6dbcd-458">Impedir que el almacén probado tome el control en el almacén activo</span><span class="sxs-lookup"><span data-stu-id="6dbcd-458">Preventing the Tested Store From Taking Over the Active Store</span></span>

-   <span data-ttu-id="6dbcd-459">Con otro almacén seleccionado, cierre Windows Media Player y reinicie el equipo.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-459">With another store selected, close Windows Media Player and restart the computer.</span></span>
-   <span data-ttu-id="6dbcd-460">Inicie Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-460">Launch Windows Media Player.</span></span>

<span data-ttu-id="6dbcd-461">**Para comprobar que el almacén probado no toma el control**</span><span class="sxs-lookup"><span data-stu-id="6dbcd-461">**To verify that the tested store does not take over**</span></span>

-   <span data-ttu-id="6dbcd-462">Compruebe que el último almacén activo aparece y que el almacén probado no aparece.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-462">Verify that the most recently active store appears and that the tested store does not appear.</span></span>

### <a name="accessing-a-store-in-high-contrast-mode"></a><span data-ttu-id="6dbcd-463">Acceso a un almacén en modo de High-Contrast</span><span class="sxs-lookup"><span data-stu-id="6dbcd-463">Accessing a Store in High-Contrast Mode</span></span>

<span data-ttu-id="6dbcd-464">En primer lugar, habilite el modo de alto contraste presionando Mayús Izq + izquierda ALT + Impr Pant y, a continuación, realice los pasos siguientes para comprobar la accesibilidad de contraste alto:</span><span class="sxs-lookup"><span data-stu-id="6dbcd-464">First enable high-contrast mode by pressing LEFT SHIFT+LEFT ALT+PRINT SCREEN, and then perform the following steps to verify high-contrast accessibility:</span></span>

<span data-ttu-id="6dbcd-465">**Para comprobar que el almacén es accesible en el modo de alto contraste**</span><span class="sxs-lookup"><span data-stu-id="6dbcd-465">**To verify that the store is accessible in high-contrast mode**</span></span>

1.  <span data-ttu-id="6dbcd-466">Compruebe que la interfaz de usuario de inicio de sesión está intacta y funciona.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-466">Verify that the log-in user interface is intact and functional.</span></span>
2.  <span data-ttu-id="6dbcd-467">Compruebe que todas las ventanas y cuadros de diálogo aparecen correctamente.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-467">Verify that all windows and dialog boxes appear correctly.</span></span>
3.  <span data-ttu-id="6dbcd-468">Compra de medios.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-468">Purchase media.</span></span> <span data-ttu-id="6dbcd-469">Compruebe que estén visibles los botones de compra y descarga, los administradores de descargas, la información de precios, etc.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-469">Verify that purchase and download buttons, download managers, price information, and so on is visible.</span></span>
4.  <span data-ttu-id="6dbcd-470">Compruebe que puede transmitir, grabar y sincronizar.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-470">Verify that you can stream, burn, and synchronize.</span></span>
5.  <span data-ttu-id="6dbcd-471">Busque texto recortado y elementos de la interfaz de usuario, texto que no sea legible y otros defectos visibles.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-471">Look for clipped text and user-interface elements, text that is not legible, and other visible defects.</span></span>

### <a name="securing-a-store"></a><span data-ttu-id="6dbcd-472">Protección de un almacén</span><span class="sxs-lookup"><span data-stu-id="6dbcd-472">Securing a Store</span></span>

<span data-ttu-id="6dbcd-473">Realice los pasos siguientes para comprobar la seguridad de la cuenta:</span><span class="sxs-lookup"><span data-stu-id="6dbcd-473">Perform the following steps to verify account security:</span></span>

<span data-ttu-id="6dbcd-474">**Para comprobar la seguridad de la cuenta**</span><span class="sxs-lookup"><span data-stu-id="6dbcd-474">**To verify account security**</span></span>

1.  <span data-ttu-id="6dbcd-475">Escriba la información de cuenta con formato incorrecto en la página de inicio de sesión y el cuadro de diálogo y compruebe que el almacén lo rechaza.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-475">Enter malformed account information into the log-in page and dialog box and verify that the store rejects it.</span></span>
2.  <span data-ttu-id="6dbcd-476">Inicie sesión, vea la página cuenta y cierre la sesión.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-476">Sign in, view the account page, and sign out.</span></span>
3.  <span data-ttu-id="6dbcd-477">Haga clic en el botón atrás de Windows Media Player y compruebe que no ve la información de la cuenta de usuario anterior.</span><span class="sxs-lookup"><span data-stu-id="6dbcd-477">Click the back button in Windows Media Player, and verify that you do not see the previous user account information.</span></span>

 

 




