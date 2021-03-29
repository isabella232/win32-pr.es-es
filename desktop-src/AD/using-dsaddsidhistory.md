---
title: Usar DsAddSidHistory
description: En este tema se describe cómo usar la función DsAddSidHistory.
ms.assetid: cbf4983c-551d-4771-870e-a192ed898eb7
ms.tgt_platform: multiple
keywords:
- Usar DsAddSidHistory Active Directory
- Active Directory Active Directory, usar, uso de DsAddSidHistory
- DsAddSidHistory Active Directory, usar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d45792dbd8c7a2bfa2dd047111a3ed165a2011e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773045"
---
# <a name="using-dsaddsidhistory"></a>Usar DsAddSidHistory

La función [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) obtiene el identificador de seguridad (SID) de la cuenta principal de una entidad de seguridad de un dominio (el dominio de origen) y lo agrega al atributo **SIDHistory** de una entidad de seguridad en otro dominio (destino) de un bosque diferente. Cuando el dominio de origen está en modo nativo de Windows 2000, esta función también recupera los valores de **SIDHistory** de la entidad de seguridad de origen y los agrega al **SIDHistory** de la entidad de destino.

La adición de SID al **SIDHistory** de una entidad de seguridad es una operación que tiene en cuenta la seguridad que concede de manera eficaz al principal de destino acceso a todos los recursos a los que puede tener acceso la entidad de seguridad de origen, siempre que existan confianzas desde los dominios de recursos aplicables al dominio de destino.

En un dominio de Windows 2000 en modo nativo, un inicio de sesión de usuario crea un token de acceso que contiene el SID de la cuenta principal del usuario y los SID de grupo, así como el **SIDHistory** del usuario y el **SIDHistory** de los grupos de los que el usuario es miembro. Tener estos SID anteriores (valores **SIDHistory** ) en el token del usuario concede al usuario acceso a los recursos protegidos por las listas de control de acceso (ACL) que contienen los SID anteriores.

Esta operación facilita determinados escenarios de implementación de Windows 2000. En concreto, admite un escenario en el que se crean cuentas en un nuevo bosque de Windows 2000 para usuarios y grupos que ya existen en un entorno de producción de Windows NT 4,0. Al colocar el SID de cuenta de Windows NT 4,0 en la cuenta de Windows 2000 **SIDHistory**, se conserva el acceso a los recursos de red para el usuario que inicia sesión en su nueva cuenta de Windows 2000.

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) también admite la migración de servidores de recursos de controladores de dominio de copia de seguridad (BDC) de windows NT 4,0 (o controladores de dominio y servidores miembro en un dominio de Windows 2000 en modo nativo) a un dominio de Windows 2000 como servidores miembro. Esta migración requiere la creación, en el dominio de destino de Windows 2000, de los grupos locales de dominio que contengan, en su **SIDHistory**, los SID primarios de los grupos locales definidos en el BDC (o los grupos locales de dominio a los que se hace referencia en las ACL de los servidores de Windows 2000) del dominio de origen. Al crear un grupo local de destino que contiene el **SIDHistory** y todos los miembros del grupo local de origen, el acceso a los recursos de servidor migrados, protegidos por las ACL que hacen referencia al grupo local de origen, se mantiene para todos los miembros.

> [!Note]  
> El uso de [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) requiere un conocimiento de sus implicaciones administrativas y de seguridad más amplias en estos y otros escenarios. Para obtener más información, vea las notas del producto "planear la migración desde Windows NT a Microsoft Windows 2000", que se proporciona como Dommig.doc en las herramientas de soporte de Windows 2000. Esta documentación también puede encontrarse en el CD del producto en \\ herramientas de soporte técnico \\ .

 

## <a name="authorization-requirements"></a>Requisitos de autorización

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) requiere privilegios de administrador en los dominios de origen y de destino. En concreto, el autor de la llamada de esta API debe ser miembro del grupo administradores de dominio en el dominio de destino. Se realiza una comprobación de la pertenencia codificada de forma rígida. Además, el autor de la llamada o la cuenta proporcionada en el parámetro *SrcDomainCreds* , si no **es null**, debe ser miembro del grupo administradores o administradores de dominio del dominio de origen.

## <a name="domain-and-trust-requirements"></a>Requisitos de dominio y confianza

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) requiere que el dominio de destino esté en modo nativo de Windows 2000 o posterior, porque solo este tipo de dominio admite el atributo **SIDHistory** . El dominio de origen puede ser Windows NT 4,0 o Windows 2000, modo mixto o nativo. Los dominios de origen y de destino no deben estar en el mismo bosque. Los dominios de Windows NT 4,0 son por definición y no están en un bosque. Esta restricción entre bosques garantiza que los SID duplicados, ya sean valores SID o **SIDHistory** principales, no se creen en el mismo bosque.

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) requiere una confianza externa desde el dominio de origen al dominio de destino en los casos que se indican en la tabla siguiente.



| Caso                                                                             | Descripción                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| El dominio de origen es Windows 2000.<br/>                                    | El atributo **SIDHistory** de origen, disponible solo en los dominios de origen de Windows 2000, solo puede leerse mediante LDAP, lo que requiere que esta confianza sea para la protección de la integridad.<br/>                                                                                             |
| El dominio de origen es Windows NT 4,0 y *SrcDomainCreds* es **null**.<br/> | La suplantación, necesaria para admitir las operaciones de dominio de origen con las credenciales del autor de la llamada, depende de esta confianza. La suplantación también requiere que el controlador de dominio de destino tenga habilitada la opción de confianza para delegación de forma predeterminada en los controladores de dominio.<br/> |



 

Sin embargo, no se requiere ninguna relación de confianza entre los dominios de origen y de destino si el dominio de origen es Windows NT 4,0 y *SrcDomainCreds* no es **null**.

## <a name="source-domain-controller-requirements"></a>Requisitos del controlador de dominio de origen

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) requiere que el controlador de dominio, seleccionado como destino para las operaciones en el dominio de origen, sea el PDC en los dominios de windows NT 4,0 o el emulador de PDC en los dominios de Windows 2000. La auditoría de dominios de origen se genera mediante operaciones de escritura, por lo que el PDC es necesario en los dominios de origen de Windows NT 4,0 y la restricción solo de PDC garantiza que las auditorías de **DsAddSidHistory** se generan en un único equipo. Esto reduce la necesidad de revisar los registros de auditoría de todos los controladores de archivos para supervisar el uso de esta operación.

> [!Note]  
> En los dominios de origen de Windows NT 4,0, el PDC (destino de las operaciones en el dominio de origen) debe ejecutar Service Pack 4 (SP4) y versiones posteriores para garantizar un soporte de auditoría adecuado.

 

El siguiente valor del registro debe crearse como un \_ valor de REG DWORD y establecerse en 1 en el controlador de dominio de origen para los DC de origen de Windows NT 4,0 y windows 2000.

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
            Lsa
               TcpipClientSupport
```

Al establecer este valor, se habilitan las llamadas RPC a través del transporte TCP. Esto es necesario porque, de forma predeterminada, las interfaces SAMRPC solo son remotas en las canalizaciones con nombre. El uso de canalizaciones con nombre da como resultado un sistema de administración de credenciales adecuado para los usuarios que inician sesión de forma interactiva mediante llamadas en red, pero no es flexible para un proceso del sistema que realiza llamadas de red con credenciales proporcionadas por el usuario. RPC sobre TCP es más adecuado para ese propósito. El establecimiento de este valor no reduce la seguridad del sistema. Si se crea o cambia este valor, el controlador de dominio de origen debe reiniciarse para que esta configuración surta efecto.

Se debe crear un nuevo grupo local, " <SrcDomainName> $ $ $", en el dominio de origen con fines de auditoría.

## <a name="auditing"></a>Auditoría

Las operaciones de [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) se auditan para asegurarse de que los administradores de dominio de origen y de destino pueden detectar cuándo se ha ejecutado esta función. La auditoría es obligatoria en los dominios de origen y de destino. **DsAddSidHistory** comprueba que el modo auditoría está activado en cada dominio y que la auditoría de administración de cuentas de eventos correctos y erróneos está activada. En el dominio de destino, se genera un evento de auditoría "agregar historial de Sid" único para cada operación de **DsAddSidHistory** correcta o errónea.

Los eventos de auditoría "agregar historial de Sid" únicos no están disponibles en los sistemas Windows NT 4,0. Para generar eventos de auditoría que reflejen inequívocamente el uso de [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) en el dominio de origen, realiza operaciones en un grupo especial cuyo nombre es el identificador único en el registro de auditoría. Se <SrcDomainName> debe crear en el controlador de dominio de origen un grupo local, "$ $ $", cuyo nombre se componga del nombre NetBIOS del dominio de origen con tres signos de dólar ($) (código ASCII = 0x24 y Unicode = U + 0024). Cada usuario de origen y grupo global que es un destino de esta operación se agrega a y, a continuación, se quita de la pertenencia de este grupo. Esto genera eventos de auditoría agregar miembro y eliminar miembro en el dominio de origen, que se pueden supervisar buscando eventos que hagan referencia al nombre del grupo.

> [!Note]  
> Las operaciones de [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) en grupos locales en un dominio de origen de modo mixto de windows NT 4,0 o Windows 2000 no se pueden auditar porque los grupos locales no se pueden convertir en miembros de otro grupo local y, por tanto, no se pueden agregar al <SrcDomainName> grupo local especial "$ $ $". Esta falta de auditoría no presenta un problema de seguridad en el dominio de origen, ya que esta operación no afecta al acceso a los recursos del dominio de origen. La adición del SID de un grupo local de origen a un grupo local de destino no concede acceso a los recursos de origen, protegidos por ese grupo local, a los usuarios adicionales. Al agregar miembros al grupo local de destino no se les concede acceso a los recursos de origen. A los miembros agregados solo se les concede acceso a los servidores del dominio de destino migrados desde el dominio de origen, que pueden tener recursos protegidos por el SID del grupo local de origen.

 

## <a name="data-transmission-security"></a>Seguridad de transmisión de datos

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) exige las siguientes medidas de seguridad:

-   Se llama desde una estación de trabajo de Windows 2000, las credenciales del autor de la llamada se usan para autenticar y proteger la llamada RPC en el controlador de dominio de destino. Si *SrcDomainCreds* no es **null**, la estación de trabajo y el controlador de dominio de destino deben admitir el cifrado de 128 bits para proteger las credenciales. Si el cifrado de 128 bits no está disponible y se proporcionan *SrcDomainCreds* , se debe realizar la llamada en el controlador de dominio de destino.
-   El controlador de dominio de destino se comunica con el controlador de dominio de origen mediante *SrcDomainCreds* o las credenciales del autor de la llamada para autenticar y proteger mutuamente la lectura del SID de la cuenta de origen (mediante una búsqueda de Sam) y **SIDHistory** (mediante una lectura LDAP).

## <a name="threat-models"></a>Modelos de amenazas

En la tabla siguiente se enumeran las posibles amenazas asociadas a la llamada [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) y se abordan las medidas de seguridad correspondientes a la amenaza concreta.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Posible amenaza</th>
<th>Medida de seguridad</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Ataque del intermediario<br/> Un usuario no autorizado intercepta el <em>SID de búsqueda de la llamada de devolución del objeto de origen</em> , reemplazando el SID del objeto de origen por un SID arbitrario para la inserción en un objeto de destino SIDHistory.<br/></td>
<td>El <em>SID de búsqueda del objeto de origen</em> es una RPC autenticada mediante las credenciales de administrador del autor de la llamada, con protección de mensajes de integridad de paquetes. Esto garantiza que la llamada de devolución no se puede modificar sin detección. El controlador de dominio de destino crea un &quot; evento de auditoría agregar historial de SID único &quot; que refleja el SID agregado a la cuenta de destino <strong>SIDHistory</strong>.<br/></td>
</tr>
<tr class="even">
<td>Dominio de origen troyano<br/> Un usuario no autorizado crea un &quot; &quot; dominio de origen troyano en una red privada que tiene el mismo SID de dominio y algunos de los mismos SID de cuenta que el dominio de origen legítimo. A continuación, el usuario no autorizado intenta ejecutar <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a> en un dominio de destino para obtener el SID de una cuenta de origen. Esto se hace sin necesidad de las credenciales de administrador de dominio de origen real y sin tener que mantener una traza de auditoría en el dominio de origen real. El método del usuario no autorizado para crear el dominio de origen del caballo de Troya podría ser uno de los siguientes:
<ul>
<li>Obtenga una copia (copia de seguridad de BDC) del dominio de origen SAM.</li>
<li>Cree un nuevo dominio, modificando el SID del dominio en el disco para que coincida con el SID del dominio de origen legítimo y, a continuación, cree suficientes usuarios para crear una instancia de una cuenta con el SID deseado.</li>
<li>Cree una réplica de BDC. Esto requiere credenciales de administrador de dominio de origen. Después, el usuario no autorizado toma la réplica en una red privada para implementar el ataque.</li>
</ul>
<br/></td>
<td>Aunque hay muchas maneras de que un usuario no autorizado recupere o cree un SID de objeto de origen deseado, el usuario no autorizado no podrá usarlo para actualizar el <strong>SIDHistory</strong> de una cuenta sin ser miembro del grupo administradores de dominio de destino. Dado que la comprobación, en el controlador de dominio de destino, para la pertenencia del administrador de dominio está codificada de forma rígida, en el DC de destino no hay ningún método para realizar una modificación de disco para cambiar los datos de control de acceso que protegen esta función. Un intento de clonar una cuenta de origen troyano se audita en el dominio de destino. Este ataque se mitiga al reservar la pertenencia al grupo de administradores de dominio solo para usuarios de plena confianza.<br/></td>
</tr>
<tr class="odd">
<td>Modificación en disco del historial de SID<br/> Un usuario no autorizado sofisticado, con credenciales de administrador de dominio y acceso físico a un controlador de dominio en el dominio de destino, podría modificar el valor <strong>SIDHistory</strong> de la cuenta en el disco.<br/></td>
<td>Este intento no se habilita mediante el uso de <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a>. Este ataque se mitiga al impedir el acceso físico a los controladores de dominio a todos los administradores excepto a los de plena confianza.<br/></td>
</tr>
<tr class="even">
<td>Código no autorizado usado para quitar protecciones<br/> Un usuario no autorizado o un administrador no autorizado con acceso físico al código del servicio de directorio podría crear código no autorizado que:
<ol>
<li>Quita la comprobación de la pertenencia al grupo administradores de dominio en el código.</li>
<li>Cambia las llamadas en el controlador de dominio de origen que señala el SID a un LookupSidFromName que no se audita.</li>
<li>Quita las llamadas de registro de auditoría.</li>
</ol>
<br/></td>
<td>Alguien con acceso físico al código DS y lo suficientemente conocido para crear código no autorizado tiene la capacidad de modificar arbitrariamente el atributo <strong>SIDHistory</strong> de una cuenta. La API de <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a> no aumenta este riesgo de seguridad.<br/></td>
</tr>
<tr class="odd">
<td>Recursos vulnerables a Sid robados<br/> Si un usuario no autorizado ha realizado correctamente el uso de uno de los métodos descritos aquí para modificar la cuenta <strong>SIDHistory</strong>, y si los dominios de recursos de interés confían en el dominio de cuenta de usuario no autorizado, el usuario no autorizado puede obtener acceso no autorizado a los recursos del SID robado, potencialmente sin tener una pista de auditoría en el dominio de cuenta del que se ha robado el SID<br/></td>
<td>Los administradores de dominio de recursos protegen sus recursos mediante la configuración de las relaciones de confianza que tienen sentido desde una perspectiva de seguridad. El uso de <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a> está restringido, en el dominio de destino de confianza, a los miembros del grupo administradores de dominio que ya tienen amplios permisos en el ámbito de sus responsabilidades.<br/></td>
</tr>
<tr class="even">
<td>Dominio de destino no autorizado<br/> Un usuario no autorizado crea un dominio de Windows 2000 con una cuenta cuyo <strong>SIDHistory</strong> contiene un SID que ha sido robado de un dominio de origen. El usuario no autorizado utiliza esta cuenta para el acceso no autorizado a los recursos.<br/></td>
<td>El usuario no autorizado requiere credenciales de administrador para el dominio de origen con el fin de usar <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a>y deja una pista de auditoría en el controlador de dominio de origen. El dominio de destino no autorizado obtiene acceso no autorizado solo en otros dominios que confían en el dominio no autorizado, que requiere privilegios de administrador en esos dominios de recursos.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="operational-constraints"></a>Restricciones operativas

En esta sección se describen las restricciones operativas del uso de la función [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) .

El SID de *SrcPrincipal* no debe existir ya en el bosque de destino, ya sea como SID de la cuenta principal o en el **SIDHistory** de una cuenta. La excepción es que [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) no genera un error al intentar agregar un SID a un **SIDHistory** que contiene un SID idéntico. Este comportamiento permite que **DsAddSidHistory** se ejecute varias veces con una entrada idéntica, lo que da como resultado un éxito y un estado final coherente, para facilitar el uso del desarrollador de herramientas.

> [!Note]  
> La latencia de replicación de catálogo global puede proporcionar una ventana durante la cual se pueden crear SID duplicados. Sin embargo, un administrador puede eliminar fácilmente los SID duplicados.

 

*SrcPrincipal* y *DstPrincipal* deben ser de uno de los tipos siguientes:

-   User (Usuario)
-   Grupo con seguridad habilitada, incluido:

    <dl> Grupo local  
    Grupo global  
    Grupo local de dominio (solo en modo nativo de Windows 2000)  
    Grupo universal (solo en modo nativo de Windows 2000)  
    </dl>

Los tipos de objeto de *SrcPrincipal* y *DstPrincipal* deben coincidir.

-   Si *SrcPrincipal* es un usuario, *DstPrincipal* debe ser un usuario.
-   Si *SrcPrincipal* es un grupo local de dominio o local, *DstPrincipal* debe ser un grupo local de dominio.
-   Si *SrcPrincipal* es un grupo global o universal, *DstPrincipal* debe ser un grupo global o universal.

*SrcPrincipal* y *DstPrincipal* no pueden ser de uno de los tipos siguientes: ([**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) produce un error en estos casos)

-   Equipo (estación de trabajo o controlador de dominio)
-   Confianza entre dominios
-   Cuenta temporal duplicada (característica prácticamente sin usar, una heredada de LANman)
-   Cuentas con SID conocidos. Los SID conocidos son idénticos en todos los dominios; por lo tanto, si se agregan a un **SIDHistory** , se infringiría el requisito de unicidad del SID de un bosque de Windows 2000. Entre las cuentas con SID conocidos se incluyen los siguientes grupos locales:

    <dl> Operadores de cuentas  
    Administradores  
    Operadores de copia de seguridad  
    Invitados  
    Operadores de impresión  
    Duplicadores  
    Operadores de servidores  
    Usuarios  
    </dl>

Si *SrcPrincipal* tiene un identificador relativo (RID) conocido y un prefijo específico del dominio, es decir, administradores de dominio, usuarios del dominio y equipos del dominio, *DstPrincipal* debe poseer el mismo RID conocido en orden para que [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) se realice correctamente. Entre las cuentas con RID bien conocido se incluyen los siguientes usuarios y grupos globales:

-   Administrador
-   Invitado
-   Administradores de dominio
-   Invitados de dominio
-   Usuarios de dominio

## <a name="setting-the-registry-value"></a>Establecer el valor del registro

En el procedimiento siguiente se muestra cómo establecer el valor TcpipClientSupport del registro.

**Para establecer el valor del registro TcpipClientSupport**

1.  Cree el siguiente valor del registro como un \_ valor de REG DWORD en el controlador de dominio de origen y establezca su valor en 1.

    **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ control \\ LSA \\ TcpipClientSupport**

2.  A continuación, reinicie el controlador de dominio de origen. Este valor del registro hace que SAM escuche en TCP/IP. [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) producirá un error si no se establece este valor en el controlador de dominio de origen.

## <a name="enabling-auditing-of-usergroup-management-events"></a>Habilitar la auditoría de eventos de administración de usuarios y grupos

El siguiente procedimiento muestra cómo habilitar la auditoría de eventos de administración de usuarios o grupos en un dominio de origen o destino de Windows 2000 o Windows Server 2003.

**Para habilitar la auditoría de eventos de administración de usuarios o grupos en un dominio de origen o destino de Windows 2000 o Windows Server 2003**

1.  En el complemento MMC usuarios y equipos de Active Directory, seleccione el contenedor controladores de dominio del dominio de destino.
2.  Haga clic con el botón secundario en **controladores de dominio** y elija **propiedades**.
3.  Haga clic en la pestaña **Directiva de grupo** .
4.  Seleccione la **directiva predeterminada de controladores de dominio** y haga clic en **Editar**.
5.  En **configuración del equipo Configuración de \\ Windows \\ configuración de seguridad \\ Directivas locales \\ Directiva de auditoría**, haga doble clic en **auditar la administración de cuentas**.
6.  En la ventana **Auditoría de administración de cuentas** , seleccione auditoría de **aciertos** y **errores** . Las actualizaciones de directivas surten efecto después de un reinicio o cuando se produce una actualización.
7.  Compruebe que la auditoría está habilitada mediante la visualización de la Directiva de auditoría efectiva en el complemento MMC de directiva de grupo.

El siguiente procedimiento muestra cómo habilitar la auditoría de eventos de administración de usuarios o grupos en un dominio de Windows NT 4,0.

**Para habilitar la auditoría de eventos de administración de usuarios o grupos en un dominio de Windows NT 4,0**

1.  En **Administrador de usuarios para dominios**, haga clic en el menú **directivas** y seleccione **Auditoría**.
2.  Seleccione **auditar estos eventos**.
3.  Para la **Administración de usuarios y grupos**, compruebe que la operación se ha **realizado correctamente**.

El siguiente procedimiento muestra cómo habilitar la auditoría de eventos de administración de usuarios o grupos en un dominio de origen de Windows NT 4,0, Windows 2000 o Windows Server 2003.

**Para habilitar la auditoría de eventos de administración de usuarios o grupos en un dominio de origen de Windows NT 4,0, Windows 2000 o Windows Server 2003**

1.  En **Administrador de usuarios para dominios**, haga clic en el menú **usuario** y seleccione **nuevo grupo local**.
2.  Escriba un nombre de grupo compuesto por el nombre NetBIOS del dominio de origen anexado con tres signos de dólar ($), por ejemplo, FABRIKAM $ $ $. El campo de descripción debe indicar que este grupo se utiliza para auditar el uso de [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) o las operaciones de clonación. Asegúrese de que no hay miembros en el grupo. Haga clic en **OK**.

Se produce un error en la operación [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) si la auditoría de origen y de destino no está habilitada como se describe aquí.

## <a name="set-up-trust-if-required"></a>Configuración de la confianza si es necesario

Si se cumple una de las siguientes condiciones, se debe establecer una relación de confianza desde el dominio de origen al dominio de destino (esto debe ocurrir en un bosque diferente):

-   El dominio de origen es Windows Server 2003.
-   El dominio de origen es Windows NT 4,0 y *SrcDomainCreds* es **null**.

 

 





