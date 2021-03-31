---
title: Auditoría
description: La plataforma de filtrado de Windows (WFP) proporciona auditoría de eventos relacionados con IPsec y firewall.
ms.assetid: 30ff9cf7-bf93-4979-bacd-d76e5dadbef6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cef1d4fee81afc366a987575935c1de8880092c
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/18/2020
ms.locfileid: "103995797"
---
# <a name="auditing"></a><span data-ttu-id="6c817-103">Auditoría</span><span class="sxs-lookup"><span data-stu-id="6c817-103">Auditing</span></span>

<span data-ttu-id="6c817-104">La plataforma de filtrado de Windows (WFP) proporciona auditoría de eventos relacionados con IPsec y firewall.</span><span class="sxs-lookup"><span data-stu-id="6c817-104">The Windows Filtering Platform (WFP) provides auditing of firewall and IPsec related events.</span></span> <span data-ttu-id="6c817-105">Estos eventos se almacenan en el registro de seguridad del sistema.</span><span class="sxs-lookup"><span data-stu-id="6c817-105">These events are stored in the system security log.</span></span>

<span data-ttu-id="6c817-106">Los eventos auditados son los siguientes.</span><span class="sxs-lookup"><span data-stu-id="6c817-106">The audited events are as follows.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6c817-107">Categoría de auditoría</span><span class="sxs-lookup"><span data-stu-id="6c817-107">Auditing category</span></span></th>
<th><span data-ttu-id="6c817-108">Subcategoría de auditoría</span><span class="sxs-lookup"><span data-stu-id="6c817-108">Auditing subcategory</span></span></th>
<th><span data-ttu-id="6c817-109">Eventos auditados</span><span class="sxs-lookup"><span data-stu-id="6c817-109">Audited events</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6c817-110">Cambio de directiva</span><span class="sxs-lookup"><span data-stu-id="6c817-110">Policy Change</span></span><br/> <span data-ttu-id="6c817-111">{6997984D-797A-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="6c817-111">{6997984D-797A-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="6c817-112">Filtrar cambio de directiva de plataforma</span><span class="sxs-lookup"><span data-stu-id="6c817-112">Filtering Platform Policy Change</span></span><br/> <span data-ttu-id="6c817-113">{0CCE9233-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="6c817-113">{0CCE9233-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="6c817-114">Los números representan los identificadores de evento que se muestran en Visor de eventos (eventvwr.exe).</span><span class="sxs-lookup"><span data-stu-id="6c817-114">The numbers represent the Event IDs as displayed by Event Viewer (eventvwr.exe).</span></span>
</blockquote>
<br/> <span data-ttu-id="6c817-115">Adición y eliminación de objetos de WFP:</span><span class="sxs-lookup"><span data-stu-id="6c817-115">WFP object addition and removal:</span></span><br/>
<ul>
<li><span data-ttu-id="6c817-116">5440 llamada persistente agregada</span><span class="sxs-lookup"><span data-stu-id="6c817-116">5440 Persistent callout added</span></span></li>
<li><span data-ttu-id="6c817-117">5441 tiempo de arranque o filtro persistente agregado</span><span class="sxs-lookup"><span data-stu-id="6c817-117">5441 Boot-time or persistent filter added</span></span></li>
<li><span data-ttu-id="6c817-118">5442 proveedor persistente agregado</span><span class="sxs-lookup"><span data-stu-id="6c817-118">5442 Persistent provider added</span></span></li>
<li><span data-ttu-id="6c817-119">5443 contexto de proveedor persistente agregado</span><span class="sxs-lookup"><span data-stu-id="6c817-119">5443 Persistent provider context added</span></span></li>
<li><span data-ttu-id="6c817-120">5444 subcapa persistente agregada</span><span class="sxs-lookup"><span data-stu-id="6c817-120">5444 Persistent sub-layer added</span></span></li>
<li><span data-ttu-id="6c817-121">llamada en tiempo de ejecución de 5446 agregada o quitada</span><span class="sxs-lookup"><span data-stu-id="6c817-121">5446 Run-time callout added or removed</span></span></li>
<li><span data-ttu-id="6c817-122">5447 filtro en tiempo de ejecución agregado o quitado</span><span class="sxs-lookup"><span data-stu-id="6c817-122">5447 Run-time filter added or removed</span></span></li>
<li><span data-ttu-id="6c817-123">5448 proveedor en tiempo de ejecución agregado o quitado</span><span class="sxs-lookup"><span data-stu-id="6c817-123">5448 Run-time provider added or removed</span></span></li>
<li><span data-ttu-id="6c817-124">5449 contexto de proveedor en tiempo de ejecución agregado o quitado</span><span class="sxs-lookup"><span data-stu-id="6c817-124">5449 Run-time provider context added or removed</span></span></li>
<li><span data-ttu-id="6c817-125">5450 subcapa en tiempo de ejecución agregada o quitada</span><span class="sxs-lookup"><span data-stu-id="6c817-125">5450 Run-time sub-layer added or removed</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6c817-126">Acceso a objetos</span><span class="sxs-lookup"><span data-stu-id="6c817-126">Object Access</span></span><br/> <span data-ttu-id="6c817-127">{6997984A-797A-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="6c817-127">{6997984A-797A-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="6c817-128">Filtrar eliminación de paquetes de plataforma</span><span class="sxs-lookup"><span data-stu-id="6c817-128">Filtering Platform Packet Drop</span></span> <br/> <span data-ttu-id="6c817-129">{0CCE9225-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="6c817-129">{0CCE9225-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="6c817-130">Paquetes descartados por WFP:</span><span class="sxs-lookup"><span data-stu-id="6c817-130">Packets dropped by WFP:</span></span><br/>
<ul>
<li><span data-ttu-id="6c817-131">paquete 5152 quitado</span><span class="sxs-lookup"><span data-stu-id="6c817-131">5152 Packet dropped</span></span></li>
<li><span data-ttu-id="6c817-132">paquete 5153 vetado</span><span class="sxs-lookup"><span data-stu-id="6c817-132">5153 Packet vetoed</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6c817-133">Acceso a objetos</span><span class="sxs-lookup"><span data-stu-id="6c817-133">Object Access</span></span><br/></td>
<td><span data-ttu-id="6c817-134">Filtrar conexión de plataforma</span><span class="sxs-lookup"><span data-stu-id="6c817-134">Filtering Platform Connection</span></span> <br/> <span data-ttu-id="6c817-135">{0CCE9226-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="6c817-135">{0CCE9226-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="6c817-136">Conexiones permitidas y bloqueadas:</span><span class="sxs-lookup"><span data-stu-id="6c817-136">Allowed and blocked connections:</span></span><br/>
<ul>
<li><span data-ttu-id="6c817-137">5154 escucha permitida</span><span class="sxs-lookup"><span data-stu-id="6c817-137">5154 Listen permitted</span></span></li>
<li><span data-ttu-id="6c817-138">5155 escucha bloqueada</span><span class="sxs-lookup"><span data-stu-id="6c817-138">5155 Listen blocked</span></span></li>
<li><span data-ttu-id="6c817-139">5156 conexión permitida</span><span class="sxs-lookup"><span data-stu-id="6c817-139">5156 Connection permitted</span></span></li>
<li><span data-ttu-id="6c817-140">5157 conexión bloqueada</span><span class="sxs-lookup"><span data-stu-id="6c817-140">5157 Connection blocked</span></span></li>
<li><span data-ttu-id="6c817-141">5158 enlace permitido</span><span class="sxs-lookup"><span data-stu-id="6c817-141">5158 Bind permitted</span></span></li>
<li><span data-ttu-id="6c817-142">5159 enlace bloqueado</span><span class="sxs-lookup"><span data-stu-id="6c817-142">5159 Bind blocked</span></span></li>
</ul>
<blockquote>
[!Note]<br />
<span data-ttu-id="6c817-143">Las conexiones permitidas no siempre auditan el identificador del filtro asociado.</span><span class="sxs-lookup"><span data-stu-id="6c817-143">Permitted connections do not always audit the ID of the associated filter.</span></span> <span data-ttu-id="6c817-144">El valor de FilterID para TCP será 0 a menos que se use un subconjunto de estas condiciones de filtrado: UserID, AppID, protocolo, Puerto remoto.</span><span class="sxs-lookup"><span data-stu-id="6c817-144">The FilterID for TCP will be 0 unless a subset of these filtering conditions are used: UserID, AppID, Protocol, Remote Port.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6c817-145">Acceso a objetos</span><span class="sxs-lookup"><span data-stu-id="6c817-145">Object Access</span></span><br/></td>
<td><span data-ttu-id="6c817-146">Otros eventos de acceso a objetos</span><span class="sxs-lookup"><span data-stu-id="6c817-146">Other Object Access Events</span></span><br/> <span data-ttu-id="6c817-147">{0CCE9227-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="6c817-147">{0CCE9227-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><blockquote>
[!Note]<br />
<span data-ttu-id="6c817-148">Esta subcategoría habilita muchas auditorías.</span><span class="sxs-lookup"><span data-stu-id="6c817-148">This subcategory enables many audits.</span></span> <span data-ttu-id="6c817-149">A continuación se enumeran las auditorías específicas de WFP.</span><span class="sxs-lookup"><span data-stu-id="6c817-149">WFP specific audits are listed below.</span></span>
</blockquote>
<br/> <span data-ttu-id="6c817-150">Estado de prevención de denegación de servicio:</span><span class="sxs-lookup"><span data-stu-id="6c817-150">Denial of Service prevention status:</span></span><br/>
<ul>
<li><span data-ttu-id="6c817-151">5148 modo de prevención de DoS de WFP iniciado</span><span class="sxs-lookup"><span data-stu-id="6c817-151">5148 WFP DoS prevention mode started</span></span></li>
<li><span data-ttu-id="6c817-152">5149 modo de prevención de DoS de WFP detenido</span><span class="sxs-lookup"><span data-stu-id="6c817-152">5149 WFP DoS prevention mode stopped</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6c817-153">Inicio/cierre de sesión</span><span class="sxs-lookup"><span data-stu-id="6c817-153">Logon/Logoff</span></span><br/> <span data-ttu-id="6c817-154">{69979849-797A-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="6c817-154">{69979849-797A-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="6c817-155">Modo principal de IPsec</span><span class="sxs-lookup"><span data-stu-id="6c817-155">IPsec Main Mode</span></span><br/> <span data-ttu-id="6c817-156">{0CCE9218-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="6c817-156">{0CCE9218-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="6c817-157">Negociación del modo principal de IKE y AuthIP:</span><span class="sxs-lookup"><span data-stu-id="6c817-157">IKE and AuthIP Main Mode negotiation:</span></span><br/>
<ul>
<li><span data-ttu-id="6c817-158">4650, 4651 Asociación de seguridad establecida</span><span class="sxs-lookup"><span data-stu-id="6c817-158">4650, 4651 Security association established</span></span></li>
<li><span data-ttu-id="6c817-159">4652, error de negociación de 4653</span><span class="sxs-lookup"><span data-stu-id="6c817-159">4652, 4653 Negotiation failed</span></span></li>
<li><span data-ttu-id="6c817-160">4655 finalizó la Asociación de seguridad</span><span class="sxs-lookup"><span data-stu-id="6c817-160">4655 Security association ended</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6c817-161">Inicio/cierre de sesión</span><span class="sxs-lookup"><span data-stu-id="6c817-161">Logon/Logoff</span></span><br/></td>
<td><span data-ttu-id="6c817-162">Modo rápido de IPsec</span><span class="sxs-lookup"><span data-stu-id="6c817-162">IPsec Quick Mode</span></span> <br/> <span data-ttu-id="6c817-163">{0CCE9219-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="6c817-163">{0CCE9219-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="6c817-164">Negociación de modo rápido de IKE y AuthIP:</span><span class="sxs-lookup"><span data-stu-id="6c817-164">IKE and AuthIP Quick Mode negotiation:</span></span><br/>
<ul>
<li><span data-ttu-id="6c817-165">5451 Asociación de seguridad establecida</span><span class="sxs-lookup"><span data-stu-id="6c817-165">5451 Security association established</span></span></li>
<li><span data-ttu-id="6c817-166">5452 finalizó la Asociación de seguridad</span><span class="sxs-lookup"><span data-stu-id="6c817-166">5452 Security association ended</span></span></li>
<li><span data-ttu-id="6c817-167">error de negociación 4654</span><span class="sxs-lookup"><span data-stu-id="6c817-167">4654 Negotiation failed</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6c817-168">Inicio/cierre de sesión</span><span class="sxs-lookup"><span data-stu-id="6c817-168">Logon/Logoff</span></span> <br/></td>
<td><span data-ttu-id="6c817-169">Modo extendido de IPsec</span><span class="sxs-lookup"><span data-stu-id="6c817-169">IPsec Extended Mode</span></span><br/> <span data-ttu-id="6c817-170">{0CCE921A-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="6c817-170">{0CCE921A-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="6c817-171">Negociación del modo extendido de AuthIP:</span><span class="sxs-lookup"><span data-stu-id="6c817-171">AuthIP Extended Mode negotiation:</span></span><br/>
<ul>
<li><span data-ttu-id="6c817-172">4978 paquete de negociación no válido</span><span class="sxs-lookup"><span data-stu-id="6c817-172">4978 Invalid negotiation packet</span></span></li>
<li><span data-ttu-id="6c817-173">4979, 4980, 4981, 4982 Asociación de seguridad establecida</span><span class="sxs-lookup"><span data-stu-id="6c817-173">4979, 4980, 4981, 4982 Security association established</span></span></li>
<li><span data-ttu-id="6c817-174">4983, error de negociación de 4984</span><span class="sxs-lookup"><span data-stu-id="6c817-174">4983, 4984 Negotiation failed</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6c817-175">System</span><span class="sxs-lookup"><span data-stu-id="6c817-175">System</span></span><br/> <span data-ttu-id="6c817-176">{69979848-797A-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="6c817-176">{69979848-797A-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="6c817-177">Controlador IPsec</span><span class="sxs-lookup"><span data-stu-id="6c817-177">IPsec Driver</span></span><br/> <span data-ttu-id="6c817-178">{0CCE9213-69AE-11D9-BED3-505054503030}</span><span class="sxs-lookup"><span data-stu-id="6c817-178">{0CCE9213-69AE-11D9-BED3-505054503030}</span></span><br/></td>
<td><span data-ttu-id="6c817-179">Paquetes descartados por el controlador IPsec:</span><span class="sxs-lookup"><span data-stu-id="6c817-179">Packets dropped by the IPsec driver:</span></span><br/>
<ul>
<li><span data-ttu-id="6c817-180">4963 paquete de texto no cifrado entrante quitado</span><span class="sxs-lookup"><span data-stu-id="6c817-180">4963 Inbound clear text packet dropped</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="6c817-181">De forma predeterminada, la auditoría de WFP está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="6c817-181">By default, auditing for WFP is disabled.</span></span>

<span data-ttu-id="6c817-182">La auditoría se puede habilitar por categoría a través del complemento MMC de Editor de objetos de directiva de grupo, el complemento MMC Directiva de seguridad local o el comando auditpol.exe.</span><span class="sxs-lookup"><span data-stu-id="6c817-182">Auditing can be enabled on a per-category basis through either the Group Policy Object Editor MMC snap-in, the Local Security Policy MMC snap-in, or the auditpol.exe command.</span></span>

<span data-ttu-id="6c817-183">Por ejemplo, para habilitar la auditoría de eventos de cambio de Directiva, puede:</span><span class="sxs-lookup"><span data-stu-id="6c817-183">For example, to enable the auditing of Policy Change events you may:</span></span>

-   <span data-ttu-id="6c817-184">Usar el Editor de objetos de directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="6c817-184">Use the Group Policy Object Editor</span></span>

    1.  <span data-ttu-id="6c817-185">Ejecute **gpedit. msc**.</span><span class="sxs-lookup"><span data-stu-id="6c817-185">Run **gpedit.msc**.</span></span>
    2.  <span data-ttu-id="6c817-186">Expanda Directiva de equipo local.</span><span class="sxs-lookup"><span data-stu-id="6c817-186">Expand Local Computer Policy.</span></span>
    3.  <span data-ttu-id="6c817-187">Expanda configuración del equipo.</span><span class="sxs-lookup"><span data-stu-id="6c817-187">Expand Computer Configuration.</span></span>
    4.  <span data-ttu-id="6c817-188">Expanda configuración de Windows.</span><span class="sxs-lookup"><span data-stu-id="6c817-188">Expand Windows Settings.</span></span>
    5.  <span data-ttu-id="6c817-189">Expanda configuración de seguridad.</span><span class="sxs-lookup"><span data-stu-id="6c817-189">Expand Security Settings.</span></span>
    6.  <span data-ttu-id="6c817-190">Expanda directivas locales.</span><span class="sxs-lookup"><span data-stu-id="6c817-190">Expand Local Policies.</span></span>
    7.  <span data-ttu-id="6c817-191">Haz clic en Directiva de auditoría.</span><span class="sxs-lookup"><span data-stu-id="6c817-191">Click Audit Policy.</span></span>
    8.  <span data-ttu-id="6c817-192">Haga doble clic en auditar cambio de directiva para iniciar el cuadro de diálogo Propiedades.</span><span class="sxs-lookup"><span data-stu-id="6c817-192">Double-click Audit policy change in order to launch the Properties dialog box.</span></span>
    9.  <span data-ttu-id="6c817-193">Active las casillas aciertos y errores.</span><span class="sxs-lookup"><span data-stu-id="6c817-193">Check the Success and Failure check-boxes.</span></span>

-   <span data-ttu-id="6c817-194">Usar la Directiva de seguridad local</span><span class="sxs-lookup"><span data-stu-id="6c817-194">Use the Local Security Policy</span></span>

    1.  <span data-ttu-id="6c817-195">Ejecute **SECPOL. msc**.</span><span class="sxs-lookup"><span data-stu-id="6c817-195">Run **secpol.msc**.</span></span>
    2.  <span data-ttu-id="6c817-196">Expanda directivas locales.</span><span class="sxs-lookup"><span data-stu-id="6c817-196">Expand Local Policies.</span></span>
    3.  <span data-ttu-id="6c817-197">Haz clic en Directiva de auditoría.</span><span class="sxs-lookup"><span data-stu-id="6c817-197">Click Audit Policy.</span></span>
    4.  <span data-ttu-id="6c817-198">Haga doble clic en auditar cambio de directiva para iniciar el cuadro de diálogo Propiedades.</span><span class="sxs-lookup"><span data-stu-id="6c817-198">Double-click Audit policy change in order to launch the Properties dialog box.</span></span>
    5.  <span data-ttu-id="6c817-199">Active las casillas aciertos y errores.</span><span class="sxs-lookup"><span data-stu-id="6c817-199">Check the Success and Failure check-boxes.</span></span>

-   <span data-ttu-id="6c817-200">Usar el comando auditpol.exe</span><span class="sxs-lookup"><span data-stu-id="6c817-200">Use the auditpol.exe command</span></span>

    -   <span data-ttu-id="6c817-201">**AuditPol/Set/Category: "cambio de directiva"/Success: enable/Failure: enable**</span><span class="sxs-lookup"><span data-stu-id="6c817-201">**auditpol /set /category:"Policy Change" /success:enable /failure:enable**</span></span>

<span data-ttu-id="6c817-202">La auditoría se puede habilitar en cada subcategoría solo a través del comando auditpol.exe.</span><span class="sxs-lookup"><span data-stu-id="6c817-202">Auditing can be enabled on a per-subcategory basis only through the auditpol.exe command.</span></span>

<span data-ttu-id="6c817-203">La categoría de auditoría y los nombres de subcategoría están localizados.</span><span class="sxs-lookup"><span data-stu-id="6c817-203">The auditing category and subcategory names are localized.</span></span> <span data-ttu-id="6c817-204">Para evitar la localización de scripts de auditoría, se pueden usar los GUID correspondientes en lugar de los nombres.</span><span class="sxs-lookup"><span data-stu-id="6c817-204">To avoid localization for auditing scripts, the corresponding GUIDs may be used in place of the names.</span></span>

<span data-ttu-id="6c817-205">Por ejemplo, para habilitar la auditoría de eventos de cambio de directiva de plataforma de filtrado, puede usar uno de los siguientes comandos:</span><span class="sxs-lookup"><span data-stu-id="6c817-205">For example, to enable the auditing of Filtering Platform Policy Change events you may use either one of the following commands:</span></span>

-   <span data-ttu-id="6c817-206">**AuditPol/Set/subcategory: "filtrar cambio de directiva de plataforma"/Success: enable/Failure: enable**</span><span class="sxs-lookup"><span data-stu-id="6c817-206">**auditpol /set /subcategory:"Filtering Platform Policy Change" /success:enable /failure:enable**</span></span>
-   <span data-ttu-id="6c817-207">**AuditPol/Set/subcategory: "{0CCE9233-69AE-11D9-BED3-505054503030}"/Success: enable/Failure: enable**</span><span class="sxs-lookup"><span data-stu-id="6c817-207">**auditpol /set /subcategory:"{0CCE9233-69AE-11D9-BED3-505054503030}" /success:enable /failure:enable**</span></span>

## <a name="related-topics"></a><span data-ttu-id="6c817-208">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6c817-208">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="6c817-209">[AuditPol](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc731451(v=ws.11))</span><span class="sxs-lookup"><span data-stu-id="6c817-209">[Auditpol](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc731451(v=ws.11))</span></span>
</dt> <dt>

<span data-ttu-id="6c817-210">[Registro de eventos](/previous-versions/orphan-topics/ws.10/dd996684(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="6c817-210">[Event Log](/previous-versions/orphan-topics/ws.10/dd996684(v=ws.10))</span></span>
</dt> <dt>

[<span data-ttu-id="6c817-211">Directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="6c817-211">Group Policy</span></span>](/windows/deployment/deploy-whats-new)
</dt> </dl>

