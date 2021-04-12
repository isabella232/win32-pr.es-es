---
description: La utilidad de línea de comandos de WMI (WMIC) proporciona una interfaz de línea de comandos para WMI.
ms.assetid: a0f5c1e2-9a4d-4c2b-b324-58ec01e67b6e
ms.tgt_platform: multiple
title: wmic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed46e8aeab24acb44f51099a6e813e921dd77eaa
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "104280211"
---
# <a name="wmic"></a><span data-ttu-id="9e56b-103">wmic</span><span class="sxs-lookup"><span data-stu-id="9e56b-103">wmic</span></span>

<span data-ttu-id="9e56b-104">La utilidad de línea de comandos de WMI (WMIC) proporciona una interfaz de línea de comandos para Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="9e56b-104">The WMI command-line (WMIC) utility provides a command-line interface for Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="9e56b-105">WMIC es compatible con shells y comandos de utilidad existentes.</span><span class="sxs-lookup"><span data-stu-id="9e56b-105">WMIC is compatible with existing shells and utility commands.</span></span> <span data-ttu-id="9e56b-106">A continuación se encuentra un tema de referencia general de WMIC.</span><span class="sxs-lookup"><span data-stu-id="9e56b-106">The following is a general reference topic for WMIC.</span></span> <span data-ttu-id="9e56b-107">Para obtener más información e instrucciones sobre cómo usar WMIC, incluida información adicional sobre alias, verbos, modificadores y comandos, vea [usar instrumental de administración de Windows línea de comandos](/previous-versions/windows/it-pro/windows-server-2003/cc779482(v=ws.10)) y [WMIC-Take control de línea de comandos sobre WMI](/previous-versions/windows/it-pro/windows-2000-server/bb742610(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="9e56b-107">For more information and guidelines on how to use WMIC, including additional information on aliases, verbs, switches, and commands, see [Using Windows Management Instrumentation Command-line](/previous-versions/windows/it-pro/windows-server-2003/cc779482(v=ws.10)) and [WMIC - Take Command-line Control over WMI](/previous-versions/windows/it-pro/windows-2000-server/bb742610(v=technet.10)).</span></span>

## <a name="alias"></a><span data-ttu-id="9e56b-108">Alias</span><span class="sxs-lookup"><span data-stu-id="9e56b-108">Alias</span></span>

<span data-ttu-id="9e56b-109">Un alias es un cambio descriptivo de una clase, propiedad o método que facilita el uso y la lectura de WMI.</span><span class="sxs-lookup"><span data-stu-id="9e56b-109">An alias is a friendly renaming of a class, property, or method that makes WMI easier to use and read.</span></span> <span data-ttu-id="9e56b-110">Puede determinar los alias que están disponibles para WMIC a través del **/?**</span><span class="sxs-lookup"><span data-stu-id="9e56b-110">You can determine what aliases are available for WMIC through the **/?**</span></span> <span data-ttu-id="9e56b-111">.</span><span class="sxs-lookup"><span data-stu-id="9e56b-111">command.</span></span> <span data-ttu-id="9e56b-112">También puede determinar los alias para una clase específica mediante **<className> /?**</span><span class="sxs-lookup"><span data-stu-id="9e56b-112">You can also determine the aliases for a specific class using the **<className> /?**</span></span> <span data-ttu-id="9e56b-113">.</span><span class="sxs-lookup"><span data-stu-id="9e56b-113">command.</span></span> <span data-ttu-id="9e56b-114">Para obtener más información, consulte [alias de WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc736307(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="9e56b-114">For more information, see [WMIC Aliases](/previous-versions/windows/it-pro/windows-server-2003/cc736307(v=ws.10)).</span></span>

## <a name="switch"></a><span data-ttu-id="9e56b-115">Switch</span><span class="sxs-lookup"><span data-stu-id="9e56b-115">Switch</span></span>

<span data-ttu-id="9e56b-116">Un modificador es una opción de WMIC que se puede establecer global u opcionalmente.</span><span class="sxs-lookup"><span data-stu-id="9e56b-116">A switch is a WMIC option you can set globally or optionally.</span></span> <span data-ttu-id="9e56b-117">Para obtener una lista de los modificadores disponibles, consulte [modificadores de WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc787035(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="9e56b-117">For a list of available switches, see [WMIC Switches](/previous-versions/windows/it-pro/windows-server-2003/cc787035(v=ws.10)).</span></span>

## <a name="verbs"></a><span data-ttu-id="9e56b-118">Verbos</span><span class="sxs-lookup"><span data-stu-id="9e56b-118">Verbs</span></span>

<span data-ttu-id="9e56b-119">Para usar verbos en WMIC, escriba el nombre del alias seguido del verbo.</span><span class="sxs-lookup"><span data-stu-id="9e56b-119">To use verbs in WMIC, enter the alias name followed by the verb.</span></span> <span data-ttu-id="9e56b-120">Si un alias no admite un verbo, recibirá el mensaje "el proveedor no es capaz de realizar la operación".</span><span class="sxs-lookup"><span data-stu-id="9e56b-120">If an alias does not support a verb, you receive the message "provider is not capable of the attempted operation."</span></span> <span data-ttu-id="9e56b-121">Para obtener más información, vea [verbos de WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc784966(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="9e56b-121">For more information, see [WMIC Verbs](/previous-versions/windows/it-pro/windows-server-2003/cc784966(v=ws.10)).</span></span>

<span data-ttu-id="9e56b-122">La mayoría de los alias admiten los siguientes verbos.</span><span class="sxs-lookup"><span data-stu-id="9e56b-122">Most aliases support the following verbs.</span></span>

<dl> <dt>

<span data-ttu-id="9e56b-123"><span id="ASSOC"></span><span id="assoc"></span>ASSOC</span><span class="sxs-lookup"><span data-stu-id="9e56b-123"><span id="ASSOC"></span><span id="assoc"></span>ASSOC</span></span>
</dt> <dd>

<span data-ttu-id="9e56b-124">Devuelve el resultado de la `Associators of (<wmi_object>)` consulta donde *<\_ objeto WMI>* es la ruta de acceso de los objetos devueltos por los comandos **path** o **Class** .</span><span class="sxs-lookup"><span data-stu-id="9e56b-124">Returns the result of the `Associators of (<wmi_object>)` query where *<wmi\_object>* is the path of objects returned by the **PATH** or **CLASS** commands.</span></span> <span data-ttu-id="9e56b-125">Los resultados son instancias asociadas al objeto.</span><span class="sxs-lookup"><span data-stu-id="9e56b-125">The results are instances associated with the object.</span></span> <span data-ttu-id="9e56b-126">Cuando se usa ASSOC con un alias, se devuelven las clases con la clase que subyace al alias.</span><span class="sxs-lookup"><span data-stu-id="9e56b-126">When ASSOC is used with an alias, the classes with the class underlying the alias are returned.</span></span> <span data-ttu-id="9e56b-127">De forma predeterminada, la salida se devuelve en formato HTML.</span><span class="sxs-lookup"><span data-stu-id="9e56b-127">By default the output is returned in HTML format.</span></span>

<span data-ttu-id="9e56b-128">El verbo ASSOC tiene los siguientes modificadores.</span><span class="sxs-lookup"><span data-stu-id="9e56b-128">The ASSOC verb has the following switches.</span></span>



| <span data-ttu-id="9e56b-129">Switch</span><span class="sxs-lookup"><span data-stu-id="9e56b-129">Switch</span></span>                         | <span data-ttu-id="9e56b-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="9e56b-130">Description</span></span>                                                                                                       |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e56b-131">/RESULTCLASS:<classname></span><span class="sxs-lookup"><span data-stu-id="9e56b-131">/RESULTCLASS:<classname></span></span> | <span data-ttu-id="9e56b-132">Los extremos devueltos asociados al objeto de origen deben pertenecer a o derivar de la clase especificada.</span><span class="sxs-lookup"><span data-stu-id="9e56b-132">Returned endpoints associated with the source object must belong to, or be derived from the specified class.</span></span>      |
| <span data-ttu-id="9e56b-133">/RESULTROLE:<rolename></span><span class="sxs-lookup"><span data-stu-id="9e56b-133">/RESULTROLE:<rolename></span></span>   | <span data-ttu-id="9e56b-134">Los extremos devueltos deben desempeñar un rol específico en asociaciones con el objeto de origen.</span><span class="sxs-lookup"><span data-stu-id="9e56b-134">Returned endpoints must play a specific role in associations with the source object.</span></span>                              |
| <span data-ttu-id="9e56b-135">/ASSOCCLASS:<assocclass></span><span class="sxs-lookup"><span data-stu-id="9e56b-135">/ASSOCCLASS:<assocclass></span></span> | <span data-ttu-id="9e56b-136">Los extremos devueltos deben estar asociados al origen a través de la clase especificada o de una de sus clases derivadas.</span><span class="sxs-lookup"><span data-stu-id="9e56b-136">Returned endpoints must be associated with the source through the specified class, or one of its derived classes.</span></span> |



 

<span data-ttu-id="9e56b-137">Ejemplo: **so Assoc**</span><span class="sxs-lookup"><span data-stu-id="9e56b-137">Example: **OS ASSOC**</span></span>

</dd> <dt>

<span data-ttu-id="9e56b-138"><span id="CALL"></span><span id="call"></span>LLAMA</span><span class="sxs-lookup"><span data-stu-id="9e56b-138"><span id="CALL"></span><span id="call"></span>CALL</span></span>
</dt> <dd>

<span data-ttu-id="9e56b-139">Ejecuta un método.</span><span class="sxs-lookup"><span data-stu-id="9e56b-139">Executes a method.</span></span>

<span data-ttu-id="9e56b-140">Ejemplo: **servicio en el que Caption = ' telnet ' llama a STARTSERVICE**</span><span class="sxs-lookup"><span data-stu-id="9e56b-140">Example: **SERVICE WHERE CAPTION='TELNET' CALL STARTSERVICE**</span></span>

> [!Note]  
> <span data-ttu-id="9e56b-141">Para determinar los métodos disponibles para una clase determinada, use **/?**.</span><span class="sxs-lookup"><span data-stu-id="9e56b-141">To determine the methods available for a given class, use **/?**.</span></span> <span data-ttu-id="9e56b-142">Por ejemplo, **servicio donde Caption = ' telnet ' Call/?**</span><span class="sxs-lookup"><span data-stu-id="9e56b-142">For example, **SERVICE WHERE CAPTION='TELNET' CALL /?**</span></span> <span data-ttu-id="9e56b-143">muestra las funciones disponibles para la clase de servicio.</span><span class="sxs-lookup"><span data-stu-id="9e56b-143">lists the available functions for the service class.</span></span>

 

</dd> <dt>

<span data-ttu-id="9e56b-144"><span id="CREATE"></span><span id="create"></span>A</span><span class="sxs-lookup"><span data-stu-id="9e56b-144"><span id="CREATE"></span><span id="create"></span>CREATE</span></span>
</dt> <dd>

<span data-ttu-id="9e56b-145">Crea una nueva instancia de y establece los valores de propiedad.</span><span class="sxs-lookup"><span data-stu-id="9e56b-145">Creates a new instance and sets the property values.</span></span> <span data-ttu-id="9e56b-146">CREATE no se puede usar para crear una nueva clase.</span><span class="sxs-lookup"><span data-stu-id="9e56b-146">CREATE cannot be used to create a new class.</span></span>

<span data-ttu-id="9e56b-147">Ejemplo: **entorno Create name = "Temp"; VARIABLEVALUE = "nuevo"**</span><span class="sxs-lookup"><span data-stu-id="9e56b-147">Example: **ENVIRONMENT CREATE NAME="TEMP"; VARIABLEVALUE="NEW"**</span></span>

</dd> <dt>

<span data-ttu-id="9e56b-148"><span id="DELETE"></span><span id="delete"></span>ELIMÍNELOS</span><span class="sxs-lookup"><span data-stu-id="9e56b-148"><span id="DELETE"></span><span id="delete"></span>DELETE</span></span>
</dt> <dd>

<span data-ttu-id="9e56b-149">Elimina la instancia o el conjunto de instancias actual.</span><span class="sxs-lookup"><span data-stu-id="9e56b-149">Deletes the current instance or set of instances.</span></span> <span data-ttu-id="9e56b-150">DELETE se puede usar para eliminar una clase.</span><span class="sxs-lookup"><span data-stu-id="9e56b-150">DELETE can be used to delete a class.</span></span>

<span data-ttu-id="9e56b-151">Ejemplo: **proceso donde name = "CALC.EXE" Delete**</span><span class="sxs-lookup"><span data-stu-id="9e56b-151">Example: **PROCESS WHERE NAME="CALC.EXE" DELETE**</span></span>

</dd> <dt>

<span data-ttu-id="9e56b-152"><span id="GET"></span><span id="get"></span>Obtener</span><span class="sxs-lookup"><span data-stu-id="9e56b-152"><span id="GET"></span><span id="get"></span>GET</span></span>
</dt> <dd>

<span data-ttu-id="9e56b-153">Recuperar valores de propiedad específicos.</span><span class="sxs-lookup"><span data-stu-id="9e56b-153">Retrieve specific property values.</span></span>

<span data-ttu-id="9e56b-154">GET tiene los siguientes modificadores.</span><span class="sxs-lookup"><span data-stu-id="9e56b-154">GET has the following switches.</span></span>



| <span data-ttu-id="9e56b-155">Switch</span><span class="sxs-lookup"><span data-stu-id="9e56b-155">Switch</span></span>                               | <span data-ttu-id="9e56b-156">Descripción</span><span class="sxs-lookup"><span data-stu-id="9e56b-156">Description</span></span>                                                                                                                                |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e56b-157">/VALUE</span><span class="sxs-lookup"><span data-stu-id="9e56b-157">/VALUE</span></span>                               | <span data-ttu-id="9e56b-158">La salida se formatea con cada valor que aparece en una línea independiente y con el nombre de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="9e56b-158">Output is formatted with each value listed on a separate line and with the name of the property.</span></span>                                           |
| <span data-ttu-id="9e56b-159">/ALL</span><span class="sxs-lookup"><span data-stu-id="9e56b-159">/ALL</span></span>                                 | <span data-ttu-id="9e56b-160">La salida tiene el formato de tabla.</span><span class="sxs-lookup"><span data-stu-id="9e56b-160">Output is formatted as a table.</span></span>                                                                                                            |
| <span data-ttu-id="9e56b-161">Convierte<translation table></span><span class="sxs-lookup"><span data-stu-id="9e56b-161">/TRANSLATE:<translation table></span></span> | <span data-ttu-id="9e56b-162">Traduzca la salida mediante la tabla Translation denominada por el comando.</span><span class="sxs-lookup"><span data-stu-id="9e56b-162">Translate the output using the translation table named by the command.</span></span> <span data-ttu-id="9e56b-163">Las tablas de traducción BasicXml y nomilla se incluyen con WMIC.</span><span class="sxs-lookup"><span data-stu-id="9e56b-163">The translation tables BasicXml and NoComma are included with WMIC.</span></span> |
| <span data-ttu-id="9e56b-164">Siempre<interval></span><span class="sxs-lookup"><span data-stu-id="9e56b-164">/EVERY:<interval></span></span>              | <span data-ttu-id="9e56b-165">Repita el comando cada <interval> segundos.</span><span class="sxs-lookup"><span data-stu-id="9e56b-165">Repeat the command every <interval> seconds.</span></span>                                                                                         |
| <span data-ttu-id="9e56b-166">Aplique<format specifier></span><span class="sxs-lookup"><span data-stu-id="9e56b-166">/FORMAT:<format specifier></span></span>     | <span data-ttu-id="9e56b-167">Especifica una palabra clave o un nombre de archivo XSL para dar formato a los datos.</span><span class="sxs-lookup"><span data-stu-id="9e56b-167">Specifies a key word or XSL file name to format the data.</span></span>                                                                                  |



 

<span data-ttu-id="9e56b-168">Ejemplo: **Process Get Name**</span><span class="sxs-lookup"><span data-stu-id="9e56b-168">Example: **PROCESS GET NAME**</span></span>

</dd> <dt>

<span data-ttu-id="9e56b-169"><span id="LIST"></span><span id="list"></span>LISTA</span><span class="sxs-lookup"><span data-stu-id="9e56b-169"><span id="LIST"></span><span id="list"></span>LIST</span></span>
</dt> <dd>

<span data-ttu-id="9e56b-170">Muestra los datos.</span><span class="sxs-lookup"><span data-stu-id="9e56b-170">Shows data.</span></span> <span data-ttu-id="9e56b-171">LIST es el verbo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="9e56b-171">LIST is the default verb.</span></span>

<span data-ttu-id="9e56b-172">LIST tiene los siguientes adverbios.</span><span class="sxs-lookup"><span data-stu-id="9e56b-172">LIST has the following adverbs.</span></span>



| <span data-ttu-id="9e56b-173">Adverbio</span><span class="sxs-lookup"><span data-stu-id="9e56b-173">Adverb</span></span>   | <span data-ttu-id="9e56b-174">Descripción</span><span class="sxs-lookup"><span data-stu-id="9e56b-174">Description</span></span>                                                  |
|----------|--------------------------------------------------------------|
| <span data-ttu-id="9e56b-175">INSTRUCCIONES</span><span class="sxs-lookup"><span data-stu-id="9e56b-175">BRIEF</span></span>    | <span data-ttu-id="9e56b-176">Conjunto básico de las propiedades.</span><span class="sxs-lookup"><span data-stu-id="9e56b-176">Core set of the properties.</span></span>                                  |
| <span data-ttu-id="9e56b-177">FULL</span><span class="sxs-lookup"><span data-stu-id="9e56b-177">FULL</span></span>     | <span data-ttu-id="9e56b-178">Conjunto completo de propiedades.</span><span class="sxs-lookup"><span data-stu-id="9e56b-178">Full set of properties.</span></span> <span data-ttu-id="9e56b-179">Este es el adverbio predeterminado para la lista.</span><span class="sxs-lookup"><span data-stu-id="9e56b-179">This is the default adverb for LIST.</span></span> |
| <span data-ttu-id="9e56b-180">INSTANCE</span><span class="sxs-lookup"><span data-stu-id="9e56b-180">INSTANCE</span></span> | <span data-ttu-id="9e56b-181">Solo rutas de acceso de instancia.</span><span class="sxs-lookup"><span data-stu-id="9e56b-181">Instance paths only.</span></span>                                         |
| <span data-ttu-id="9e56b-182">STATUS</span><span class="sxs-lookup"><span data-stu-id="9e56b-182">STATUS</span></span>   | <span data-ttu-id="9e56b-183">Estado de los objetos.</span><span class="sxs-lookup"><span data-stu-id="9e56b-183">Status of the objects.</span></span>                                       |
| <span data-ttu-id="9e56b-184">SYSTEM</span><span class="sxs-lookup"><span data-stu-id="9e56b-184">SYSTEM</span></span>   | <span data-ttu-id="9e56b-185">Propiedades del sistema.</span><span class="sxs-lookup"><span data-stu-id="9e56b-185">System properties.</span></span>                                           |



 

<span data-ttu-id="9e56b-186">La lista tiene los siguientes modificadores.</span><span class="sxs-lookup"><span data-stu-id="9e56b-186">LIST has the following switches.</span></span>



| <span data-ttu-id="9e56b-187">Switch</span><span class="sxs-lookup"><span data-stu-id="9e56b-187">Switch</span></span>                               | <span data-ttu-id="9e56b-188">Descripción</span><span class="sxs-lookup"><span data-stu-id="9e56b-188">Description</span></span>                                                                                                                                |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e56b-189">Convierte<translation table></span><span class="sxs-lookup"><span data-stu-id="9e56b-189">/TRANSLATE:<translation table></span></span> | <span data-ttu-id="9e56b-190">Traduzca la salida mediante la tabla Translation denominada por el comando.</span><span class="sxs-lookup"><span data-stu-id="9e56b-190">Translate the output using the translation table named by the command.</span></span> <span data-ttu-id="9e56b-191">Las tablas de traducción BasicXml y nomilla se incluyen con WMIC.</span><span class="sxs-lookup"><span data-stu-id="9e56b-191">The translation tables BasicXml and NoComma are included with WMIC.</span></span> |
| <span data-ttu-id="9e56b-192">Siempre<interval></span><span class="sxs-lookup"><span data-stu-id="9e56b-192">/EVERY:<interval></span></span>              | <span data-ttu-id="9e56b-193">Repita el comando cada <interval> segundos.</span><span class="sxs-lookup"><span data-stu-id="9e56b-193">Repeat the command every <interval> seconds.</span></span>                                                                                         |
| <span data-ttu-id="9e56b-194">Aplique<format specifier></span><span class="sxs-lookup"><span data-stu-id="9e56b-194">/FORMAT:<format specifier></span></span>     | <span data-ttu-id="9e56b-195">Especifica una palabra clave o un nombre de archivo XSL para dar formato a los datos.</span><span class="sxs-lookup"><span data-stu-id="9e56b-195">Specifies a key word or XSL file name to format the data.</span></span>                                                                                  |



 

<span data-ttu-id="9e56b-196">Ejemplo: **breve lista de procesos**</span><span class="sxs-lookup"><span data-stu-id="9e56b-196">Example: **PROCESS LIST BRIEF**</span></span>

</dd> <dt>

<span data-ttu-id="9e56b-197"><span id="SET"></span><span id="set"></span>CONJUNTO</span><span class="sxs-lookup"><span data-stu-id="9e56b-197"><span id="SET"></span><span id="set"></span>SET</span></span>
</dt> <dd>

<span data-ttu-id="9e56b-198">Asigna valores a las propiedades.</span><span class="sxs-lookup"><span data-stu-id="9e56b-198">Assigns values to properties.</span></span> <span data-ttu-id="9e56b-199">Ejemplo: **Environment Set Name = "Temp"**, **VARIABLEVALUE = "New"**</span><span class="sxs-lookup"><span data-stu-id="9e56b-199">Example: **ENVIRONMENT SET NAME="TEMP"**, **VARIABLEVALUE="NEW"**</span></span>

</dd> </dl>

## <a name="switches"></a><span data-ttu-id="9e56b-200">Conmutadores</span><span class="sxs-lookup"><span data-stu-id="9e56b-200">Switches</span></span>

<span data-ttu-id="9e56b-201">Los modificadores globales se utilizan para establecer valores predeterminados para el entorno de WMIC.</span><span class="sxs-lookup"><span data-stu-id="9e56b-201">Global switches are used to set defaults for the WMIC environment.</span></span> <span data-ttu-id="9e56b-202">Para ver el valor actual de las condiciones establecidas por estos modificadores, escriba el comando de **contexto** .</span><span class="sxs-lookup"><span data-stu-id="9e56b-202">You can view the current value of the conditions set by these switches by entering the **CONTEXT** command.</span></span>

<dl> <dt>

<span data-ttu-id="9e56b-203"><span id="_NAMESPACE"></span><span id="_namespace"></span>/NAMESPACE</span><span class="sxs-lookup"><span data-stu-id="9e56b-203"><span id="_NAMESPACE"></span><span id="_namespace"></span>/NAMESPACE</span></span>
</dt> <dd>

<span data-ttu-id="9e56b-204">Espacio de nombres que usa normalmente el alias.</span><span class="sxs-lookup"><span data-stu-id="9e56b-204">Namespace the alias uses typically.</span></span> <span data-ttu-id="9e56b-205">El valor predeterminado es la raíz \\ cimv2.</span><span class="sxs-lookup"><span data-stu-id="9e56b-205">The default is root\\cimv2.</span></span>

<span data-ttu-id="9e56b-206">Ejemplo: **/namespace: \\ \\ raíz**</span><span class="sxs-lookup"><span data-stu-id="9e56b-206">Example: **/NAMESPACE:\\\\root**</span></span>

</dd> <dt>

<span data-ttu-id="9e56b-207"><span id="_ROLE"></span><span id="_role"></span>/ROLE</span><span class="sxs-lookup"><span data-stu-id="9e56b-207"><span id="_ROLE"></span><span id="_role"></span>/ROLE</span></span>
</dt> <dd>

<span data-ttu-id="9e56b-208">Espacio de nombres WMIC normalmente busca en alias y en otra información de WMIC.</span><span class="sxs-lookup"><span data-stu-id="9e56b-208">Namespace WMIC typically looks in for aliases and other WMIC information.</span></span>

<span data-ttu-id="9e56b-209">Ejemplo: **/role: \\ \\ root**</span><span class="sxs-lookup"><span data-stu-id="9e56b-209">Example: **/ROLE:\\\\root**</span></span>

</dd> <dt>

<span data-ttu-id="9e56b-210"><span id="_NODE"></span><span id="_node"></span>/NODE</span><span class="sxs-lookup"><span data-stu-id="9e56b-210"><span id="_NODE"></span><span id="_node"></span>/NODE</span></span>
</dt> <dd>

<span data-ttu-id="9e56b-211">Nombres de equipo, delimitados por comas.</span><span class="sxs-lookup"><span data-stu-id="9e56b-211">Computer names, comma delimited.</span></span> <span data-ttu-id="9e56b-212">Todos los comandos se ejecutan sincrónicamente en todos los equipos incluidos en este valor.</span><span class="sxs-lookup"><span data-stu-id="9e56b-212">All commands are synchronously executed against all computers listed in this value.</span></span> <span data-ttu-id="9e56b-213">Los nombres de archivo deben ir precedidos de &.</span><span class="sxs-lookup"><span data-stu-id="9e56b-213">File names must be prefixed with &.</span></span> <span data-ttu-id="9e56b-214">Los nombres de equipo dentro de un archivo deben ser delimitados por comas o en líneas independientes.</span><span class="sxs-lookup"><span data-stu-id="9e56b-214">Computer names within a file must be comma delimited or on separate lines.</span></span>

</dd> <dt>

<span data-ttu-id="9e56b-215"><span id="_IMPLEVEL"></span><span id="_implevel"></span>/IMPLEVEL</span><span class="sxs-lookup"><span data-stu-id="9e56b-215"><span id="_IMPLEVEL"></span><span id="_implevel"></span>/IMPLEVEL</span></span>
</dt> <dd>

<span data-ttu-id="9e56b-216">Nivel de suplantación.</span><span class="sxs-lookup"><span data-stu-id="9e56b-216">Impersonation level.</span></span>

<span data-ttu-id="9e56b-217">Ejemplo: **/IMPLEVEL: Anonymous**</span><span class="sxs-lookup"><span data-stu-id="9e56b-217">Example: **/IMPLEVEL:Anonymous**</span></span>

</dd> <dt>

<span data-ttu-id="9e56b-218"><span id="_AUTHLEVEL"></span><span id="_authlevel"></span>/AUTHLEVEL</span><span class="sxs-lookup"><span data-stu-id="9e56b-218"><span id="_AUTHLEVEL"></span><span id="_authlevel"></span>/AUTHLEVEL</span></span>
</dt> <dd>

<span data-ttu-id="9e56b-219">Nivel de autenticación.</span><span class="sxs-lookup"><span data-stu-id="9e56b-219">Authentication level.</span></span>

<span data-ttu-id="9e56b-220">Ejemplo: **/AUTHLEVEL: PKT**</span><span class="sxs-lookup"><span data-stu-id="9e56b-220">Example: **/AUTHLEVEL:Pkt**</span></span>

</dd> <dt>

<span data-ttu-id="9e56b-221"><span id="_LOCALE"></span><span id="_locale"></span>/LOCALE</span><span class="sxs-lookup"><span data-stu-id="9e56b-221"><span id="_LOCALE"></span><span id="_locale"></span>/LOCALE</span></span>
</dt> <dd>

<span data-ttu-id="9e56b-222">Configuración regional.</span><span class="sxs-lookup"><span data-stu-id="9e56b-222">Locale.</span></span>

<span data-ttu-id="9e56b-223">Ejemplo: **/locale: MS \_ 411**</span><span class="sxs-lookup"><span data-stu-id="9e56b-223">Example: **/LOCALE:MS\_411**</span></span>

</dd> <dt>

<span data-ttu-id="9e56b-224"><span id="_PRIVILEGES"></span><span id="_privileges"></span>/PRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="9e56b-224"><span id="_PRIVILEGES"></span><span id="_privileges"></span>/PRIVILEGES</span></span>
</dt> <dd>

<span data-ttu-id="9e56b-225">Habilitar o deshabilitar todos los privilegios.</span><span class="sxs-lookup"><span data-stu-id="9e56b-225">Enable or disable all privileges.</span></span>

<span data-ttu-id="9e56b-226">Ejemplo: **/privileges: enable** o **/privileges: disable**</span><span class="sxs-lookup"><span data-stu-id="9e56b-226">Example: **/PRIVILEGES:ENABLE** or **/PRIVILEGES:DISABLE**</span></span>

</dd> <dt>

<span data-ttu-id="9e56b-227"><span id="_TRACE"></span><span id="_trace"></span>/TRACE</span><span class="sxs-lookup"><span data-stu-id="9e56b-227"><span id="_TRACE"></span><span id="_trace"></span>/TRACE</span></span>
</dt> <dd>

<span data-ttu-id="9e56b-228">Muestra el éxito o el fracaso de todas las funciones utilizadas para ejecutar comandos de WMIC.</span><span class="sxs-lookup"><span data-stu-id="9e56b-228">Display the success or failure of all functions used to execute WMIC commands.</span></span>

<span data-ttu-id="9e56b-229">Ejemplo: **/Trace: on** o **/Trace: OFF**</span><span class="sxs-lookup"><span data-stu-id="9e56b-229">Example: **/TRACE:ON** or **/TRACE:OFF**</span></span>

</dd> <dt>

<span data-ttu-id="9e56b-230"><span id="_RECORD"></span><span id="_record"></span>/RECORD</span><span class="sxs-lookup"><span data-stu-id="9e56b-230"><span id="_RECORD"></span><span id="_record"></span>/RECORD</span></span>
</dt> <dd>

<span data-ttu-id="9e56b-231">Registra todos los resultados en un archivo XML.</span><span class="sxs-lookup"><span data-stu-id="9e56b-231">Records all output to an XML file.</span></span> <span data-ttu-id="9e56b-232">La salida también se muestra en el símbolo del sistema.</span><span class="sxs-lookup"><span data-stu-id="9e56b-232">Output is also displayed at the command prompt.</span></span>

<span data-ttu-id="9e56b-233">Ejemplo: **/Record:** _MyOutput.xml_</span><span class="sxs-lookup"><span data-stu-id="9e56b-233">Example: **/RECORD:**_MyOutput.xml_</span></span>

</dd> <dt>

<span data-ttu-id="9e56b-234"><span id="_INTERACTIVE"></span><span id="_interactive"></span>/INTERACTIVE</span><span class="sxs-lookup"><span data-stu-id="9e56b-234"><span id="_INTERACTIVE"></span><span id="_interactive"></span>/INTERACTIVE</span></span>
</dt> <dd>

<span data-ttu-id="9e56b-235">Normalmente, se confirman los comandos de eliminación.</span><span class="sxs-lookup"><span data-stu-id="9e56b-235">Typically, delete commands are confirmed.</span></span>

<span data-ttu-id="9e56b-236">Ejemplo: **/Interactive: on** o **/Interactive: OFF**</span><span class="sxs-lookup"><span data-stu-id="9e56b-236">Example: **/INTERACTIVE:ON** or **/INTERACTIVE:OFF**</span></span>

</dd> <dt>

<span data-ttu-id="9e56b-237"><span id="_FAILFAST_on_off_TimeoutInMilliseconds"></span><span id="_failfast_on_off_timeoutinmilliseconds"></span><span id="_FAILFAST_ON_OFF_TIMEOUTINMILLISECONDS"></span>/FailFast **en** \| **OFF** \| *TimeoutInMilliseconds*</span><span class="sxs-lookup"><span data-stu-id="9e56b-237"><span id="_FAILFAST_on_off_TimeoutInMilliseconds"></span><span id="_failfast_on_off_timeoutinmilliseconds"></span><span id="_FAILFAST_ON_OFF_TIMEOUTINMILLISECONDS"></span>/FAILFAST **on**\|**off**\|*TimeoutInMilliseconds*</span></span>
</dt> <dd>

<span data-ttu-id="9e56b-238">Si se hace ping en los equipos con/NODE antes de enviarles comandos de WMIC.</span><span class="sxs-lookup"><span data-stu-id="9e56b-238">If ON the /NODE computers are pinged before sending WMIC commands to them.</span></span> <span data-ttu-id="9e56b-239">Si un equipo no responde, no se le envían los comandos de WMIC.</span><span class="sxs-lookup"><span data-stu-id="9e56b-239">If a computer does not respond the WMIC commands are not sent to it.</span></span>

<span data-ttu-id="9e56b-240">Ejemplo: "/FAILFAST: ON" o "/FAILFAST: OFF"</span><span class="sxs-lookup"><span data-stu-id="9e56b-240">Example: "/FAILFAST:ON" or "/FAILFAST:OFF"</span></span>

<span data-ttu-id="9e56b-241">**WMIC/FAILFAST: 1000**</span><span class="sxs-lookup"><span data-stu-id="9e56b-241">**WMIC /FAILFAST:1000**</span></span>

</dd> <dt>

<span data-ttu-id="9e56b-242"><span id="_USER"></span><span id="_user"></span>/USER</span><span class="sxs-lookup"><span data-stu-id="9e56b-242"><span id="_USER"></span><span id="_user"></span>/USER</span></span>
</dt> <dd>

<span data-ttu-id="9e56b-243">Nombre de usuario utilizado por WMIC al obtener acceso a los equipos o equipos especificados en los alias.</span><span class="sxs-lookup"><span data-stu-id="9e56b-243">User name used by WMIC when accessing the /NODE computers or computers specified in the aliases.</span></span> <span data-ttu-id="9e56b-244">Se le pedirá la contraseña.</span><span class="sxs-lookup"><span data-stu-id="9e56b-244">You are prompted for the password.</span></span> <span data-ttu-id="9e56b-245">No se puede usar un nombre de usuario con el equipo local.</span><span class="sxs-lookup"><span data-stu-id="9e56b-245">A user name cannot be used with the local computer.</span></span>

<span data-ttu-id="9e56b-246">Ejemplo: **/User:**_JSMITH_</span><span class="sxs-lookup"><span data-stu-id="9e56b-246">Example: **/USER:**_JSMITH_</span></span>

</dd> <dt>

<span data-ttu-id="9e56b-247"><span id="_PASSWORD"></span><span id="_password"></span>/PASSWORD</span><span class="sxs-lookup"><span data-stu-id="9e56b-247"><span id="_PASSWORD"></span><span id="_password"></span>/PASSWORD</span></span>
</dt> <dd>

<span data-ttu-id="9e56b-248">Contraseña usada por WMIC al obtener acceso a los equipos/NPDE.</span><span class="sxs-lookup"><span data-stu-id="9e56b-248">Password used by WMIC when accessing the /NPDE computers.</span></span> <span data-ttu-id="9e56b-249">La contraseña es visible en la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="9e56b-249">The password is visible at the command line.</span></span>

<span data-ttu-id="9e56b-250">Ejemplo: **/password:**_contraseña_</span><span class="sxs-lookup"><span data-stu-id="9e56b-250">Example: **/PASSWORD:**_password_</span></span>

</dd> <dt>

<span data-ttu-id="9e56b-251"><span id="_OUTPUT"></span><span id="_output"></span>/OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9e56b-251"><span id="_OUTPUT"></span><span id="_output"></span>/OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="9e56b-252">Especifica un modo para la redirección de salida.</span><span class="sxs-lookup"><span data-stu-id="9e56b-252">Specifies a mode for all output redirection.</span></span> <span data-ttu-id="9e56b-253">La salida no aparece en la línea de comandos y se borra el destino antes de que empiece la salida.</span><span class="sxs-lookup"><span data-stu-id="9e56b-253">Output does not appear at the command line and the destination is cleared before output begins.</span></span> <span data-ttu-id="9e56b-254">Los valores válidos son STDOUT, CLIPBOARD o un nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="9e56b-254">Valid values are STDOUT, CLIPBOARD or a file name.</span></span>

<span data-ttu-id="9e56b-255">Ejemplo: **/Output: Clipboard**</span><span class="sxs-lookup"><span data-stu-id="9e56b-255">Example: **/OUTPUT:CLIPBOARD**</span></span>

</dd> <dt>

<span data-ttu-id="9e56b-256"><span id="_APPEND"></span><span id="_append"></span>/APPEND</span><span class="sxs-lookup"><span data-stu-id="9e56b-256"><span id="_APPEND"></span><span id="_append"></span>/APPEND</span></span>
</dt> <dd>

<span data-ttu-id="9e56b-257">Especifica un modo para la redirección de salida.</span><span class="sxs-lookup"><span data-stu-id="9e56b-257">Specifies a mode for all output redirection.</span></span> <span data-ttu-id="9e56b-258">La salida no aparece en la línea de comandos y el destino no se borra antes de que se inicie la salida y se anexa la salida al final del contenido actual del destino.</span><span class="sxs-lookup"><span data-stu-id="9e56b-258">Output does not appear at the command line and the destination is not cleared before output begins and output is appended to the end of the current contents of the destination.</span></span> <span data-ttu-id="9e56b-259">Los valores válidos son STDOUT, CLIPBOARD o un nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="9e56b-259">Valid values are STDOUT, CLIPBOARD or a file name.</span></span>

<span data-ttu-id="9e56b-260">Ejemplo: **/Append: Clipboard**</span><span class="sxs-lookup"><span data-stu-id="9e56b-260">Example: **/APPEND:CLIPBOARD**</span></span>

</dd> <dt>

<span data-ttu-id="9e56b-261"><span id="_AGGREGATE"></span><span id="_aggregate"></span>/AGGREGATE</span><span class="sxs-lookup"><span data-stu-id="9e56b-261"><span id="_AGGREGATE"></span><span id="_aggregate"></span>/AGGREGATE</span></span>
</dt> <dd>

<span data-ttu-id="9e56b-262">Se usa con los modificadores **List** y **Get/Every** .</span><span class="sxs-lookup"><span data-stu-id="9e56b-262">Used with the **LIST** and **GET /EVERY** switch.</span></span> <span data-ttu-id="9e56b-263">Si Aggregate está activado, LIST y GET muestran los resultados cuando todos los equipos de la/NODE han respondido o han agotado el tiempo de espera. Si Aggregate está desactivado, LIST y GET muestran los resultados en cuanto se reciben.</span><span class="sxs-lookup"><span data-stu-id="9e56b-263">If AGGREGATE is ON, LIST and GET display their results when all computers in the /NODE have either responded or timed out. If AGGREGATE is OFF, LIST and GET display their results as soon as they are received.</span></span>

<span data-ttu-id="9e56b-264">Ejemplo: **/Aggregate: OFF** o **/Aggregate: on**</span><span class="sxs-lookup"><span data-stu-id="9e56b-264">Example: **/AGGREGATE:OFF** or **/AGGREGATE:ON**</span></span>

</dd> </dl>

## <a name="commands"></a><span data-ttu-id="9e56b-265">Comandos:</span><span class="sxs-lookup"><span data-stu-id="9e56b-265">Commands</span></span>

<span data-ttu-id="9e56b-266">Los siguientes comandos de WMIC están disponibles en todo momento.</span><span class="sxs-lookup"><span data-stu-id="9e56b-266">The following WMIC commands are available at all times.</span></span> <span data-ttu-id="9e56b-267">Para obtener más información, vea [comandos de WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc779647(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="9e56b-267">For more information, see [WMIC Commands](/previous-versions/windows/it-pro/windows-server-2003/cc779647(v=ws.10)).</span></span>

<dl> <dt>

<span data-ttu-id="9e56b-268"><span id="CLASS"></span><span id="class"></span>LAS</span><span class="sxs-lookup"><span data-stu-id="9e56b-268"><span id="CLASS"></span><span id="class"></span>CLASS</span></span>
</dt> <dd>

<span data-ttu-id="9e56b-269">Salga del modo de alias predeterminado de WMIC para tener acceso directamente a las clases del esquema WMI.</span><span class="sxs-lookup"><span data-stu-id="9e56b-269">Escape from the default alias mode of WMIC to access classes in the WMI schema directly.</span></span> <span data-ttu-id="9e56b-270">Para obtener más información sobre las clases WMI disponibles, vea [clases WMI](wmi-classes.md).</span><span class="sxs-lookup"><span data-stu-id="9e56b-270">For more information on available WMI classes, see [WMI Classes](wmi-classes.md).</span></span>

<span data-ttu-id="9e56b-271">Ejemplo: **WMIC/Output: c: \\ClassOutput.htm clase Win32 \_ SoundDevice**</span><span class="sxs-lookup"><span data-stu-id="9e56b-271">Example: **WMIC /OUTPUT:c:\\ClassOutput.htm CLASS Win32\_SoundDevice**</span></span>

</dd> <dt>

<span data-ttu-id="9e56b-272"><span id="PATH"></span><span id="path"></span>CAMINO</span><span class="sxs-lookup"><span data-stu-id="9e56b-272"><span id="PATH"></span><span id="path"></span>PATH</span></span>
</dt> <dd>

<span data-ttu-id="9e56b-273">Salga del modo de alias predeterminado de WMIC para tener acceso directamente a las instancias del esquema WMI.</span><span class="sxs-lookup"><span data-stu-id="9e56b-273">Escape from the default alias mode of WMIC to access instances in the WMI schema directly.</span></span>

<span data-ttu-id="9e56b-274">Ejemplo: **WMIC/Output: c: \\PathOutput.txt path Win32 \_ SoundDevice Get/Value**</span><span class="sxs-lookup"><span data-stu-id="9e56b-274">Example: **WMIC /OUTPUT:c:\\PathOutput.txt PATH Win32\_SoundDevice GET /VALUE**</span></span>

</dd> <dt>

<span data-ttu-id="9e56b-275"><span id="CONTEXT"></span><span id="context"></span>CONTEXTO</span><span class="sxs-lookup"><span data-stu-id="9e56b-275"><span id="CONTEXT"></span><span id="context"></span>CONTEXT</span></span>
</dt> <dd>

<span data-ttu-id="9e56b-276">Mostrar los valores actuales de todos los conmutadores globales.</span><span class="sxs-lookup"><span data-stu-id="9e56b-276">Display the current values of all global switches.</span></span>

<span data-ttu-id="9e56b-277">Ejemplo: **contexto de WMIC**</span><span class="sxs-lookup"><span data-stu-id="9e56b-277">Example: **WMIC CONTEXT**</span></span>

</dd> <dt>

<span data-ttu-id="9e56b-278"><span id="QUIT"></span><span id="quit"></span>INTERRUMPI</span><span class="sxs-lookup"><span data-stu-id="9e56b-278"><span id="QUIT"></span><span id="quit"></span>QUIT</span></span>
</dt> <dd>

<span data-ttu-id="9e56b-279">Salga de WMIC.</span><span class="sxs-lookup"><span data-stu-id="9e56b-279">Exit from WMIC.</span></span>

<span data-ttu-id="9e56b-280">Ejemplo: **WMIC Quit**</span><span class="sxs-lookup"><span data-stu-id="9e56b-280">Example: **WMIC QUIT**</span></span>

</dd> <dt>

<span data-ttu-id="9e56b-281"><span id="EXIT"></span><span id="exit"></span>ABANDONAR</span><span class="sxs-lookup"><span data-stu-id="9e56b-281"><span id="EXIT"></span><span id="exit"></span>EXIT</span></span>
</dt> <dd>

<span data-ttu-id="9e56b-282">Salga de WMIC.</span><span class="sxs-lookup"><span data-stu-id="9e56b-282">Exit from WMIC.</span></span>

<span data-ttu-id="9e56b-283">Ejemplo: **WMIC Exit**</span><span class="sxs-lookup"><span data-stu-id="9e56b-283">Example: **WMIC EXIT**</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="9e56b-284">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9e56b-284">Examples</span></span>

<span data-ttu-id="9e56b-285">El [script para establecer la configuración de IP/subred/Puerta de enlace/DNS con WMIC](https://Gallery.TechNet.Microsoft.Com/Batch-per-settare-487c1b3f) en la galería de TechNet describe cómo modificar y actualizar la configuración de IP, subred, puerta de enlace y DNS.</span><span class="sxs-lookup"><span data-stu-id="9e56b-285">The [Script for setting IP/Subnet/Gateway/DNS using wmic](https://Gallery.TechNet.Microsoft.Com/Batch-per-settare-487c1b3f) sample on TechNet Gallery describes how to modify and update IP, Subnet, Gateway, and DNS settings.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e56b-286">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e56b-286">Requirements</span></span>



| <span data-ttu-id="9e56b-287">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e56b-287">Requirement</span></span> | <span data-ttu-id="9e56b-288">Value</span><span class="sxs-lookup"><span data-stu-id="9e56b-288">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="9e56b-289">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e56b-289">Minimum supported client</span></span><br/> | <span data-ttu-id="9e56b-290">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9e56b-290">Windows Vista</span></span><br/>       |
| <span data-ttu-id="9e56b-291">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e56b-291">Minimum supported server</span></span><br/> | <span data-ttu-id="9e56b-292">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9e56b-292">Windows Server 2008</span></span><br/> |



 

