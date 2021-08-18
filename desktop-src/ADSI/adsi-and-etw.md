---
title: Seguimiento de eventos en ADSI
description: Windows Server 2008 y Windows Vista presentan el seguimiento de eventos en Active Directory Service Interfaces (ADSI).
ms.assetid: 743aeeba-5b48-47c7-aaf5-0e9b48e206db
ms.tgt_platform: multiple
keywords:
- ADSI de seguimiento de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a59b2db3775c8c578ad361667a2d89c36240caf4b3bbb4bcd5cdd2798011514b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023983"
---
# <a name="event-tracing-in-adsi"></a>Seguimiento de eventos en ADSI

Windows Server 2008 y Windows Vista presentan el seguimiento de [eventos](/windows/desktop/ETW/event-tracing-portal) [en Active Directory Service Interfaces](active-directory-service-interfaces-adsi.md) (ADSI). Algunas áreas del proveedor LDAP ADSI tienen una implementación subyacente que es compleja o que implica una secuencia de pasos que dificulta el diagnóstico de problemas. Para ayudar a los desarrolladores de aplicaciones a solucionar problemas, el seguimiento de eventos se ha agregado a las áreas siguientes:

## <a name="schema-parsing-and-downloading"></a>Análisis y descarga de esquemas

La interfaz IADs de ADSI requiere que el esquema LDAP se almacene en caché en el cliente para que los atributos se puedan serializar correctamente (como se describe en el modelo de esquema [ADSI](adsi-schema-model.md)). Para ello, ADSI carga el esquema para cada proceso (y para cada servidor LDAP o dominio) en la memoria desde un archivo de esquema (.sch) que se guarda en el disco local o descargándose desde el servidor LDAP. Los distintos procesos de la misma máquina cliente usan el esquema almacenado en caché en disco si está disponible y es aplicable.

Si el esquema no se puede obtener del disco o del servidor, ADSI usa un esquema predeterminado codificado de forma rígida. Cuando esto sucede, los atributos que no forman parte de este esquema predeterminado no se pueden serializar y ADSI devuelve un error al recuperar estos atributos. Una serie de factores podrían provocar que esto suceda, incluidos problemas al analizar el esquema y privilegios insuficientes para descargar el esquema. A menudo es difícil determinar por qué se usa un determinado esquema predeterminado. El uso del seguimiento de eventos en esta área le ayudará a diagnosticar el problema y corregirlo más rápidamente.

## <a name="changing-and-setting-the-password"></a>Cambiar y establecer la contraseña

[**ChangePassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-changepassword) y [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) emplean más de un mecanismo para realizar la operación solicitada en función de la configuración disponible (como se describe en Establecer y cambiar contraseñas de usuario con el [proveedor LDAP](setting-user-passwords-for-ldap-providers.md)). Cuando se produce un error en **ChangePassword** y **SetPassword,** puede ser difícil determinar exactamente por qué, y el seguimiento de eventos le ayudará a solucionar problemas con estos métodos.

## <a name="adsi-bind-cache"></a>Caché de enlace ADSI

ADSI intenta reutilizar internamente las conexiones LDAP siempre que sea posible (consulte [Almacenamiento en caché de conexiones).](connection-caching.md) Al solucionar problemas, resulta útil hacer un seguimiento de si se abrió una nueva conexión para la comunicación con el servidor o si se usó una conexión existente. También puede ser útil realizar un seguimiento del ciclo de vida de la caché de conexiones (a veces denominada caché de enlace) y su creación o cierre, y si se produjo una referencia de conexión. En el caso de [un](/windows/desktop/AD/serverless-binding-and-rootdse)enlace sin servidor, ADSI llama al localizador de controlador de dominio para seleccionar un servidor para el dominio del contexto del usuario. A continuación, ADSI mantiene una caché de la asignación de dominio-servidor para las conexiones posteriores. Seguimiento de eventos ayuda a realizar un seguimiento de la selección del controlador de dominio y, por tanto, resulta útil para solucionar problemas relacionados con la conexión.

## <a name="enabling-tracing-and-starting-a-tracing-session"></a>Habilitar el seguimiento e iniciar una sesión de seguimiento

Para activar el seguimiento de ADSI, cree la siguiente clave del Registro:

**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **adsi** \\ **Tracing** \\ **_ProcessName_**

*ProcessName* es el nombre completo del proceso del que desea hacer un seguimiento, incluida su extensión (por ejemplo, "Svchost.exe"). Además, puede colocar un valor opcional de tipo **DWORD** denominado PID en esta clave. Se recomienda encarecidamente establecer este valor y, por tanto, realizar un seguimiento solo de un proceso determinado. De lo contrario, se realizará el seguimiento de todas las instancias de la aplicación especificadas por *ProcessName.*

A continuación, ejecute el siguiente comando:

**tracelog.exe -start** *sessionname* **-guid \# provider** _\_ guid_ **-f** *filename* **-flag** *traceFlags* **-level** *traceLevel*

*sessionname* es simplemente un identificador arbitrario que se usa para etiquetar la sesión de seguimiento (tendrá que hacer referencia a este nombre de sesión más adelante cuando detenga la sesión de seguimiento). El GUID del proveedor de seguimiento adsi es "7288c9f8-d63c-4932-a345-89d6b060174d". *filename* especifica el archivo de registro en el que se escribirán los eventos. *traceFlags* debe ser uno de los siguientes valores:



|         Marca                        |         Value              |
|---------------------------------|-----------------------|
| **ESQUEMA DE \_ DEPURACIÓN**<br/>    | 0x00000001<br/> |
| **DEPURAR \_ CHANGEPWD**<br/> | 0x00000002<br/> |
| **DEBUG \_ SETPWD**<br/>    | 0x00000004<br/> |
| **DEBUG \_ BINDCACHE**<br/> | 0x00000008<br/> |



 

Estas marcas determinan los métodos [ADSI](active-directory-service-interfaces-adsi.md) de los que se realizará el seguimiento, según la tabla siguiente:



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
<li>CADsUser::ChangePassword</li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><strong>DEBUG_SETPWD</strong><br/></td>
<td><ul>
<li>CADsUser::SetPassword</li>
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



 

Puede combinar marcas combinando los bits adecuados en el *argumento traceFlags.* Por ejemplo, para especificar las marcas **DEBUG \_ SCHEMA** y **DEBUG \_ BINDCACHE,** se usaría el valor *traceFlags* 0x00000009.

Por último, *la marca traceLevel* debe ser uno de los siguientes valores:



|      Marca                                    |       Value                |
|------------------------------------------|-----------------------|
| **ERROR \_ DE NIVEL DE \_ SEGUIMIENTO**<br/>       | 0x00000002<br/> |
| **INFORMACIÓN \_ DE NIVEL DE \_ SEGUIMIENTO**<br/> | 0x00000004<br/> |



 

**TRACE \_ LEVEL \_ INFORMATION hace** que el proceso de seguimiento registre todos los eventos, mientras que TRACE LEVEL **\_ \_ ERROR** hace que el proceso de seguimiento registre solo eventos de error.

Para finalizar el seguimiento, ejecute el siguiente comando:

**tracelog.exe -stop** *sessionname*

En el ejemplo anterior, *sessionname* es el mismo nombre que el que se proporcionó con el comando que inició la sección de seguimiento.

## <a name="remarks"></a>Comentarios

Es más eficaz hacer un seguimiento solo de procesos específicos especificando un PID determinado que hacer un seguimiento de todos los procesos de un equipo. Si necesita realizar un seguimiento de varias aplicaciones en el mismo equipo, puede haber un impacto en el rendimiento. hay una salida de depuración considerable en secciones orientadas al rendimiento del código. Además, los administradores deben tener cuidado de establecer correctamente los permisos de los archivos de registro al realizar el seguimiento de varios procesos. De lo contrario, cualquier usuario podría leer los registros de seguimiento y otros usuarios podrán realizar un seguimiento de los procesos que contienen información segura.

Por ejemplo, supone que el administrador configura el seguimiento de una aplicación "Test.exe" y no especifica un PID en el registro para realizar el seguimiento de varias instancias del proceso. Ahora, otro usuario desea hacer un seguimiento de la aplicación "Secure.exe". Si los archivos de registro de seguimiento no están correctamente restringidos, lo único que debe hacer el usuario es cambiar el nombre de "Secure.exe" a "Test.exe" y se realizará el seguimiento. En general, es mejor realizar un seguimiento solo de procesos específicos durante la solución de problemas y quitar la clave del Registro de seguimiento en cuanto se realiza la solución de problemas.

Puesto que la habilitación del seguimiento de eventos producirá archivos de registro adicionales, los administradores deben supervisar cuidadosamente los tamaños de los archivos de registro. la falta de espacio en disco en el equipo local puede provocar una denegación de servicio.

## <a name="example-scenarios"></a>Escenarios de ejemplo

Escenario 1: el administrador ve un error inesperado en una aplicación que establece contraseñas para las cuentas de usuario, por lo que realizaría los pasos siguientes para corregir el problema mediante el seguimiento de eventos.

1.  Escribir un script que reproduzca el problema y crear la clave del Registro

    **HKEY \_ Sistema \_ DE MÁQUINA LOCAL** \\  \\ **CurrentControlSet** \\ **Services** \\ **adsi** \\ **Tracing** \\ **cscript.exe**

2.  Inicie una sesión de seguimiento, estableciendo *traceFlags* en 0x2 (**DEBUG \_ CHANGEPASSWD**) y *traceLevel* en 0x4 (**TRACE LEVEL \_ \_ INFORMATION**), mediante el siguiente comando:

    **tracelog.exe -start scripttrace -guid \# 7288c9f8-d63c-4932-a345-89d6b060174d -f . \\ adsi.etl -flag 0x2 -level 0x4**

3.  Ejecute cscript.exe con su script de prueba para reproducir el problema y, a continuación, finalice la sesión de seguimiento:

    **tracelog.exe -stop scripttrace**

4.  Eliminación de la clave del Registro

    **HKEY \_ Sistema \_ DE MÁQUINA LOCAL** \\  \\ **CurrentControlSet** \\ **Services** \\ **adsi** \\ **Tracing** \\ **cscript.exe**

5.  Ejecute la herramienta ETW Tracerpt.exe para analizar la información de seguimiento del registro:

    **tracelog.exe -start scripttrace -guid \# 7288c9f8-d63c-4932-a345-89d6b060174d -f . \\ adsi.etl -flag 0x2 -level 0x4**

Escenario 2: el administrador desea realizar un seguimiento de las operaciones de análisis y descarga de esquemas en una aplicación [ASP](https://msdn.microsoft.com/asp.net/default.aspx) denominada w3wp.exe que ya se está ejecutando. Para ello, el administrador realizaría los pasos siguientes:

1.  Creación de la clave del Registro

    **HKEY \_ Sistema \_ DE MÁQUINA LOCAL** \\  \\ **CurrentControlSet** \\ **Services** \\ **adsi** \\ **Tracing** \\ **w3wp.exe**

    y dentro de esa clave, cree un valor de tipo DWORD denominado PID y esta establezca en el identificador de proceso de la instancia de w3wp.exe que se ejecuta actualmente en el equipo local.

2.  A continuación, crean una sesión de seguimiento, estableciendo *traceFlags* en 0x1 (**DEBUG \_ SCHEMA**) y *traceLevel* en 0x4 (**TRACE LEVEL \_ \_ INFORMATION**):

    **tracelog.exe -start w3wptrace -guid \# 7288c9f8-d63c-4932-a345-89d6b060174d -f . \\ w3wp.etl -flag 0x1 -level 0x4**

3.  Reproduzca la operación que necesita solución de problemas.
4.  Finalice la sesión de seguimiento:

    **tracelog.exe -stop w3wptrace**

5.  Elimine la clave del Registro **HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **adsi** \\ **Tracing** \\ **w3wp.exe**.
6.  Ejecute la herramienta ETW tracerpt.exe para analizar la información de seguimiento del registro:

    **tracerpt.exe . \\ w3wp.etl -o -report**

 

