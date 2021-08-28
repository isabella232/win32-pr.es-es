---
title: Uso de DsAddSidHistory
description: En este tema se describe cómo usar la función DsAddSidHistory.
ms.assetid: cbf4983c-551d-4771-870e-a192ed898eb7
ms.tgt_platform: multiple
keywords:
- Uso de DsAddSidHistory Active Directory
- Active Directory Active Directory , mediante, Usar DsAddSidHistory
- DsAddSidHistory Active Directory , mediante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6e987a55f7fe39a8e4705f6aca9e44189e0f7a2
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881841"
---
# <a name="using-dsaddsidhistory"></a>Uso de DsAddSidHistory

La función [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) obtiene el identificador de seguridad de la cuenta principal (SID) de una entidad de seguridad de un dominio (el dominio de origen) y lo agrega al atributo **sIDHistory** de una entidad de seguridad de otro dominio (destino) en un bosque diferente. Cuando el dominio de origen está en modo nativo Windows 2000, esta función también recupera los valores **sIDHistory** de la entidad de seguridad de origen y los agrega al **sIDHistory** de la entidad de seguridad de destino.

Agregar SID a **sIDHistory** de una entidad de seguridad es una operación que tiene en cuenta la seguridad y que concede de forma eficaz a la entidad de seguridad de destino acceso a todos los recursos accesibles para la entidad de seguridad de origen, siempre que existan confianzas desde los dominios de recursos aplicables al dominio de destino.

En un modo nativo Windows dominio 2000, un inicio de sesión de usuario crea un token de acceso que contiene el SID de la cuenta principal de usuario y los SID de grupo, así como el **usuario sIDHistory** y **sIDHistory** de los grupos de los que el usuario es miembro. Tener estos SID anteriores (valores **sIDHistory)** en el token del usuario concede al usuario acceso a los recursos protegidos por listas de control de acceso (ACL) que contienen los antiguos SID.

Esta operación facilita ciertos Windows escenarios de implementación de 2000. En concreto, admite un escenario en el que se crean cuentas en un nuevo bosque de Windows 2000 para usuarios y grupos que ya existen en un entorno de producción de Windows NT 4.0. Al colocar el SID de la cuenta de Windows NT 4.0 en la cuenta de Windows 2000 **sIDHistory,** se conserva el acceso a los recursos de red para que el usuario acceda a su nueva cuenta de Windows 2000.

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) también admite la migración de servidores de recursos de controladores de dominio de copia de seguridad (BDC) de Windows NT 4.0 (o controladores de dominio y servidores miembros en un modo nativo Windows un dominio 2000) a un dominio de Windows 2000 como servidores miembro. Esta migración requiere la creación, en el dominio de destino Windows 2000, de grupos locales de dominio que contienen, en **su sIDHistory,** los SID principales de los grupos locales definidos en el BDC (o grupos locales de dominio a los que se hace referencia en las ACL en los servidores Windows 2000) en el dominio de origen. Al crear un grupo local de destino que contenga **sIDHistory** y todos los miembros del grupo local de origen, se mantiene el acceso a los recursos de servidor migrados, protegidos por ACL que hacen referencia al grupo local de origen, para todos los miembros.

> [!Note]  
> El uso [**de DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) requiere una comprensión de sus implicaciones administrativas y de seguridad más amplias en estos y otros escenarios. Para obtener más información, vea las white paper "Planning Migration from Windows NT to Microsoft Windows 2000" (Planeación de la migración de Windows NT a Microsoft Windows 2000), que se entrega como Dommig.doc en las herramientas de soporte técnico de Windows 2000. Esta documentación también se puede encontrar en el CD del producto en herramientas \\ de \\ soporte técnico.

 

## <a name="authorization-requirements"></a>Requisitos de autorización

[**DsAddSidHistory requiere**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) privilegios de administrador en los dominios de origen y destino. En concreto, el autor de la llamada de esta API debe ser miembro del grupo Administradores de dominio del dominio de destino. Se realiza una comprobación codificada de forma hard-code para esta pertenencia. Además, el autor de la llamada o la cuenta proporcionada en el parámetro *SrcDomainCreds,* si no es **NULL,** debe ser miembro del grupo Administradores o Administradores de dominio del dominio de origen.

## <a name="domain-and-trust-requirements"></a>Requisitos de dominio y confianza

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) requiere que el dominio de destino esté en modo nativo Windows 2000 o posterior, porque solo este tipo de dominio admite el atributo **sIDHistory.** El dominio de origen puede ser Windows NT 4.0 o Windows 2000, modo mixto o nativo. Los dominios de origen y destino no deben estar en el mismo bosque. Windows Los dominios NT 4.0 no están por definición en un bosque. Esta restricción entre bosques garantiza que los SID duplicados, tanto si aparecen como SID principales o valores **sIDHistory,** no se crean en el mismo bosque.

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) requiere una confianza externa del dominio de origen al dominio de destino en los casos enumerados en la tabla siguiente.



| Caso                                                                             | Descripción                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| El dominio de origen Windows 2000.<br/>                                    | El atributo **sIDHistory** de origen, disponible solo en Windows 2000 dominios de origen, puede ser de solo lectura mediante LDAP, lo que requiere esta confianza para la protección de la integridad.<br/>                                                                                             |
| El dominio de origen Windows NT 4.0 y *SrcDomainCreds* es **NULL.**<br/> | La suplantación, necesaria para admitir operaciones de dominio de origen mediante las credenciales del autor de la llamada, depende de esta confianza. La suplantación también requiere que el controlador de dominio de destino tenga habilitada la opción "Confianza para delegación" de forma predeterminada en los controladores de dominio.<br/> |



 

Sin embargo, no se requiere ninguna confianza entre los dominios de origen y de destino si el dominio de origen es Windows NT 4.0 y *SrcDomainCreds* no es **NULL.**

## <a name="source-domain-controller-requirements"></a>Requisitos del controlador de dominio de origen

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) requiere que el controlador de dominio, seleccionado como destino de las operaciones en el dominio de origen, sea el PDC en los dominios de Windows NT 4.0 o el pdc Emulator en Windows 2000 dominios. La auditoría de dominio de origen se genera mediante operaciones de escritura, por lo tanto, el PDC es necesario en dominios de origen de Windows NT 4.0 y la restricción de solo PDC garantiza que las auditorías **DsAddSidHistory** se generan en un solo equipo. Esto reduce la necesidad de revisar los registros de auditoría de todos los DCs para supervisar el uso de esta operación.

> [!Note]  
> En Windows dominios de origen NT 4.0, el PDC (destino de las operaciones en el dominio de origen) debe ejecutar Service Pack 4 (SP4) y versiones posteriores para garantizar la compatibilidad de auditoría adecuada.

 

El siguiente valor del Registro debe crearse como un valor REG DWORD y establecerse en 1 en el controlador de dominio de origen para los controladores de dominio de \_ Windows NT 4.0 y Windows 2000.

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
            Lsa
               TcpipClientSupport
```

Al establecer este valor, se habilitan las llamadas RPC a través del transporte TCP. Esto es necesario porque, de forma predeterminada, las interfaces SAMRPC solo se pueden remotar en canalizaciones con nombre. El uso de canalizaciones con nombre da como resultado un sistema de administración de credenciales adecuado para los usuarios que han iniciado sesión interactivamente que hacen llamadas en red, pero no es flexible para un proceso del sistema que realiza llamadas de red con credenciales proporcionadas por el usuario. RPC a través de TCP es más adecuado para ese propósito. Establecer este valor no disminuye la seguridad del sistema. Si se crea o cambia este valor, se debe reiniciar el controlador de dominio de origen para que esta configuración suba.

Se debe crear un nuevo grupo local, &lt; "SrcDomainName $$$", en el dominio de origen con fines &gt; de auditoría.

## <a name="auditing"></a>Auditoría

[**Las operaciones DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) se auditan para garantizar que los administradores de dominio de origen y de destino puedan detectar cuándo se ha ejecutado esta función. La auditoría es obligatoria en los dominios de origen y de destino. **DsAddSidHistory** comprueba que el modo de auditoría está en cada dominio y que la auditoría de administración de cuentas de eventos correctos o con errores está en funcionamiento. En el dominio de destino, se genera un evento de auditoría "Agregar historial de sid" único para cada operación **DsAddSidHistory** correcta o con errores.

Los eventos de auditoría "Agregar historial de sid" únicos no están disponibles Windows sistemas NT 4.0. Para generar eventos de auditoría que reflejen inequívocamente el uso de [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) en el dominio de origen, realiza operaciones en un grupo especial cuyo nombre es el identificador único en el registro de auditoría. Un grupo local, "SrcDomainName $$$", cuyo nombre se compone del nombre NetBIOS del dominio de origen anexado con tres signos de dólar &lt; ($) (código ASCII = 0x24 y Unicode = U+0024), debe crearse en el controlador de dominio de origen antes de llamar a &gt; **DsAddSidHistory.** Cada usuario de origen y grupo global que es el destino de esta operación se agrega a y, a continuación, se quita de la pertenencia de este grupo. Esto genera eventos de auditoría Agregar miembro y Eliminar miembro en el dominio de origen, que se pueden supervisar mediante la búsqueda de eventos que hacen referencia al nombre del grupo.

> [!Note]  
> Las operaciones [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) en grupos locales de un dominio de origen en modo mixto de Windows NT 4.0 o Windows 2000 no se pueden auditar porque los grupos locales no se pueden convertir en miembros de otro grupo local y, por tanto, no se pueden agregar al grupo &lt; local especial "SrcDomainName &gt; $$$". Esta falta de auditoría no presenta un problema de seguridad para el dominio de origen, ya que el acceso a los recursos del dominio de origen no se ve afectado por esta operación. Agregar el SID de un grupo local de origen a un grupo local de destino no concede acceso a los recursos de origen, protegidos por ese grupo local, a ningún usuario adicional. Agregar miembros al grupo local de destino no les concede acceso a los recursos de origen. A los miembros agregados solo se les concede acceso a los servidores del dominio de destino migrados desde el dominio de origen, que puede tener recursos protegidos por el SID del grupo local de origen.

 

## <a name="data-transmission-security"></a>Seguridad de transmisión de datos

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) aplica las siguientes medidas de seguridad:

-   Se llama desde Windows estación de trabajo 2000, las credenciales del autor de la llamada se usan para autenticar y proteger la privacidad de la llamada RPC al controlador de dominio de destino. Si *SrcDomainCreds* no es **NULL,** tanto la estación de trabajo como el controlador de dominio de destino deben admitir el cifrado de 128 bits para proteger la privacidad de las credenciales. Si el cifrado de 128 bits no está disponible y se proporciona *SrcDomainCreds,* la llamada debe realizarse en el controlador de dominio de destino.
-   El controlador de dominio de destino se comunica con el controlador de dominio de origen mediante *SrcDomainCreds* o las credenciales del autor de la llamada para autenticarse mutuamente y proteger la integridad y la lectura del SID de la cuenta de origen (mediante una búsqueda SAM) y **sIDHistory** (mediante una lectura LDAP).

## <a name="threat-models"></a>Modelos de amenazas

En la tabla siguiente se enumeran las posibles amenazas asociadas a la llamada [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) y se abordan las medidas de seguridad pertinentes a la amenaza determinada.




| Amenaza potencial | Medida de seguridad | 
|------------------|------------------|
| Man in the Middle Attack<br /> Un usuario no autorizado intercepta el <em>SID</em> de búsqueda de la llamada de devolución de objeto de origen, reemplazando el SID del objeto de origen por un SID arbitrario para la inserción en un siElemento de objeto de destino.<br /> | El <em>SID de búsqueda del objeto de origen</em> es una RPC autenticada, con las credenciales de administrador del autor de la llamada, con protección de mensajes de integridad de paquetes. Esto garantiza que la llamada de devolución no se puede modificar sin detección. El controlador de dominio de destino crea un evento de auditoría "Agregar historial de SID" único que refleja el SID agregado a la cuenta de destino <strong>sIDHistory</strong>.<br /> | 
| Dominio de origen de Troyano<br /> Un usuario no autorizado crea un dominio de origen "Troyano" en una red privada que tiene el mismo SID de dominio y algunos de los mismos SID de cuenta que el dominio de origen legítimo. A continuación, el usuario no autorizado intenta ejecutar <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a> en un dominio de destino para obtener el SID de una cuenta de origen. Esto se hace sin necesidad de las credenciales de administrador de dominio de origen real y sin dejar un registro de auditoría en el dominio de origen real. El método del usuario no autorizado para crear el dominio de origen del troyano podría ser uno de los siguientes:<ul><li>Obtenga una copia (copia de seguridad del BDC) del dominio de origen SAM.</li><li>Cree un nuevo dominio, altere el SID del dominio en el disco para que coincida con el SID del dominio de origen legítimo y, a continuación, cree suficientes usuarios para crear una instancia de una cuenta con el SID deseado.</li><li>Cree una réplica de BDC. Esto requiere credenciales de administrador del dominio de origen. A continuación, el usuario no autorizado lleva la réplica a una red privada para implementar el ataque.</li></ul><br /> | Aunque hay muchas maneras de que un usuario no autorizado recupere o cree un SID de objeto de origen deseado, el usuario no autorizado no puede usarlo para actualizar el <strong>valor de sIDHistory</strong> de una cuenta sin ser miembro del grupo administradores de dominio de destino. Dado que la comprobación, en el controlador de dominio de destino, para la pertenencia al administrador de dominio está codificada de forma automática, en el controlador de dominio de destino, no hay ningún método para realizar una modificación del disco para cambiar los datos de control de acceso que protegen esta función. Se audita un intento de clonar una cuenta de origen de troyano en el dominio de destino. Este ataque se mitiga al reservar la pertenencia al grupo Administradores de dominio solo para personas de confianza alta.<br /> | 
| Modificación en disco del historial de SID<br /> Un usuario no autorizado sofisticado, con credenciales de administrador de dominio y con acceso físico a un controlador de dominio en el dominio de destino, podría modificar un valor <strong>sIDHistory</strong> de la cuenta en el disco.<br /> | Este intento no está habilitado mediante <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a>. Este ataque se mitiga al impedir el acceso físico a los controladores de dominio a todos, excepto a los administradores de alta confianza.<br /> | 
| Código no fiable usado para quitar protecciones<br /> Un usuario no autorizado o un administrador no autorizado con acceso físico al código del servicio de directorio podría crear código no autorizado que:<ol><li>Quita la comprobación de pertenencia al grupo Administradores de dominio en el código.</li><li>Cambia las llamadas en el controlador de dominio de origen que señala el SID a un lookupSidFromName que no está auditado.</li><li>Quita las llamadas al registro de auditoría.</li></ol><br /> | Alguien con acceso físico al código DS y lo suficientemente conocedor como para crear código no autorizado tiene la capacidad de modificar arbitrariamente el atributo <strong>sIDHistory</strong> de una cuenta. La API <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a> no aumenta este riesgo de seguridad.<br /> | 
| Recursos vulnerables a SID robados<br /> Si un usuario no autorizado ha logrado usar uno de los métodos descritos aquí para modificar una <strong>cuenta sIDHistory</strong>y si los dominios de recursos de interés confían en el dominio de cuenta de usuario no autorizado, el usuario no autorizado puede obtener acceso no autorizado a los recursos del SID robado, posiblemente sin dejar un registro de auditoría en el dominio de cuenta del que se ha robado el SID.<br /> | Los administradores de dominio de recursos protegen sus recursos configurando solo las relaciones de confianza que tienen sentido desde una perspectiva de seguridad. El uso <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>de DsAddSidHistory</strong></a> está restringido, en el dominio de destino de confianza, a los miembros del grupo Administradores de dominio que ya tienen permisos amplios dentro del ámbito de sus responsabilidades.<br /> | 
| Dominio de destino no dirigido<br /> Un usuario no autorizado crea un dominio Windows 2000 con una cuenta cuyo <strong>sIDHistory</strong> contiene un SID que se ha robado de un dominio de origen. El usuario no autorizado usa esta cuenta para el acceso no autorizado a los recursos.<br /> | El usuario no autorizado requiere credenciales de administrador para el dominio de origen con el fin de usar <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a>y deja una pista de auditoría en el controlador de dominio de origen. El dominio de destino no autorizado obtiene acceso no autorizado solo en otros dominios que confían en el dominio no autorizado, lo que requiere privilegios de administrador en esos dominios de recursos.<br /> | 




 

## <a name="operational-constraints"></a>Restricciones operativas

En esta sección se describen las restricciones operativas del uso de la [**función DsAddSidHistory.**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya)

El SID de *SrcPrincipal* no debe existir en el bosque de destino, ya sea como SID de cuenta principal o en **el sIDHistory** de una cuenta. La excepción es [**que DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) no genera un error al intentar agregar un SID a **un sIDHistory** que contiene un SID idéntico. Este comportamiento permite que **DsAddSidHistory** se ejecute varias veces con una entrada idéntica, lo que da lugar a un estado final coherente y correcto, para facilitar el uso del desarrollador de herramientas.

> [!Note]  
> La latencia de replicación del catálogo global puede proporcionar una ventana durante la cual se pueden crear SID duplicados. Sin embargo, un administrador puede eliminar fácilmente los SID duplicados.

 

*SrcPrincipal* y *DstPrincipal* deben ser uno de los siguientes tipos:

-   Usuario
-   Grupo habilitado para seguridad, incluido:

    <dl> Grupo local  
    Grupo global  
    Grupo local de dominio (Windows modo nativo 2000)  
    Grupo universal (Windows modo nativo 2000)  
    </dl>

Los tipos de objeto *de SrcPrincipal* y *DstPrincipal* deben coincidir.

-   Si *SrcPrincipal* es un usuario, *DstPrincipal* debe ser un usuario.
-   Si *SrcPrincipal* es un grupo local o un grupo local de dominio, *DstPrincipal* debe ser un grupo local de dominio.
-   Si *SrcPrincipal* es un grupo global o universal, *DstPrincipal* debe ser un grupo global o universal.

*SrcPrincipal* y *DstPrincipal* no pueden ser uno de los siguientes tipos: ([**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) produce un error en estos casos)

-   Equipo (estación de trabajo o controlador de dominio)
-   Confianza entre dominios
-   Cuenta duplicada temporal (característica prácticamente sin usar, un heredado de LANman)
-   Cuentas con SID conocidos. Los SID conocidos son idénticos en todos los dominios; Por lo tanto, agregarlas a **un sIDHistory** infringiría el requisito de unidad de SID de un Windows 2000. Las cuentas con SID conocidos incluyen los siguientes grupos locales:

    <dl> Operadores de cuenta  
    Administradores  
    Operadores de copia de seguridad  
    Invitados  
    Operadores de impresión  
    Duplicadores  
    Operadores de servidores  
    Usuarios  
    </dl>

Si *SrcPrincipal* tiene un identificador relativo conocido (RID) y un prefijo específico del dominio, es decir, administradores de dominio, usuarios de dominio y equipos de dominio, *DstPrincipal* debe poseer el mismo RID conocido para que [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) se haga correctamente. Las cuentas con RID conocidos incluyen los siguientes usuarios y grupos globales:

-   Administrador
-   Invitado
-   Administradores de dominio
-   Invitados de dominio
-   Usuarios de dominio

## <a name="setting-the-registry-value"></a>Establecer el valor del Registro

El procedimiento siguiente muestra cómo establecer el valor del Registro TcpipClientSupport.

**Para establecer el valor del Registro TcpipClientSupport**

1.  Cree el siguiente valor del Registro como un valor REG DWORD en el controlador de \_ dominio de origen y establezca su valor en 1.

    **HKEY \_ LOCAL \_ MACHINE \\ SYSTEM \\ CurrentControlSet \\ Control \\ Lsa \\ TcpipClientSupport**

2.  A continuación, reinicie el controlador de dominio de origen. Este valor del Registro hace que SAM escuche en TCP/IP. [**DsAddSidHistory producirá**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) un error si este valor no está establecido en el controlador de dominio de origen.

## <a name="enabling-auditing-of-usergroup-management-events"></a>Habilitación de la auditoría de eventos de administración de usuarios o grupos

El procedimiento siguiente muestra cómo habilitar la auditoría de eventos de administración de usuarios o grupos en un dominio de origen o destino de Windows 2000 o Windows Server 2003.

**Para habilitar la auditoría de eventos de administración de usuarios o grupos en un dominio de origen o destino de Windows 2000 o Windows Server 2003**

1.  En el Usuarios y equipos de Active Directory complemento MMC, seleccione el contenedor controladores de dominio del dominio de destino.
2.  Haga clic con el botón **derecho en Controladores de dominio** y elija **Propiedades.**
3.  Haga clic en **directiva de grupo** pestaña.
4.  Seleccione la **Directiva predeterminada de controladores de dominio y** haga clic en **Editar.**
5.  En Configuración del equipo Windows Configuración seguridad Configuración directiva de auditoría de directivas **\\ \\ \\ \\ locales**, haga doble clic **en Auditar administración de cuentas**.
6.  En la ventana **Audit Account Management (Administración de cuentas** de auditoría), seleccione Success **(Correcto)** **y Failure auditing (Auditoría de** errores). Las actualizaciones de directivas tienen efecto después de un reinicio o después de que se produzca una actualización.
7.  Compruebe que la auditoría está habilitada; para ello, vea la directiva de auditoría efectiva en directiva de grupo complemento MMC.

El procedimiento siguiente muestra cómo habilitar la auditoría de eventos de administración de usuarios o grupos en un Windows NT 4.0.

**Para habilitar la auditoría de eventos de administración de usuarios o grupos en un Windows NT 4.0**

1.  En **El Administrador de usuarios para dominios**, haga clic en el menú **Directivas** y seleccione **Auditar**.
2.  Seleccione **Auditar estos eventos.**
3.  En **Administración de usuarios y grupos,** active Correcto y **error.**

El procedimiento siguiente muestra cómo habilitar la auditoría de eventos de administración de usuarios o grupos en un dominio de origen de Windows NT 4.0, Windows 2000 o Windows Server 2003.

**Para habilitar la auditoría de eventos de administración de usuarios o grupos en un dominio de origen de Windows NT 4.0, Windows 2000 o Windows Server 2003**

1.  En **Administrador de usuarios para dominios**, haga clic en el menú **Usuario** y seleccione Nuevo **grupo local.**
2.  Escriba un nombre de grupo compuesto por el nombre NetBIOS del dominio de origen anexado con tres signos de dólar ($), por ejemplo, FABRIKAM$$$. El campo de descripción debe indicar que este grupo se usa para auditar el uso de [**operaciones DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) o clonación. Asegúrese de que no haya ningún miembro en el grupo. Haga clic en **Aceptar**.

Se [**produce un error en la operación DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) si la auditoría de origen y destino no está habilitada como se describe aquí.

## <a name="set-up-trust-if-required"></a>Configurar confianza si es necesario

Si se cumple una de las condiciones siguientes, se debe establecer una confianza desde el dominio de origen al dominio de destino (esto debe producirse en un bosque diferente):

-   El dominio de origen Windows Server 2003.
-   El dominio de origen Windows NT 4.0 y *SrcDomainCreds* es **NULL.**

 

 





