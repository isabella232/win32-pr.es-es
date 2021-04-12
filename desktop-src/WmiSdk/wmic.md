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
# <a name="wmic"></a>wmic

La utilidad de línea de comandos de WMI (WMIC) proporciona una interfaz de línea de comandos para Instrumental de administración de Windows (WMI). WMIC es compatible con shells y comandos de utilidad existentes. A continuación se encuentra un tema de referencia general de WMIC. Para obtener más información e instrucciones sobre cómo usar WMIC, incluida información adicional sobre alias, verbos, modificadores y comandos, vea [usar instrumental de administración de Windows línea de comandos](/previous-versions/windows/it-pro/windows-server-2003/cc779482(v=ws.10)) y [WMIC-Take control de línea de comandos sobre WMI](/previous-versions/windows/it-pro/windows-2000-server/bb742610(v=technet.10)).

## <a name="alias"></a>Alias

Un alias es un cambio descriptivo de una clase, propiedad o método que facilita el uso y la lectura de WMI. Puede determinar los alias que están disponibles para WMIC a través del **/?** . También puede determinar los alias para una clase específica mediante **<className> /?** . Para obtener más información, consulte [alias de WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc736307(v=ws.10)).

## <a name="switch"></a>Switch

Un modificador es una opción de WMIC que se puede establecer global u opcionalmente. Para obtener una lista de los modificadores disponibles, consulte [modificadores de WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc787035(v=ws.10)).

## <a name="verbs"></a>Verbos

Para usar verbos en WMIC, escriba el nombre del alias seguido del verbo. Si un alias no admite un verbo, recibirá el mensaje "el proveedor no es capaz de realizar la operación". Para obtener más información, vea [verbos de WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc784966(v=ws.10)).

La mayoría de los alias admiten los siguientes verbos.

<dl> <dt>

<span id="ASSOC"></span><span id="assoc"></span>ASSOC
</dt> <dd>

Devuelve el resultado de la `Associators of (<wmi_object>)` consulta donde *<\_ objeto WMI>* es la ruta de acceso de los objetos devueltos por los comandos **path** o **Class** . Los resultados son instancias asociadas al objeto. Cuando se usa ASSOC con un alias, se devuelven las clases con la clase que subyace al alias. De forma predeterminada, la salida se devuelve en formato HTML.

El verbo ASSOC tiene los siguientes modificadores.



| Switch                         | Descripción                                                                                                       |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------|
| /RESULTCLASS:<classname> | Los extremos devueltos asociados al objeto de origen deben pertenecer a o derivar de la clase especificada.      |
| /RESULTROLE:<rolename>   | Los extremos devueltos deben desempeñar un rol específico en asociaciones con el objeto de origen.                              |
| /ASSOCCLASS:<assocclass> | Los extremos devueltos deben estar asociados al origen a través de la clase especificada o de una de sus clases derivadas. |



 

Ejemplo: **so Assoc**

</dd> <dt>

<span id="CALL"></span><span id="call"></span>LLAMA
</dt> <dd>

Ejecuta un método.

Ejemplo: **servicio en el que Caption = ' telnet ' llama a STARTSERVICE**

> [!Note]  
> Para determinar los métodos disponibles para una clase determinada, use **/?**. Por ejemplo, **servicio donde Caption = ' telnet ' Call/?** muestra las funciones disponibles para la clase de servicio.

 

</dd> <dt>

<span id="CREATE"></span><span id="create"></span>A
</dt> <dd>

Crea una nueva instancia de y establece los valores de propiedad. CREATE no se puede usar para crear una nueva clase.

Ejemplo: **entorno Create name = "Temp"; VARIABLEVALUE = "nuevo"**

</dd> <dt>

<span id="DELETE"></span><span id="delete"></span>ELIMÍNELOS
</dt> <dd>

Elimina la instancia o el conjunto de instancias actual. DELETE se puede usar para eliminar una clase.

Ejemplo: **proceso donde name = "CALC.EXE" Delete**

</dd> <dt>

<span id="GET"></span><span id="get"></span>Obtener
</dt> <dd>

Recuperar valores de propiedad específicos.

GET tiene los siguientes modificadores.



| Switch                               | Descripción                                                                                                                                |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| /VALUE                               | La salida se formatea con cada valor que aparece en una línea independiente y con el nombre de la propiedad.                                           |
| /ALL                                 | La salida tiene el formato de tabla.                                                                                                            |
| Convierte<translation table> | Traduzca la salida mediante la tabla Translation denominada por el comando. Las tablas de traducción BasicXml y nomilla se incluyen con WMIC. |
| Siempre<interval>              | Repita el comando cada <interval> segundos.                                                                                         |
| Aplique<format specifier>     | Especifica una palabra clave o un nombre de archivo XSL para dar formato a los datos.                                                                                  |



 

Ejemplo: **Process Get Name**

</dd> <dt>

<span id="LIST"></span><span id="list"></span>LISTA
</dt> <dd>

Muestra los datos. LIST es el verbo predeterminado.

LIST tiene los siguientes adverbios.



| Adverbio   | Descripción                                                  |
|----------|--------------------------------------------------------------|
| INSTRUCCIONES    | Conjunto básico de las propiedades.                                  |
| FULL     | Conjunto completo de propiedades. Este es el adverbio predeterminado para la lista. |
| INSTANCE | Solo rutas de acceso de instancia.                                         |
| STATUS   | Estado de los objetos.                                       |
| SYSTEM   | Propiedades del sistema.                                           |



 

La lista tiene los siguientes modificadores.



| Switch                               | Descripción                                                                                                                                |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| Convierte<translation table> | Traduzca la salida mediante la tabla Translation denominada por el comando. Las tablas de traducción BasicXml y nomilla se incluyen con WMIC. |
| Siempre<interval>              | Repita el comando cada <interval> segundos.                                                                                         |
| Aplique<format specifier>     | Especifica una palabra clave o un nombre de archivo XSL para dar formato a los datos.                                                                                  |



 

Ejemplo: **breve lista de procesos**

</dd> <dt>

<span id="SET"></span><span id="set"></span>CONJUNTO
</dt> <dd>

Asigna valores a las propiedades. Ejemplo: **Environment Set Name = "Temp"**, **VARIABLEVALUE = "New"**

</dd> </dl>

## <a name="switches"></a>Conmutadores

Los modificadores globales se utilizan para establecer valores predeterminados para el entorno de WMIC. Para ver el valor actual de las condiciones establecidas por estos modificadores, escriba el comando de **contexto** .

<dl> <dt>

<span id="_NAMESPACE"></span><span id="_namespace"></span>/NAMESPACE
</dt> <dd>

Espacio de nombres que usa normalmente el alias. El valor predeterminado es la raíz \\ cimv2.

Ejemplo: **/namespace: \\ \\ raíz**

</dd> <dt>

<span id="_ROLE"></span><span id="_role"></span>/ROLE
</dt> <dd>

Espacio de nombres WMIC normalmente busca en alias y en otra información de WMIC.

Ejemplo: **/role: \\ \\ root**

</dd> <dt>

<span id="_NODE"></span><span id="_node"></span>/NODE
</dt> <dd>

Nombres de equipo, delimitados por comas. Todos los comandos se ejecutan sincrónicamente en todos los equipos incluidos en este valor. Los nombres de archivo deben ir precedidos de &. Los nombres de equipo dentro de un archivo deben ser delimitados por comas o en líneas independientes.

</dd> <dt>

<span id="_IMPLEVEL"></span><span id="_implevel"></span>/IMPLEVEL
</dt> <dd>

Nivel de suplantación.

Ejemplo: **/IMPLEVEL: Anonymous**

</dd> <dt>

<span id="_AUTHLEVEL"></span><span id="_authlevel"></span>/AUTHLEVEL
</dt> <dd>

Nivel de autenticación.

Ejemplo: **/AUTHLEVEL: PKT**

</dd> <dt>

<span id="_LOCALE"></span><span id="_locale"></span>/LOCALE
</dt> <dd>

Configuración regional.

Ejemplo: **/locale: MS \_ 411**

</dd> <dt>

<span id="_PRIVILEGES"></span><span id="_privileges"></span>/PRIVILEGES
</dt> <dd>

Habilitar o deshabilitar todos los privilegios.

Ejemplo: **/privileges: enable** o **/privileges: disable**

</dd> <dt>

<span id="_TRACE"></span><span id="_trace"></span>/TRACE
</dt> <dd>

Muestra el éxito o el fracaso de todas las funciones utilizadas para ejecutar comandos de WMIC.

Ejemplo: **/Trace: on** o **/Trace: OFF**

</dd> <dt>

<span id="_RECORD"></span><span id="_record"></span>/RECORD
</dt> <dd>

Registra todos los resultados en un archivo XML. La salida también se muestra en el símbolo del sistema.

Ejemplo: **/Record:** _MyOutput.xml_

</dd> <dt>

<span id="_INTERACTIVE"></span><span id="_interactive"></span>/INTERACTIVE
</dt> <dd>

Normalmente, se confirman los comandos de eliminación.

Ejemplo: **/Interactive: on** o **/Interactive: OFF**

</dd> <dt>

<span id="_FAILFAST_on_off_TimeoutInMilliseconds"></span><span id="_failfast_on_off_timeoutinmilliseconds"></span><span id="_FAILFAST_ON_OFF_TIMEOUTINMILLISECONDS"></span>/FailFast **en** \| **OFF** \| *TimeoutInMilliseconds*
</dt> <dd>

Si se hace ping en los equipos con/NODE antes de enviarles comandos de WMIC. Si un equipo no responde, no se le envían los comandos de WMIC.

Ejemplo: "/FAILFAST: ON" o "/FAILFAST: OFF"

**WMIC/FAILFAST: 1000**

</dd> <dt>

<span id="_USER"></span><span id="_user"></span>/USER
</dt> <dd>

Nombre de usuario utilizado por WMIC al obtener acceso a los equipos o equipos especificados en los alias. Se le pedirá la contraseña. No se puede usar un nombre de usuario con el equipo local.

Ejemplo: **/User:**_JSMITH_

</dd> <dt>

<span id="_PASSWORD"></span><span id="_password"></span>/PASSWORD
</dt> <dd>

Contraseña usada por WMIC al obtener acceso a los equipos/NPDE. La contraseña es visible en la línea de comandos.

Ejemplo: **/password:**_contraseña_

</dd> <dt>

<span id="_OUTPUT"></span><span id="_output"></span>/OUTPUT
</dt> <dd>

Especifica un modo para la redirección de salida. La salida no aparece en la línea de comandos y se borra el destino antes de que empiece la salida. Los valores válidos son STDOUT, CLIPBOARD o un nombre de archivo.

Ejemplo: **/Output: Clipboard**

</dd> <dt>

<span id="_APPEND"></span><span id="_append"></span>/APPEND
</dt> <dd>

Especifica un modo para la redirección de salida. La salida no aparece en la línea de comandos y el destino no se borra antes de que se inicie la salida y se anexa la salida al final del contenido actual del destino. Los valores válidos son STDOUT, CLIPBOARD o un nombre de archivo.

Ejemplo: **/Append: Clipboard**

</dd> <dt>

<span id="_AGGREGATE"></span><span id="_aggregate"></span>/AGGREGATE
</dt> <dd>

Se usa con los modificadores **List** y **Get/Every** . Si Aggregate está activado, LIST y GET muestran los resultados cuando todos los equipos de la/NODE han respondido o han agotado el tiempo de espera. Si Aggregate está desactivado, LIST y GET muestran los resultados en cuanto se reciben.

Ejemplo: **/Aggregate: OFF** o **/Aggregate: on**

</dd> </dl>

## <a name="commands"></a>Comandos:

Los siguientes comandos de WMIC están disponibles en todo momento. Para obtener más información, vea [comandos de WMIC](/previous-versions/windows/it-pro/windows-server-2003/cc779647(v=ws.10)).

<dl> <dt>

<span id="CLASS"></span><span id="class"></span>LAS
</dt> <dd>

Salga del modo de alias predeterminado de WMIC para tener acceso directamente a las clases del esquema WMI. Para obtener más información sobre las clases WMI disponibles, vea [clases WMI](wmi-classes.md).

Ejemplo: **WMIC/Output: c: \\ClassOutput.htm clase Win32 \_ SoundDevice**

</dd> <dt>

<span id="PATH"></span><span id="path"></span>CAMINO
</dt> <dd>

Salga del modo de alias predeterminado de WMIC para tener acceso directamente a las instancias del esquema WMI.

Ejemplo: **WMIC/Output: c: \\PathOutput.txt path Win32 \_ SoundDevice Get/Value**

</dd> <dt>

<span id="CONTEXT"></span><span id="context"></span>CONTEXTO
</dt> <dd>

Mostrar los valores actuales de todos los conmutadores globales.

Ejemplo: **contexto de WMIC**

</dd> <dt>

<span id="QUIT"></span><span id="quit"></span>INTERRUMPI
</dt> <dd>

Salga de WMIC.

Ejemplo: **WMIC Quit**

</dd> <dt>

<span id="EXIT"></span><span id="exit"></span>ABANDONAR
</dt> <dd>

Salga de WMIC.

Ejemplo: **WMIC Exit**

</dd> </dl>

## <a name="examples"></a>Ejemplos

El [script para establecer la configuración de IP/subred/Puerta de enlace/DNS con WMIC](https://Gallery.TechNet.Microsoft.Com/Batch-per-settare-487c1b3f) en la galería de TechNet describe cómo modificar y actualizar la configuración de IP, subred, puerta de enlace y DNS.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |



 

