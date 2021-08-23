---
description: Los identificadores de seguridad (SID) conocidos identifican grupos genéricos y usuarios genéricos.
ms.assetid: eb2f95c4-9465-409b-b76c-9ccae1d05eda
title: SID conocidos
ms.topic: article
ms.date: 03/04/2020
ms.custom: 19H1
ms.openlocfilehash: 17fe8827100f9e3684ac0219fc83f183581017cc5738af5933b7bb7cc4ea3ff8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119623095"
---
# <a name="well-known-sids"></a>SID conocidos

Los identificadores de seguridad (SID) [*conocidos*](/windows/desktop/SecGloss/s-gly) identifican grupos genéricos y usuarios genéricos. Por ejemplo, hay SID conocidos para identificar los siguientes grupos y usuarios:

-   Todos o Mundo, que es un grupo que incluye todos los usuarios.
-   CREATOR \_ OWNER, que se usa como marcador de posición en una ACE heredable. Cuando se hereda la ACE, el sistema reemplaza el SID CREATOR OWNER por el SID del creador \_ del objeto.
-   El grupo Administradores del dominio integrado en el equipo local.

Hay [*SID universales conocidos,*](/windows/desktop/SecGloss/u-gly)que son significativos en todos los sistemas seguros que usan este modelo de seguridad, incluidos los sistemas operativos distintos de Windows. Además, hay SID conocidos que solo son significativos en Windows sistemas.

La Windows API define un conjunto de constantes para valores [](/windows/desktop/SecGloss/r-gly) conocidos de autoridad de identificador y identificador relativo (RID). Puede usar estas constantes para crear SID conocidos. En el ejemplo siguiente se combinan las constantes SECURITY WORLD SID AUTHORITY y SECURITY WORLD RID para mostrar el SID conocido universal para el grupo especial que representa a todos los usuarios (Todos o \_ \_ \_ \_ \_ Mundo):

S-1-1-0

En este ejemplo se usa la notación de cadena para los SID en los que S identifica la cadena como SID, la primera es el nivel de revisión del SID y los dos \_ \_ \_ \_ dígitos restantes son las constantes SECURITY WORLD SID AUTHORITY y SECURITY WORLD \_ RID.

Puede usar la [**función AllocateAndInitializeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-allocateandinitializesid) para compilar un SID combinando un valor de entidad de identificador con hasta ocho valores de subautoridad. Por ejemplo, para determinar si el usuario que inició sesión es miembro de un grupo conocido determinado, llame a **AllocateAndInitializeSid** para compilar un SID para el grupo conocido y use la función [**EqualSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-equalsid) para comparar ese SID con los SID del grupo en el token de acceso del [*usuario.*](/windows/desktop/SecGloss/a-gly) Para obtener un ejemplo, vea [Buscar un SID en un token de acceso en C++.](searching-for-a-sid-in-an-access-token-in-c--.md) Debe llamar a la [**función FreeSid**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-freesid) para liberar un SID asignado por **AllocateAndInitializeSid**.

El resto de esta sección contiene tablas de SID conocidos y tablas de constantes de autoridad de identificador y subautoridad que puede usar para crear SID conocidos.

Estos son algunos [*SID universales conocidos.*](/windows/desktop/SecGloss/u-gly)



| SID conocido universal    | Valor de cadena       | Identifica                                                                                                                                               |
|-----------------------------|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| SID nulo<br/>         | S-1-0-0<br/> | Un grupo sin miembros. Esto se usa a menudo cuando no se conoce un valor de SID.<br/>                                                                    |
| World<br/>            | S-1-1-0<br/> | Grupo que incluye todos los usuarios.<br/>                                                                                                              |
| Local<br/>            | S-1-2-0<br/> | Usuarios que inician sesión en [*terminales*](/windows/desktop/SecGloss/t-gly) localmente (físicamente) conectados al sistema.<br/> |
| Id. de propietario del creador<br/> | S-1-3-0<br/> | Identificador de seguridad que se va a reemplazar por el identificador de seguridad del usuario que creó un nuevo objeto. Este SID se usa en ace heredables.<br/>   |
| Identificador de grupo de Creator<br/> | S-1-3-1<br/> | Identificador de seguridad que se va a reemplazar por el SID del grupo principal del usuario que creó un nuevo objeto. Use este SID en ace heredables.<br/>         |



 

En la tabla siguiente se enumeran las constantes predefinidas de autoridad de identificador. Los cuatro primeros valores se usan con SID conocidos universales; el último valor se usa con Windows SID conocidos.



| Entidad de identificador                         | Valor        | Valor de cadena |
|----------------------------------------------|--------------|-------------------|
| ENTIDAD \_ DE \_ SID NULL DE \_ SEGURIDAD<br/>    | 0<br/> | S-1-0<br/>  |
| AUTORIDAD \_ DE \_ SID DEL MUNDO DE \_ SEGURIDAD<br/>   | 1<br/> | S-1-1<br/>  |
| ENTIDAD \_ DE SID LOCAL \_ DE \_ SEGURIDAD<br/>   | 2<br/> | S-1-2<br/>  |
| ENTIDAD \_ DE SID DE CREADOR \_ DE \_ SEGURIDAD<br/> | 3<br/> | S-1-3<br/>  |
| ENTIDAD \_ DE SEGURIDAD \_ NT<br/>           | 5<br/> | S-1-5<br/>  |



 

Los siguientes [*valores de RID*](/windows/desktop/SecGloss/r-gly) se usan con [*SID conocidos universales.*](/windows/desktop/SecGloss/u-gly) La columna Entidad de identificador muestra el prefijo de la entidad de identificador con la que puede combinar el RID para crear un SID conocido universal.



| Autoridad de identificador relativo            | Value        | Valor de cadena |
|------------------------------------------|--------------|----------------------|
| RID \_ DE VALORES NULL DE \_ SEGURIDAD<br/>           | 0<br/> | S-1-0<br/>     |
| RID \_ DEL MUNDO DE \_ SEGURIDAD<br/>          | 0<br/> | S-1-1<br/>     |
| RID \_ LOCAL \_ DE SEGURIDAD<br/>          | 0<br/> | S-1-2<br/>     |
| RID \_ DE INICIO DE SESIÓN LOCAL DE \_ \_ SEGURIDAD<br/>   | 1<br/> | S-1-2<br/>     |
| RID \_ DEL PROPIETARIO DEL CREADOR DE \_ \_ SEGURIDAD<br/> | 0<br/> | S-1-3<br/>     |
| RID DE GRUPO DE CREADOR \_ \_ DE \_ SEGURIDAD<br/> | 1<br/> | S-1-3<br/>     |



 

La entidad de identificación predefinida SECURITY \_ NT AUTHORITY (S-1-5) genera SID que no son universales, pero que solo son significativos en \_ Windows instalaciones. Puede usar los siguientes valores de RID con SECURITY \_ NT AUTHORITY para crear \_ SID conocidos.



| Constante                                          | Valor de cadena               | Identifica                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RID \_ DE ACCESO TELEFÓNICO DE \_ SEGURIDAD<br/>                  | S-1-5-1<br/>         | Usuarios que inician sesión en [*terminales*](/windows/desktop/SecGloss/t-gly) mediante un módem telefónico. Se trata de un identificador de grupo.<br/>                                                                                                                                                                                                                                                                                                                                                                  |
| RID \_ DE RED DE \_ SEGURIDAD<br/>                 | S-1-5-2<br/>         | Usuarios que inician sesión a través de una red. Se trata de un identificador de grupo agregado al token de un proceso cuando se inició sesión a través de una red. El tipo de inicio de sesión correspondiente es LOGON32 \_ LOGON \_ NETWORK.<br/>                                                                                                                                                                                                                                                                                                                      |
| RID DE \_ LOTE DE \_ SEGURIDAD<br/>                   | S-1-5-3<br/>         | Usuarios que inician sesión con una instalación de cola por lotes. Se trata de un identificador de grupo agregado al token de un proceso cuando se registró como un trabajo por lotes. El tipo de inicio de sesión correspondiente es LOGON32 \_ LOGON \_ BATCH.<br/>                                                                                                                                                                                                                                                                                                                 |
| RID \_ INTERACTIVO \_ DE SEGURIDAD<br/>             | S-1-5-4<br/>         | Usuarios que inician sesión para una operación interactiva. Se trata de un identificador de grupo agregado al token de un proceso cuando se inició sesión de forma interactiva. El tipo de inicio de sesión correspondiente es LOGON32 \_ LOGON \_ INTERACTIVE.<br/>                                                                                                                                                                                                                                                                                                            |
| RID DE \_ IDENTIFICADORES \_ DE INICIO DE SESIÓN DE \_ SEGURIDAD<br/>              | S-1-5-5-*X* - *Y*<br/> | Una sesión de inicio de sesión. Esto se usa para asegurarse de que [*solo*](/windows/desktop/SecGloss/p-gly) los procesos de una sesión de inicio de sesión determinada puedan obtener acceso a los objetos de la estación de ventana para esa sesión. Los *valores X* e Y *de* estos SID son diferentes para cada sesión de inicio de sesión. El valor SECURITY LOGON IDS RID COUNT es el número de RID de este \_ \_ identificador \_ \_ (5-*X* - *Y).*<br/>                                                                                                                   |
| RID \_ DEL SERVICIO DE \_ SEGURIDAD<br/>                 | S-1-5-6<br/>         | Cuentas autorizadas para iniciar sesión como servicio. Se trata de un identificador de grupo agregado al token de un proceso cuando se registró como un servicio. El tipo de inicio de sesión correspondiente es LOGON32 \_ LOGON \_ SERVICE.<br/>                                                                                                                                                                                                                                                                                                                    |
| RID DE \_ INICIO DE SESIÓN ANÓNIMO DE \_ \_ SEGURIDAD<br/>        | S-1-5-7<br/>         | Inicio de sesión anónimo o inicio de sesión nulo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| RID \_ DE PROXY DE \_ SEGURIDAD<br/>                   | S-1-5-8<br/>         | Proxy.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| RID \_ DE CONTROLADORES \_ EMPRESARIALES DE \_ SEGURIDAD<br/> | S-1-5-9<br/>         | Enterprise controladores.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| AUTO \_ RID DE LA ENTIDAD DE \_ \_ SEGURIDAD<br/>         | S-1-5-10<br/>        | El identificador \_ de seguridad PRINCIPAL SELF se puede usar en la ACL de un objeto de usuario o grupo. Durante una comprobación de acceso, el sistema reemplaza el SID por el SID del objeto. El SELF SID de entidad de seguridad es útil para especificar una ACE heredable que se aplique al objeto de usuario o grupo \_ que hereda la ACE. Es la única manera de representar el SID de un objeto creado en el descriptor de [*seguridad predeterminado*](/windows/desktop/SecGloss/s-gly) del esquema.<br/> |
| RID \_ DE USUARIO \_ AUTENTICADO POR \_ SEGURIDAD<br/>     | S-1-5-11<br/>        | Usuarios autenticados.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| RID \_ DE CÓDIGO RESTRINGIDO DE \_ \_ SEGURIDAD<br/>        | S-1-5-12<br/>        | Código restringido.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| RID \_ DE TERMINAL SERVER DE \_ \_ SEGURIDAD<br/>        | S-1-5-13<br/>        | Terminal Services. Se agrega automáticamente al token de seguridad de un usuario que inicia sesión en un servidor de terminal.<br/>                                                                                                                                                                                                                                                                                                                                                                                                            |
| RID \_ DEL SISTEMA LOCAL DE \_ \_ SEGURIDAD<br/>           | S-1-5-18<br/>        | Una cuenta especial utilizada por el sistema operativo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| SECURITY \_ NT \_ NON \_ UNIQUE<br/>              | S-1-5-21<br/>        | Los SID no son únicos.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| SECURITY \_ BUILTIN \_ DOMAIN \_ RID<br/>         | S-1-5-32<br/>        | Dominio del sistema integrado.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| RID DE \_ CÓDIGO RESTRINGIDO DE ESCRITURA DE \_ \_ \_ SEGURIDAD<br/> | S-1-5-33<br/>        | Escribir código restringido.<br/> |


 

Los siguientes RID son relativos a cada dominio.



| RID                                                                | Valor       | Identifica                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DOMINIO \_ ALIAS \_ RID \_ CERTSVC \_ DCOM ACCESS \_ \_ GROUP<br/>              | 0x0000023E | El grupo de usuarios que pueden conectarse a entidades de certificación mediante el Modelo de objetos de componentes distribuidos (DCOM).<br/>                                                                                                                          |
| ADMINISTRADOR DE \_ RID DE USUARIO DE \_ \_ DOMINIO<br/>                                      | 0x000001F4 | La cuenta de usuario administrativo de un dominio.<br/>                                                                                                                                                                                              |
| INVITADO DE \_ RID DE USUARIO DE \_ \_ DOMINIO<br/>                                      | 0x000001F5 | La cuenta de usuario invitado en un dominio. Los usuarios que no tienen una cuenta pueden iniciar sesión automáticamente en esta cuenta.<br/>                                                                                                                            |
| ADMINISTRADORES \_ DE RID DE GRUPO DE \_ \_ DOMINIO<br/>                                    | 0x00000200 | Grupo de administradores de dominio. Esta cuenta solo existe en sistemas que ejecutan sistemas operativos de servidor.<br/>                                                                                                                                   |
| USUARIOS DE \_ RID DE GRUPO DE \_ \_ DOMINIO<br/>                                     | 0x00000201 | Grupo que contiene todas las cuentas de usuario de un dominio. Todos los usuarios se agregan automáticamente a este grupo.<br/>                                                                                                                                     |
| INVITADOS \_ DE RID DE GRUPO DE \_ \_ DOMINIO<br/>                                    | 0x00000202 | La cuenta de grupo de invitados de un dominio.<br/>                                                                                                                                                                                                      |
| EQUIPOS RID \_ DE \_ GRUPO DE \_ DOMINIO<br/>                                 | 0x00000203 | Grupo de equipos de dominio. Todos los equipos del dominio son miembros de este grupo.<br/>                                                                                                                                                       |
| CONTROLADORES DE \_ RID DE GRUPO DE \_ \_ DOMINIO<br/>                               | 0x00000204 | Grupo de controladores de dominio. Todos los controladores de dominio del dominio son miembros de este grupo.<br/>                                                                                                                                                           |
| ADMINISTRADORES \_ DE CERTIFICADOS RID DE GRUPO DE \_ \_ \_ DOMINIO<br/>                              | 0x00000205 | Grupo de publicadores de certificados. Los equipos que ejecutan Servicios de certificados son miembros de este grupo.<br/>                                                                                                                                      |
| CONTROLADORES DE DOMINIO DE SOLO LECTURA DE ENTERPRISE RID \_ \_ DE GRUPO DE \_ \_ \_ \_ DOMINIO<br/> | 0x000001F2 | Grupo de controladores de dominio de solo lectura empresariales.<br/>                                                                                                                                                                                     |
| ADMINISTRADORES \_ DE ESQUEMAS RID DE GRUPO DE \_ \_ \_ DOMINIO<br/>                            | 0x00000206 | Grupo de administradores de esquema. Los miembros de este grupo pueden modificar el esquema de Active Directory.<br/>                                                                                                                                           |
| ADMINISTRADORES \_ DE LA EMPRESA DE RID DE GRUPO DE \_ \_ \_ DOMINIO<br/>                        | 0x00000207 | El grupo de administradores de empresa. Los miembros de este grupo tienen acceso total a todos los dominios del Active Directory de datos. Enterprise administradores son responsables de las operaciones de nivel de bosque, como agregar o quitar nuevos dominios.<br/> |
| ADMINISTRADORES \_ DE DIRECTIVAS DE RID DE GRUPO DE \_ \_ \_ DOMINIO<br/>                            | 0x00000208 | Grupo de administradores de directivas.<br/>                                                                                                                                                                                                         |
| CONTROLADORES \_ DE SOLO LECTURA DE RID DE GRUPO DE \_ \_ \_ DOMINIO<br/>                     | 0x00000209 | Grupo de controladores de dominio de solo lectura.<br/>                                                                                                                                                                                                |                                             
| CONTROLADORES \_ CLONABLES \_ DE RID DE GRUPO DE \_ \_ DOMINIO<br />                   | 0x0000020A | Grupo de controladores de dominio clonables.<br/>                                                                                                                                                                                                |
| RID DE \_ GRUPO \_ DE DOMINIO \_ RESERVADO \_<br />                            | 0x0000020C | Grupo CDC reservado.<br/>                                                                                                                                                                                                                   |
| USUARIOS \_ PROTEGIDOS POR RID DE GRUPO DE \_ \_ \_ DOMINIO<br />                         | 0x0000020D | Grupo de usuarios protegidos.</br>                                                                                                                                                                                                                |
| ADMINISTRADORES \_ DE CLAVES DE RID DE GRUPO DE \_ \_ \_ DOMINIO<br />                              | 0x0000020E | El grupo de administradores de claves.<br/>                                                                                                                                                                                                                     |
| ADMINISTRADORES \_ DE \_ CLAVES EMPRESARIALES DE RID \_ DE GRUPO DE \_ \_ DOMINIO<br />                  | 0x0000020F | El grupo de administradores de claves empresariales</br>                                                                                                                                                                                                           |



 

Los siguientes RID se usan para especificar el nivel de integridad obligatorio.



| RID                                                     | Valor                                               | Identifica                        |
|---------------------------------------------------------|-----------------------------------------------------|-----------------------------------|
| RID \_ OBLIGATORIO DE SEGURIDAD QUE NO ES DE \_ \_ CONFIANZA<br/>          | 0x00000000<br/>                               | Untrusted.<br/>             |
| RID \_ BAJO OBLIGATORIO DE \_ \_ SEGURIDAD<br/>                | 0x00001000<br/>                               | Integridad baja.<br/>         |
| RID \_ MEDIO OBLIGATORIO DE \_ \_ SEGURIDAD<br/>             | 0x00002000<br/>                               | Integridad media.<br/>      |
| MEDIO \_ OBLIGATORIO DE SEGURIDAD MÁS \_ \_ \_ RID<br/>       | RID \_ MEDIO OBLIGATORIO DE SEGURIDAD + \_ \_ 0x100<br/> | Integridad media alta.<br/> |
| RID \_ ALTO OBLIGATORIO DE \_ \_ SEGURIDAD<br/>               | 0X00003000<br/>                               | Alta integridad.<br/>        |
| RID \_ OBLIGATORIO DEL SISTEMA DE \_ \_ SEGURIDAD<br/>             | 0x00004000<br/>                               | Integridad del sistema.<br/>      |
| RID \_ DE PROCESO PROTEGIDO OBLIGATORIO DE \_ \_ \_ SEGURIDAD<br/> | 0x00005000<br/>                               | Proceso protegido.<br/>     |



 

En la tabla siguiente se incluyen ejemplos de RID relativos al dominio que puede usar para formar SID conocidos para grupos locales (alias). Para obtener más información sobre los grupos locales y globales, vea [Funciones de grupo local](/windows/desktop/NetMgmt/local-group-functions) y Funciones de [grupo](/windows/desktop/NetMgmt/group-functions).



| RID                                                              | Value                 |Valor de cadena  | Identifica                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------|-----------------|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ADMINISTRADORES \_ DE RID DE ALIAS DE \_ \_ DOMINIO<br/>                            | 0x00000220<br/> | S-1-5-32-544<br/> | Grupo local que se usa para la administración del dominio.<br/>                                                                                                                                                                                                                            |
| USUARIOS \_ DE RID DE ALIAS DE \_ \_ DOMINIO<br/>                             | 0x00000221<br/> | S-1-5-32-545<br/> | Grupo local que representa a todos los usuarios del dominio.<br/>                                                                                                                                                                                                                          |
| INVITADOS \_ DE RID DE ALIAS DE \_ \_ DOMINIO<br/>                            | 0x00000222<br/> | S-1-5-32-546<br/> | Grupo local que representa a los invitados del dominio.<br/>                                                                                                                                                                                                                             |
| USUARIOS \_ AVANZADOS \_ DE RID DE ALIAS \_ DE \_ DOMINIO<br/>                      | 0x00000223<br/> | S-1-5-32-547<br/> | Un grupo local que se usa para representar un usuario o un conjunto de usuarios que esperan tratar un sistema como si fuera su equipo personal en lugar de como una estación de trabajo para varios usuarios.<br/>                                                                                                      |
| OPERACIONES DE \_ CUENTA DE RID DE ALIAS DE \_ \_ \_ DOMINIO<br/>                      | 0x00000224<br/> | S-1-5-32-548<br/> | Un grupo local que solo existe en sistemas que ejecutan sistemas operativos de servidor. Este grupo local permite el control sobre las cuentas que no son administradores.<br/>                                                                                                                                    |
| OPERACIONES DEL \_ SISTEMA DE RID DE ALIAS DE \_ \_ \_ DOMINIO<br/>                       | 0x00000225<br/> | S-1-5-32-549<br/> | Un grupo local que solo existe en sistemas que ejecutan sistemas operativos de servidor. Este grupo local realiza funciones administrativas del sistema, sin incluir las funciones de seguridad. Establece recursos compartidos de red, controla impresoras, desbloquea estaciones de trabajo y realiza otras operaciones.<br/> |
| OPERACIONES DE \_ IMPRESIÓN DE RID DE ALIAS DE \_ \_ \_ DOMINIO<br/>                        | 0x00000226<br/> | S-1-5-32-550<br/> | Un grupo local que solo existe en sistemas que ejecutan sistemas operativos de servidor. Este grupo local controla las impresoras y las colas de impresión.<br/>                                                                                                                                                |
| OPERACIONES DE \_ COPIA DE SEGURIDAD DE RID DE ALIAS DE \_ \_ \_ DOMINIO<br/>                       | 0x00000227<br/> | S-1-5-32-551<br/> | Grupo local que se usa para controlar la asignación de privilegios de copia de seguridad y restauración de archivos.<br/>                                                                                                                                                                                            |
| REPLICADOR \_ DE RID DE ALIAS DE \_ \_ DOMINIO<br/>                        | 0x00000228<br/> | S-1-5-32-552<br/> | Un grupo local responsable de copiar las bases de datos de seguridad desde el controlador de dominio principal a los controladores de dominio de copia de seguridad. El sistema solo usa estas cuentas.<br/>                                                                                                       |
| SERVIDORES \_ \_ RAS DE RID DE ALIAS \_ DE \_ DOMINIO<br/>                      | 0x00000229<br/> | S-1-5-32-553<br/> | Un grupo local que representa los servidores RAS e IAS. Este grupo permite el acceso a varios atributos de objetos de usuario.<br/>                                                                                                                                                             |
| RID \_ DE ALIAS DE DOMINIO \_ \_ PREW2KCOMPACCESS<br/>                  | 0x0000022A<br/> | S-1-5-32-554<br/> | Grupo local que solo existe en sistemas que ejecutan Windows 2000 Server. Para obtener más información, [vea Permitir el acceso anónimo.](allowing-anonymous-access.md)<br/>                                                                                                                    |
| USUARIOS DE \_ ESCRITORIO REMOTO DE RID DE ALIAS DE \_ \_ \_ \_ DOMINIO<br/>            | 0x0000022B<br/> | S-1-5-32-555<br/> | Un grupo local que representa a todos los usuarios de Escritorio remoto.<br/>                                                                                                                                                                                                                         |
| OPERACIONES DE \_ CONFIGURACIÓN DE RED DE RID DE ALIAS DE \_ \_ \_ \_ DOMINIO<br/>       | 0x0000022C<br/> | S-1-5-32-556<br/> | Grupo local que representa la configuración de red. <br/>                                                                                                                                                                                                                       |
| GENERADORES DE CONFIANZA DE BOSQUE ENTRANTE DE RID DE ALIAS \_ \_ DE \_ \_ \_ \_ DOMINIO<br/> | 0x0000022D<br/> | S-1-5-32-557<br/> | Un grupo local que representa cualquier usuario de confianza de bosque.<br/>                                                                                                                                                                                                                           |
| USUARIOS DE \_ SUPERVISIÓN DE RID DE ALIAS DE \_ \_ \_ DOMINIO<br/>                 | 0x0000022E<br/> | S-1-5-32-558<br/> | Un grupo local que representa todos los usuarios que se supervisan.<br/>                                                                                                                                                                                                                        |
| USUARIOS DE \_ REGISTRO DE RID DE ALIAS DE \_ \_ \_ DOMINIO<br/>                    | 0x0000022F<br/> | S-1-5-32-559<br/> | Un grupo local responsable de registrar a los usuarios.<br/>                                                                                                                                                                                                                                    |
| AUTORIZACIÓN \_ DE RID DE ALIAS DE \_ \_ DOMINIOACCESO<br/>               | 0x00000230<br/> | S-1-5-32-560<br/> | Grupo local que representa todo el acceso autorizado.<br/>                                                                                                                                                                                                                            |
| SERVIDORES \_ DE LICENCIAS DE \_ TS DE RID \_ DE ALIAS DE \_ \_ DOMINIO<br/>              | 0x00000231<br/> | S-1-5-32-561<br/> | Un grupo local que solo existe en sistemas que ejecutan sistemas operativos de servidor que permiten servicios terminales y acceso remoto.<br/>                                                                                                                                                  |
| USUARIOS \_ \_ DCOM DE RID DE ALIAS \_ DE \_ DOMINIO<br/>                       | 0x00000232<br/> | S-1-5-32-562<br/> | Un grupo local que representa a los usuarios que pueden usar el Modelo de objetos componentes distribuidos (DCOM).<br/>                                                                                                                                                                                      |
| \_IUSERS DE RID DE ALIAS DE \_ \_ DOMINIO<br/>                            | 0X00000238<br/> | S-1-5-32-568<br/> | Un grupo local que representa a los usuarios de Internet.<br/>                                                                                                                                                                                                                                   |
| OPERADORES \_ \_ CRIPTOGRÁFICOS DE RID DE ALIAS \_ \_ DE DOMINIO<br/>                 | 0x00000239<br/> | S-1-5-32-569<br/> | Un grupo local que representa el acceso a los operadores de criptografía.<br/>                                                                                                                                                                                                                 |
| GRUPO DE \_ ENTIDADES DE \_ SEGURIDAD \_ \_ ALMACENABLES EN \_ CACHÉ DE ALIAS DE DOMINIO<br/>      | 0x0000023B<br/> | S-1-5-32-571<br/> | Grupo local que representa entidades de seguridad que se pueden almacenar en caché.<br/>                                                                                                                                                                                                                    |
| GRUPO DE ENTIDADES DE SEGURIDAD \_ \_ NO \_ \_ \_ ALMACENABLES EN CACHÉ \_ DE ALIAS DE DOMINIO<br/> | 0x0000023C<br/> | S-1-5-32-572<br/> | Grupo local que representa entidades de seguridad que no se pueden almacenar en caché.<br/>                                                                                                                                                                                                                 |
| GRUPO DE LECTORES DEL REGISTRO DE EVENTOS RID DE ALIAS \_ \_ DE \_ \_ \_ \_ DOMINIO<br/>        | 0x0000023D<br/> | S-1-5-32-573<br/> | Un grupo local que representa los lectores del registro de eventos.<br/>                                                                                                                                                                                                                                |
| DOMINIO \_ ALIAS \_ RID \_ CERTSVC \_ DCOM ACCESS \_ \_ GROUP<br/>      | 0x0000023E<br/> | S-1-5-32-574<br/> | Grupo local de usuarios que pueden conectarse a entidades de certificación mediante el Modelo de objetos de componentes distribuidos (DCOM).<br/>                                                                                                                                                          |
| SERVIDORES DE \_ ACCESO REMOTO DE RDS DE RID DE ALIAS DE \_ \_ \_ \_ \_ DOMINIO<br />     | 0x0000023F<br/> | S-1-5-32-575<br/> | Un grupo local que representa los servidores de acceso remoto de RDS.<br/> |
| SERVIDORES DE \_ PUNTOS DE CONEXIÓN RDS DE RID DE ALIAS DE \_ \_ \_ \_ DOMINIO                 | 0x00000240<br/> | S-1-5-32-576<br/> | Un grupo local que representa los servidores de puntos de conexión.<br/> |
| SERVIDORES DE \_ ADMINISTRACIÓN DE RDS DE RID DE ALIAS DE \_ \_ \_ \_ DOMINIO               | 0x00000241<br/> | S-1-5-32-577<br/> | Un grupo local que representa los servidores de administración. <br/>|
| ADMINISTRADORES DE HYPER V DE \_ RID DE ALIAS DE \_ \_ \_ \_ DOMINIO                       | 0x00000242<br/> | S-1-5-32-578<br/> | Un grupo local que representa a los administradores de Hyper-V <br/>|
| OPERACIONES DE \_ ASISTENCIA PARA EL CONTROL DE ACCESO DE RID DE ALIAS DE \_ \_ \_ \_ \_ DOMINIO       | 0x00000243<br/> | S-1-5-32-579<br/> | Un grupo local que representa la asistencia de control de acceso OPS.<br/> |
| USUARIOS DE \_ ADMINISTRACIÓN REMOTA DE RID DE ALIAS DE \_ \_ \_ \_ DOMINIO              | 0x00000244<br/> | S-1-5-32-580<br/> | Un grupo local que representa a los usuarios de administración remota. <br/>|
| CUENTA \_ PREDETERMINADA DE RID DE ALIAS DE \_ \_ \_ DOMINIO                       | 0x00000245<br/> | S-1-5-32-581<br/> | Grupo local que representa la cuenta predeterminada. <br/>|
| ADMINISTRADORES \_ DE \_ RÉPLICAS DE ALMACENAMIENTO DE RID DE ALIAS \_ \_ DE \_ DOMINIO               | 0x00000246<br/> | S-1-5-32-582<br/> | Un grupo local que representa a los administradores de réplicas de almacenamiento. <br/>|
| PROPIETARIOS \_ DE \_ DISPOSITIVOS RID DE ALIAS \_ DE \_ DOMINIO                            | 0x00000247<br/> | S-1-5-32-583<br/> | Un grupo local que representa puede hacer que la configuración sea esperada para los propietarios de dispositivos.<br/>|


 

La [**\_ enumeración WELL KNOWN \_ SID \_ TYPE**](/windows/desktop/api/Winnt/ne-winnt-well_known_sid_type) define la lista de SID usados habitualmente. Además, el Lenguaje de definición [de descriptores](security-descriptor-definition-language.md) de seguridad (SDDL) usa [cadenas SID](sid-strings.md) para hacer referencia a SID conocidos en un formato de cadena.

 

