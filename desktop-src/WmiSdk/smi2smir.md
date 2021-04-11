---
description: El compilador SNMP se ejecuta como un único archivo ejecutable en el modo de línea de comandos.
ms.assetid: 0e85fe84-dacb-4720-8242-ffa0046780f3
ms.tgt_platform: multiple
title: smi2smir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34e1d757293b5ee128f2ce1bc2bd5ec8479d9b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104279113"
---
# <a name="smi2smir"></a><span data-ttu-id="a3488-103">smi2smir</span><span class="sxs-lookup"><span data-stu-id="a3488-103">smi2smir</span></span>

<span data-ttu-id="a3488-104">El compilador SNMP se ejecuta como un único archivo ejecutable en el modo de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="a3488-104">The SNMP compiler runs as a single executable file in the command-line mode.</span></span> <span data-ttu-id="a3488-105">El compilador acepta un módulo de información SNMP como entrada y acepta los módulos adicionales necesarios para resolver referencias externas.</span><span class="sxs-lookup"><span data-stu-id="a3488-105">The compiler accepts one SNMP information module as input, and accepts any additional modules necessary to resolve external references.</span></span> <span data-ttu-id="a3488-106">Use uno de los siguientes ejemplos de sintaxis de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="a3488-106">Use one of the following command-line syntax examples.</span></span>

<span data-ttu-id="a3488-107">Para obtener más información acerca de Cuándo se usa este compilador, consulte [configuración del entorno WMI SNMP](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="a3488-107">For more information about when this compiler is used, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

``` syntax
smi2smir [<DiagnosticArgs>] [<VersionArgs>]
     <CommandArgs> <MIB file> [<Import Files>]

smi2smir [<DiagnosticArgs>] <RegistryArgs> [<Directory>]

smi2smir <ModuleInfoArgs> <MIB file>

smi2smir <HelpArgs>
```

## <a name="switches"></a><span data-ttu-id="a3488-108">Conmutadores</span><span class="sxs-lookup"><span data-stu-id="a3488-108">Switches</span></span>

<dl> <span data-ttu-id="a3488-109"><dt>

<span id="_DiagnosticArgs_"></span><span id="_diagnosticargs_"></span><span id="_DIAGNOSTICARGS_"></span><*DiagnosticArgs*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="a3488-109"><dt>

<span id="_DiagnosticArgs_"></span><span id="_diagnosticargs_"></span><span id="_DIAGNOSTICARGS_"></span><*DiagnosticArgs*>
</dt> </span></span><dd>

<span data-ttu-id="a3488-110">El compilador acepta los siguientes argumentos de diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="a3488-110">The compiler accepts the following diagnostic arguments.</span></span>

<dl> <dt>

<span data-ttu-id="a3488-111"><span id="_m__diagnostic-level_"></span><span id="_M__DIAGNOSTIC-LEVEL_"></span>**/m** **<** _nivel de diagnóstico_*_>_*</span><span class="sxs-lookup"><span data-stu-id="a3488-111"><span id="_m__diagnostic-level_"></span><span id="_M__DIAGNOSTIC-LEVEL_"></span>**/m** **<**_diagnostic-level_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="a3488-112">Tipo de diagnóstico que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="a3488-112">Type of diagnostics to display.</span></span> <span data-ttu-id="a3488-113">El valor predeterminado es 2.</span><span class="sxs-lookup"><span data-stu-id="a3488-113">The default is 2.</span></span>

<span data-ttu-id="a3488-114">A continuación se muestra una lista de los valores de nivel de diagnóstico que se pueden establecer:</span><span class="sxs-lookup"><span data-stu-id="a3488-114">The following is a list of the diagnostic level values that can be set:</span></span>

-   <span data-ttu-id="a3488-115">0 = silenciosa</span><span class="sxs-lookup"><span data-stu-id="a3488-115">0 = Silent</span></span>
-   <span data-ttu-id="a3488-116">1 = irrecuperable</span><span class="sxs-lookup"><span data-stu-id="a3488-116">1 = Fatal</span></span>
-   <span data-ttu-id="a3488-117">2 = fatal y ADVERTENCIA</span><span class="sxs-lookup"><span data-stu-id="a3488-117">2 = Fatal and warning</span></span>
-   <span data-ttu-id="a3488-118">3 = mensajes irrecuperables, de advertencia y de información</span><span class="sxs-lookup"><span data-stu-id="a3488-118">3 = Fatal, warning, and information messages</span></span>

</dd> <dt>

<span data-ttu-id="a3488-119"><span id="_c__count_"></span><span id="_C__COUNT_"></span>**/c** **<** _recuento_*_>_*</span><span class="sxs-lookup"><span data-stu-id="a3488-119"><span id="_c__count_"></span><span id="_C__COUNT_"></span>**/c** **<**_count_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="a3488-120">Número máximo de mensajes irrecuperables y de advertencia que se van a mostrar; *Count* debe ser un entero decimal positivo.</span><span class="sxs-lookup"><span data-stu-id="a3488-120">Maximum number of fatal and warning messages to display; *count* must be a positive decimal integer.</span></span> <span data-ttu-id="a3488-121">Si no se especifica **/c** , no hay ningún límite en el número de errores que se pueden informar.</span><span class="sxs-lookup"><span data-stu-id="a3488-121">If **/c** is not specified, there is no limit to the number of errors that can be reported.</span></span>

<span data-ttu-id="a3488-122"></dd> </dl> </dd> <dt>

<span id="_VersionArgs_"></span><span id="_versionargs_"></span><span id="_VERSIONARGS_"></span><*VersionArgs*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="a3488-122"></dd> </dl> </dd> <dt>

<span id="_VersionArgs_"></span><span id="_versionargs_"></span><span id="_VERSIONARGS_"></span><*VersionArgs*>
</dt> </span></span><dd>

<span data-ttu-id="a3488-123">El compilador acepta los siguientes argumentos de la versión.</span><span class="sxs-lookup"><span data-stu-id="a3488-123">The compiler accepts the following version arguments.</span></span>

<dl> <dt>

<span data-ttu-id="a3488-124"><span id="_v1"></span><span id="_V1"></span>**/v1**</span><span class="sxs-lookup"><span data-stu-id="a3488-124"><span id="_v1"></span><span id="_V1"></span>**/v1**</span></span>
</dt> <dd>

<span data-ttu-id="a3488-125">Especifica la conformidad estricta con la SMI de SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="a3488-125">Specifies strict conformance to the SNMPv1 SMI.</span></span> <span data-ttu-id="a3488-126">El compilador informa de un error si detecta instrucciones que no son SNMPv1.</span><span class="sxs-lookup"><span data-stu-id="a3488-126">The compiler reports an error if it detects non-SNMPv1 statements.</span></span>

</dd> <dt>

<span data-ttu-id="a3488-127"><span id="_v2c"></span><span id="_V2C"></span>**/v2c**</span><span class="sxs-lookup"><span data-stu-id="a3488-127"><span id="_v2c"></span><span id="_V2C"></span>**/v2c**</span></span>
</dt> <dd>

<span data-ttu-id="a3488-128">Especifica la conformidad estricta con la SMI de SNMPv2.</span><span class="sxs-lookup"><span data-stu-id="a3488-128">Specifies strict conformance to the SNMPv2 SMI.</span></span> <span data-ttu-id="a3488-129">El compilador informa de un error si detecta instrucciones que no son de SNMPv2.</span><span class="sxs-lookup"><span data-stu-id="a3488-129">The compiler reports an error if it detects non-SNMPv2 statements.</span></span>

<span data-ttu-id="a3488-130"></dd> </dl> </dd> <dt>

<span id="_CommandArgs_"></span><span id="_commandargs_"></span><span id="_COMMANDARGS_"></span><*CommandArgs*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="a3488-130"></dd> </dl> </dd> <dt>

<span id="_CommandArgs_"></span><span id="_commandargs_"></span><span id="_COMMANDARGS_"></span><*CommandArgs*>
</dt> </span></span><dd>

<span data-ttu-id="a3488-131">El compilador acepta los siguientes argumentos de comando.</span><span class="sxs-lookup"><span data-stu-id="a3488-131">The compiler accepts the following command arguments.</span></span>

<dl> <dt>

<span data-ttu-id="a3488-132"><span id="_d"></span><span id="_D"></span>**/d.**</span><span class="sxs-lookup"><span data-stu-id="a3488-132"><span id="_d"></span><span id="_D"></span>**/d**</span></span>
</dt> <dd>

<span data-ttu-id="a3488-133">Elimina el módulo especificado de SMIR.</span><span class="sxs-lookup"><span data-stu-id="a3488-133">Deletes the specified module from the SMIR.</span></span>

</dd> <dt>

<span data-ttu-id="a3488-134"><span id="_p"></span><span id="_P"></span>**/p**</span><span class="sxs-lookup"><span data-stu-id="a3488-134"><span id="_p"></span><span id="_P"></span>**/p**</span></span>
</dt> <dd>

<span data-ttu-id="a3488-135">Elimina todos los módulos de SMIR.</span><span class="sxs-lookup"><span data-stu-id="a3488-135">Deletes all modules in the SMIR.</span></span>

</dd> <dt>

<span data-ttu-id="a3488-136"><span id="_l"></span><span id="_L"></span>**l**</span><span class="sxs-lookup"><span data-stu-id="a3488-136"><span id="_l"></span><span id="_L"></span>**/l**</span></span>
</dt> <dd>

<span data-ttu-id="a3488-137">Enumera todos los módulos de SMIR.</span><span class="sxs-lookup"><span data-stu-id="a3488-137">Lists all modules in the SMIR.</span></span>

</dd> <dt>

<span data-ttu-id="a3488-138"><span id="_lc"></span><span id="_LC"></span>**/lc**</span><span class="sxs-lookup"><span data-stu-id="a3488-138"><span id="_lc"></span><span id="_LC"></span>**/lc**</span></span>
</dt> <dd>

<span data-ttu-id="a3488-139">Realiza una comprobación de sintaxis local en el módulo.</span><span class="sxs-lookup"><span data-stu-id="a3488-139">Performs a local syntax check on the module.</span></span>

</dd> <dt>

<span data-ttu-id="a3488-140"><span id="_ec___CommandModifier__"></span><span id="_ec___commandmodifier__"></span><span id="_EC___COMMANDMODIFIER__"></span>**/EC** **\[<** _CommandModifier_*_>\]_*</span><span class="sxs-lookup"><span data-stu-id="a3488-140"><span id="_ec___CommandModifier__"></span><span id="_ec___commandmodifier__"></span><span id="_EC___COMMANDMODIFIER__"></span>**/ec** **\[<**_CommandModifier_*_>\]_*</span></span>
</dt> <dd>

<span data-ttu-id="a3488-141">Realiza comprobaciones locales y externas en el módulo.</span><span class="sxs-lookup"><span data-stu-id="a3488-141">Performs local and external checks on the module.</span></span>

</dd> <dt>

<span data-ttu-id="a3488-142"><span id="_a__CommandModifier__"></span><span id="_a__commandmodifier__"></span><span id="_A__COMMANDMODIFIER__"></span>**\[ /a <** _CommandModifier_*_>\]_*</span><span class="sxs-lookup"><span data-stu-id="a3488-142"><span id="_a__CommandModifier__"></span><span id="_a__commandmodifier__"></span><span id="_A__COMMANDMODIFIER__"></span>**/a\[<**_CommandModifier_*_>\]_*</span></span>
</dt> <dd>

<span data-ttu-id="a3488-143">Realiza comprobaciones locales y externas y carga el módulo en el SMIR.</span><span class="sxs-lookup"><span data-stu-id="a3488-143">Performs local and external checks and loads the module into the SMIR.</span></span>

</dd> <dt>

<span data-ttu-id="a3488-144"><span id="_sa__CommandModifier__"></span><span id="_sa__commandmodifier__"></span><span id="_SA__COMMANDMODIFIER__"></span>**\[ /SA <** _CommandModifier_*_>\]_*</span><span class="sxs-lookup"><span data-stu-id="a3488-144"><span id="_sa__CommandModifier__"></span><span id="_sa__commandmodifier__"></span><span id="_SA__COMMANDMODIFIER__"></span>**/sa\[<**_CommandModifier_*_>\]_*</span></span>
</dt> <dd>

<span data-ttu-id="a3488-145">Igual que **/a**, pero funciona en modo silencioso.</span><span class="sxs-lookup"><span data-stu-id="a3488-145">Same as **/a**, but works silently.</span></span>

</dd> <dt>

<span data-ttu-id="a3488-146"><span id="_g__CommandModifier__"></span><span id="_g__commandmodifier__"></span><span id="_G__COMMANDMODIFIER__"></span>**\[ /g <** _CommandModifier_*_>\]_*</span><span class="sxs-lookup"><span data-stu-id="a3488-146"><span id="_g__CommandModifier__"></span><span id="_g__commandmodifier__"></span><span id="_G__COMMANDMODIFIER__"></span>**/g\[<**_CommandModifier_*_>\]_*</span></span>
</dt> <dd>

<span data-ttu-id="a3488-147">Genera un archivo SMIR. mof que se puede cargar posteriormente en WMI mediante el compilador MOF.</span><span class="sxs-lookup"><span data-stu-id="a3488-147">Generates a SMIR .mof file that you can later load into WMI using the MOF compiler.</span></span> <span data-ttu-id="a3488-148">Lo utiliza el proveedor de clase SNMP para proporcionar clases de forma dinámica a uno o varios espacios de nombres.</span><span class="sxs-lookup"><span data-stu-id="a3488-148">Used by the SNMP class provider to provide classes dynamically to one or more namespaces.</span></span> <span data-ttu-id="a3488-149">Utilice esta opción si no sabe qué MIB son compatibles con los dispositivos SNMP que se están administrando.</span><span class="sxs-lookup"><span data-stu-id="a3488-149">Use this option when you do not know which MIBs are supported by the SNMP devices being managed.</span></span> <span data-ttu-id="a3488-150">El proveedor de clase SNMP comprueba el dispositivo en tiempo de ejecución para la presencia de esta MIB y proporciona las clases dinámicamente al espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="a3488-150">The SNMP class provider checks the device at runtime for the presence of this MIB and supplies the classes dynamically to the namespace.</span></span>

</dd> <dt>

<span data-ttu-id="a3488-151"><span id="_gc__CommandModifier__"></span><span id="_gc__commandmodifier__"></span><span id="_GC__COMMANDMODIFIER__"></span>**\[ /GC <** _CommandModifier_*_>\]_*</span><span class="sxs-lookup"><span data-stu-id="a3488-151"><span id="_gc__CommandModifier__"></span><span id="_gc__commandmodifier__"></span><span id="_GC__COMMANDMODIFIER__"></span>**/gc\[<**_CommandModifier_*_>\]_*</span></span>
</dt> <dd>

<span data-ttu-id="a3488-152">Genera un archivo. mof estático que se puede cargar más adelante en WMI como clases estáticas para un espacio de nombres determinado.</span><span class="sxs-lookup"><span data-stu-id="a3488-152">Generates a static .mof file that can be loaded later into WMI as static classes for a particular namespace.</span></span> <span data-ttu-id="a3488-153">Utilice esta opción cuando sepa qué MIB son compatibles con los dispositivos SNMP que se están administrando.</span><span class="sxs-lookup"><span data-stu-id="a3488-153">Use this option when you know which MIBs are supported by the SNMP devices being managed.</span></span> <span data-ttu-id="a3488-154">Puede definir el archivo. mof que se generará dirigiendo la salida del comando a un archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="a3488-154">You can define the .mof file to be generated by directing the output of your command to a specified file.</span></span> <span data-ttu-id="a3488-155">No se usa con **/ext/o**.</span><span class="sxs-lookup"><span data-stu-id="a3488-155">Do not use with **/ext/o**.</span></span>

<span data-ttu-id="a3488-156"></dd> </dl> </dd> <dt>

<span id="_CommandModifiers_"></span><span id="_commandmodifiers_"></span><span id="_COMMANDMODIFIERS_"></span><*CommandModifiers*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="a3488-156"></dd> </dl> </dd> <dt>

<span id="_CommandModifiers_"></span><span id="_commandmodifiers_"></span><span id="_COMMANDMODIFIERS_"></span><*CommandModifiers*>
</dt> </span></span><dd>

<span data-ttu-id="a3488-157">El compilador acepta los siguientes modificadores de comando.</span><span class="sxs-lookup"><span data-stu-id="a3488-157">The compiler accepts the following command modifiers.</span></span>

<dl> <dt>

<span data-ttu-id="a3488-158"><span id="_i_directory_"></span><span id="_I_DIRECTORY_"></span>**/i<** _directorio_*_>_*</span><span class="sxs-lookup"><span data-stu-id="a3488-158"><span id="_i_directory_"></span><span id="_I_DIRECTORY_"></span>**/i<**_directory_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="a3488-159">Especifica el directorio en el que se buscarán los módulos MIB dependientes.</span><span class="sxs-lookup"><span data-stu-id="a3488-159">Specifies a directory to be searched for dependent MIB modules.</span></span> <span data-ttu-id="a3488-160">Use con **/a**, **/EC**, **/g**, **/GC** y **/SA**.</span><span class="sxs-lookup"><span data-stu-id="a3488-160">Use with **/a**, **/ec**, **/g**, **/gc**, and **/sa**.</span></span> <span data-ttu-id="a3488-161">La opción **/i** puede aparecer varias veces en el comando. los directorios se buscan en el orden especificado en el comando.</span><span class="sxs-lookup"><span data-stu-id="a3488-161">The **/i** option can appear multiple times in the command; directories are searched in the order specified in the command.</span></span>

</dd> <dt>

<span data-ttu-id="a3488-162"><span id="_ch"></span><span id="_CH"></span>**/CH**</span><span class="sxs-lookup"><span data-stu-id="a3488-162"><span id="_ch"></span><span id="_CH"></span>**/ch**</span></span>
</dt> <dd>

<span data-ttu-id="a3488-163">Genera información de contexto, como la fecha, la hora, el host o el usuario, en el encabezado del archivo MOF.</span><span class="sxs-lookup"><span data-stu-id="a3488-163">Generates context information, such as the date, time, host, or user, in the MOF file header.</span></span> <span data-ttu-id="a3488-164">Use con **/g** y **/GC**.</span><span class="sxs-lookup"><span data-stu-id="a3488-164">Use with **/g** and **/gc**.</span></span>

</dd> <dt>

<span data-ttu-id="a3488-165"><span id="_t"></span><span id="_T"></span>**/t**</span><span class="sxs-lookup"><span data-stu-id="a3488-165"><span id="_t"></span><span id="_T"></span>**/t**</span></span>
</dt> <dd>

<span data-ttu-id="a3488-166">Genera clases [SnmpNotification](snmpnotification.md) .</span><span class="sxs-lookup"><span data-stu-id="a3488-166">Generates [SnmpNotification](snmpnotification.md) classes.</span></span> <span data-ttu-id="a3488-167">Use con **/a**, **/g** y **/SA**.</span><span class="sxs-lookup"><span data-stu-id="a3488-167">Use with **/a**, **/g**, and **/sa**.</span></span>

</dd> <dt>

<span data-ttu-id="a3488-168"><span id="_ext"></span><span id="_EXT"></span>**/ext**</span><span class="sxs-lookup"><span data-stu-id="a3488-168"><span id="_ext"></span><span id="_EXT"></span>**/ext**</span></span>
</dt> <dd>

<span data-ttu-id="a3488-169">Genera clases [SnmpExtendedNotification](snmpextendednotification.md) .</span><span class="sxs-lookup"><span data-stu-id="a3488-169">Generates [SnmpExtendedNotification](snmpextendednotification.md) classes.</span></span> <span data-ttu-id="a3488-170">Use con **/a**, **/g** y **/SA**.</span><span class="sxs-lookup"><span data-stu-id="a3488-170">Use with **/a**, **/g**, and **/sa**.</span></span>

</dd> <dt>

<span data-ttu-id="a3488-171"><span id="_t_o"></span><span id="_T_O"></span>**/t/o**</span><span class="sxs-lookup"><span data-stu-id="a3488-171"><span id="_t_o"></span><span id="_T_O"></span>**/t/o**</span></span>
</dt> <dd>

<span data-ttu-id="a3488-172">Genera solo clases [SnmpNotification](snmpnotification.md) .</span><span class="sxs-lookup"><span data-stu-id="a3488-172">Generates only [SnmpNotification](snmpnotification.md) classes.</span></span> <span data-ttu-id="a3488-173">Use con **/a**, **/g** y **/SA**.</span><span class="sxs-lookup"><span data-stu-id="a3488-173">Use with **/a**, **/g**, and **/sa**.</span></span>

</dd> <dt>

<span data-ttu-id="a3488-174"><span id="_ext_o"></span><span id="_EXT_O"></span>**/ext/o**</span><span class="sxs-lookup"><span data-stu-id="a3488-174"><span id="_ext_o"></span><span id="_EXT_O"></span>**/ext/o**</span></span>
</dt> <dd>

<span data-ttu-id="a3488-175">Genera solo clases [SnmpExtendedNotification](snmpextendednotification.md) .</span><span class="sxs-lookup"><span data-stu-id="a3488-175">Generates only [SnmpExtendedNotification](snmpextendednotification.md) classes.</span></span> <span data-ttu-id="a3488-176">Use con **/a**, **/g** y **/SA**.</span><span class="sxs-lookup"><span data-stu-id="a3488-176">Use with **/a**, **/g**, and **/sa**.</span></span>

</dd> <dt>

<span data-ttu-id="a3488-177"><span id="_s"></span><span id="_S"></span>**modificado**</span><span class="sxs-lookup"><span data-stu-id="a3488-177"><span id="_s"></span><span id="_S"></span>**/s**</span></span>
</dt> <dd>

<span data-ttu-id="a3488-178">No asigna el texto de la cláusula Description.</span><span class="sxs-lookup"><span data-stu-id="a3488-178">Does not map the text of the DESCRIPTION clause.</span></span> <span data-ttu-id="a3488-179">Use con **/a**, **/g**, **/GC** y **/SA**.</span><span class="sxs-lookup"><span data-stu-id="a3488-179">Use with **/a**, **/g**, **/gc**, and **/sa**.</span></span> <span data-ttu-id="a3488-180">Utilice esta opción si desea minimizar los requisitos de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="a3488-180">Use this option when you want to minimize storage requirements.</span></span>

</dd> <dt>

<span data-ttu-id="a3488-181"><span id="_auto"></span><span id="_AUTO"></span>**/auto**</span><span class="sxs-lookup"><span data-stu-id="a3488-181"><span id="_auto"></span><span id="_AUTO"></span>**/auto**</span></span>
</dt> <dd>

<span data-ttu-id="a3488-182">Vuelve a generar la tabla de búsqueda de MIB antes de completar el <conmutador de> *CommandArg* .</span><span class="sxs-lookup"><span data-stu-id="a3488-182">Rebuilds the MIB lookup table before completing the <*CommandArg*> switch.</span></span> <span data-ttu-id="a3488-183">Use con **/a**, **/EC**, **/g** y **/GC**.</span><span class="sxs-lookup"><span data-stu-id="a3488-183">Use with **/a**, **/ec**, **/g**, and **/gc**.</span></span>

<span data-ttu-id="a3488-184"></dd> </dl> </dd> <dt>

<span id="_RegistryArgs_"></span><span id="_registryargs_"></span><span id="_REGISTRYARGS_"></span><*RegistryArgs*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="a3488-184"></dd> </dl> </dd> <dt>

<span id="_RegistryArgs_"></span><span id="_registryargs_"></span><span id="_REGISTRYARGS_"></span><*RegistryArgs*>
</dt> </span></span><dd>

<span data-ttu-id="a3488-185">El compilador acepta los siguientes argumentos del registro.</span><span class="sxs-lookup"><span data-stu-id="a3488-185">The compiler accepts the following registry arguments.</span></span>

<dl> <dt>

<span data-ttu-id="a3488-186"><span id="_pa"></span><span id="_PA"></span>**/pa**</span><span class="sxs-lookup"><span data-stu-id="a3488-186"><span id="_pa"></span><span id="_PA"></span>**/pa**</span></span>
</dt> <dd>

<span data-ttu-id="a3488-187">Agrega el directorio especificado al registro.</span><span class="sxs-lookup"><span data-stu-id="a3488-187">Adds the specified directory to the registry.</span></span> <span data-ttu-id="a3488-188">El valor predeterminado es el directorio actual.</span><span class="sxs-lookup"><span data-stu-id="a3488-188">The default is the current directory.</span></span>

</dd> <dt>

<span data-ttu-id="a3488-189"><span id="_pd"></span><span id="_PD"></span>**/PD**</span><span class="sxs-lookup"><span data-stu-id="a3488-189"><span id="_pd"></span><span id="_PD"></span>**/pd**</span></span>
</dt> <dd>

<span data-ttu-id="a3488-190">Elimina el directorio especificado del registro.</span><span class="sxs-lookup"><span data-stu-id="a3488-190">Deletes the specified directory from the registry.</span></span> <span data-ttu-id="a3488-191">El valor predeterminado es el directorio actual.</span><span class="sxs-lookup"><span data-stu-id="a3488-191">The default is the current directory.</span></span>

</dd> <dt>

<span data-ttu-id="a3488-192"><span id="_pl"></span><span id="_PL"></span>**/pl**</span><span class="sxs-lookup"><span data-stu-id="a3488-192"><span id="_pl"></span><span id="_PL"></span>**/pl**</span></span>
</dt> <dd>

<span data-ttu-id="a3488-193">Enumera los directorios de búsqueda MIB en el registro.</span><span class="sxs-lookup"><span data-stu-id="a3488-193">Lists the MIB lookup directories in the registry.</span></span>

</dd> <dt>

<span data-ttu-id="a3488-194"><span id="_r"></span><span id="_R"></span>**/r**</span><span class="sxs-lookup"><span data-stu-id="a3488-194"><span id="_r"></span><span id="_R"></span>**/r**</span></span>
</dt> <dd>

<span data-ttu-id="a3488-195">Vuelve a generar la tabla de búsqueda MIB completa.</span><span class="sxs-lookup"><span data-stu-id="a3488-195">Rebuilds the entire MIB lookup table.</span></span>

<span data-ttu-id="a3488-196"></dd> </dl> </dd> <dt>

<span id="_ModuleInfoArgs_"></span><span id="_moduleinfoargs_"></span><span id="_MODULEINFOARGS_"></span><*ModuleInfoArgs*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="a3488-196"></dd> </dl> </dd> <dt>

<span id="_ModuleInfoArgs_"></span><span id="_moduleinfoargs_"></span><span id="_MODULEINFOARGS_"></span><*ModuleInfoArgs*>
</dt> </span></span><dd>

<span data-ttu-id="a3488-197">El compilador acepta los siguientes argumentos de información del módulo.</span><span class="sxs-lookup"><span data-stu-id="a3488-197">The compiler accepts the following module information arguments.</span></span>

<dl> <dt>

<span data-ttu-id="a3488-198"><span id="_n"></span><span id="_N"></span>**/n**</span><span class="sxs-lookup"><span data-stu-id="a3488-198"><span id="_n"></span><span id="_N"></span>**/n**</span></span>
</dt> <dd>

<span data-ttu-id="a3488-199">Devuelve el nombre ASN. 1 del módulo especificado.</span><span class="sxs-lookup"><span data-stu-id="a3488-199">Returns the ASN.1 name of the specified module.</span></span>

</dd> <dt>

<span data-ttu-id="a3488-200"><span id="_ni"></span><span id="_NI"></span>**/ni**</span><span class="sxs-lookup"><span data-stu-id="a3488-200"><span id="_ni"></span><span id="_NI"></span>**/ni**</span></span>
</dt> <dd>

<span data-ttu-id="a3488-201">Devuelve los nombres ASN. 1 de todos los módulos de importación a los que hace referencia el módulo de entrada.</span><span class="sxs-lookup"><span data-stu-id="a3488-201">Returns the ASN.1 names of all import modules referred to by the input module.</span></span>

<span data-ttu-id="a3488-202"></dd> </dl> </dd> <dt>

<span id="_HelpArgs_"></span><span id="_helpargs_"></span><span id="_HELPARGS_"></span><*HelpArgs*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="a3488-202"></dd> </dl> </dd> <dt>

<span id="_HelpArgs_"></span><span id="_helpargs_"></span><span id="_HELPARGS_"></span><*HelpArgs*>
</dt> </span></span><dd>

<span data-ttu-id="a3488-203">El compilador acepta los siguientes argumentos de la ayuda.</span><span class="sxs-lookup"><span data-stu-id="a3488-203">The compiler accepts the following help arguments.</span></span>

<dl> <dt>

<span data-ttu-id="a3488-204"><span id="_h"></span><span id="_H"></span>**/h**</span><span class="sxs-lookup"><span data-stu-id="a3488-204"><span id="_h"></span><span id="_H"></span>**/h**</span></span>
</dt> <dd>

<span data-ttu-id="a3488-205">Muestra ayuda sobre la sintaxis del compilador SNMP.</span><span class="sxs-lookup"><span data-stu-id="a3488-205">Displays help on the SNMP compiler syntax.</span></span>

</dd> <dt>

<span data-ttu-id="a3488-206"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="a3488-206"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="a3488-207">Muestra ayuda sobre la sintaxis del compilador SNMP.</span><span class="sxs-lookup"><span data-stu-id="a3488-207">Displays help on the SNMP compiler syntax.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a3488-208">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a3488-208">Remarks</span></span>

<span data-ttu-id="a3488-209">Los módulos de información SNMP se escriben en un subconjunto de la notación de sintaxis abstracta uno (ASN. 1) el compilador realiza las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="a3488-209">SNMP information modules are written in a subset of the Abstract Syntax Notation One (ASN.1) The compiler performs the following functions:</span></span>

-   <span data-ttu-id="a3488-210">Carga los datos del módulo de información SNMP.</span><span class="sxs-lookup"><span data-stu-id="a3488-210">Loads the data from the SNMP information module.</span></span>
-   <span data-ttu-id="a3488-211">Realiza operaciones de comprobación en el módulo de información.</span><span class="sxs-lookup"><span data-stu-id="a3488-211">Performs checking operations on the information module.</span></span> <span data-ttu-id="a3488-212">Por ejemplo, comprueba la sintaxis local y comprueba las referencias externas con respecto a la información de los módulos subsidiarios.</span><span class="sxs-lookup"><span data-stu-id="a3488-212">For example, it checks the local syntax and it checks external references against information in the subsidiary modules.</span></span>
-   <span data-ttu-id="a3488-213">Quita todos los datos previamente cargados del SMIR, o bien los datos cargados desde un módulo de información.</span><span class="sxs-lookup"><span data-stu-id="a3488-213">Removes all previously loaded data from the SMIR, or removes data loaded from one information module.</span></span>
-   <span data-ttu-id="a3488-214">Devuelve el nombre de módulo ASN. 1 de un archivo especificado o devuelve los nombres de módulo ASN. 1 de todos los módulos importados de un archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="a3488-214">Returns the ASN.1 module name of a specified file or returns the ASN.1 module names of all imported modules in a specified file.</span></span>
-   <span data-ttu-id="a3488-215">Devuelve los nombres de módulo ASN.1 de todos los módulos de información SNMP cargados actualmente en el SMIR.</span><span class="sxs-lookup"><span data-stu-id="a3488-215">Returns the ASN.1 module names of all SNMP information modules currently loaded in the SMIR.</span></span>
-   <span data-ttu-id="a3488-216">Realiza la resolución automática de los módulos importados en lugar de solicitar a los usuarios que especifiquen manualmente los módulos necesarios.</span><span class="sxs-lookup"><span data-stu-id="a3488-216">Performs automatic resolution of imported modules rather than requiring users to specify the required modules manually.</span></span>
-   <span data-ttu-id="a3488-217">Realiza una operación de carga silenciosa que no genera ningún resultado, pero se puede usar para cargar datos en el SMIR durante una operación de instalación.</span><span class="sxs-lookup"><span data-stu-id="a3488-217">Performs a silent-loading mode of operation that does not generate any output, but can be used to load data into the SMIR during an installation operation.</span></span>
-   <span data-ttu-id="a3488-218">Genera los datos del módulo de información SNMP en el SMIR.</span><span class="sxs-lookup"><span data-stu-id="a3488-218">Outputs the data from the SNMP information module into the SMIR.</span></span>
-   <span data-ttu-id="a3488-219">Opcionalmente, crea un archivo MOF estático o SMIR que contiene la salida del módulo de información.</span><span class="sxs-lookup"><span data-stu-id="a3488-219">Optionally creates a static or SMIR MOF file containing the output from the information module.</span></span>

    <span data-ttu-id="a3488-220">Si es necesario, puede cargar el archivo. mof estático en un espacio de nombres WMI.</span><span class="sxs-lookup"><span data-stu-id="a3488-220">If necessary, you can load the static .mof file into a WMI namespace.</span></span> <span data-ttu-id="a3488-221">Un archivo SMIR. mof contiene el nombre del espacio de nombres SNMP en el que deben residir las clases.</span><span class="sxs-lookup"><span data-stu-id="a3488-221">A SMIR .mof file contains the name of the SNMP namespace in which the classes should reside.</span></span>

## <a name="examples"></a><span data-ttu-id="a3488-222">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a3488-222">Examples</span></span>

<span data-ttu-id="a3488-223">En el ejemplo siguiente se define el archivo pra. mof para que sea la salida del archivo pra. MIB.</span><span class="sxs-lookup"><span data-stu-id="a3488-223">The following example defines the pra.mof file to be the output from the pra.mib file.</span></span>

``` syntax
smi2smir /m 3 /v1 /gc /pra.mib > pra.mof
```

## <a name="requirements"></a><span data-ttu-id="a3488-224">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3488-224">Requirements</span></span>



| <span data-ttu-id="a3488-225">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3488-225">Requirement</span></span> | <span data-ttu-id="a3488-226">Value</span><span class="sxs-lookup"><span data-stu-id="a3488-226">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="a3488-227">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3488-227">Minimum supported client</span></span><br/> | <span data-ttu-id="a3488-228">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a3488-228">Windows Vista</span></span><br/>       |
| <span data-ttu-id="a3488-229">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3488-229">Minimum supported server</span></span><br/> | <span data-ttu-id="a3488-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a3488-230">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a3488-231">Vea también</span><span class="sxs-lookup"><span data-stu-id="a3488-231">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3488-232">Mensajes de error del compilador SNMP</span><span class="sxs-lookup"><span data-stu-id="a3488-232">SNMP Compiler Error Messages</span></span>](snmp-compiler-error-messages.md)
</dt> <dt>

[<span data-ttu-id="a3488-233">Configuración del entorno SNMP de WMI</span><span class="sxs-lookup"><span data-stu-id="a3488-233">Setting up the WMI SNMP Environment</span></span>](setting-up-the-wmi-snmp-environment.md)
</dt> <dt>

[<span data-ttu-id="a3488-234">Acceso a dispositivos SNMP</span><span class="sxs-lookup"><span data-stu-id="a3488-234">Accessing SNMP Devices</span></span>](accessing-snmp-devices.md)
</dt> </dl>

 

 




