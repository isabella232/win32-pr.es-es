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
# <a name="smi2smir"></a>smi2smir

El compilador SNMP se ejecuta como un único archivo ejecutable en el modo de línea de comandos. El compilador acepta un módulo de información SNMP como entrada y acepta los módulos adicionales necesarios para resolver referencias externas. Use uno de los siguientes ejemplos de sintaxis de línea de comandos.

Para obtener más información acerca de Cuándo se usa este compilador, consulte [configuración del entorno WMI SNMP](setting-up-the-wmi-snmp-environment.md).

``` syntax
smi2smir [<DiagnosticArgs>] [<VersionArgs>]
     <CommandArgs> <MIB file> [<Import Files>]

smi2smir [<DiagnosticArgs>] <RegistryArgs> [<Directory>]

smi2smir <ModuleInfoArgs> <MIB file>

smi2smir <HelpArgs>
```

## <a name="switches"></a>Conmutadores

<dl> <dt>

<span id="_DiagnosticArgs_"></span><span id="_diagnosticargs_"></span><span id="_DIAGNOSTICARGS_"></span><*DiagnosticArgs*>
</dt> <dd>

El compilador acepta los siguientes argumentos de diagnóstico.

<dl> <dt>

<span id="_m__diagnostic-level_"></span><span id="_M__DIAGNOSTIC-LEVEL_"></span>**/m** **<** _nivel de diagnóstico_*_>_*
</dt> <dd>

Tipo de diagnóstico que se va a mostrar. El valor predeterminado es 2.

A continuación se muestra una lista de los valores de nivel de diagnóstico que se pueden establecer:

-   0 = silenciosa
-   1 = irrecuperable
-   2 = fatal y ADVERTENCIA
-   3 = mensajes irrecuperables, de advertencia y de información

</dd> <dt>

<span id="_c__count_"></span><span id="_C__COUNT_"></span>**/c** **<** _recuento_*_>_*
</dt> <dd>

Número máximo de mensajes irrecuperables y de advertencia que se van a mostrar; *Count* debe ser un entero decimal positivo. Si no se especifica **/c** , no hay ningún límite en el número de errores que se pueden informar.

</dd> </dl> </dd> <dt>

<span id="_VersionArgs_"></span><span id="_versionargs_"></span><span id="_VERSIONARGS_"></span><*VersionArgs*>
</dt> <dd>

El compilador acepta los siguientes argumentos de la versión.

<dl> <dt>

<span id="_v1"></span><span id="_V1"></span>**/v1**
</dt> <dd>

Especifica la conformidad estricta con la SMI de SNMPv1. El compilador informa de un error si detecta instrucciones que no son SNMPv1.

</dd> <dt>

<span id="_v2c"></span><span id="_V2C"></span>**/v2c**
</dt> <dd>

Especifica la conformidad estricta con la SMI de SNMPv2. El compilador informa de un error si detecta instrucciones que no son de SNMPv2.

</dd> </dl> </dd> <dt>

<span id="_CommandArgs_"></span><span id="_commandargs_"></span><span id="_COMMANDARGS_"></span><*CommandArgs*>
</dt> <dd>

El compilador acepta los siguientes argumentos de comando.

<dl> <dt>

<span id="_d"></span><span id="_D"></span>**/d.**
</dt> <dd>

Elimina el módulo especificado de SMIR.

</dd> <dt>

<span id="_p"></span><span id="_P"></span>**/p**
</dt> <dd>

Elimina todos los módulos de SMIR.

</dd> <dt>

<span id="_l"></span><span id="_L"></span>**l**
</dt> <dd>

Enumera todos los módulos de SMIR.

</dd> <dt>

<span id="_lc"></span><span id="_LC"></span>**/lc**
</dt> <dd>

Realiza una comprobación de sintaxis local en el módulo.

</dd> <dt>

<span id="_ec___CommandModifier__"></span><span id="_ec___commandmodifier__"></span><span id="_EC___COMMANDMODIFIER__"></span>**/EC** **\[<** _CommandModifier_*_>\]_*
</dt> <dd>

Realiza comprobaciones locales y externas en el módulo.

</dd> <dt>

<span id="_a__CommandModifier__"></span><span id="_a__commandmodifier__"></span><span id="_A__COMMANDMODIFIER__"></span>**\[ /a <** _CommandModifier_*_>\]_*
</dt> <dd>

Realiza comprobaciones locales y externas y carga el módulo en el SMIR.

</dd> <dt>

<span id="_sa__CommandModifier__"></span><span id="_sa__commandmodifier__"></span><span id="_SA__COMMANDMODIFIER__"></span>**\[ /SA <** _CommandModifier_*_>\]_*
</dt> <dd>

Igual que **/a**, pero funciona en modo silencioso.

</dd> <dt>

<span id="_g__CommandModifier__"></span><span id="_g__commandmodifier__"></span><span id="_G__COMMANDMODIFIER__"></span>**\[ /g <** _CommandModifier_*_>\]_*
</dt> <dd>

Genera un archivo SMIR. mof que se puede cargar posteriormente en WMI mediante el compilador MOF. Lo utiliza el proveedor de clase SNMP para proporcionar clases de forma dinámica a uno o varios espacios de nombres. Utilice esta opción si no sabe qué MIB son compatibles con los dispositivos SNMP que se están administrando. El proveedor de clase SNMP comprueba el dispositivo en tiempo de ejecución para la presencia de esta MIB y proporciona las clases dinámicamente al espacio de nombres.

</dd> <dt>

<span id="_gc__CommandModifier__"></span><span id="_gc__commandmodifier__"></span><span id="_GC__COMMANDMODIFIER__"></span>**\[ /GC <** _CommandModifier_*_>\]_*
</dt> <dd>

Genera un archivo. mof estático que se puede cargar más adelante en WMI como clases estáticas para un espacio de nombres determinado. Utilice esta opción cuando sepa qué MIB son compatibles con los dispositivos SNMP que se están administrando. Puede definir el archivo. mof que se generará dirigiendo la salida del comando a un archivo especificado. No se usa con **/ext/o**.

</dd> </dl> </dd> <dt>

<span id="_CommandModifiers_"></span><span id="_commandmodifiers_"></span><span id="_COMMANDMODIFIERS_"></span><*CommandModifiers*>
</dt> <dd>

El compilador acepta los siguientes modificadores de comando.

<dl> <dt>

<span id="_i_directory_"></span><span id="_I_DIRECTORY_"></span>**/i<** _directorio_*_>_*
</dt> <dd>

Especifica el directorio en el que se buscarán los módulos MIB dependientes. Use con **/a**, **/EC**, **/g**, **/GC** y **/SA**. La opción **/i** puede aparecer varias veces en el comando. los directorios se buscan en el orden especificado en el comando.

</dd> <dt>

<span id="_ch"></span><span id="_CH"></span>**/CH**
</dt> <dd>

Genera información de contexto, como la fecha, la hora, el host o el usuario, en el encabezado del archivo MOF. Use con **/g** y **/GC**.

</dd> <dt>

<span id="_t"></span><span id="_T"></span>**/t**
</dt> <dd>

Genera clases [SnmpNotification](snmpnotification.md) . Use con **/a**, **/g** y **/SA**.

</dd> <dt>

<span id="_ext"></span><span id="_EXT"></span>**/ext**
</dt> <dd>

Genera clases [SnmpExtendedNotification](snmpextendednotification.md) . Use con **/a**, **/g** y **/SA**.

</dd> <dt>

<span id="_t_o"></span><span id="_T_O"></span>**/t/o**
</dt> <dd>

Genera solo clases [SnmpNotification](snmpnotification.md) . Use con **/a**, **/g** y **/SA**.

</dd> <dt>

<span id="_ext_o"></span><span id="_EXT_O"></span>**/ext/o**
</dt> <dd>

Genera solo clases [SnmpExtendedNotification](snmpextendednotification.md) . Use con **/a**, **/g** y **/SA**.

</dd> <dt>

<span id="_s"></span><span id="_S"></span>**modificado**
</dt> <dd>

No asigna el texto de la cláusula Description. Use con **/a**, **/g**, **/GC** y **/SA**. Utilice esta opción si desea minimizar los requisitos de almacenamiento.

</dd> <dt>

<span id="_auto"></span><span id="_AUTO"></span>**/auto**
</dt> <dd>

Vuelve a generar la tabla de búsqueda de MIB antes de completar el <conmutador de> *CommandArg* . Use con **/a**, **/EC**, **/g** y **/GC**.

</dd> </dl> </dd> <dt>

<span id="_RegistryArgs_"></span><span id="_registryargs_"></span><span id="_REGISTRYARGS_"></span><*RegistryArgs*>
</dt> <dd>

El compilador acepta los siguientes argumentos del registro.

<dl> <dt>

<span id="_pa"></span><span id="_PA"></span>**/pa**
</dt> <dd>

Agrega el directorio especificado al registro. El valor predeterminado es el directorio actual.

</dd> <dt>

<span id="_pd"></span><span id="_PD"></span>**/PD**
</dt> <dd>

Elimina el directorio especificado del registro. El valor predeterminado es el directorio actual.

</dd> <dt>

<span id="_pl"></span><span id="_PL"></span>**/pl**
</dt> <dd>

Enumera los directorios de búsqueda MIB en el registro.

</dd> <dt>

<span id="_r"></span><span id="_R"></span>**/r**
</dt> <dd>

Vuelve a generar la tabla de búsqueda MIB completa.

</dd> </dl> </dd> <dt>

<span id="_ModuleInfoArgs_"></span><span id="_moduleinfoargs_"></span><span id="_MODULEINFOARGS_"></span><*ModuleInfoArgs*>
</dt> <dd>

El compilador acepta los siguientes argumentos de información del módulo.

<dl> <dt>

<span id="_n"></span><span id="_N"></span>**/n**
</dt> <dd>

Devuelve el nombre ASN. 1 del módulo especificado.

</dd> <dt>

<span id="_ni"></span><span id="_NI"></span>**/ni**
</dt> <dd>

Devuelve los nombres ASN. 1 de todos los módulos de importación a los que hace referencia el módulo de entrada.

</dd> </dl> </dd> <dt>

<span id="_HelpArgs_"></span><span id="_helpargs_"></span><span id="_HELPARGS_"></span><*HelpArgs*>
</dt> <dd>

El compilador acepta los siguientes argumentos de la ayuda.

<dl> <dt>

<span id="_h"></span><span id="_H"></span>**/h**
</dt> <dd>

Muestra ayuda sobre la sintaxis del compilador SNMP.

</dd> <dt>

<span id="__"></span>**/?**
</dt> <dd>

Muestra ayuda sobre la sintaxis del compilador SNMP.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Observaciones

Los módulos de información SNMP se escriben en un subconjunto de la notación de sintaxis abstracta uno (ASN. 1) el compilador realiza las siguientes funciones:

-   Carga los datos del módulo de información SNMP.
-   Realiza operaciones de comprobación en el módulo de información. Por ejemplo, comprueba la sintaxis local y comprueba las referencias externas con respecto a la información de los módulos subsidiarios.
-   Quita todos los datos previamente cargados del SMIR, o bien los datos cargados desde un módulo de información.
-   Devuelve el nombre de módulo ASN. 1 de un archivo especificado o devuelve los nombres de módulo ASN. 1 de todos los módulos importados de un archivo especificado.
-   Devuelve los nombres de módulo ASN.1 de todos los módulos de información SNMP cargados actualmente en el SMIR.
-   Realiza la resolución automática de los módulos importados en lugar de solicitar a los usuarios que especifiquen manualmente los módulos necesarios.
-   Realiza una operación de carga silenciosa que no genera ningún resultado, pero se puede usar para cargar datos en el SMIR durante una operación de instalación.
-   Genera los datos del módulo de información SNMP en el SMIR.
-   Opcionalmente, crea un archivo MOF estático o SMIR que contiene la salida del módulo de información.

    Si es necesario, puede cargar el archivo. mof estático en un espacio de nombres WMI. Un archivo SMIR. mof contiene el nombre del espacio de nombres SNMP en el que deben residir las clases.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se define el archivo pra. mof para que sea la salida del archivo pra. MIB.

``` syntax
smi2smir /m 3 /v1 /gc /pra.mib > pra.mof
```

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

 




