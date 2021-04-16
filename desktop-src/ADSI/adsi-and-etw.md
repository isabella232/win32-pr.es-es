---
title: Seguimiento de eventos en ADSI
description: Windows Server 2008 y Windows Vista introducen el seguimiento de eventos en Active Directory interfaces de servicio (ADSI).
ms.assetid: 743aeeba-5b48-47c7-aaf5-0e9b48e206db
ms.tgt_platform: multiple
keywords:
- seguimiento de eventos ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f43c0d840cd1f3f70d293a0a4f5c299fd129efe
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105656397"
---
# <a name="event-tracing-in-adsi"></a>Seguimiento de eventos en ADSI

Windows Server 2008 y Windows Vista introducen el [seguimiento de eventos](/windows/desktop/ETW/event-tracing-portal) en [Active Directory interfaces de servicio](active-directory-service-interfaces-adsi.md) (ADSI). Ciertas áreas del proveedor LDAP de ADSI tienen una implementación subyacente compleja o que implica una secuencia de pasos que dificulta el diagnóstico de problemas. Para ayudar a los desarrolladores de aplicaciones a solucionar problemas, se ha agregado seguimiento de eventos a las siguientes áreas:

## <a name="schema-parsing-and-downloading"></a>Análisis y descarga de esquemas

La interfaz IADs en ADSI requiere que el esquema LDAP se almacene en caché en el cliente para que se puedan calcular las referencias de los atributos correctamente (como se describe en el [modelo de esquema ADSI](adsi-schema-model.md)). Para ello, ADSI carga el esquema de cada proceso (y para cada servidor o dominio LDAP) en la memoria, ya sea desde un archivo de esquema (. SCH) guardado en el disco local o descargándolo desde el servidor LDAP. Los distintos procesos en el mismo equipo cliente usan el esquema almacenado en caché en disco si está disponible y es aplicable.

Si el esquema no se puede obtener del disco o del servidor, ADSI utiliza un esquema predeterminado codificado de forma rígida. Cuando esto ocurre, no se pueden calcular las referencias de los atributos que no forman parte de este esquema predeterminado y ADSI devuelve un error al recuperar estos atributos. Una serie de factores podría provocar que esto suceda, incluidos los problemas en el análisis del esquema, y privilegios insuficientes para descargar el esquema. A menudo resulta difícil determinar por qué se está usando cierto esquema predeterminado. El uso del seguimiento de eventos en esta área le ayudará a diagnosticar más rápidamente el problema y solucionarlo.

## <a name="changing-and-setting-the-password"></a>Cambiar y establecer la contraseña

[**ChangePassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-changepassword) y [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) emplean más de un mecanismo para realizar la operación solicitada en función de la configuración disponible (como se describe en [establecer y cambiar las contraseñas de usuario con el proveedor LDAP](setting-user-passwords-for-ldap-providers.md)). Cuando se produce un error en **ChangePassword** y **SetPassword** , puede ser difícil determinar exactamente por qué y el seguimiento de eventos ayuda a solucionar problemas con estos métodos.

## <a name="adsi-bind-cache"></a>Caché de enlace de ADSI

ADSI intenta internamente reutilizar las conexiones LDAP siempre que sea posible (consulte [almacenamiento en caché de conexiones](connection-caching.md)). Al solucionar problemas, es útil realizar un seguimiento de si se ha abierto una conexión nueva para la comunicación con el servidor o si se ha utilizado una conexión existente. También puede ser útil para realizar un seguimiento del ciclo de vida de la memoria caché de conexiones (a veces denominada caché de enlace) y su creación o cierre, y si tuvo lugar una referencia de conexión. En el caso de un [enlace sin servidor](/windows/desktop/AD/serverless-binding-and-rootdse), ADSI llama al Ubicador de DC para seleccionar un servidor para el dominio del contexto del usuario. ADSI mantiene una memoria caché de la asignación de servidor de dominio para las conexiones posteriores. El seguimiento de eventos ayuda a realizar un seguimiento de la selección del controlador de dominio y, por tanto, es útil para solucionar problemas relacionados con la conexión.

## <a name="enabling-tracing-and-starting-a-tracing-session"></a>Habilitar el seguimiento e iniciar una sesión de seguimiento

Para activar el seguimiento ADSI, cree la siguiente clave del registro:

**HKEY \_ \_** \\  \\  \\  \\  \\ **Seguimiento** \\  ADSI del sistema del equipo local de System CurrentControlSet

*ProcessName* es el nombre completo del proceso del que se desea realizar un seguimiento, incluida su extensión (por ejemplo, "Svchost.exe"). Además, puede colocar un valor opcional de tipo **DWORD** denominado PID en esta clave. Se recomienda establecer este valor y, por tanto, realizar un seguimiento solo de un proceso determinado. De lo contrario, se realizará un seguimiento de todas las instancias de la aplicación especificadas por *processName* .

Después, ejecute el siguiente comando:

**tracelog.exe-Start** *nombresesión*  * *-GUID \# * * * proveedor \_ GUID* **-f** *nombre* **-marca** *traceFlags* **-LEVEL** *TraceLevel*

*nombresesión* es simplemente un identificador arbitrario que se usa para etiquetar la sesión de seguimiento (deberá hacer referencia a este nombre de sesión más adelante cuando detenga la sesión de seguimiento). El GUID del proveedor de seguimiento de ADSI es "7288c9f8-d63c-4932-A345-89d6b060174d". *filename* especifica el archivo de registro en el que se escribirán los eventos. *traceFlags* debe ser uno de los siguientes valores:



|                                 |                       |
|---------------------------------|-----------------------|
| **esquema de depuración \_**<br/>    | 0x00000001<br/> |
| **depurar \_ CHANGEPWD**<br/> | 0x00000002<br/> |
| **depuración \_ SETPWD**<br/>    | 0x00000004<br/> |
| **depurar \_ BINDCACHE**<br/> | 0x00000008<br/> |



 

Estas marcas determinan a qué métodos [ADSI](active-directory-service-interfaces-adsi.md) se realizará un seguimiento, de acuerdo con la tabla siguiente:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>DEBUG_SCHEMA</strong><br/></td>
<td><ul>
<li>LdapGetSchema</li>
<li>GetSchemaInfoTime</li>
<li>LdapReadSchemaInfoFromServer</li>
<li>ProcessSchemaInfo</li>
<li>HelperReadLdapSchemaInfo</li>
<li>ProcessClassInfoArray</li>
<li>ReadSchemaInfoFromRegistry</li>
<li>StoreSchemaInfoFromRegistry</li>
<li>AttributeTypeDescription</li>
<li>ObjectClassDescription</li>
<li>DITContentRuleDescription</li>
<li>DirectoryString</li>
<li>DirectoryStrings</li>
<li>DITContentRuleDescription</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><strong>DEBUG_CHANGEPWD</strong><br/></td>
<td><ul>
<li>CADsUser:: ChangePassword</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><strong>DEBUG_SETPWD</strong><br/></td>
<td><ul>
<li>CADsUser:: SetPassword</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><strong>DEBUG_BINDCACHE</strong><br/></td>
<td><ul>
<li>GetServerBasedObject</li>
<li>GetServerLessBasedObject</li>
<li>GetGCDomainName</li>
<li>GetDefaultDomainName</li>
<li>GetUserDomainFlatName</li>
<li>BindCacheLookup</li>
<li>EquivalentPortNumbers</li>
<li>CanCredentialsBeReused</li>
<li>BindCacheAdd</li>
<li>BindCacheAddRef</li>
<li>AddReferralLink</li>
<li>CommonRemoveEntry</li>
<li>BindCacheDerefHelper</li>
<li>NotifyNewConnection</li>
<li>QueryForConnection</li>
<li>LdapOpenBindWithCredentials</li>
<li>LdapOpenBindWithDefaultCredentials</li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

Puede combinar marcas combinando los bits adecuados en el argumento *traceFlags* . Por ejemplo, para especificar el **\_ esquema de depuración** y **depurar las marcas \_ BINDCACHE** , el valor de *traceFlags* adecuado sería 0x00000009.

Por último, la marca *TraceLevel* debe ser uno de los valores siguientes:



|                                          |                       |
|------------------------------------------|-----------------------|
| **\_error de nivel de seguimiento \_**<br/>       | 0x00000002<br/> |
| **\_información del nivel de seguimiento \_**<br/> | 0x00000004<br/> |



 

**Seguimiento \_ de La \_ información de nivel** hace que el proceso de seguimiento grabe todos los eventos, mientras que el **error de \_ nivel \_ de seguimiento** hace que el proceso de seguimiento registre solo los eventos de error.

Para finalizar el seguimiento, ejecute el siguiente comando:

**tracelog.exe-STOP** *nombresesión*

En el ejemplo anterior, *nombresesión* es el mismo nombre que el que se proporcionó con el comando que inició la sección de seguimiento.

## <a name="remarks"></a>Observaciones

Es más eficaz realizar un seguimiento de los procesos específicos mediante la especificación de un determinado PID que para realizar el seguimiento de todos los procesos de un equipo. Si necesita realizar un seguimiento de varias aplicaciones en el mismo equipo, puede haber un impacto en el rendimiento. hay una salida de depuración considerable en las secciones orientadas al rendimiento del código. Además, los administradores deben tener cuidado para establecer correctamente los permisos de los archivos de registro al realizar un seguimiento de varios procesos. de lo contrario, cualquier usuario podría leer los registros de seguimiento y otros usuarios podrán realizar un seguimiento de los procesos que contienen información segura.

Por ejemplo, supongamos que el administrador configura el seguimiento para una aplicación "Test.exe" y no especifica un PID en el registro para realizar un seguimiento de varias instancias del proceso. Ahora otro usuario desea realizar un seguimiento de la aplicación "Secure.exe". Si los archivos de registro de seguimiento no están restringidos correctamente, lo único que debe hacer el usuario es cambiar el nombre de "Secure.exe" a "Test.exe" y se realizará un seguimiento. En general, es mejor realizar un seguimiento solo de procesos específicos durante la solución de problemas y quitar la clave del registro de seguimiento en cuanto se realiza la solución de problemas.

Dado que la habilitación del seguimiento de eventos generará archivos de registro adicionales, los administradores deben supervisar cuidadosamente los tamaños de los archivos de registro. la falta de espacio en disco en el equipo local puede producir una denegación de servicio.

## <a name="example-scenarios"></a>Escenarios de ejemplo

Escenario 1: el administrador ve un error inesperado en una aplicación que establece contraseñas para las cuentas de usuario, por lo que llevaría a cabo los pasos siguientes para solucionar el problema con el seguimiento de eventos.

1.  Escriba un script que reproduzca el problema y cree la clave del registro.

    **HKEY \_ Sistema \_ equipo local** \\  \\ **CurrentControlSet** \\ **Services** \\  \\ **seguimiento** ADSI \\ **cscript.exe**

2.  Inicie una sesión de seguimiento, estableciendo *traceFlags* en 0X2 (**Debug \_ CHANGEPASSWD**) y *TraceLevel* en 0x4 (**\_ \_ información del nivel de seguimiento**) con el siguiente comando:

    **tracelog.exe-Start scripttrace-GUID \# 7288c9f8-d63c-4932-A345-89d6b060174d-f. \\ ADSI. ETL: marca 0X2-nivel 0x4**

3.  Ejecute cscript.exe con su script de prueba para reproducir el problema y, a continuación, finalice la sesión de seguimiento:

    **tracelog.exe: detener scripttrace**

4.  Eliminar la clave del registro

    **HKEY \_ Sistema \_ equipo local** \\  \\ **CurrentControlSet** \\ **Services** \\  \\ **seguimiento** ADSI \\ **cscript.exe**

5.  Ejecute la herramienta ETW Tracerpt.exe para analizar la información de seguimiento del registro:

    **tracelog.exe-Start scripttrace-GUID \# 7288c9f8-d63c-4932-A345-89d6b060174d-f. \\ ADSI. ETL: marca 0X2-nivel 0x4**

Escenario 2: el administrador desea realizar un seguimiento de las operaciones de análisis y descarga de esquemas en una aplicación [asp](https://msdn.microsoft.com/asp.net/default.aspx) denominada w3wp.exe que ya se está ejecutando. Para ello, el administrador llevaría a cabo los siguientes pasos:

1.  Crear la clave del registro

    **HKEY \_ Sistema \_ equipo local** \\  \\ **CurrentControlSet** \\ **Services** \\  \\ **seguimiento** ADSI \\ **w3wp.exe**

    y dentro de esa clave, cree un valor de tipo DWORD que se denomine PID y establézcalo en el ID. de proceso de la instancia de w3wp.exe que se está ejecutando actualmente en el equipo local.

2.  A continuación, se crea una sesión de seguimiento, se establece el valor de *traceFlags* en 0x1 (**\_ esquema de depuración**) y *TraceLevel* en 0x4 (**información del \_ nivel \_ de seguimiento**):

    **tracelog.exe-Start w3wptrace-GUID \# 7288c9f8-d63c-4932-A345-89d6b060174d-f. \\ w3wp. ETL: marca 0x1-nivel 0x4**

3.  Reproduzca la operación que necesita solucionar problemas.
4.  Finalice la sesión de seguimiento:

    **tracelog.exe: detener w3wptrace**

5.  Elimine la clave del registro **HKEY \_ local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **ADSI** \\ **Tracing** \\ **w3wp.exe**.
6.  Ejecute la herramienta ETW tracerpt.exe para analizar la información de seguimiento del registro:

    **tracerpt.exe. \\ w3wp. ETL-o-Report**

 

