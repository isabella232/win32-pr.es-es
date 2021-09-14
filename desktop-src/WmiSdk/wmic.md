---
title: wmic
description: La utilidad de línea de comandos WMI (WMIC) proporciona una interfaz de línea de comandos para WMI.
ms.assetid: a0f5c1e2-9a4d-4c2b-b324-58ec01e67b6e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 09/10/2021
ms.openlocfilehash: 9fabf53f3f4479bbeb49f7391e4bb6d6608f723e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172526"
---
# <a name="wmic"></a>wmic

La utilidad de línea de comandos wmi (WMIC) proporciona una interfaz de línea de comandos para Windows Management Instrumentation (WMI). WMIC es compatible con los shells y comandos de utilidad existentes. A continuación se muestra un tema de referencia general para WMIC. Para obtener más información e instrucciones sobre cómo usar WMIC, incluida información adicional sobre alias, verbos, modificadores y comandos, vea Using [Windows Management Instrumentation command-line](/previous-versions/windows/it-pro/windows-server-2003/cc779482(v=ws.10)) (Usar la línea de comandos del instrumental de administración de Windows) y WMIC take command-line control over WMI (Uso de la línea de comandos de instrumental de administración de Windows) y WMIC take command-line control over WMI (Uso de la línea de comandos de instrumental de administración de Windows) y WMIC take command-line control over WMI (Uso de la línea de comandos de instrumental de administración de Windows) y [WMIC take &mdash; command-line control over WMI](/previous-versions/windows/it-pro/windows-2000-server/bb742610(v=technet.10))(Uso de la línea de comandos de

## <a name="alias"></a>Alias

Un alias es un nombre descriptivo de una clase, propiedad o método que facilita el uso y la lectura de WMI. Puede determinar qué alias están disponibles para WMIC a través de **/?** . También puede determinar los alias de una clase específica mediante **&lt; className &gt; /?** . Para obtener más información, vea [Alias de WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc736307(v=ws.10)).

## <a name="switch"></a>Switch

Un modificador es una opción de WMIC que se puede establecer global u opcionalmente. Para obtener una lista de los modificadores disponibles, vea [WMIC switches](/previous-versions/windows/it-pro/windows-server-2003/cc787035(v=ws.10)).

## <a name="verbs"></a>Verbos

Para usar verbos en WMIC, escriba el nombre del alias seguido del verbo . Si un alias no admite un verbo, recibirá el mensaje "provider is not capable of the attempted operation". Para obtener más información, vea [Verbos de WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc784966(v=ws.10)).

La mayoría de los alias admiten los verbos siguientes.

### <a name="assoc"></a>ASSOC

Devuelve el resultado de la consulta donde<objeto wmi>es la ruta de acceso de los objetos devueltos por los comandos `Associators of (<wmi_object>)` **PATH** **o CLASS.** *\_* Los resultados son instancias asociadas al objeto . Cuando se usa ASSOC con un alias, se devuelven las clases con la clase subyacente al alias. De forma predeterminada, la salida se devuelve en formato HTML.

El verbo ASSOC tiene los modificadores siguientes.

| Switch                         | Descripción                                                                                                       |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------|
| /RESULTCLASS: &lt; classname&gt; | Los puntos de conexión devueltos asociados al objeto de origen deben pertenecer a o derivarse de la clase especificada.      |
| /RESULTROLE: &lt; rolename&gt;   | Los puntos de conexión devueltos deben desempeñar un rol específico en las asociaciones con el objeto de origen.                              |
| /ASSOCCLASS: &lt; assocclass&gt; | Los puntos de conexión devueltos deben estar asociados al origen a través de la clase especificada o de una de sus clases derivadas. |

Ejemplo: **ASSOC del sistema operativo**

### <a name="call"></a>CALL

Ejecuta un método .

Ejemplo: **SERVICE WHERE CAPTION='TELNET' CALL STARTSERVICE**

> [!NOTE]  
> Para determinar los métodos disponibles para una clase determinada, use **/?**. Por ejemplo, **SERVICE WHERE CAPTION='TELNET' CALL /?** enumera las funciones disponibles para la clase de servicio.

### <a name="create"></a>CREATE

Crea una nueva instancia de y establece los valores de propiedad. CREATE no se puede usar para crear una nueva clase.

Ejemplo: **ENVIRONMENT CREATE NAME="TEMP"; VARIABLEVALUE="NEW"**

### <a name="delete"></a>DELETE

Elimina la instancia actual o el conjunto de instancias. DELETE se puede usar para eliminar una clase.

Ejemplo: **PROCESS WHERE NAME="CALC.EXE" DELETE**

### <a name="get"></a>GET

Recuperar valores de propiedad específicos.

GET tiene los modificadores siguientes.

| Switch                               | Descripción                                                                                                                                |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| /VALUE                               | La salida tiene formato con cada valor enumerado en una línea independiente y con el nombre de la propiedad.                                           |
| /ALL                                 | La salida tiene formato de tabla.                                                                                                            |
| /TRANSLATE: &lt; tabla de traducción&gt; | Traduzca la salida mediante la tabla de traducción denominada por el comando . Las tablas de traducción BasicXml y NoComma se incluyen con WMIC. |
| /EVERY: &lt; interval&gt;              | Repita el comando cada &lt; intervalo de &gt; segundos.                                                                                         |
| /FORMAT: &lt; especificador de formato&gt;     | Especifica una palabra clave o un nombre de archivo XSL para dar formato a los datos.                                                                                  |

Ejemplo: **PROCESS GET NAME**

### <a name="list"></a>LISTA

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
| /TRANSLATE: &lt; tabla de traducción&gt; | Traduzca la salida mediante la tabla de traducción denominada por el comando . Las tablas de traducción BasicXml y NoComma se incluyen con WMIC. |
| /EVERY: &lt; interval&gt;              | Repita el comando cada &lt; intervalo de &gt; segundos.                                                                                         |
| /FORMAT: &lt; especificador de formato&gt;     | Especifica una palabra clave o un nombre de archivo XSL para dar formato a los datos.                                                                                  |

Ejemplo: **PROCESS LIST BRIEF**

### <a name="set"></a>SET

Asigna valores a las propiedades. Ejemplo: **ENVIRONMENT SET NAME="TEMP"**, **VARIABLEVALUE="NEW"**

## <a name="switches"></a>Conmutadores

Los conmutadores globales se usan para establecer valores predeterminados para el entorno WMIC. Para ver el valor actual de las condiciones establecidas por estos modificadores, escriba el **comando CONTEXT.**

### <a name="namespace"></a>/NAMESPACE

Espacio de nombres que el alias usa normalmente. El valor predeterminado es root \\ cimv2.

Ejemplo: **/NAMESPACE: \\ \\ root**

### <a name="role"></a>/ROLE

WMIC de espacio de nombres normalmente busca alias y otra información de WMIC.

Ejemplo: **/ROLE: \\ \\ root**

### <a name="node"></a>/NODE

Nombres de equipo, delimitados por comas. Todos los comandos se ejecutan sincrónicamente en todos los equipos enumerados en este valor. Los nombres de archivo deben tener el prefijo &. Los nombres de equipo dentro de un archivo deben estar delimitados por comas o en líneas independientes.

### <a name="implevel"></a>/IMPLEVEL

Nivel de suplantación.

Ejemplo: **/IMPLEVEL:Anonymous**

### <a name="authlevel"></a>/AUTHLEVEL

Nivel de autenticación.

Ejemplo: **/AUTHLEVEL:Pkt**

### <a name="locale"></a>/LOCALE

Configuración regional.

Ejemplo: **/LOCALE:MS \_ 411**

### <a name="privileges"></a>/PRIVILEGES

Habilite o deshabilite todos los privilegios.

Ejemplo: **/PRIVILEGES:ENABLE** o **/PRIVILEGES:DISABLE**

### <a name="trace"></a>/TRACE

Muestra el éxito o el error de todas las funciones usadas para ejecutar comandos WMIC.

Ejemplo: **/TRACE:ON** o **/TRACE:OFF**

### <a name="record"></a>/RECORD

Registra todos los resultados en un archivo XML. La salida también se muestra en el símbolo del sistema.

Ejemplo: **/RECORD:** _MyOutput.xml_

### <a name="interactive"></a>/INTERACTIVE

Normalmente, se confirman los comandos delete.

Ejemplo: **/INTERACTIVE:ON** o **/INTERACTIVE:OFF**

### <a name="failfast-onofftimeoutinmilliseconds"></a>/FAILFAST **on** \| **off** \| *TimeoutInMilliseconds*

Si es ON, se hace ping a los equipos /NODE antes de enviarles comandos WMIC. Si un equipo no responde, los comandos de WMIC no se le envían.

Ejemplo: "/FAILFAST:ON" o "/FAILFAST:OFF"

**WMIC /FAILFAST:1000**

### <a name="user"></a>/USER

Nombre de usuario utilizado por WMIC al acceder a los equipos o equipos /NODE especificados en los alias. Se le pedirá la contraseña. No se puede usar un nombre de usuario con el equipo local.

Ejemplo: **/USER:**_JSMITH_

### <a name="password"></a>/PASSWORD

Contraseña usada por WMIC al acceder a los equipos /NODE. La contraseña está visible en la línea de comandos.

Ejemplo: **/PASSWORD:**_password_

### <a name="output"></a>/OUTPUT

Especifica un modo para todos los redireccionamientos de salida. La salida no aparece en la línea de comandos y el destino se borra antes de que comience la salida. Los valores válidos son STDOUT, CLIPBOARD o un nombre de archivo.

Ejemplo: **/OUTPUT:CLIPBOARD**

### <a name="append"></a>/APPEND

Especifica un modo para todos los redireccionamientos de salida. La salida no aparece en la línea de comandos y el destino no se borra antes de que comience la salida y la salida se anexe al final del contenido actual del destino. Los valores válidos son STDOUT, CLIPBOARD o un nombre de archivo.

Ejemplo: **/APPEND:CLIPBOARD**

### <a name="aggregate"></a>/AGGREGATE

Se usa con **los modificadores LIST** **y GET /EVERY.** Si AGGREGATE es ON, LIST y GET muestran sus resultados cuando todos los equipos de /NODE han respondido o se ha pasado el tiempo de espera. Si AGGREGATE es OFF, LIST y GET muestran sus resultados en cuanto se reciben.

Ejemplo: **/AGGREGATE:OFF** o **/AGGREGATE:ON**

## <a name="commands"></a>Comandos:

Los siguientes comandos WMIC están disponibles en todo momento. Para obtener más información, [vea Comandos de WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc779647(v=ws.10)).

### <a name="class"></a>CLASS

Escape del modo de alias predeterminado de WMIC para acceder directamente a las clases del esquema WMI. Para obtener más información sobre las clases WMI disponibles, vea [Clases WMI](wmi-classes.md).

Ejemplo: **WMIC /OUTPUT:c: \\ClassOutput.htm CLASS Win32 \_ SoundDevice**

### <a name="path"></a>PATH

Escape del modo de alias predeterminado de WMIC para acceder directamente a las instancias del esquema WMI.

Ejemplo: **WMIC /OUTPUT:c: \\PathOutput.txt PATH Win32 \_ SoundDevice GET /VALUE**

### <a name="context"></a>CONTEXTO

Muestra los valores actuales de todos los modificadores globales.

Ejemplo: **WMIC CONTEXT**

### <a name="quit"></a>QUIT

Salga de WMIC.

Ejemplo: **WMIC QUIT**

### <a name="exit"></a>EXIT

Salga de WMIC.

Ejemplo: **WMIC EXIT**

## <a name="requirements"></a>Requisitos

| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
