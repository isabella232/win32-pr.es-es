---
description: La utilidad de línea de comandos WMI (WMIC) proporciona una interfaz de línea de comandos para WMI.
ms.assetid: a0f5c1e2-9a4d-4c2b-b324-58ec01e67b6e
ms.tgt_platform: multiple
title: wmic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0248ea4ac6a584816da20e8feb8d278d7feab0a018739fa4328c3023179d4b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117921005"
---
# <a name="wmic"></a>wmic

La utilidad de línea de comandos WMI (WMIC) proporciona una interfaz de línea de comandos para Windows Management Instrumentation (WMI). WMIC es compatible con los shells y comandos de utilidad existentes. A continuación se muestra un tema de referencia general para WMIC. Para obtener más información e instrucciones sobre cómo usar WMIC, incluida información adicional sobre alias, verbos, modificadores y comandos, vea Using [Windows Management Instrumentation Command-line](/previous-versions/windows/it-pro/windows-server-2003/cc779482(v=ws.10)) and [WMIC - Take Command-line Control over WMI](/previous-versions/windows/it-pro/windows-2000-server/bb742610(v=technet.10)).

## <a name="alias"></a>Alias

Un alias es un nombre descriptivo de una clase, propiedad o método que facilita el uso y la lectura de WMI. Puede determinar qué alias están disponibles para WMIC a través de **/?** . También puede determinar los alias de una clase específica mediante **<className> /?** . Para obtener más información, vea [Alias de WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc736307(v=ws.10)).

## <a name="switch"></a>Switch

Un modificador es una opción de WMIC que se puede establecer global u opcionalmente. Para obtener una lista de los modificadores disponibles, vea [WMIC Switches](/previous-versions/windows/it-pro/windows-server-2003/cc787035(v=ws.10)).

## <a name="verbs"></a>Verbos

Para usar verbos en WMIC, escriba el nombre del alias seguido del verbo . Si un alias no admite un verbo, recibirá el mensaje "provider is not capable of the attempted operation". Para obtener más información, vea [Verbos de WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc784966(v=ws.10)).

La mayoría de los alias admiten los verbos siguientes.

<dl> <dt>

<span id="ASSOC"></span><span id="assoc"></span>Assoc
</dt> <dd>

Devuelve el resultado de la consulta donde<objeto wmi>es la ruta de acceso de los objetos devueltos por los comandos `Associators of (<wmi_object>)` **PATH** **o CLASS.** *\_* Los resultados son instancias asociadas al objeto . Cuando se usa ASSOC con un alias, se devuelven las clases con la clase subyacente al alias. De forma predeterminada, la salida se devuelve en formato HTML.

El verbo ASSOC tiene los modificadores siguientes.



| Switch                         | Descripción                                                                                                       |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------|
| /RESULTCLASS:<classname> | Los puntos de conexión devueltos asociados al objeto de origen deben pertenecer a o derivarse de la clase especificada.      |
| /RESULTROLE:<rolename>   | Los puntos de conexión devueltos deben desempeñar un rol específico en las asociaciones con el objeto de origen.                              |
| /ASSOCCLASS:<assocclass> | Los puntos de conexión devueltos deben estar asociados al origen a través de la clase especificada o de una de sus clases derivadas. |



 

Ejemplo: **ASSOC del sistema operativo**

</dd> <dt>

<span id="CALL"></span><span id="call"></span>Llamar
</dt> <dd>

Ejecuta un método .

Ejemplo: **SERVICE WHERE CAPTION='TELNET' CALL STARTSERVICE**

> [!Note]  
> Para determinar los métodos disponibles para una clase determinada, use **/?**. Por ejemplo, **SERVICE WHERE CAPTION='TELNET' CALL /?** enumera las funciones disponibles para la clase de servicio.

 

</dd> <dt>

<span id="CREATE"></span><span id="create"></span>Crear
</dt> <dd>

Crea una nueva instancia de y establece los valores de propiedad. CREATE no se puede usar para crear una nueva clase.

Ejemplo: **ENVIRONMENT CREATE NAME="TEMP"; VARIABLEVALUE="NEW"**

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>Eliminar
</dt> <dd>

Elimina la instancia actual o el conjunto de instancias. DELETE se puede usar para eliminar una clase.

Ejemplo: **PROCESS WHERE NAME="CALC.EXE" DELETE**

</dd> <dt>

<span id="GET"></span><span id="get"></span>Obtener
</dt> <dd>

Recuperar valores de propiedad específicos.

GET tiene los modificadores siguientes.



| Switch                               | Descripción                                                                                                                                |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| /VALUE                               | La salida tiene formato con cada valor enumerado en una línea independiente y con el nombre de la propiedad.                                           |
| /ALL                                 | La salida tiene formato de tabla.                                                                                                            |
| /TRANSLATE:<translation table> | Traduzca la salida mediante la tabla de traducción denominada por el comando . Las tablas de traducción BasicXml y NoComma se incluyen con WMIC. |
| /EVERY:<interval>              | Repita el comando cada <interval> segundos.                                                                                         |
| /FORMAT:<format specifier>     | Especifica una palabra clave o un nombre de archivo XSL para dar formato a los datos.                                                                                  |



 

Ejemplo: **PROCESS GET NAME**

</dd> <dt>

<span id="LIST"></span><span id="list"></span>Lista
</dt> <dd>

Muestra los datos. LIST es el verbo predeterminado.

LIST tiene los siguientes adverberos.



| Adverbio   | Descripción                                                  |
|----------|--------------------------------------------------------------|
| INSTRUCCIONES    | Conjunto principal de las propiedades.                                  |
| FULL     | Conjunto completo de propiedades. Este es el adverb predeterminado para LIST. |
| INSTANCE | Solo rutas de acceso de instancia.                                         |
| STATUS   | Estado de los objetos.                                       |
| SYSTEM   | Propiedades del sistema.                                           |



 

LIST tiene los modificadores siguientes.



| Switch                               | Descripción                                                                                                                                |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| /TRANSLATE:<translation table> | Traduzca la salida mediante la tabla de traducción denominada por el comando . Las tablas de traducción BasicXml y NoComma se incluyen con WMIC. |
| /EVERY:<interval>              | Repita el comando cada <interval> segundos.                                                                                         |
| /FORMAT:<format specifier>     | Especifica una palabra clave o un nombre de archivo XSL para dar formato a los datos.                                                                                  |



 

Ejemplo: **PROCESS LIST BRIEF**

</dd> <dt>

<span id="SET"></span><span id="set"></span>Establecer
</dt> <dd>

Asigna valores a las propiedades. Ejemplo: **ENVIRONMENT SET NAME="TEMP"**, **VARIABLEVALUE="NEW"**

</dd> </dl>

## <a name="switches"></a>Modificadores

Los modificadores globales se usan para establecer valores predeterminados para el entorno WMIC. Para ver el valor actual de las condiciones establecidas por estos modificadores, escriba el **comando CONTEXT.**

<dl> <dt>

<span id="_NAMESPACE"></span><span id="_namespace"></span>/NAMESPACE
</dt> <dd>

Espacio de nombres que el alias usa normalmente. El valor predeterminado es root \\ cimv2.

Ejemplo: **/NAMESPACE: \\ \\ root**

</dd> <dt>

<span id="_ROLE"></span><span id="_role"></span>/ROLE
</dt> <dd>

El espacio de nombres WMIC normalmente busca alias y otra información de WMIC.

Ejemplo: **/ROLE: \\ \\ root**

</dd> <dt>

<span id="_NODE"></span><span id="_node"></span>/NODE
</dt> <dd>

Nombres de equipo, delimitados por comas. Todos los comandos se ejecutan sincrónicamente en todos los equipos enumerados en este valor. Los nombres de archivo deben tener el prefijo &. Los nombres de equipo dentro de un archivo deben estar delimitados por comas o en líneas independientes.

</dd> <dt>

<span id="_IMPLEVEL"></span><span id="_implevel"></span>/IMPLEVEL
</dt> <dd>

Nivel de suplantación.

Ejemplo: **/IMPLEVEL:Anonymous**

</dd> <dt>

<span id="_AUTHLEVEL"></span><span id="_authlevel"></span>/AUTHLEVEL
</dt> <dd>

Nivel de autenticación.

Ejemplo: **/AUTHLEVEL:Pkt**

</dd> <dt>

<span id="_LOCALE"></span><span id="_locale"></span>/LOCALE
</dt> <dd>

Configuración regional.

Ejemplo: **/LOCALE:MS \_ 411**

</dd> <dt>

<span id="_PRIVILEGES"></span><span id="_privileges"></span>/PRIVILEGES
</dt> <dd>

Habilite o deshabilite todos los privilegios.

Ejemplo: **/PRIVILEGES:ENABLE** o **/PRIVILEGES:DISABLE**

</dd> <dt>

<span id="_TRACE"></span><span id="_trace"></span>/TRACE
</dt> <dd>

Muestra el éxito o el error de todas las funciones usadas para ejecutar comandos WMIC.

Ejemplo: **/TRACE:ON** o **/TRACE:OFF**

</dd> <dt>

<span id="_RECORD"></span><span id="_record"></span>/RECORD
</dt> <dd>

Registra todos los resultados en un archivo XML. La salida también se muestra en el símbolo del sistema.

Ejemplo: **/RECORD:** _MyOutput.xml_

</dd> <dt>

<span id="_INTERACTIVE"></span><span id="_interactive"></span>/INTERACTIVE
</dt> <dd>

Normalmente, se confirman los comandos delete.

Ejemplo: **/INTERACTIVE:ON** o **/INTERACTIVE:OFF**

</dd> <dt>

<span id="_FAILFAST_on_off_TimeoutInMilliseconds"></span><span id="_failfast_on_off_timeoutinmilliseconds"></span><span id="_FAILFAST_ON_OFF_TIMEOUTINMILLISECONDS"></span>/FAILFAST **on** \| **off** \| *TimeoutInMilliseconds*
</dt> <dd>

Si on se hace ping a los equipos /NODE antes de enviarles comandos WMIC. Si un equipo no responde, los comandos WMIC no se le envían.

Ejemplo: "/FAILFAST:ON" o "/FAILFAST:OFF"

**WMIC /FAILFAST:1000**

</dd> <dt>

<span id="_USER"></span><span id="_user"></span>/USER
</dt> <dd>

Nombre de usuario utilizado por WMIC al acceder a los equipos /NODE o a los equipos especificados en los alias. Se le pedirá la contraseña. No se puede usar un nombre de usuario con el equipo local.

Ejemplo: **/USER:**_JSMITH_

</dd> <dt>

<span id="_PASSWORD"></span><span id="_password"></span>/PASSWORD
</dt> <dd>

Contraseña usada por WMIC al acceder a los equipos /NODE. La contraseña está visible en la línea de comandos.

Ejemplo: **/PASSWORD:**_password_

</dd> <dt>

<span id="_OUTPUT"></span><span id="_output"></span>/OUTPUT
</dt> <dd>

Especifica un modo para todos los redireccionamientos de salida. La salida no aparece en la línea de comandos y el destino se borra antes de que comience la salida. Los valores válidos son STDOUT, CLIPBOARD o un nombre de archivo.

Ejemplo: **/OUTPUT:CLIPBOARD**

</dd> <dt>

<span id="_APPEND"></span><span id="_append"></span>/APPEND
</dt> <dd>

Especifica un modo para todos los redireccionamientos de salida. La salida no aparece en la línea de comandos y el destino no se borra antes de que comience la salida y la salida se anexa al final del contenido actual del destino. Los valores válidos son STDOUT, CLIPBOARD o un nombre de archivo.

Ejemplo: **/APPEND:CLIPBOARD**

</dd> <dt>

<span id="_AGGREGATE"></span><span id="_aggregate"></span>/AGGREGATE
</dt> <dd>

Se usa con **los modificadores LIST** **y GET /EVERY.** Si AGGREGATE es ON, LIST y GET muestran sus resultados cuando todos los equipos de /NODE han respondido o se ha producido un tiempo de espera. Si AGGREGATE es OFF, LIST y GET muestran sus resultados en cuanto se reciben.

Ejemplo: **/AGGREGATE:OFF** o **/AGGREGATE:ON**

</dd> </dl>

## <a name="commands"></a>Comandos

Los siguientes comandos WMIC están disponibles en todo momento. Para obtener más información, vea [Comandos de WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc779647(v=ws.10)).

<dl> <dt>

<span id="CLASS"></span><span id="class"></span>Clase
</dt> <dd>

Escape del modo de alias predeterminado de WMIC para acceder directamente a las clases del esquema WMI. Para obtener más información sobre las clases WMI disponibles, vea [Clases WMI](wmi-classes.md).

Ejemplo: **WMIC /OUTPUT:c: \\ClassOutput.htm CLASS Win32 \_ SoundDevice**

</dd> <dt>

<span id="PATH"></span><span id="path"></span>Camino
</dt> <dd>

Escape del modo de alias predeterminado de WMIC para acceder directamente a las instancias del esquema WMI.

Ejemplo: **WMIC /OUTPUT:c: \\PathOutput.txt PATH Win32 \_ SoundDevice GET /VALUE**

</dd> <dt>

<span id="CONTEXT"></span><span id="context"></span>Contexto
</dt> <dd>

Muestra los valores actuales de todos los modificadores globales.

Ejemplo: **CONTEXTO WMIC**

</dd> <dt>

<span id="QUIT"></span><span id="quit"></span>Dejar
</dt> <dd>

Salga de WMIC.

Ejemplo: **WMIC QUIT**

</dd> <dt>

<span id="EXIT"></span><span id="exit"></span>Salida
</dt> <dd>

Salga de WMIC.

Ejemplo: **WMIC EXIT**

</dd> </dl>

## <a name="examples"></a>Ejemplos

El script para establecer [IP/Subnet/Gateway/DNS](https://Gallery.TechNet.Microsoft.Com/Batch-per-settare-487c1b3f) mediante el ejemplo wmic en la Galería de TechNet describe cómo modificar y actualizar la configuración de IP, subred, puerta de enlace y DNS.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



 

