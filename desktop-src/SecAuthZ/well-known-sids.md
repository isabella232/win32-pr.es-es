---
description: Los identificadores de seguridad conocidos (SID) identifican los grupos genéricos y los usuarios genéricos.
ms.assetid: eb2f95c4-9465-409b-b76c-9ccae1d05eda
title: SID conocidos
ms.topic: article
ms.date: 03/04/2020
ms.custom: 19H1
ms.openlocfilehash: 1fdde933b3e4f844e63785ff130aaf89204fe0af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668048"
---
# <a name="well-known-sids"></a>SID conocidos

Los [*identificadores de seguridad*](/windows/desktop/SecGloss/s-gly) conocidos (SID) identifican los grupos genéricos y los usuarios genéricos. Por ejemplo, hay SID conocidos para identificar los siguientes grupos y usuarios:

-   Todos o todo el mundo, que es un grupo que incluye a todos los usuarios.
-   CREATOR \_ Owner, que se usa como marcador de posición en una ACE heredable. Cuando se hereda la ACE, el sistema reemplaza el SID del propietario del creador \_ por el SID del creador del objeto.
-   El grupo administradores del dominio integrado en el equipo local.

Existen [*SID universales conocidos*](/windows/desktop/SecGloss/u-gly), que son significativos en todos los sistemas seguros que usan este modelo de seguridad, incluidos los sistemas operativos distintos de Windows. Además, hay SID conocidos que solo son significativos en los sistemas Windows.

La API de Windows define un conjunto de constantes para los valores conocidos de autoridad de identificador y de [*identificador relativo*](/windows/desktop/SecGloss/r-gly) (RID). Estas constantes se pueden usar para crear SID conocidos. En el ejemplo siguiente se combinan las constantes de RID del mundo de seguridad \_ \_ y el \_ \_ WWN del mundo de seguridad \_ para mostrar el SID universal conocido para el grupo especial que representa a todos los usuarios (todo el mundo):

S-1-1-0

En este ejemplo se usa la notación de cadena para los SID en los que S identifica la cadena como un SID, el primer nivel de revisión del SID y los dos dígitos restantes son las \_ constantes de RID del mundo de seguridad \_ y el mundo de \_ seguridad \_ \_ .

Puede usar la función [**AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) para crear un SID mediante la combinación de un valor de autoridad de identificador con un máximo de ocho valores de subautoridad. Por ejemplo, para determinar si el usuario que ha iniciado sesión es miembro de un grupo conocido determinado, llame a **AllocateAndInitializeSid** para crear un SID para el grupo conocido y use la función [**EqualSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-equalsid) para comparar ese SID con los SID de grupo en el [*token de acceso*](/windows/desktop/SecGloss/a-gly)del usuario. Para obtener un ejemplo, vea [Buscar un SID en un token de acceso en C++](searching-for-a-sid-in-an-access-token-in-c--.md). Debe llamar a la función [**FreeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-freesid) para liberar un SID asignado por **AllocateAndInitializeSid**.

El resto de esta sección contiene tablas de SID conocidos y tablas de constantes de entidad de certificación y subautor que puede usar para crear SID conocidos.

A continuación se muestran algunos [*SID universales conocidos*](/windows/desktop/SecGloss/u-gly).



| SID conocido universal    | Valor de cadena       | Identifica                                                                                                                                               |
|-----------------------------|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| SID nulo<br/>         | S-1-0-0<br/> | Grupo sin miembros. Se suele usar cuando no se conoce un valor de SID.<br/>                                                                    |
| World<br/>            | S-1-1-0<br/> | Grupo que incluye todos los usuarios.<br/>                                                                                                              |
| Local<br/>            | S-1-2-0<br/> | Usuarios que inician sesión [*localmente (*](/windows/desktop/SecGloss/t-gly) físicamente) conectados al sistema.<br/> |
| IDENTIFICADOR del propietario del creador<br/> | S-1-3-0<br/> | Un identificador de seguridad que se va a reemplazar por el identificador de seguridad del usuario que creó un nuevo objeto. Este SID se usa en las ACE heredables.<br/>   |
| ID. de grupo de Creator<br/> | S-1-3-1<br/> | Identificador de seguridad que se va a reemplazar por el SID del grupo principal del usuario que creó un nuevo objeto. Use este SID en las ACE heredables.<br/>         |



 

En la tabla siguiente se enumeran las constantes de entidad de identificación predefinidas. Los primeros cuatro valores se usan con SID conocidos universales; el último valor se usa con SID conocidos de Windows.



| Autoridad del identificador                         | Value        | Valor de cadena |
|----------------------------------------------|--------------|-------------------|
| entidad de SID de seguridad \_ nula \_ \_<br/>    | 0<br/> | S-1-0<br/>  |
| \_autoridad de \_ SID del mundo de seguridad \_<br/>   | 1<br/> | S-1-1<br/>  |
| \_entidad de \_ SID \_ local de seguridad<br/>   | 2<br/> | S-1-2<br/>  |
| \_entidad de \_ SID del creador de seguridad \_<br/> | 3<br/> | S-1-3<br/>  |
| autoridad de seguridad de \_ NT \_<br/>           | 5<br/> | S-1-5<br/>  |



 

Los siguientes valores [*RID*](/windows/desktop/SecGloss/r-gly) se usan con [*SID conocidos universales*](/windows/desktop/SecGloss/u-gly). La columna identificador de entidad muestra el prefijo de la autoridad del identificador con el que se puede combinar el RID para crear un SID universal conocido.



| Autoridad de identificador relativo            | Value        | Valor de cadena |
|------------------------------------------|--------------|----------------------|
| RID de seguridad \_ nula \_<br/>           | 0<br/> | S-1-0<br/>     |
| \_RID del mundo de seguridad \_<br/>          | 0<br/> | S-1-1<br/>     |
| \_RID local de seguridad \_<br/>          | 0<br/> | S-1-2<br/>     |
| \_RID de \_ Inicio de sesión local de seguridad \_<br/>   | 1<br/> | S-1-2<br/>     |
| \_RID del \_ propietario del creador de seguridad \_<br/> | 0<br/> | S-1-3<br/>     |
| \_RID de \_ grupo de creadores de seguridad \_<br/> | 1<br/> | S-1-3<br/>     |



 

La \_ autoridad de \_ identificadores predefinidos de la entidad de seguridad NT (S-1-5) genera SID que no son universales pero que solo son significativos en las instalaciones de Windows. Puede usar los siguientes valores RID con la autoridad de seguridad \_ NT \_ para crear SID conocidos.



| Constante                                          | Valor de cadena               | Identifica                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_RID de acceso telefónico de seguridad \_<br/>                  | S-1-5-1<br/>         | Usuarios que inician sesión en [*terminales*](/windows/desktop/SecGloss/t-gly) con un módem de acceso telefónico. Este es un identificador de grupo.<br/>                                                                                                                                                                                                                                                                                                                                                                  |
| RID de la red de seguridad \_ \_<br/>                 | S-1-5-2<br/>         | Usuarios que inician sesión a través de una red. Se trata de un identificador de grupo que se agrega al token de un proceso cuando inició sesión a través de una red. El tipo de inicio de sesión correspondiente es LOGON32 \_ Logon \_ Network.<br/>                                                                                                                                                                                                                                                                                                                      |
| \_RID de batch de seguridad \_<br/>                   | S-1-5-3<br/>         | Usuarios que inician sesión con un servicio de cola de batch. Se trata de un identificador de grupo que se agrega al token de un proceso cuando se registró como un trabajo por lotes. El tipo de inicio de sesión correspondiente es el lote de inicio de sesión LOGON32 \_ \_ .<br/>                                                                                                                                                                                                                                                                                                                 |
| \_RID interactivo de seguridad \_<br/>             | S-1-5-4<br/>         | Usuarios que inician sesión para una operación interactiva. Se trata de un identificador de grupo que se agrega al token de un proceso cuando se inició sesión de forma interactiva. El tipo de inicio de sesión correspondiente es LOGON32 \_ Logon \_ Interactive.<br/>                                                                                                                                                                                                                                                                                                            |
| RID de ID. de inicio de sesión de seguridad \_ \_ \_<br/>              | S-1-5-5-*X* - *Y*<br/> | Una sesión de inicio de sesión. Se utiliza para asegurarse de que solo [*los procesos*](/windows/desktop/SecGloss/p-gly) de una sesión de inicio de sesión determinada puedan obtener acceso a los objetos de la estación de ventana de esa sesión. Los  valores X *e y* de estos SID son diferentes para cada sesión de inicio de sesión. El valor \_ \_ recuento de RID de ID. de inicio de sesión \_ de seguridad \_ es el número de RID en este identificador (5-*X* - *Y*).<br/>                                                                                                                   |
| \_RID del servicio de seguridad \_<br/>                 | S-1-5-6<br/>         | Cuentas autorizadas para iniciar sesión como servicio. Se trata de un identificador de grupo que se agrega al token de un proceso cuando se registró como un servicio. El tipo de inicio de sesión correspondiente es LOGON32 \_ Logon \_ Service.<br/>                                                                                                                                                                                                                                                                                                                    |
| \_RID de \_ Inicio de sesión anónimo de seguridad \_<br/>        | S-1-5-7<br/>         | Inicio de sesión anónimo o inicio de sesión de sesión nula.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| \_RID del proxy de seguridad \_<br/>                   | S-1-5-8<br/>         | Proxi.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| \_RID de \_ controladores de empresa de seguridad \_<br/> | S-1-5-9<br/>         | Controladores empresariales.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| \_ \_ RID independiente de \_ seguridad<br/>         | S-1-5-10<br/>        | El \_ identificador de autoseguridad de la entidad de seguridad se puede usar en la ACL de un objeto de usuario o grupo. Durante una comprobación de acceso, el sistema reemplaza el SID por el SID del objeto. El \_ SID propio principal es útil para especificar una ACE heredable que se aplica al usuario o al objeto de grupo que hereda la ACE. Es la única manera de representar el SID de un objeto creado en el [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly) predeterminado del esquema.<br/> |
| \_RID de usuario autenticado de seguridad \_ \_<br/>     | S-1-5-11<br/>        | Los usuarios autenticados.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| \_RID de \_ código restringido de seguridad \_<br/>        | S-1-5-12<br/>        | Código restringido.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| RID de SECURITY \_ terminal \_ Server \_<br/>        | S-1-5-13<br/>        | Terminal Services. Se agrega automáticamente al token de seguridad de un usuario que inicia sesión en un servidor de Terminal Server.<br/>                                                                                                                                                                                                                                                                                                                                                                                                            |
| \_ \_ RID del sistema local de seguridad \_<br/>           | S-1-5-18<br/>        | Una cuenta especial utilizada por el sistema operativo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| SEGURIDAD \_ NT \_ no \_ única<br/>              | S-1-5-21<br/>        | Los SID no son únicos.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| \_ \_ RID de dominio integrado de seguridad \_<br/>         | S-1-5-32<br/>        | Dominio del sistema integrado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| \_RID de \_ código restringido de escritura \_ de seguridad \_<br/> | S-1-5-33<br/>        | Escribir código restringido.<br/> |


 

Los siguientes RID son relativos a cada dominio.



| RID                                                                | Value       | Identifica                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ALIAS de dominio \_ \_ RID \_ CERTSVC \_ grupo de acceso de DCOM \_ \_<br/>              | 0x0000023E | Grupo de usuarios que pueden conectarse a las entidades de certificación mediante el modelo de objetos componentes distribuido (DCOM).<br/>                                                                                                                          |
| \_Administrador de \_ RID de usuario de dominio \_<br/>                                      | 0x000001F4 | La cuenta de usuario administrativo en un dominio.<br/>                                                                                                                                                                                              |
| \_invitado de \_ RID de usuario de dominio \_<br/>                                      | 0x000001F5 | La cuenta de usuario invitado en un dominio. Los usuarios que no tienen una cuenta pueden iniciar sesión automáticamente en esta cuenta.<br/>                                                                                                                            |
| \_administradores de \_ RID de grupo de dominio \_<br/>                                    | 0x00000200 | El grupo administradores de dominio. Esta cuenta solo existe en sistemas que ejecutan sistemas operativos de servidor.<br/>                                                                                                                                   |
| \_usuarios de \_ RID de grupo de dominio \_<br/>                                     | 0x00000201 | Un grupo que contiene todas las cuentas de usuario de un dominio. Todos los usuarios se agregan automáticamente a este grupo.<br/>                                                                                                                                     |
| \_invitados de \_ RID de grupo de dominio \_<br/>                                    | 0x00000202 | La cuenta de grupo invitado en un dominio.<br/>                                                                                                                                                                                                      |
| \_ \_ equipos RID del grupo de dominio \_<br/>                                 | 0x00000203 | Grupo de equipos del dominio. Todos los equipos del dominio son miembros de este grupo.<br/>                                                                                                                                                       |
| \_controladores de \_ RID de grupo de dominio \_<br/>                               | 0x00000204 | Grupo de controladores de dominio. Todos los controladores de dominio del dominio son miembros de este grupo.<br/>                                                                                                                                                           |
| \_administradores de \_ \_ certificados RID de grupo \_ de dominio<br/>                              | 0x00000205 | Grupo de publicadores de certificados. Los equipos que ejecutan servicios de Certificate Server son miembros de este grupo.<br/>                                                                                                                                      |
| Controladores de dominio de \_ \_ \_ \_ solo lectura empresarial \_ \_ RID de grupo de dominio<br/> | 0x000001F2 | Grupo de controladores de dominio empresariales de solo lectura.<br/>                                                                                                                                                                                     |
| \_administradores de \_ \_ esquema RID del grupo \_ de dominio<br/>                            | 0x00000206 | El grupo administradores de esquema. Los miembros de este grupo pueden modificar el esquema de Active Directory.<br/>                                                                                                                                           |
| \_administradores de \_ \_ empresa RID de grupo \_ de dominio<br/>                        | 0x00000207 | El grupo administradores de empresas. Los miembros de este grupo tienen acceso total a todos los dominios del bosque de Active Directory. Los administradores de empresa son responsables de las operaciones de nivel de bosque, como agregar o quitar nuevos dominios.<br/> |
| \_administradores de \_ directivas de RID de grupo de dominio \_ \_<br/>                            | 0x00000208 | El grupo administradores de directivas.<br/>                                                                                                                                                                                                         |
| \_controladores de \_ \_ solo lectura de RID de grupo de dominio \_<br/>                     | 0x00000209 | Grupo de controladores de dominio de solo lectura.<br/>                                                                                                                                                                                                |                                             
| \_ \_ \_ Controladores clonables de RID de grupo de dominio \_<br />                   | 0x0000020A | Grupo de controladores de dominio clonables.<br/>                                                                                                                                                                                                |
| CDC de RID de grupo de dominio \_ \_ \_ \_ reservado<br />                            | 0x0000020C | Grupo CDC reservado.<br/>                                                                                                                                                                                                                   |
| \_ \_ usuarios protegidos de RID de grupo de \_ dominio \_<br />                         | 0x0000020D | Grupo usuarios protegidos.</br>                                                                                                                                                                                                                |
| \_administradores de \_ claves de RID de grupo de dominio \_ \_<br />                              | 0x0000020E | El grupo administradores de claves.<br/>                                                                                                                                                                                                                     |
| \_administradores de \_ \_ clave empresarial \_ RID \_ del grupo de dominio<br />                  | 0x0000020F | El grupo administradores de claves de empresa</br>                                                                                                                                                                                                           |



 

Los siguientes RID se usan para especificar el nivel de integridad obligatorio.



| RID                                                     | Value                                               | Identifica                        |
|---------------------------------------------------------|-----------------------------------------------------|-----------------------------------|
| RID de seguridad obligatoria que no es de \_ \_ confianza \_<br/>          | 0x00000000<br/>                               | Confianza.<br/>             |
| \_RID de \_ baja seguridad obligatoria \_<br/>                | 0x00001000<br/>                               | Integridad baja.<br/>         |
| \_ \_ RID mediana de seguridad obligatoria \_<br/>             | 0x00002000<br/>                               | Integridad media.<br/>      |
| \_medio obligatorio de seguridad \_ \_ más \_ RID<br/>       | RID de seguridad \_ \_ medio \_ RID + 0x100<br/> | Integridad media alta.<br/> |
| \_RID de \_ alta seguridad obligatoria \_<br/>               | 0X00003000<br/>                               | Alta integridad.<br/>        |
| \_ \_ RID del sistema obligatorio de seguridad \_<br/>             | 0x00004000<br/>                               | Integridad del sistema.<br/>      |
| \_RID de \_ \_ proceso protegido \_ de seguridad obligatorio<br/> | 0x00005000<br/>                               | Proceso protegido.<br/>     |



 

En la tabla siguiente se incluyen ejemplos de RID relativos al dominio que puede usar para formar SID conocidos para grupos locales (alias). Para obtener más información acerca de los grupos locales y globales, consulte funciones de grupo [locales](/windows/desktop/NetMgmt/local-group-functions) y [funciones de grupo](/windows/desktop/NetMgmt/group-functions).



| RID                                                              | Value                 |Valor de cadena  | Identifica                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------|-----------------|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_administradores de \_ RID de alias de dominio \_<br/>                            | 0x00000220<br/> | S-1-5-32-544<br/> | Grupo local que se usa para la administración del dominio.<br/>                                                                                                                                                                                                                            |
| \_alias de \_ dominio \_ usuarios RID<br/>                             | 0x00000221<br/> | S-1-5-32-545<br/> | Un grupo local que representa todos los usuarios del dominio.<br/>                                                                                                                                                                                                                          |
| los \_ \_ invitados RID de alias de dominio \_<br/>                            | 0x00000222<br/> | S-1-5-32-546<br/> | Un grupo local que representa a los invitados del dominio.<br/>                                                                                                                                                                                                                             |
| ALIAS de dominio \_ \_ \_ usuarios de energía RID \_<br/>                      | 0x00000223<br/> | S-1-5-32-547<br/> | Grupo local que se usa para representar a un usuario o a un conjunto de usuarios que esperan tratar un sistema como si fuera su equipo personal en lugar de una estación de trabajo para varios usuarios.<br/>                                                                                                      |
| \_operaciones de \_ cuenta de RID de alias de dominio \_ \_<br/>                      | 0x00000224<br/> | S-1-5-32-548<br/> | Un grupo local que existe solo en sistemas que ejecutan sistemas operativos de servidor. Este grupo local permite el control de las cuentas que no son de administrador.<br/>                                                                                                                                    |
| \_ \_ \_ operaciones del sistema RID del alias de dominio \_<br/>                       | 0x00000225<br/> | S-1-5-32-549<br/> | Un grupo local que existe solo en sistemas que ejecutan sistemas operativos de servidor. Este grupo local realiza funciones administrativas del sistema, sin incluir funciones de seguridad. Establece recursos compartidos de red, controla impresoras, desbloquea estaciones de trabajo y realiza otras operaciones.<br/> |
| \_operaciones de \_ impresión de RID de alias de dominio \_ \_<br/>                        | 0x00000226<br/> | S-1-5-32-550<br/> | Un grupo local que existe solo en sistemas que ejecutan sistemas operativos de servidor. Este grupo local controla las impresoras y las colas de impresión.<br/>                                                                                                                                                |
| \_operadores de \_ copia de \_ seguridad RID \_ de alias de dominio<br/>                       | 0x00000227<br/> | S-1-5-32-551<br/> | Grupo local que se usa para controlar la asignación de privilegios de copia de seguridad y restauración de archivos.<br/>                                                                                                                                                                                            |
| \_ \_ replicador RID de alias de dominio \_<br/>                        | 0x00000228<br/> | S-1-5-32-552<br/> | Grupo local responsable de copiar las bases de datos de seguridad del controlador de dominio principal a los controladores de dominio de reserva. Estas cuentas solo se usan en el sistema.<br/>                                                                                                       |
| \_ \_ \_ servidores RAS RID de alias de dominio \_<br/>                      | 0x00000229<br/> | S-1-5-32-553<br/> | Un grupo local que representa los servidores RAS e IAS. Este grupo permite el acceso a varios atributos de objetos de usuario.<br/>                                                                                                                                                             |
| ALIAS de dominio \_ \_ RID \_ PREW2KCOMPACCESS<br/>                  | 0x0000022A<br/> | S-1-5-32-554<br/> | Un grupo local que solo existe en sistemas que ejecutan Windows 2000 Server. Para obtener más información, consulte [permitir el acceso anónimo](allowing-anonymous-access.md).<br/>                                                                                                                    |
| ALIAS de dominio \_ \_ \_ usuarios de escritorio remoto RID \_ \_<br/>            | 0x0000022B<br/> | S-1-5-32-555<br/> | Un grupo local que representa todos los usuarios de escritorio remoto.<br/>                                                                                                                                                                                                                         |
| \_operaciones de \_ \_ configuración de red RID de alias \_ de dominio \_<br/>       | 0x0000022C<br/> | S-1-5-32-556<br/> | Un grupo local que representa la configuración de red. <br/>                                                                                                                                                                                                                       |
| \_creadores de \_ \_ confianza de bosque de entrada RID \_ \_ de alias de dominio \_<br/> | 0x0000022D<br/> | S-1-5-32-557<br/> | Un grupo local que representa a cualquier usuario de confianza de bosque.<br/>                                                                                                                                                                                                                           |
| \_usuarios de \_ supervisión de RID de alias de dominio \_ \_<br/>                 | 0x0000022E<br/> | S-1-5-32-558<br/> | Un grupo local que representa todos los usuarios que se están supervisando.<br/>                                                                                                                                                                                                                        |
| \_usuarios de \_ registro de RID de alias de dominio \_ \_<br/>                    | 0x0000022F<br/> | S-1-5-32-559<br/> | Un grupo local responsable del registro de usuarios.<br/>                                                                                                                                                                                                                                    |
| ALIAS de dominio \_ \_ RID \_ AUTHORIZATIONACCESS<br/>               | 0x00000230<br/> | S-1-5-32-560<br/> | Un grupo local que representa todo el acceso autorizado.<br/>                                                                                                                                                                                                                            |
| ALIAS de dominio \_ \_ RID \_ servidor de licencias de TS \_ \_<br/>              | 0x00000231<br/> | S-1-5-32-561<br/> | Un grupo local que existe solo en sistemas que ejecutan sistemas operativos de servidor que permiten servicios de Terminal Server y acceso remoto.<br/>                                                                                                                                                  |
| ALIAS de dominio \_ \_ RID de \_ usuarios de DCOM \_<br/>                       | 0x00000232<br/> | S-1-5-32-562<br/> | Grupo local que representa a los usuarios que pueden utilizar el modelo de objetos componentes distribuido (DCOM).<br/>                                                                                                                                                                                      |
| ALIAS de dominio \_ \_ RID \_ IUSERS<br/>                            | 0X00000238<br/> | S-1-5-32-568<br/> | Un grupo local que representa a los usuarios de Internet.<br/>                                                                                                                                                                                                                                   |
| \_operadores de \_ \_ cifrado RID de alias de dominio \_<br/>                 | 0x00000239<br/> | S-1-5-32-569<br/> | Un grupo local que representa el acceso a los operadores de criptografía.<br/>                                                                                                                                                                                                                 |
| ALIAS de dominio grupo de entidades de seguridad RID que se \_ \_ \_ almacenan en caché \_ \_<br/>      | 0x0000023B<br/> | S-1-5-32-571<br/> | Un grupo local que representa las entidades de seguridad que se pueden almacenar en caché.<br/>                                                                                                                                                                                                                    |
| Grupo de entidades de seguridad \_ \_ RID \_ no \_ almacenable en \_ \_ el alias de dominio<br/> | 0x0000023C<br/> | S-1-5-32-572<br/> | Un grupo local que representa las entidades de seguridad que no se pueden almacenar en caché.<br/>                                                                                                                                                                                                                 |
| \_grupo de \_ \_ lectores de registro de eventos RID \_ \_ de alias de dominio \_<br/>        | 0x0000023D<br/> | S-1-5-32-573<br/> | Un grupo local que representa los lectores del registro de eventos.<br/>                                                                                                                                                                                                                                |
| ALIAS de dominio \_ \_ RID \_ CERTSVC \_ grupo de acceso de DCOM \_ \_<br/>      | 0x0000023E<br/> | S-1-5-32-574<br/> | Grupo local de usuarios que pueden conectarse a las entidades de certificación mediante el modelo de objetos componentes distribuido (DCOM).<br/>                                                                                                                                                          |
| ALIAS de dominio \_ \_ RID \_ \_ Remote \_ Access \_ servers<br />     | 0x0000023F<br/> | S-1-5-32-575<br/> | Un grupo local que representa los servidores de acceso remoto de RDS.<br/> |
| ALIAS de dominio \_ \_ RID de \_ \_ los servidores de extremo RDS \_                 | 0x00000240<br/> | S-1-5-32-576<br/> | Un grupo local que representa los servidores de extremo.<br/> |
| \_servidores de \_ \_ Administración de RDS RID de alias \_ de dominio \_               | 0x00000241<br/> | S-1-5-32-577<br/> | Un grupo local que representa los servidores de administración. <br/>|
| ALIAS de dominio \_ \_ RID de \_ Hyper \_ V \_ Admins                       | 0x00000242<br/> | S-1-5-32-578<br/> | Un grupo local que representa a los administradores de Hyper-v <br/>|
| \_operaciones de \_ \_ asistencia de control de acceso RID \_ \_ de alias de dominio \_       | 0x00000243<br/> | S-1-5-32-579<br/> | Un grupo local que representa las operaciones de asistencia para el control de acceso.<br/> |
| ALIAS de dominio \_ \_ \_ usuarios de administración remota RID \_ \_              | 0x00000244<br/> | S-1-5-32-580<br/> | Un grupo local que representa a los usuarios de administración remota. <br/>|
| \_ \_ cuenta predeterminada de RID de alias de \_ dominio \_                       | 0x00000245<br/> | S-1-5-32-581<br/> | Un grupo local que representa la cuenta predeterminada. <br/>|
| \_administradores de \_ \_ réplica de almacenamiento RID de alias \_ de dominio \_               | 0x00000246<br/> | S-1-5-32-582<br/> | Un grupo local que representa A los administradores de réplica de almacenamiento. <br/>|
| \_propietarios de \_ \_ dispositivos RID de alias \_ de dominio                            | 0x00000247<br/> | S-1-5-32-583<br/> | Un grupo local que representa puede establecer la configuración esperada para los propietarios de dispositivos.<br/>|


 

La enumeración [**\_ known \_ \_ Type de SID**](/windows/desktop/api/Winnt/ne-winnt-well_known_sid_type) define la lista de SID utilizados con frecuencia. Además, el [lenguaje de definición de descriptores de seguridad](security-descriptor-definition-language.md) (SDDL) utiliza [cadenas de SID](sid-strings.md) para hacer referencia a SID conocidos en un formato de cadena.

 

