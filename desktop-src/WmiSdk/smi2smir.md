---
description: El compilador SNMP se ejecuta como un único archivo ejecutable en el modo de línea de comandos.
ms.assetid: 0e85fe84-dacb-4720-8242-ffa0046780f3
ms.tgt_platform: multiple
title: smi2smir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3909ef1df4047ba0b797fe4a01088c62e60b287969445d311214180e4fa441a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050173"
---
# <a name="smi2smir"></a>smi2smir

El compilador SNMP se ejecuta como un único archivo ejecutable en el modo de línea de comandos. El compilador acepta un módulo de información SNMP como entrada y acepta los módulos adicionales necesarios para resolver referencias externas. Use uno de los siguientes ejemplos de sintaxis de línea de comandos.

Para obtener más información sobre cuándo se usa este compilador, vea [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).

``` syntax
smi2smir [<DiagnosticArgs>] [<VersionArgs>]
     <CommandArgs> <MIB file> [<Import Files>]

smi2smir [<DiagnosticArgs>] <RegistryArgs> [<Directory>]

smi2smir <ModuleInfoArgs> <MIB file>

smi2smir <HelpArgs>
```

## <a name="switches"></a>Modificadores

<dl> <dt>

<span id="_DiagnosticArgs_"></span><span id="_diagnosticargs_"></span><span id="_DIAGNOSTICARGS_"></span><*DiagnosticArgs*>
</dt> <dd>

El compilador acepta los siguientes argumentos de diagnóstico.

<dl> <dt>

<span id="_m__diagnostic-level_"></span><span id="_M__DIAGNOSTIC-LEVEL_"></span>**/m** **<** _nivel de diagnóstico_*_>_*
</dt> <dd>

Tipo de diagnóstico que se mostrará. El valor predeterminado es 2.

A continuación se muestra una lista de los valores de nivel de diagnóstico que se pueden establecer:

-   0 = Silencioso
-   1 = Fatal
-   2 = Grave y advertencia
-   3 = Mensajes de información, advertencias y graves

</dd> <dt>

<span id="_c__count_"></span><span id="_C__COUNT_"></span>**/c** **<** _count_*_>_*
</dt> <dd>

Número máximo de mensajes graves y de advertencia que se mostrarán; *count* debe ser un entero decimal positivo. Si no se especifica **/c,** no hay ningún límite en el número de errores que se pueden notifica.

</dd> </dl> </dd> <dt>

<span id="_VersionArgs_"></span><span id="_versionargs_"></span><span id="_VERSIONARGS_"></span><*VersionArgs*>
</dt> <dd>

El compilador acepta los siguientes argumentos de versión.

<dl> <dt>

<span id="_v1"></span><span id="_V1"></span>**/v1**
</dt> <dd>

Especifica la conformidad estricta con SMI de SNMPv1. El compilador notifica un error si detecta instrucciones que no son SNMPv1.

</dd> <dt>

<span id="_v2c"></span><span id="_V2C"></span>**/v2c**
</dt> <dd>

Especifica la conformidad estricta con SMI de SNMPv2. El compilador notifica un error si detecta instrucciones que no son SNMPv2.

</dd> </dl> </dd> <dt>

<span id="_CommandArgs_"></span><span id="_commandargs_"></span><span id="_COMMANDARGS_"></span><*CommandArgs*>
</dt> <dd>

El compilador acepta los siguientes argumentos de comando.

<dl> <dt>

<span id="_d"></span><span id="_D"></span>**/d**
</dt> <dd>

Elimina el módulo especificado del SMIR.

</dd> <dt>

<span id="_p"></span><span id="_P"></span>**/p**
</dt> <dd>

Elimina todos los módulos del SMIR.

</dd> <dt>

<span id="_l"></span><span id="_L"></span>**/l**
</dt> <dd>

Enumera todos los módulos de SMIR.

</dd> <dt>

<span id="_lc"></span><span id="_LC"></span>**/lc**
</dt> <dd>

Realiza una comprobación de sintaxis local en el módulo.

</dd> <dt>

<span id="_ec___CommandModifier__"></span><span id="_ec___commandmodifier__"></span><span id="_EC___COMMANDMODIFIER__"></span>**/ec** **\[<** _CommandModifier_*_>\]_*
</dt> <dd>

Realiza comprobaciones locales y externas en el módulo.

</dd> <dt>

<span id="_a__CommandModifier__"></span><span id="_a__commandmodifier__"></span><span id="_A__COMMANDMODIFIER__"></span>**/a \[ <** _CommandModifier_*_>\]_*
</dt> <dd>

Realiza comprobaciones locales y externas y carga el módulo en el SMIR.

</dd> <dt>

<span id="_sa__CommandModifier__"></span><span id="_sa__commandmodifier__"></span><span id="_SA__COMMANDMODIFIER__"></span>**/sa \[ <** _CommandModifier_*_>\]_*
</dt> <dd>

Igual que **/a**, pero funciona en modo silencioso.

</dd> <dt>

<span id="_g__CommandModifier__"></span><span id="_g__commandmodifier__"></span><span id="_G__COMMANDMODIFIER__"></span>**/g \[ <** _CommandModifier_*_>\]_*
</dt> <dd>

Genera un archivo SMIR .mof que se puede cargar más adelante en WMI mediante el compilador MOF. Usado por el proveedor de clases SNMP para proporcionar clases dinámicamente a uno o varios espacios de nombres. Use esta opción si no sabe qué MIB son compatibles con los dispositivos SNMP que se administran. El proveedor de clases SNMP comprueba la presencia de este MIB en el dispositivo en tiempo de ejecución y proporciona las clases dinámicamente al espacio de nombres .

</dd> <dt>

<span id="_gc__CommandModifier__"></span><span id="_gc__commandmodifier__"></span><span id="_GC__COMMANDMODIFIER__"></span>**/gc \[ <** _CommandModifier_*_>\]_*
</dt> <dd>

Genera un archivo .mof estático que se puede cargar más adelante en WMI como clases estáticas para un espacio de nombres determinado. Use esta opción cuando sepa qué MIB son compatibles con los dispositivos SNMP que se administran. Puede definir el archivo .mof que se va a generar si dirige la salida del comando a un archivo especificado. No use con **/ext/o**.

</dd> </dl> </dd> <dt>

<span id="_CommandModifiers_"></span><span id="_commandmodifiers_"></span><span id="_COMMANDMODIFIERS_"></span><*CommandModifiers*>
</dt> <dd>

El compilador acepta los siguientes modificadores de comando.

<dl> <dt>

<span id="_i_directory_"></span><span id="_I_DIRECTORY_"></span>**Directorio de</i** *_>_*
</dt> <dd>

Especifica un directorio en el que se buscarán módulos MIB dependientes. Use con **/a**, **/ec**, **/g**, **/gc** y **/sa**. La **opción /i** puede aparecer varias veces en el comando; Los directorios se buscan en el orden especificado en el comando .

</dd> <dt>

<span id="_ch"></span><span id="_CH"></span>**/ch**
</dt> <dd>

Genera información de contexto, como la fecha, hora, host o usuario, en el encabezado de archivo MOF. Use con **/g** y **/gc**.

</dd> <dt>

<span id="_t"></span><span id="_T"></span>**/t**
</dt> <dd>

Genera clases [SnmpNotification.](snmpnotification.md) Use con **/a**, **/g** y **/sa**.

</dd> <dt>

<span id="_ext"></span><span id="_EXT"></span>**/ext**
</dt> <dd>

Genera clases [SnmpExtendedNotification.](snmpextendednotification.md) Use con **/a**, **/g** y **/sa**.

</dd> <dt>

<span id="_t_o"></span><span id="_T_O"></span>**/t/o**
</dt> <dd>

Genera solo clases [SnmpNotification.](snmpnotification.md) Use con **/a**, **/g** y **/sa**.

</dd> <dt>

<span id="_ext_o"></span><span id="_EXT_O"></span>**/ext/o**
</dt> <dd>

Genera solo [clases SnmpExtendedNotification.](snmpextendednotification.md) Use con **/a**, **/g** y **/sa**.

</dd> <dt>

<span id="_s"></span><span id="_S"></span>**/s**
</dt> <dd>

No asigna el texto de la cláusula DESCRIPTION. Use con **/a**, **/g**, **/gc** y **/sa**. Use esta opción cuando desee minimizar los requisitos de almacenamiento.

</dd> <dt>

<span id="_auto"></span><span id="_AUTO"></span>**/auto**
</dt> <dd>

Vuelve a generar la tabla de búsqueda de MIB antes de completar el <*commandArg*> modificador. Use con **/a**, **/ec**, **/g** y **/gc**.

</dd> </dl> </dd> <dt>

<span id="_RegistryArgs_"></span><span id="_registryargs_"></span><span id="_REGISTRYARGS_"></span><*RegistryArgs*>
</dt> <dd>

El compilador acepta los siguientes argumentos del Registro.

<dl> <dt>

<span id="_pa"></span><span id="_PA"></span>**/pa**
</dt> <dd>

Agrega el directorio especificado al Registro. El valor predeterminado es el directorio actual.

</dd> <dt>

<span id="_pd"></span><span id="_PD"></span>**/pd**
</dt> <dd>

Elimina el directorio especificado del Registro. El valor predeterminado es el directorio actual.

</dd> <dt>

<span id="_pl"></span><span id="_PL"></span>**/pl**
</dt> <dd>

Enumera los directorios de búsqueda de MIB en el Registro.

</dd> <dt>

<span id="_r"></span><span id="_R"></span>**/r**
</dt> <dd>

Vuelve a generar toda la tabla de búsqueda de MIB.

</dd> </dl> </dd> <dt>

<span id="_ModuleInfoArgs_"></span><span id="_moduleinfoargs_"></span><span id="_MODULEINFOARGS_"></span><*ModuleInfoArgs*>
</dt> <dd>

El compilador acepta los siguientes argumentos de información del módulo.

<dl> <dt>

<span id="_n"></span><span id="_N"></span>**/n**
</dt> <dd>

Devuelve el nombre ASN.1 del módulo especificado.

</dd> <dt>

<span id="_ni"></span><span id="_NI"></span>**/ni**
</dt> <dd>

Devuelve los nombres asn.1 de todos los módulos de importación a los que hace referencia el módulo de entrada.

</dd> </dl> </dd> <dt>

<span id="_HelpArgs_"></span><span id="_helpargs_"></span><span id="_HELPARGS_"></span><*HelpArgs*>
</dt> <dd>

El compilador acepta los siguientes argumentos de ayuda.

<dl> <dt>

<span id="_h"></span><span id="_H"></span>**/h**
</dt> <dd>

Muestra ayuda sobre la sintaxis del compilador SNMP.

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Muestra ayuda sobre la sintaxis del compilador SNMP.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Comentarios

Los módulos de información SNMP se escriben en un subconjunto de la notación de sintaxis abstracta Uno (ASN.1) El compilador realiza las siguientes funciones:

-   Carga los datos del módulo de información de SNMP.
-   Realiza operaciones de comprobación en el módulo de información. Por ejemplo, comprueba la sintaxis local y comprueba las referencias externas con la información de los módulos de subsidiarias.
-   Quita todos los datos previamente cargados del SMIR, o bien los datos cargados desde un módulo de información.
-   Devuelve el nombre del módulo ASN.1 de un archivo especificado o devuelve los nombres de módulo ASN.1 de todos los módulos importados en un archivo especificado.
-   Devuelve los nombres de módulo ASN.1 de todos los módulos de información SNMP cargados actualmente en el SMIR.
-   Realiza la resolución automática de los módulos importados en lugar de requerir a los usuarios que especifiquen los módulos necesarios manualmente.
-   Realiza un modo de operación de carga silenciosa que no genera ninguna salida, pero que se puede usar para cargar datos en SCLUS durante una operación de instalación.
-   Genera los datos del módulo de información SNMP en el SMIR.
-   Opcionalmente, crea un archivo MOF estático o SMIR que contiene la salida del módulo de información.

    Si es necesario, puede cargar el archivo .mof estático en un espacio de nombres WMI. Un archivo .mof SMIR contiene el nombre del espacio de nombres SNMP en el que deben residir las clases.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se define el archivo pra.mof para que sea la salida del archivo pra.mib.

``` syntax
smi2smir /m 3 /v1 /gc /pra.mib > pra.mof
```

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Mensajes de error del compilador SNMP](snmp-compiler-error-messages.md)
</dt> <dt>

[Configuración del entorno SNMP de WMI](setting-up-the-wmi-snmp-environment.md)
</dt> <dt>

[Acceso a dispositivos SNMP](accessing-snmp-devices.md)
</dt> </dl>

 

 




