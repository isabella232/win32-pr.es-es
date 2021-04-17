---
title: Configuración de WER
description: Configuración para personalizar la experiencia de informes de problemas. Todos estos valores se pueden establecer mediante directiva de grupo. Algunos también se pueden cambiar en el centro de actividades para Windows 7 y Windows 8. En el caso de Windows 10, use la función de búsqueda en configuración para ver la configuración avanzada del sistema.
ms.assetid: 031c5591-31b0-42f1-9a98-ecf10a5d5571
keywords:
- Informe de errores de Windows Informe de errores de Windows, configuración
ms.topic: article
ms.date: 03/12/2021
ms.openlocfilehash: 28b6abbda7d851daddb75ec534b8128d1a831b3f
ms.sourcegitcommit: 434d5437d4c31c47358598ea5275177c2698f557
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/13/2021
ms.locfileid: "105653267"
---
# <a name="wer-settings"></a><span data-ttu-id="2b5c2-107">Configuración de WER</span><span class="sxs-lookup"><span data-stu-id="2b5c2-107">WER Settings</span></span>

<span data-ttu-id="2b5c2-108">Informe de errores de Windows (WER) proporciona muchas opciones para personalizar la experiencia de informes de problemas.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-108">Windows Error Reporting (WER) provides many settings to customize the problem reporting experience.</span></span> <span data-ttu-id="2b5c2-109">Todos estos valores se pueden establecer mediante directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-109">All of these settings can be set using Group Policy.</span></span> <span data-ttu-id="2b5c2-110">Algunos también se pueden cambiar en el **centro de actividades** para Windows 7 y Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-110">Some can also be changed in **Action Center** for Windows 7 and Windows 8.</span></span> <span data-ttu-id="2b5c2-111">En el caso de Windows 10, use la función de búsqueda en configuración para **ver la configuración avanzada del sistema**.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-111">For Windows 10, use the search function in Settings to locate **View advanced system settings**.</span></span> <span data-ttu-id="2b5c2-112">La configuración de WER se encuentra en una de las siguientes subclaves del registro:</span><span class="sxs-lookup"><span data-stu-id="2b5c2-112">WER settings are located in one of the following registry subkeys:</span></span>

-   <span data-ttu-id="2b5c2-113">**HKEY \_ Software de \_ usuario actual** \\  \\ **Microsoft** \\ **Windows** \\ **Informe de errores de Windows**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-113">**HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Windows**\\**Windows Error Reporting**</span></span>
-   <span data-ttu-id="2b5c2-114">**HKEY \_ Software de \_ equipo local** \\  \\ **Microsoft** \\ **Windows** \\ **Informe de errores de Windows**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-114">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows**\\**Windows Error Reporting**</span></span>

## <a name="windows-error-reporting-subkey"></a><span data-ttu-id="2b5c2-115">Subclave Informe de errores de Windows</span><span class="sxs-lookup"><span data-stu-id="2b5c2-115">Windows Error Reporting subkey</span></span>

<dl> <dt>

<span data-ttu-id="2b5c2-116"><span id="BypassDataThrottling"></span><span id="bypassdatathrottling"></span><span id="BYPASSDATATHROTTLING"></span>**BypassDataThrottling**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-116"><span id="BypassDataThrottling"></span><span id="bypassdatathrottling"></span><span id="BYPASSDATATHROTTLING"></span>**BypassDataThrottling**</span></span>
</dt> <dd>

<span data-ttu-id="2b5c2-117">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-117">**REG\_DWORD**</span></span>

<span data-ttu-id="2b5c2-118">Valores posibles:</span><span class="sxs-lookup"><span data-stu-id="2b5c2-118">Possible values:</span></span><dl> <dd>

<span data-ttu-id="2b5c2-119">0: deshabilitar la limitación de derivación de datos.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-119">0 - Disable data bypass throttling.</span></span> <span data-ttu-id="2b5c2-120">Si la omisión está deshabilitada o no está configurada como una configuración de Directiva, WER limita los datos de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-120">If the bypass is disabled or not configured as a policy setting, WER throttles data by default.</span></span> <span data-ttu-id="2b5c2-121">WER no carga más de un archivo CAB para un informe que contiene datos sobre los mismos tipos de eventos.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-121">WER does not upload more than one CAB file for a report that contains data about the same event types.</span></span>

</dd> <dd>

<span data-ttu-id="2b5c2-122">1-habilitar la limitación de derivación de datos.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-122">1 - Enable data bypass throttling.</span></span> <span data-ttu-id="2b5c2-123">WER no limita los datos.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-123">WER does not throttle data.</span></span> <span data-ttu-id="2b5c2-124">WER carga archivos CAB adicionales que pueden contener datos sobre los mismos tipos de eventos que un informe cargado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-124">WER uploads additional CAB files that can contain data about the same event types as an earlier uploaded report.</span></span>

</dd> </dl>

<span data-ttu-id="2b5c2-125">Indica si se debe habilitar la omisión de la limitación de datos del cliente de WER</span><span class="sxs-lookup"><span data-stu-id="2b5c2-125">Whether to enable the bypass of WER client data throttling</span></span>

</dd> <dt>

<span data-ttu-id="2b5c2-126"><span id="ConfigureArchive"></span><span id="configurearchive"></span><span id="CONFIGUREARCHIVE"></span>**ConfigureArchive**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-126"><span id="ConfigureArchive"></span><span id="configurearchive"></span><span id="CONFIGUREARCHIVE"></span>**ConfigureArchive**</span></span>
</dt> <dd>

<span data-ttu-id="2b5c2-127">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-127">**REG\_DWORD**</span></span>

<span data-ttu-id="2b5c2-128">Valores posibles:</span><span class="sxs-lookup"><span data-stu-id="2b5c2-128">Possible values:</span></span><dl> <dd><span data-ttu-id="2b5c2-129">1-solo parámetros (valor predeterminado en Windows 7)</span><span class="sxs-lookup"><span data-stu-id="2b5c2-129">1 - Parameters only (default on Windows 7)</span></span></dd> <dd><span data-ttu-id="2b5c2-130">2-todos los datos (predeterminado en Windows Vista)</span><span class="sxs-lookup"><span data-stu-id="2b5c2-130">2 - All data (default on Windows Vista)</span></span></dd> </dl>

<span data-ttu-id="2b5c2-131">Si se van a archivar solo los parámetros o todos los datos</span><span class="sxs-lookup"><span data-stu-id="2b5c2-131">Whether to archive parameters only or all data</span></span>

</dd> <dt>

<span data-ttu-id="2b5c2-132"><span id="Consent_DefaultConsent"></span><span id="consent_defaultconsent"></span><span id="CONSENT_DEFAULTCONSENT"></span>**DefaultConsent de consentimiento \\**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-132"><span id="Consent_DefaultConsent"></span><span id="consent_defaultconsent"></span><span id="CONSENT_DEFAULTCONSENT"></span>**Consent\\DefaultConsent**</span></span>
</dt> <dd>

<span data-ttu-id="2b5c2-133">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-133">**REG\_DWORD**</span></span>

<span data-ttu-id="2b5c2-134">Valores posibles:</span><span class="sxs-lookup"><span data-stu-id="2b5c2-134">Possible values:</span></span><dl> <dd><span data-ttu-id="2b5c2-135">1-preguntar siempre (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="2b5c2-135">1 - Always ask (default)</span></span></dd> <dd><span data-ttu-id="2b5c2-136">2-solo parámetros</span><span class="sxs-lookup"><span data-stu-id="2b5c2-136">2 - Parameters only</span></span></dd> <dd><span data-ttu-id="2b5c2-137">3-parámetros y datos seguros</span><span class="sxs-lookup"><span data-stu-id="2b5c2-137">3 - Parameters and safe data</span></span></dd> <dd><span data-ttu-id="2b5c2-138">4-todos los datos</span><span class="sxs-lookup"><span data-stu-id="2b5c2-138">4 - All data</span></span></dd> </dl>

<span data-ttu-id="2b5c2-139">Elección de consentimiento predeterminado</span><span class="sxs-lookup"><span data-stu-id="2b5c2-139">Default consent choice</span></span>

</dd> <dt>

<span data-ttu-id="2b5c2-140"><span id="Consent_DefaultOverrideBehavior"></span><span id="consent_defaultoverridebehavior"></span><span id="CONSENT_DEFAULTOVERRIDEBEHAVIOR"></span>**DefaultOverrideBehavior de consentimiento \\**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-140"><span id="Consent_DefaultOverrideBehavior"></span><span id="consent_defaultoverridebehavior"></span><span id="CONSENT_DEFAULTOVERRIDEBEHAVIOR"></span>**Consent\\DefaultOverrideBehavior**</span></span>
</dt> <dd>

<span data-ttu-id="2b5c2-141">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-141">**REG\_DWORD**</span></span>

<span data-ttu-id="2b5c2-142">Valores posibles:</span><span class="sxs-lookup"><span data-stu-id="2b5c2-142">Possible values:</span></span><dl> <dd><span data-ttu-id="2b5c2-143">0: el consentimiento vertical invalidará el consentimiento predeterminado (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="2b5c2-143">0 - Vertical consent will override the default consent (default)</span></span></dd> <dd><span data-ttu-id="2b5c2-144">1: el consentimiento predeterminado invalidará el consentimiento específico de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-144">1 - Default consent will override the application-specific consent</span></span></dd> </dl>

<span data-ttu-id="2b5c2-145">Si el consentimiento predeterminado invalida el consentimiento vertical</span><span class="sxs-lookup"><span data-stu-id="2b5c2-145">Whether default consent overrides vertical consent</span></span>

</dd> <dt>

<span data-ttu-id="2b5c2-146"><span id="Consent__VerticalName_"></span><span id="consent__verticalname_"></span><span id="CONSENT__VERTICALNAME_"></span>**VerticalName de consentimiento \\ \[\]**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-146"><span id="Consent__VerticalName_"></span><span id="consent__verticalname_"></span><span id="CONSENT__VERTICALNAME_"></span>**Consent\\\[VerticalName\]**</span></span>
</dt> <dd>

<span data-ttu-id="2b5c2-147">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-147">**REG\_DWORD**</span></span>

<span data-ttu-id="2b5c2-148">Valores posibles:</span><span class="sxs-lookup"><span data-stu-id="2b5c2-148">Possible values:</span></span><dl> <dd><span data-ttu-id="2b5c2-149">1-preguntar siempre (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="2b5c2-149">1 - Always ask (default)</span></span></dd> <dd><span data-ttu-id="2b5c2-150">2-solo parámetros</span><span class="sxs-lookup"><span data-stu-id="2b5c2-150">2 - Parameters only</span></span></dd> <dd><span data-ttu-id="2b5c2-151">3-parámetros y datos seguros</span><span class="sxs-lookup"><span data-stu-id="2b5c2-151">3 - Parameters and safe data</span></span></dd> <dd><span data-ttu-id="2b5c2-152">4-todos los datos</span><span class="sxs-lookup"><span data-stu-id="2b5c2-152">4 - All data</span></span></dd> </dl>

<span data-ttu-id="2b5c2-153">Elección de consentimiento para el complemento WER</span><span class="sxs-lookup"><span data-stu-id="2b5c2-153">Consent choice for the WER plug-in</span></span>

</dd> <dt>

<span data-ttu-id="2b5c2-154"><span id="CorporateWERDirectory"></span><span id="corporatewerdirectory"></span><span id="CORPORATEWERDIRECTORY"></span>**CorporateWERDirectory**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-154"><span id="CorporateWERDirectory"></span><span id="corporatewerdirectory"></span><span id="CORPORATEWERDIRECTORY"></span>**CorporateWERDirectory**</span></span>
</dt> <dd>

<span data-ttu-id="2b5c2-155">**Registro \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-155">**REG\_SZ**</span></span>

<span data-ttu-id="2b5c2-156">La ruta de acceso del directorio</span><span class="sxs-lookup"><span data-stu-id="2b5c2-156">The directory path</span></span>

<span data-ttu-id="2b5c2-157">Directorio de destino en el servidor</span><span class="sxs-lookup"><span data-stu-id="2b5c2-157">Target directory on the server</span></span>

</dd> <dt>

<span data-ttu-id="2b5c2-158"><span id="CorporateWERPortNumber"></span><span id="corporatewerportnumber"></span><span id="CORPORATEWERPORTNUMBER"></span>**CorporateWERPortNumber**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-158"><span id="CorporateWERPortNumber"></span><span id="corporatewerportnumber"></span><span id="CORPORATEWERPORTNUMBER"></span>**CorporateWERPortNumber**</span></span>
</dt> <dd>

<span data-ttu-id="2b5c2-159">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-159">**REG\_DWORD**</span></span>

<span data-ttu-id="2b5c2-160">El número de Puerto</span><span class="sxs-lookup"><span data-stu-id="2b5c2-160">The port number</span></span>

<span data-ttu-id="2b5c2-161">Número de puerto que se va a usar con el servidor corporativo</span><span class="sxs-lookup"><span data-stu-id="2b5c2-161">Port number to be used with the corporate server</span></span>

</dd> <dt>

<span data-ttu-id="2b5c2-162"><span id="CorporateWERServer"></span><span id="corporatewerserver"></span><span id="CORPORATEWERSERVER"></span>**CorporateWERServer**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-162"><span id="CorporateWERServer"></span><span id="corporatewerserver"></span><span id="CORPORATEWERSERVER"></span>**CorporateWERServer**</span></span>
</dt> <dd>

<span data-ttu-id="2b5c2-163">**Registro \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-163">**REG\_SZ**</span></span>

<span data-ttu-id="2b5c2-164">El nombre del servidor.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-164">The name of the server</span></span>

<span data-ttu-id="2b5c2-165">Nombre del servidor corporativo</span><span class="sxs-lookup"><span data-stu-id="2b5c2-165">Corporate server name</span></span>

</dd> <dt>

<span data-ttu-id="2b5c2-166"><span id="CorporateWERUseAuthentication"></span><span id="corporateweruseauthentication"></span><span id="CORPORATEWERUSEAUTHENTICATION"></span>**CorporateWERUseAuthentication**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-166"><span id="CorporateWERUseAuthentication"></span><span id="corporateweruseauthentication"></span><span id="CORPORATEWERUSEAUTHENTICATION"></span>**CorporateWERUseAuthentication**</span></span>
</dt> <dd>

<span data-ttu-id="2b5c2-167">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-167">**REG\_DWORD**</span></span>

<span data-ttu-id="2b5c2-168">Valores posibles:</span><span class="sxs-lookup"><span data-stu-id="2b5c2-168">Possible values:</span></span><dl> <dd><span data-ttu-id="2b5c2-169">0: no (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="2b5c2-169">0 - No (default)</span></span></dd> <dd><span data-ttu-id="2b5c2-170">1: Sí</span><span class="sxs-lookup"><span data-stu-id="2b5c2-170">1 - Yes</span></span></dd> </dl>

<span data-ttu-id="2b5c2-171">Si se va a usar la autenticación integrada de Windows</span><span class="sxs-lookup"><span data-stu-id="2b5c2-171">Whether to use Windows Integrated Authentication</span></span>

</dd> <dt>

<span data-ttu-id="2b5c2-172"><span id="CorporateWERUseSSL"></span><span id="corporatewerusessl"></span><span id="CORPORATEWERUSESSL"></span>**CorporateWERUseSSL**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-172"><span id="CorporateWERUseSSL"></span><span id="corporatewerusessl"></span><span id="CORPORATEWERUSESSL"></span>**CorporateWERUseSSL**</span></span>
</dt> <dd>

<span data-ttu-id="2b5c2-173">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-173">**REG\_DWORD**</span></span>

<span data-ttu-id="2b5c2-174">Valores posibles:</span><span class="sxs-lookup"><span data-stu-id="2b5c2-174">Possible values:</span></span><dl> <dd><span data-ttu-id="2b5c2-175">0: no (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="2b5c2-175">0 - No (default)</span></span></dd> <dd><span data-ttu-id="2b5c2-176">1: Sí</span><span class="sxs-lookup"><span data-stu-id="2b5c2-176">1 - Yes</span></span></dd> </dl>

<span data-ttu-id="2b5c2-177">Si se va a usar SSL</span><span class="sxs-lookup"><span data-stu-id="2b5c2-177">Whether to use SSL</span></span>

</dd> <dt>

<span data-ttu-id="2b5c2-178"><span id="DebugApplications__ExeName___replace___ExeName___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="debugapplications__exename___replace___exename___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="DEBUGAPPLICATIONS__EXENAME___REPLACE___EXENAME___WITH_AN_ACTUAL_NAME_OF_AN_.EXE_FILE__FOR_EXAMPLE___NOTEPAD.EXE__"></span>**DebugApplications \\ \[ ExeName \] (reemplace " \[ ExeName \] " por el nombre real de un archivo. exe, por ejemplo, "notepad.exe")**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-178"><span id="DebugApplications__ExeName___replace___ExeName___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="debugapplications__exename___replace___exename___with_an_actual_name_of_an_.exe_file__for_example___notepad.exe__"></span><span id="DEBUGAPPLICATIONS__EXENAME___REPLACE___EXENAME___WITH_AN_ACTUAL_NAME_OF_AN_.EXE_FILE__FOR_EXAMPLE___NOTEPAD.EXE__"></span>**DebugApplications\\\[ExeName\] (replace "\[ExeName\]" with an actual name of an .exe file, for example, "notepad.exe")**</span></span>
</dt> <dd>

<span data-ttu-id="2b5c2-179">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-179">**REG\_DWORD**</span></span>

<span data-ttu-id="2b5c2-180">Valores posibles:</span><span class="sxs-lookup"><span data-stu-id="2b5c2-180">Possible values:</span></span>

<dl> <dd><span data-ttu-id="2b5c2-181">0: los procesos con el nombre de la imagen ejecutable de **\[ ExeName \]** no requieren que el usuario elija **depurar** o **continuar** (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="2b5c2-181">0 - Processes with an executable image name of **\[ExeName\]** do not require the user to choose **Debug** or **Continue** (default)</span></span></dd> <dd><span data-ttu-id="2b5c2-182">1: los procesos con el nombre de la imagen ejecutable de **\[ ExeName \]** requieren que el usuario elija **depurar** o **continuar** .</span><span class="sxs-lookup"><span data-stu-id="2b5c2-182">1 - Processes with an executable image name of **\[ExeName\]** require the user to choose **Debug** or **Continue**</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="2b5c2-183"><span id="DebugApplications________is_the_literal_value_name_"></span><span id="debugapplications________is_the_literal_value_name_"></span><span id="DEBUGAPPLICATIONS________IS_THE_LITERAL_VALUE_NAME_"></span>**DebugApplications \\ \* (" \* " es el nombre del valor literal)**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-183"><span id="DebugApplications________is_the_literal_value_name_"></span><span id="debugapplications________is_the_literal_value_name_"></span><span id="DEBUGAPPLICATIONS________IS_THE_LITERAL_VALUE_NAME_"></span>**DebugApplications\\\* ("\*" is the literal value name)**</span></span>
</dt> <dd>

<span data-ttu-id="2b5c2-184">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-184">**REG\_DWORD**</span></span>

<span data-ttu-id="2b5c2-185">Valores posibles:</span><span class="sxs-lookup"><span data-stu-id="2b5c2-185">Possible values:</span></span>

<dl> <dd><span data-ttu-id="2b5c2-186">0: todos los procesos excepto los especificados explícitamente en el valor **DebugApplications \\ \[ ExeName \]** no requieren que el usuario elija **depurar** o **continuar** (valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="2b5c2-186">0 - All processes except ones specified explicitly in the setting **DebugApplications\\\[ExeName\]** do not require the user to choose **Debug** or **Continue** (default)</span></span></dd> <dd><span data-ttu-id="2b5c2-187">1-todos los procesos excepto los especificados explícitamente en el valor de **DebugApplications \\ \[ ExeName \]** requieren que el usuario elija **depurar** o **continuar** .</span><span class="sxs-lookup"><span data-stu-id="2b5c2-187">1 - All processes except ones specified explicitly in the setting **DebugApplications\\\[ExeName\]** require the user to choose **Debug** or **Continue**</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="2b5c2-188"><span id="DisableArchive"></span><span id="disablearchive"></span><span id="DISABLEARCHIVE"></span>**DisableArchive**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-188"><span id="DisableArchive"></span><span id="disablearchive"></span><span id="DISABLEARCHIVE"></span>**DisableArchive**</span></span>
</dt> <dd>

<span data-ttu-id="2b5c2-189">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-189">**REG\_DWORD**</span></span>

<span data-ttu-id="2b5c2-190">Valores posibles:</span><span class="sxs-lookup"><span data-stu-id="2b5c2-190">Possible values:</span></span><dl> <dd><span data-ttu-id="2b5c2-191">0 - Habilitado</span><span class="sxs-lookup"><span data-stu-id="2b5c2-191">0 - Enabled</span></span></dd> <dd><span data-ttu-id="2b5c2-192">1 - Deshabilitado</span><span class="sxs-lookup"><span data-stu-id="2b5c2-192">1 - Disabled</span></span></dd> </dl>

<span data-ttu-id="2b5c2-193">Habilitar o deshabilitar el archivo</span><span class="sxs-lookup"><span data-stu-id="2b5c2-193">Enable or disable the archive</span></span>

</dd> <dt>

<span data-ttu-id="2b5c2-194"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disponible**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-194"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled**</span></span>
</dt> <dd>

<span data-ttu-id="2b5c2-195">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-195">**REG\_DWORD**</span></span>

<span data-ttu-id="2b5c2-196">Valores posibles:</span><span class="sxs-lookup"><span data-stu-id="2b5c2-196">Possible values:</span></span><dl> <dd><span data-ttu-id="2b5c2-197">0: habilitado (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="2b5c2-197">0 - Enabled (default)</span></span></dd> <dd><span data-ttu-id="2b5c2-198">1 - Deshabilitado</span><span class="sxs-lookup"><span data-stu-id="2b5c2-198">1 - Disabled</span></span></dd> </dl>

<span data-ttu-id="2b5c2-199">Habilitar o deshabilitar WER</span><span class="sxs-lookup"><span data-stu-id="2b5c2-199">Enable or disable WER</span></span>

</dd> <dt>

<span data-ttu-id="2b5c2-200"><span id="DisableQueue"></span><span id="disablequeue"></span><span id="DISABLEQUEUE"></span>**DisableQueue**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-200"><span id="DisableQueue"></span><span id="disablequeue"></span><span id="DISABLEQUEUE"></span>**DisableQueue**</span></span>
</dt> <dd>

<span data-ttu-id="2b5c2-201">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-201">**REG\_DWORD**</span></span>

<span data-ttu-id="2b5c2-202">Valores posibles:</span><span class="sxs-lookup"><span data-stu-id="2b5c2-202">Possible values:</span></span><dl> <dd><span data-ttu-id="2b5c2-203">0 - Habilitado</span><span class="sxs-lookup"><span data-stu-id="2b5c2-203">0 - Enabled</span></span></dd> <dd><span data-ttu-id="2b5c2-204">1 - Deshabilitado</span><span class="sxs-lookup"><span data-stu-id="2b5c2-204">1 - Disabled</span></span></dd> </dl>

<span data-ttu-id="2b5c2-205">Habilitar o deshabilitar la puesta en cola de informes</span><span class="sxs-lookup"><span data-stu-id="2b5c2-205">Enable or disable report queuing</span></span>

</dd> <dt>

<span data-ttu-id="2b5c2-206"><span id="DontShowUI"></span><span id="dontshowui"></span><span id="DONTSHOWUI"></span>**DontShowUI**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-206"><span id="DontShowUI"></span><span id="dontshowui"></span><span id="DONTSHOWUI"></span>**DontShowUI**</span></span>
</dt> <dd>

<span data-ttu-id="2b5c2-207">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-207">**REG\_DWORD**</span></span>

<span data-ttu-id="2b5c2-208">Valores posibles:</span><span class="sxs-lookup"><span data-stu-id="2b5c2-208">Possible values:</span></span><dl> <dd><span data-ttu-id="2b5c2-209">0: interfaz de usuario (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="2b5c2-209">0 - UI (default)</span></span></dd> <dd><span data-ttu-id="2b5c2-210">1-sin interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="2b5c2-210">1 - No UI</span></span></dd> </dl>

<span data-ttu-id="2b5c2-211">Habilitar o deshabilitar la interfaz de usuario de WER</span><span class="sxs-lookup"><span data-stu-id="2b5c2-211">Enable or disable the WER UI</span></span>

</dd> <dt>

<span data-ttu-id="2b5c2-212"><span id="DontSendAdditionalData"></span><span id="dontsendadditionaldata"></span><span id="DONTSENDADDITIONALDATA"></span>**DontSendAdditionalData**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-212"><span id="DontSendAdditionalData"></span><span id="dontsendadditionaldata"></span><span id="DONTSENDADDITIONALDATA"></span>**DontSendAdditionalData**</span></span>
</dt> <dd>

<span data-ttu-id="2b5c2-213">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-213">**REG\_DWORD**</span></span>

<span data-ttu-id="2b5c2-214">Valores posibles:</span><span class="sxs-lookup"><span data-stu-id="2b5c2-214">Possible values:</span></span><dl> <dd><span data-ttu-id="2b5c2-215">0: enviar (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="2b5c2-215">0 - Send (default)</span></span></dd> <dd><span data-ttu-id="2b5c2-216">1: no enviar</span><span class="sxs-lookup"><span data-stu-id="2b5c2-216">1 - Do not send</span></span></dd> </dl>

<span data-ttu-id="2b5c2-217">Si se va a impedir el envío de datos de segundo nivel</span><span class="sxs-lookup"><span data-stu-id="2b5c2-217">Whether to prevent sending second-level data</span></span>

</dd> <dt>

<span data-ttu-id="2b5c2-218"><span id="ExcludedApplications__Application_Name_"></span><span id="excludedapplications__application_name_"></span><span id="EXCLUDEDAPPLICATIONS__APPLICATION_NAME_"></span>**Nombre de la \\ \[ aplicación ExcludedApplications\]**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-218"><span id="ExcludedApplications__Application_Name_"></span><span id="excludedapplications__application_name_"></span><span id="EXCLUDEDAPPLICATIONS__APPLICATION_NAME_"></span>**ExcludedApplications\\\[Application Name\]**</span></span>
</dt> <dd>

<span data-ttu-id="2b5c2-219">**Registro \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-219">**REG\_SZ**</span></span>

<span data-ttu-id="2b5c2-220">Usar [ **WerAddExcludedApplication**](/windows/desktop/api/Werapi/nf-werapi-weraddexcludedapplication)</span><span class="sxs-lookup"><span data-stu-id="2b5c2-220">Use [**WerAddExcludedApplication**](/windows/desktop/api/Werapi/nf-werapi-weraddexcludedapplication)</span></span>

<span data-ttu-id="2b5c2-221">Lista de aplicaciones excluidas</span><span class="sxs-lookup"><span data-stu-id="2b5c2-221">List of excluded applications</span></span>

</dd> <dt>

<span data-ttu-id="2b5c2-222"><span id="ForceQueue"></span><span id="forcequeue"></span><span id="FORCEQUEUE"></span>**ForceQueue**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-222"><span id="ForceQueue"></span><span id="forcequeue"></span><span id="FORCEQUEUE"></span>**ForceQueue**</span></span>
</dt> <dd>

<span data-ttu-id="2b5c2-223">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-223">**REG\_DWORD**</span></span>

<span data-ttu-id="2b5c2-224">Valores posibles:</span><span class="sxs-lookup"><span data-stu-id="2b5c2-224">Possible values:</span></span><dl> <dd><span data-ttu-id="2b5c2-225">0: no (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="2b5c2-225">0 - No (default)</span></span></dd> <dd><span data-ttu-id="2b5c2-226">1: Sí</span><span class="sxs-lookup"><span data-stu-id="2b5c2-226">1 - Yes</span></span></dd> </dl>

<span data-ttu-id="2b5c2-227">Si se van a enviar todos los informes a la cola del usuario</span><span class="sxs-lookup"><span data-stu-id="2b5c2-227">Whether to send all reports to the user's queue</span></span>

</dd> <dt>

<span data-ttu-id="2b5c2-228"><span id="LocalDumps_DumpFolder_or_LocalDumps__Application_Name__DumpFolder"></span><span id="localdumps_dumpfolder_or_localdumps__application_name__dumpfolder"></span><span id="LOCALDUMPS_DUMPFOLDER_OR_LOCALDUMPS__APPLICATION_NAME__DUMPFOLDER"></span>**LocalDumps \\ DumpFolder** o **LocalDumps \\ \[ nombre de aplicación \] \\ DumpFolder**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-228"><span id="LocalDumps_DumpFolder_or_LocalDumps__Application_Name__DumpFolder"></span><span id="localdumps_dumpfolder_or_localdumps__application_name__dumpfolder"></span><span id="LOCALDUMPS_DUMPFOLDER_OR_LOCALDUMPS__APPLICATION_NAME__DUMPFOLDER"></span>**LocalDumps\\DumpFolder** or **LocalDumps\\\[Application Name\]\\DumpFolder**</span></span>
</dt> <dd>

<span data-ttu-id="2b5c2-229">**REG \_ expandir \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-229">**REG\_EXPAND\_SZ**</span></span>

<span data-ttu-id="2b5c2-230">Ruta de acceso al directorio.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-230">The directory path.</span></span> <span data-ttu-id="2b5c2-231">El valor predeterminado es% LOCALAPPDATA% \\ CrashDumps.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-231">The default value is %LOCALAPPDATA%\\CrashDumps.</span></span> <span data-ttu-id="2b5c2-232">Si no se usa el valor predeterminado, la aplicación debe asegurarse de que la carpeta tiene una ACL suficiente.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-232">If the default is not used, the application must ensure that the folder has a sufficient ACL.</span></span>

<span data-ttu-id="2b5c2-233">**Windows Vista:** No se admiten los valores del registro en la clave **LocalDumps** .</span><span class="sxs-lookup"><span data-stu-id="2b5c2-233">**Windows Vista:** The registry values under the **LocalDumps** key are not supported.</span></span> <span data-ttu-id="2b5c2-234">Tenga en cuenta que este comportamiento cambió con Windows Server 2008 y Windows Vista con Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="2b5c2-234">Note that this behavior changed with Windows Server 2008 and Windows Vista with Service Pack 1 (SP1).</span></span>

<span data-ttu-id="2b5c2-235">La ruta de acceso donde se almacenarán los archivos de volcado.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-235">The path where the dump files are to be stored.</span></span>

<span data-ttu-id="2b5c2-236">Tenga en cuenta que la configuración por proceso invalidará cualquier configuración global que exista para obtener más información, consulte [recopilación de volcados de User-Mode](collecting-user-mode-dumps.md).</span><span class="sxs-lookup"><span data-stu-id="2b5c2-236">Note that per-process settings will override any global settings that exist For more information, see [Collecting User-Mode Dumps](collecting-user-mode-dumps.md).</span></span>

<span data-ttu-id="2b5c2-237">Esta configuración no se admite en el subárbol del registro de **\_ \_ usuario actual HKEY** .</span><span class="sxs-lookup"><span data-stu-id="2b5c2-237">This setting is not supported in the **HKEY\_CURRENT\_USER** registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="2b5c2-238"><span id="LocalDumps_DumpCount_or_LocalDumps__Application_Name__DumpCount"></span><span id="localdumps_dumpcount_or_localdumps__application_name__dumpcount"></span><span id="LOCALDUMPS_DUMPCOUNT_OR_LOCALDUMPS__APPLICATION_NAME__DUMPCOUNT"></span>**LocalDumps \\ DumpCount** o **LocalDumps \\ \[ nombre de aplicación \] \\ DumpCount**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-238"><span id="LocalDumps_DumpCount_or_LocalDumps__Application_Name__DumpCount"></span><span id="localdumps_dumpcount_or_localdumps__application_name__dumpcount"></span><span id="LOCALDUMPS_DUMPCOUNT_OR_LOCALDUMPS__APPLICATION_NAME__DUMPCOUNT"></span>**LocalDumps\\DumpCount** or **LocalDumps\\\[Application Name\]\\DumpCount**</span></span>
</dt> <dd>

<span data-ttu-id="2b5c2-239">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-239">**REG\_DWORD**</span></span>

<span data-ttu-id="2b5c2-240">Número máximo.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-240">The maximum number.</span></span> <span data-ttu-id="2b5c2-241">El valor predeterminado es 10.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-241">The default is 10.</span></span> <span data-ttu-id="2b5c2-242">Cuando se supera el valor máximo, el archivo de volcado más antiguo de la carpeta se reemplazará por el nuevo archivo de volcado de memoria.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-242">When the maximum value is exceeded, the oldest dump file in the folder will be replaced with the new dump file.</span></span>

<span data-ttu-id="2b5c2-243">**Windows Vista:** No se admiten los valores del registro en la clave **LocalDumps** .</span><span class="sxs-lookup"><span data-stu-id="2b5c2-243">**Windows Vista:** The registry values under the **LocalDumps** key are not supported.</span></span> <span data-ttu-id="2b5c2-244">Tenga en cuenta que este comportamiento cambió con Windows Server 2008 y Windows Vista con SP1.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-244">Note that this behavior changed with Windows Server 2008 and Windows Vista with SP1.</span></span>

<span data-ttu-id="2b5c2-245">Número máximo de archivos de volcado en la carpeta.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-245">The maximum number of dump files in the folder.</span></span>

<span data-ttu-id="2b5c2-246">Esta configuración no se admite en el subárbol del registro de **\_ \_ usuario actual HKEY** .</span><span class="sxs-lookup"><span data-stu-id="2b5c2-246">This setting is not supported in the **HKEY\_CURRENT\_USER** registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="2b5c2-247"><span id="LocalDumps_DumpType_or_LocalDumps__Application_Name__DumpType"></span><span id="localdumps_dumptype_or_localdumps__application_name__dumptype"></span><span id="LOCALDUMPS_DUMPTYPE_OR_LOCALDUMPS__APPLICATION_NAME__DUMPTYPE"></span>**LocalDumps \\ DumpType** o **LocalDumps \\ \[ nombre de aplicación \] \\ DumpType**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-247"><span id="LocalDumps_DumpType_or_LocalDumps__Application_Name__DumpType"></span><span id="localdumps_dumptype_or_localdumps__application_name__dumptype"></span><span id="LOCALDUMPS_DUMPTYPE_OR_LOCALDUMPS__APPLICATION_NAME__DUMPTYPE"></span>**LocalDumps\\DumpType** or **LocalDumps\\\[Application Name\]\\DumpType**</span></span>
</dt> <dd>

<span data-ttu-id="2b5c2-248">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-248">**REG\_DWORD**</span></span>

<span data-ttu-id="2b5c2-249">Valores posibles:</span><span class="sxs-lookup"><span data-stu-id="2b5c2-249">Possible values:</span></span><dl> <dd><span data-ttu-id="2b5c2-250">0: volcado de memoria personalizado</span><span class="sxs-lookup"><span data-stu-id="2b5c2-250">0 - Custom dump</span></span></dd> <dd><span data-ttu-id="2b5c2-251">1-minivolcado (predeterminado)</span><span class="sxs-lookup"><span data-stu-id="2b5c2-251">1 - Minidump (default)</span></span></dd> <dd><span data-ttu-id="2b5c2-252">2-volcado completo</span><span class="sxs-lookup"><span data-stu-id="2b5c2-252">2 - Full dump</span></span></dd> </dl>

<span data-ttu-id="2b5c2-253">**Windows Vista:** No se admiten los valores del registro en la clave **LocalDumps** .</span><span class="sxs-lookup"><span data-stu-id="2b5c2-253">**Windows Vista:** The registry values under the **LocalDumps** key are not supported.</span></span> <span data-ttu-id="2b5c2-254">Tenga en cuenta que este comportamiento cambió con Windows Server 2008 y Windows Vista con SP1.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-254">Note that this behavior changed with Windows Server 2008 and Windows Vista with SP1.</span></span>

<span data-ttu-id="2b5c2-255">El tipo de volcado.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-255">The dump type.</span></span>

<span data-ttu-id="2b5c2-256">Esta configuración no se admite en el subárbol del registro de **\_ \_ usuario actual HKEY** .</span><span class="sxs-lookup"><span data-stu-id="2b5c2-256">This setting is not supported in the **HKEY\_CURRENT\_USER** registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="2b5c2-257"><span id="LocalDumps_CustomDumpFlags_or_LocalDumps__Application_Name__CustomDumpFlags"></span><span id="localdumps_customdumpflags_or_localdumps__application_name__customdumpflags"></span><span id="LOCALDUMPS_CUSTOMDUMPFLAGS_OR_LOCALDUMPS__APPLICATION_NAME__CUSTOMDUMPFLAGS"></span>**LocalDumps \\ CustomDumpFlags** o **LocalDumps \\ \[ nombre de aplicación \] \\ CustomDumpFlags**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-257"><span id="LocalDumps_CustomDumpFlags_or_LocalDumps__Application_Name__CustomDumpFlags"></span><span id="localdumps_customdumpflags_or_localdumps__application_name__customdumpflags"></span><span id="LOCALDUMPS_CUSTOMDUMPFLAGS_OR_LOCALDUMPS__APPLICATION_NAME__CUSTOMDUMPFLAGS"></span>**LocalDumps\\CustomDumpFlags** or **LocalDumps\\\[Application Name\]\\CustomDumpFlags**</span></span>
</dt> <dd>

<span data-ttu-id="2b5c2-258">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-258">**REG\_DWORD**</span></span>

<span data-ttu-id="2b5c2-259">Uno o más valores de la enumeración de [**\_ tipo de minivolcado**](/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type) .</span><span class="sxs-lookup"><span data-stu-id="2b5c2-259">One or more values from the [**MINIDUMP\_TYPE**](/windows/desktop/api/minidumpapiset/ne-minidumpapiset-minidump_type) enumeration.</span></span> <span data-ttu-id="2b5c2-260">El valor predeterminado es {**MiniDumpWithDataSegs** \| **MiniDumpWithUnloadedModules** \| **MiniDumpWithProcessThreadData**}.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-260">The default is {**MiniDumpWithDataSegs**\|**MiniDumpWithUnloadedModules**\|**MiniDumpWithProcessThreadData**}.</span></span>

<span data-ttu-id="2b5c2-261">**Windows Vista:** No se admiten los valores del registro en la clave **LocalDumps** .</span><span class="sxs-lookup"><span data-stu-id="2b5c2-261">**Windows Vista:** The registry values under the **LocalDumps** key are not supported.</span></span> <span data-ttu-id="2b5c2-262">Tenga en cuenta que este comportamiento cambió con Windows Server 2008 y Windows Vista con SP1.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-262">Note that this behavior changed with Windows Server 2008 and Windows Vista with SP1.</span></span>

<span data-ttu-id="2b5c2-263">Opciones de volcado de memoria personalizadas que se van a utilizar.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-263">The custom dump options to be used.</span></span> <span data-ttu-id="2b5c2-264">Este valor solo se usa cuando **DumpType** se establece en 0.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-264">This value is used only when **DumpType** is set to 0.</span></span>

<span data-ttu-id="2b5c2-265">Esta configuración no se admite en el subárbol del registro de **\_ \_ usuario actual HKEY** .</span><span class="sxs-lookup"><span data-stu-id="2b5c2-265">This setting is not supported in the **HKEY\_CURRENT\_USER** registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="2b5c2-266"><span id="LoggingDisabled"></span><span id="loggingdisabled"></span><span id="LOGGINGDISABLED"></span>**LoggingDisabled**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-266"><span id="LoggingDisabled"></span><span id="loggingdisabled"></span><span id="LOGGINGDISABLED"></span>**LoggingDisabled**</span></span>
</dt> <dd>

<span data-ttu-id="2b5c2-267">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-267">**REG\_DWORD**</span></span>

<span data-ttu-id="2b5c2-268">Valores posibles:</span><span class="sxs-lookup"><span data-stu-id="2b5c2-268">Possible values:</span></span><dl> <dd><span data-ttu-id="2b5c2-269">0: habilitado (valor predeterminado)</span><span class="sxs-lookup"><span data-stu-id="2b5c2-269">0–Enabled (default)</span></span></dd> <dd><span data-ttu-id="2b5c2-270">1: deshabilitado</span><span class="sxs-lookup"><span data-stu-id="2b5c2-270">1–Disabled</span></span></dd> </dl>

<span data-ttu-id="2b5c2-271">Habilitar o deshabilitar el registro</span><span class="sxs-lookup"><span data-stu-id="2b5c2-271">Enable or disable logging</span></span>

</dd> <dt>

<span data-ttu-id="2b5c2-272"><span id="MaxArchiveCount"></span><span id="maxarchivecount"></span><span id="MAXARCHIVECOUNT"></span>**MaxArchiveCount**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-272"><span id="MaxArchiveCount"></span><span id="maxarchivecount"></span><span id="MAXARCHIVECOUNT"></span>**MaxArchiveCount**</span></span>
</dt> <dd>

<span data-ttu-id="2b5c2-273">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-273">**REG\_DWORD**</span></span>

<span data-ttu-id="2b5c2-274">Rango de valores posibles: 1 – 5000.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-274">Range of possible values: 1–5000.</span></span> <span data-ttu-id="2b5c2-275">El valor predeterminado es 1000.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-275">The default is 1000.</span></span>

<span data-ttu-id="2b5c2-276">Tamaño máximo del archivo, en archivos</span><span class="sxs-lookup"><span data-stu-id="2b5c2-276">Maximum size of the archive, in files</span></span>

</dd> <dt>

<span data-ttu-id="2b5c2-277"><span id="MaxQueueCount"></span><span id="maxqueuecount"></span><span id="MAXQUEUECOUNT"></span>**MaxQueueCount**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-277"><span id="MaxQueueCount"></span><span id="maxqueuecount"></span><span id="MAXQUEUECOUNT"></span>**MaxQueueCount**</span></span>
</dt> <dd>

<span data-ttu-id="2b5c2-278">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-278">**REG\_DWORD**</span></span>

<span data-ttu-id="2b5c2-279">Rango de valores posibles: 1 – 500.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-279">Range of possible values: 1–500.</span></span> <span data-ttu-id="2b5c2-280">El valor predeterminado es 50.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-280">The default is 50.</span></span>

<span data-ttu-id="2b5c2-281">Tamaño máximo de la cola</span><span class="sxs-lookup"><span data-stu-id="2b5c2-281">Maximum size of the queue</span></span>

</dd> <dt>

<span data-ttu-id="2b5c2-282"><span id="QueuePesterInterval"></span><span id="queuepesterinterval"></span><span id="QUEUEPESTERINTERVAL"></span>**QueuePesterInterval**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-282"><span id="QueuePesterInterval"></span><span id="queuepesterinterval"></span><span id="QUEUEPESTERINTERVAL"></span>**QueuePesterInterval**</span></span>
</dt> <dd>

<span data-ttu-id="2b5c2-283">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-283">**REG\_DWORD**</span></span>

<span data-ttu-id="2b5c2-284">Número de días</span><span class="sxs-lookup"><span data-stu-id="2b5c2-284">Number of days</span></span>

<span data-ttu-id="2b5c2-285">Intervalo entre recordatorios al usuario para buscar soluciones, en días</span><span class="sxs-lookup"><span data-stu-id="2b5c2-285">Interval between reminders to the user to check for solutions, in days</span></span>

</dd> <dt>

<span data-ttu-id="2b5c2-286"><span id="RuntimeExceptionHelperModules___pwszOutOfProcessCallbackDll_name_including_path_"></span><span id="runtimeexceptionhelpermodules___pwszoutofprocesscallbackdll_name_including_path_"></span><span id="RUNTIMEEXCEPTIONHELPERMODULES___PWSZOUTOFPROCESSCALLBACKDLL_NAME_INCLUDING_PATH_"></span>**RuntimeExceptionHelperModules! \[ nombre de pwszOutOfProcessCallbackDll que incluye la ruta de acceso\]**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-286"><span id="RuntimeExceptionHelperModules___pwszOutOfProcessCallbackDll_name_including_path_"></span><span id="runtimeexceptionhelpermodules___pwszoutofprocesscallbackdll_name_including_path_"></span><span id="RUNTIMEEXCEPTIONHELPERMODULES___PWSZOUTOFPROCESSCALLBACKDLL_NAME_INCLUDING_PATH_"></span>**RuntimeExceptionHelperModules!\[ pwszOutOfProcessCallbackDll name including path\]**</span></span>
</dt> <dd>

<span data-ttu-id="2b5c2-287">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-287">**REG\_DWORD**</span></span>

<span data-ttu-id="2b5c2-288">Se omite el contenido del valor.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-288">The contents of the value are ignored.</span></span>

<span data-ttu-id="2b5c2-289">El nombre del valor se usa para capturar el valor de pwszOutOfProcessCallbackDll.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-289">The name of the value is used to fetch the pwszOutOfProcessCallbackDll value.</span></span>

<span data-ttu-id="2b5c2-290">**Windows server 2008, Windows Vista, Windows server 2003 y Windows XP:** No se admite este valor del registro.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-290">**Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:** This registry value is not supported.</span></span>

</dd> </dl>

## <a name="wer-live-kernel-reports-settings"></a><span data-ttu-id="2b5c2-291">Configuración de informes de kernel Live de WER</span><span class="sxs-lookup"><span data-stu-id="2b5c2-291">WER Live Kernel Reports Settings</span></span>

<span data-ttu-id="2b5c2-292">La configuración de informes de kernel en directo de WER, que se describe a continuación, se encuentra en la siguiente subclave del registro:</span><span class="sxs-lookup"><span data-stu-id="2b5c2-292">WER's Live Kernel Reports settings, which are described next, are both located under the following registry subkey:</span></span>

-   <span data-ttu-id="2b5c2-293">**HKEY \_ \_** \\  \\  \\ **Control** CurrentControlSet del sistema \\  de equipo local CrashControl</span><span class="sxs-lookup"><span data-stu-id="2b5c2-293">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Control**\\**CrashControl**</span></span>

## <a name="fulllivekernelreports-subkey"></a><span data-ttu-id="2b5c2-294">Subclave FullLiveKernelReports</span><span class="sxs-lookup"><span data-stu-id="2b5c2-294">FullLiveKernelReports subkey</span></span>

<dl> <dt>

<span data-ttu-id="2b5c2-295"><span id="ComponentThrottleThreshold"></span><span id="componentthrottlethreshold"></span><span id="COMPONENTTHROTTLETHRESHOLD"></span>**ComponentThrottleThreshold**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-295"><span id="ComponentThrottleThreshold"></span><span id="componentthrottlethreshold"></span><span id="COMPONENTTHROTTLETHRESHOLD"></span>**ComponentThrottleThreshold**</span></span>
</dt> <dd>

<span data-ttu-id="2b5c2-296">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-296">**REG\_DWORD**</span></span>

<span data-ttu-id="2b5c2-297">El umbral (en horas) de la frecuencia con la que cualquier componente individual puede crear un volcado en vivo completo.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-297">The threshold (in hours) of how often any single component can create a full live dump.</span></span> <span data-ttu-id="2b5c2-298">Este valor debe ser mayor o igual que **SystemThrottleThreshold**.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-298">This value must be greater than or equal to **SystemThrottleThreshold**.</span></span> <span data-ttu-id="2b5c2-299">Si se establece en cero (0), se deshabilitará toda la limitación basada en el tiempo.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-299">Setting both to zero (0) will disable all time-based throttling.</span></span> <span data-ttu-id="2b5c2-300">El valor predeterminado es 168 (7 días).</span><span class="sxs-lookup"><span data-stu-id="2b5c2-300">The default is 168 (7 days).</span></span>

</dd> <dt>

<span data-ttu-id="2b5c2-301"><span id="FullLiveReportsMax"></span><span id="fulllivereportsmax"></span><span id="FULLLIVEREPORTSMAX"></span>**FullLiveReportsMax**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-301"><span id="FullLiveReportsMax"></span><span id="fulllivereportsmax"></span><span id="FULLLIVEREPORTSMAX"></span>**FullLiveReportsMax**</span></span>
</dt> <dd>

<span data-ttu-id="2b5c2-302">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-302">**REG\_DWORD**</span></span>

<span data-ttu-id="2b5c2-303">El número máximo de volcados en vivo completos que pueden estar en el disco en un momento dado.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-303">The maximum number of full live dumps that may be on disk at any given time.</span></span> <span data-ttu-id="2b5c2-304">El valor predeterminado es 1.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-304">The default is 1.</span></span> <span data-ttu-id="2b5c2-305">Si se establece este valor en cero (0), se deshabilitará la característica de volcado en vivo.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-305">Setting this value to zero (0) will disable the live dump feature.</span></span>

</dd> <dt>

<span data-ttu-id="2b5c2-306"><span id="LastFullLiveReport"></span><span id="lastfulllivereport"></span><span id="LASTFULLLIVEREPORT"></span>**LastFullLiveReport**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-306"><span id="LastFullLiveReport"></span><span id="lastfulllivereport"></span><span id="LASTFULLLIVEREPORT"></span>**LastFullLiveReport**</span></span>
</dt> <dd>

<span data-ttu-id="2b5c2-307">**QWord de REG \_**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-307">**REG\_QWORD**</span></span>

<span data-ttu-id="2b5c2-308">Un [SystemTime](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) que indica la hora del último informe activo, del sistema o de un reportType específico.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-308">A [SystemTime](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) indicating the last full live report time, for the system or a specific ReportType.</span></span> <span data-ttu-id="2b5c2-309">Se usa para calcular si se ha satisfecho un umbral de la Directiva.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-309">This is used to calculate whether a policy threshold has been satisfied.</span></span>

</dd> <dt>

<span data-ttu-id="2b5c2-310"><span id="SystemThrottleThreshold"></span><span id="systemthrottlethreshold"></span><span id="SYSTEMTHROTTLETHRESHOLD"></span>**SystemThrottleThreshold**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-310"><span id="SystemThrottleThreshold"></span><span id="systemthrottlethreshold"></span><span id="SYSTEMTHROTTLETHRESHOLD"></span>**SystemThrottleThreshold**</span></span>
</dt> <dd>

<span data-ttu-id="2b5c2-311">**\_valor DWORD reg**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-311">**REG\_DWORD**</span></span>

<span data-ttu-id="2b5c2-312">El umbral (en horas) de la frecuencia con la que cualquier componente del sistema puede crear un volcado en vivo completo.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-312">The threshold (in hours) of how often any component on the system can create a full live dump.</span></span> <span data-ttu-id="2b5c2-313">El valor predeterminado es 120 (5 días).</span><span class="sxs-lookup"><span data-stu-id="2b5c2-313">The default is 120 (5 days).</span></span>

</dd> </dl>

## <a name="livekernelreports-subkey"></a><span data-ttu-id="2b5c2-314">Subclave LiveKernelReports</span><span class="sxs-lookup"><span data-stu-id="2b5c2-314">LiveKernelReports subkey</span></span>

<dl> <dt>

<span data-ttu-id="2b5c2-315"><span id="LiveKernelReportsPath"></span><span id="livekernelreportspath"></span><span id="LIVEKERNELREPORTSPATH"></span>**LiveKernelReportsPath**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-315"><span id="LiveKernelReportsPath"></span><span id="livekernelreportspath"></span><span id="LIVEKERNELREPORTSPATH"></span>**LiveKernelReportsPath**</span></span>
</dt> <dd>

<span data-ttu-id="2b5c2-316">**Registro \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="2b5c2-316">**REG\_SZ**</span></span>


<span data-ttu-id="2b5c2-317">La ubicación de almacenamiento Redirigido de los informes de kernel en vivo.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-317">The redirected storage location of live kernel reports.</span></span> <span data-ttu-id="2b5c2-318">La ubicación predeterminada es%systemroot%\LiveKernelReports.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-318">The default location is %systemroot%\LiveKernelReports.</span></span> <span data-ttu-id="2b5c2-319">Este valor debe ser una ruta de acceso válida.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-319">This value must be a valid path.</span></span> <span data-ttu-id="2b5c2-320">La ruta de acceso debe tener el formato de ruta de acceso NT.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-320">The path must be in NT path format.</span></span> <span data-ttu-id="2b5c2-321">Por ejemplo, \? ? \c: \LiveDumpsFolder.</span><span class="sxs-lookup"><span data-stu-id="2b5c2-321">For example, \??\C:\LiveDumpsFolder.</span></span>  <span data-ttu-id="2b5c2-322">Para obtener más información sobre los formatos de ruta de acceso, vea  [formatos de ruta de acceso de archivo en sistemas Windows](/dotnet/standard/io/file-path-formats).</span><span class="sxs-lookup"><span data-stu-id="2b5c2-322">For more information on path formats, see  [File path formats on Windows systems](/dotnet/standard/io/file-path-formats).</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="2b5c2-323">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2b5c2-323">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b5c2-324">Referencia de WER</span><span class="sxs-lookup"><span data-stu-id="2b5c2-324">WER Reference</span></span>](wer-reference.md)
</dt> </dl>

 

 
