---
title: Atributos de seguridad del usuario
description: Además de asignar nombres a las propiedades de los objetos de usuario, por ejemplo, objectGUID, objectSid, cn, distinguishedName, entre otras, hay otras propiedades de seguridad que se usan para el inicio de sesión, el acceso a la red y el control de acceso.
ms.assetid: eeb16938-4380-4622-804f-6b2ff19aa68d
ms.tgt_platform: multiple
keywords:
- Atributos de seguridad, mediante AD
- Atributos de seguridad de usuario ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dfe23252002f2ffbbba3f8e8a8faf5a2d36ce348bdbd7503c0d99a816a81902
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024893"
---
# <a name="user-security-attributes"></a>Atributos de seguridad del usuario

Además de asignar nombres a las propiedades de los objetos de usuario, por ejemplo, [**objectGUID**](/windows/desktop/ADSchema/a-objectguid), [**objectSid**](/windows/desktop/ADSchema/a-objectsid), [**cn**](/windows/desktop/ADSchema/a-cn), [**distinguishedName,**](/windows/desktop/ADSchema/a-distinguishedname)y así sucesivamente, hay otras propiedades de seguridad que se usan para el inicio de sesión, el acceso a la red y el control de acceso. El sistema de seguridad Windows 2000 usa estas propiedades. Estas propiedades se pueden ver y administrar mediante el complemento Active Directory usuario y equipos.

<dl> <dt>

<span id="accountExpires"></span><span id="accountexpires"></span><span id="ACCOUNTEXPIRES"></span>[**accountExpires**](/windows/desktop/ADSchema/a-accountexpires)
</dt> <dd>

El [**atributo accountExpires**](/windows/desktop/ADSchema/a-accountexpires) especifica cuándo expira una cuenta. Este valor se almacena como un entero grande que representa el número de intervalos de 100 nanosegundos desde el 1 de enero de 1601 (UTC). Un valor de **TIMEQ \_ FOREVER** (definido en Lmaccess.h) indica que una cuenta nunca expira.

</dd> <dt>

<span id="altSecurityIdentities"></span><span id="altsecurityidentities"></span><span id="ALTSECURITYIDENTITIES"></span>[**altSecurityIdentities**](/windows/desktop/ADSchema/a-altsecurityidentities)
</dt> <dd>

El [**atributo altSecurityIdentities**](/windows/desktop/ADSchema/a-altsecurityidentities) es un atributo multivalor que contiene asignaciones de certificados X.509 o cuentas de usuario kerberos externas a este usuario para la autenticación. Varios paquetes de seguridad, incluidos el paquete de autenticación de clave pública y Kerberos, usan estos datos para autenticar a los usuarios cuando presentan la forma alternativa de identificación, como certificado, UNIX vale Kerberos, y así sucesivamente. Compile un token Windows 2000 basado en la cuenta de usuario correspondiente para que pueda acceder a los recursos del sistema.

En el caso de los certificados X.509, los valores deben ser los nombres issuer y Subject en los certificados 509v3, emitidos por una entidad de certificación pública externa, que se asignan a la cuenta de usuario usada para buscar una cuenta para la autenticación. El paquete SSL (Schannel) usa la sintaxis siguiente: X509: <somecertinfotype> somecertinfo. Por ejemplo, el siguiente valor especifica el DN emisor " " con el \<I\> DN "C=US,O=InternetCA,CN=APublicCertificateAuthority" y el DN sujeto " " con el \<S\> DN "C=US,O=Fabrikam,OU=Sales,CN=Jeff Smith".


```C++
X509:<I>C=US,O=InternetCA,CN=APublicCertificateAuthority<S>C=US,O=Fabrikam,OU=Sales,CN=Jeff Smith
```



Tenga en cuenta que \<S\> se admiten " " o \<I> " " y " " \<S\> . No se admite \<I\> tener solo "". Las aplicaciones no deben modificar los valores de " " o " " porque no se admite la coincidencia \<I\> \<S\> de DN parcial.

En el caso de las cuentas de Kerberos externas, los valores deben ser el nombre de la cuenta kerberos. El paquete kerberos usa la siguiente sintaxis: "Kerberos:MITaccountname". Por ejemplo, el siguiente es el valor de una cuenta en Fabrikam.com:


```C++
Kerberos:Jeff.Smith@Fabrikam.com
```



</dd> <dt>

<span id="badPasswordTime"></span><span id="badpasswordtime"></span><span id="BADPASSWORDTIME"></span>[**badPasswordTime**](/windows/desktop/ADSchema/a-badpasswordtime)
</dt> <dd>

No replicado. El [**atributo badPasswordTime**](/windows/desktop/ADSchema/a-badpasswordtime) especifica la última vez que el usuario intentó iniciar sesión en la cuenta con una contraseña incorrecta. Este valor se almacena como un entero grande que representa el número de intervalos de 100 nanosegundos desde el 1 de enero de 1601 (UTC). Este atributo se mantiene por separado en cada controlador de dominio del dominio. Un valor de cero significa que se desconoce la hora de la última contraseña incorrecta. Para obtener un valor preciso para la hora de la última contraseña incorrecta del usuario en el dominio, se debe consultar cada controlador de dominio del dominio y se debe usar el valor más grande.

</dd> <dt>

<span id="badPwdCount"></span><span id="badpwdcount"></span><span id="BADPWDCOUNT"></span>[**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount)
</dt> <dd>

No replicado. El [**atributo badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount) especifica el número de veces que el usuario intentó iniciar sesión en la cuenta con una contraseña incorrecta. Este atributo se mantiene por separado en cada controlador de dominio del dominio. Un valor de 0 indica que el valor es desconocido. Para obtener un valor preciso para el total de intentos de contraseña incorrecta del usuario en el dominio, se debe consultar cada controlador de dominio del dominio y se debe usar la suma de los valores.

</dd> <dt>

<span id="codePage"></span><span id="codepage"></span><span id="CODEPAGE"></span>[**Codepage**](/windows/desktop/ADSchema/a-codepage)
</dt> <dd>

El [**atributo codePage**](/windows/desktop/ADSchema/a-codepage) especifica la página de códigos para el idioma elegido del usuario. Este valor no lo usa Windows 2000.

</dd> <dt>

<span id="countryCode"></span><span id="countrycode"></span><span id="COUNTRYCODE"></span>[**countryCode**](/windows/desktop/ADSchema/a-countrycode)
</dt> <dd>

El [**atributo countryCode**](/windows/desktop/ADSchema/a-countrycode) especifica el código de país o región para el idioma del usuario. Este valor no lo usa Windows 2000.

</dd> <dt>

<span id="homeDirectory"></span><span id="homedirectory"></span><span id="HOMEDIRECTORY"></span>[**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory)
</dt> <dd>

El [**atributo homeDirectory**](/windows/desktop/ADSchema/a-homedirectory) especifica la ruta de acceso del directorio principal del usuario. La cadena puede ser NULL.

Si [**homeDrive**](/windows/desktop/ADSchema/a-homedrive) está establecido y especifica una letra de unidad, [**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory) debe ser una ruta de acceso UNC. La ruta de acceso debe ser una ruta de acceso UNC de red del directorio del recurso \\ \\ compartido del servidor de \\ \\ formularios. Este valor puede ser una cadena nula.

Si [**homeDrive**](/windows/desktop/ADSchema/a-homedrive) no está establecido, [**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory) debe ser una ruta de acceso local, por ejemplo, C: \\ mylocaldir.

</dd> <dt>

<span id="homeDrive"></span><span id="homedrive"></span><span id="HOMEDRIVE"></span>[**homeDrive**](/windows/desktop/ADSchema/a-homedrive)
</dt> <dd>

El [**atributo homeDrive**](/windows/desktop/ADSchema/a-homedrive) especifica la letra de unidad a la que se asignará la ruta de acceso UNC especificada por **homeDirectory**. La letra de unidad debe especificarse con el formato siguiente:


```C++
<drive letter>:
```



donde " \<drive letter\> " es la letra de la unidad que se va a asignar. Por ejemplo:


```C++
Z:
```



Si no se establece este atributo, [**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory) debe ser una ruta de acceso local, por ejemplo, C: \\ mylocaldir.

</dd> <dt>

<span id="lastLogoff"></span><span id="lastlogoff"></span><span id="LASTLOGOFF"></span>[**lastLogoff**](/windows/desktop/ADSchema/a-lastlogoff)
</dt> <dd>

No replicado. El [**atributo lastLogoff**](/windows/desktop/ADSchema/a-lastlogoff) especifica cuándo se produjo el último cierre de sesión. Este valor se almacena como un entero grande que representa el número de intervalos de 100 nanosegundos desde el 1 de enero de 1601 (UTC). La parte alta de este entero grande corresponde al miembro **dwHighDateTime** de la estructura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) y la parte baja corresponde al miembro **dwLowDateTime** de la estructura **FILETIME.** Este atributo se mantiene por separado en cada controlador de dominio del dominio. Un valor de cero significa que se desconoce la última hora de cierre de sesión. Para obtener un valor preciso para el último cierre de sesión del usuario en el dominio, se debe consultar cada controlador de dominio del dominio y se debe usar el valor más grande.

</dd> <dt>

<span id="lastLogon"></span><span id="lastlogon"></span><span id="LASTLOGON"></span>[**lastLogon**](/windows/desktop/ADSchema/a-lastlogon)
</dt> <dd>

No replicado. El [**atributo lastLogon**](/windows/desktop/ADSchema/a-lastlogon) especifica cuándo se produjo el último inicio de sesión. Este valor se almacena como un entero grande que representa el número de intervalos de 100 nanosegundos desde el 1 de enero de 1601 (UTC). La parte alta de este entero grande corresponde al miembro **dwHighDateTime** de la estructura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) y la parte baja corresponde al miembro **dwLowDateTime** de la estructura **FILETIME.** Este atributo se mantiene por separado en cada controlador de dominio del dominio. Un valor de cero significa que se desconoce la hora del último inicio de sesión. Para obtener un valor preciso para el último inicio de sesión del usuario en el dominio, se debe consultar cada controlador de dominio del dominio y se debe usar el valor más grande.

</dd> <dt>

<span id="lmPwdHistory"></span><span id="lmpwdhistory"></span><span id="LMPWDHISTORY"></span>[**lmPwdHistory**](/windows/desktop/ADSchema/a-lmpwdhistory)
</dt> <dd>

El [**atributo lmPwdHistory**](/windows/desktop/ADSchema/a-lmpwdhistory) es el historial de contraseñas del usuario en formato unívivo (OWF) de LAN Manager (LM). Lm OWF se usa para la compatibilidad con clientes de LAN Manager 2.x, Windows 95 y Windows 98. Este atributo solo lo usa el sistema operativo. Tenga en cuenta que no puede derivar la contraseña de texto no cifrado del formulario OWF de la contraseña.

</dd> <dt>

<span id="logonCount"></span><span id="logoncount"></span><span id="LOGONCOUNT"></span>[**logonCount**](/windows/desktop/ADSchema/a-logoncount)
</dt> <dd>

No replicado. El [**atributo logonCount**](/windows/desktop/ADSchema/a-logoncount) cuenta el número de veces que el usuario intentó iniciar sesión en esta cuenta. Este atributo se mantiene en cada controlador de dominio del dominio. Un valor de 0 indica que el valor es desconocido. Para obtener un valor preciso para el número total de intentos de inicio de sesión correctos del usuario en el dominio, se debe consultar cada controlador de dominio del dominio y se debe usar la suma de los valores.

</dd> <dt>

<span id="mail"></span><span id="MAIL"></span>[**Correo**](/windows/desktop/ADSchema/a-mail)
</dt> <dd>

El [**atributo mail**](/windows/desktop/ADSchema/a-mail) es un atributo de un solo valor que contiene la dirección SMTP del usuario, por ejemplo, " jeff@Fabrikam.com ".

</dd> <dt>

<span id="maxStorage"></span><span id="maxstorage"></span><span id="MAXSTORAGE"></span>[**maxStorage**](/windows/desktop/ADSchema/a-maxstorage)
</dt> <dd>

El [**atributo maxStorage**](/windows/desktop/ADSchema/a-maxstorage) especifica la cantidad máxima de espacio en disco duro que el usuario puede usar. Use el **valor \_ USER MAXSTORAGE \_ UNLIMITED** (definido en Lmaccess.h) para usar todo el espacio en disco disponible.

</dd> <dt>

<span id="memberOf"></span><span id="memberof"></span><span id="MEMBEROF"></span>[**Miembro**](/windows/desktop/ADSchema/a-memberof)
</dt> <dd>

El [**atributo memberOf**](/windows/desktop/ADSchema/a-memberof) es un atributo de varios valores que contiene grupos de los que el usuario es miembro directo, excepto para el grupo principal, representado por [**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid). La pertenencia a grupos depende del controlador de dominio (DC) del que se recupera este atributo:

-   En un controlador de dominio para el dominio que contiene el usuario, [**memberOf**](/windows/desktop/ADSchema/a-memberof) para el usuario se completa con respecto a la pertenencia a grupos de ese dominio; sin embargo, **memberOf** no contiene la pertenencia del usuario a grupos locales y globales del dominio en otros dominios.
-   En un servidor GC, [**memberOf**](/windows/desktop/ADSchema/a-memberof) para el usuario se completa con respecto a todas las pertenencias a grupos universales.

Si se cumplen ambas condiciones para el controlador de dominio, ambos conjuntos de datos se incluyen en [**memberOf**](/windows/desktop/ADSchema/a-memberof).

Tenga en cuenta que este atributo enumera los grupos que contienen el usuario en su atributo de miembro; no contiene la lista recursiva de predecesores anidados. Por ejemplo, si el usuario O es miembro del grupo C y los grupos B y B estaban anidados en el grupo A, el atributo [**memberOf**](/windows/desktop/ADSchema/a-memberof) del usuario O enumeraría el grupo C y el grupo B, pero no el grupo A.

Este atributo no se almacena, es un atributo back-link calculado.

</dd> <dt>

<span id="ntPwdHistory"></span><span id="ntpwdhistory"></span><span id="NTPWDHISTORY"></span>[**ntPwdHistory**](/windows/desktop/ADSchema/a-ntpwdhistory)
</dt> <dd>

El [**atributo ntPwdHistory**](/windows/desktop/ADSchema/a-ntpwdhistory) es el historial de contraseñas del usuario en Windows nt un way format (OWF). Windows 2000 usa el Windows NT OWF. Este atributo solo lo usa el sistema operativo. Tenga en cuenta que no puede volver a derivar la contraseña de texto no cifrado del formulario OWF de la contraseña.

</dd> <dt>

<span id="otherMailbox"></span><span id="othermailbox"></span><span id="OTHERMAILBOX"></span>[**otherMailbox**](/windows/desktop/ADSchema/a-othermailbox)
</dt> <dd>

El [**otro atributoMailbox**](/windows/desktop/ADSchema/a-othermailbox) es un atributo de varios valores que contiene otras direcciones de correo adicionales en un formulario, por ejemplo, "CCMAIL: JeffSmith".

</dd> <dt>

<span id="PasswordExpirationDate"></span><span id="passwordexpirationdate"></span><span id="PASSWORDEXPIRATIONDATE"></span>[**PasswordExpirationDate**](/windows/desktop/ADSI/iadsuser-property-methods)
</dt> <dd>

La fecha de expiración de la contraseña no es un atributo en el objeto de usuario. Es un valor calculado basado en la suma de [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset) para el usuario y [**maxPwdAge**](/windows/desktop/ADSchema/a-maxpwdage) del dominio del usuario. Para obtener la fecha de expiración de la contraseña, obtenga la propiedad [**IADsUser.PasswordExpirationDate.**](/windows/desktop/ADSI/iadsuser-property-methods) No se puede modificar este atributo para un usuario; en su lugar, establezca [**la propiedad IADsDomain.MaxPasswordAge**](/windows/desktop/ADSI/iadsdomain-property-methods) para cambiar la configuración del dominio.

</dd> <dt>

<span id="primaryGroupID"></span><span id="primarygroupid"></span><span id="PRIMARYGROUPID"></span>[**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid)
</dt> <dd>

El [**atributo primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid) es un atributo de un solo valor que contiene [**primaryGroupToken**](/windows/desktop/ADSchema/a-primarygrouptoken) del grupo que es el grupo principal del objeto. El grupo principal del objeto no se incluye en el [**atributo memberOf.**](/windows/desktop/ADSchema/a-memberof) Por ejemplo, de forma predeterminada, el grupo principal de un objeto de usuario es **primaryGroupToken** del grupo Usuarios del dominio, pero el grupo Usuarios del dominio no forma parte del atributo **memberOf** del objeto de usuario.

</dd> <dt>

<span id="profilePath"></span><span id="profilepath"></span><span id="PROFILEPATH"></span>[**profilePath**](/windows/desktop/ADSchema/a-profilepath)
</dt> <dd>

El [**atributo profilePath**](/windows/desktop/ADSchema/a-profilepath) especifica una ruta de acceso al perfil del usuario. Este valor puede ser una cadena nula, una ruta de acceso absoluta local o una ruta de acceso UNC.

</dd> <dt>

<span id="pwdLastSet"></span><span id="pwdlastset"></span><span id="PWDLASTSET"></span>[**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset)
</dt> <dd>

El [**atributo pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset) especifica cuándo se cambió la contraseña por última vez. Este valor se almacena como un entero grande que representa el número de intervalos de 100 nanosegundos desde el 1 de enero de 1601 (UTC).

El sistema usa el valor de este atributo y el atributo [**maxPwdAge**](/windows/desktop/ADSchema/a-maxpwdage) del dominio que contiene el objeto de usuario para calcular la fecha de expiración de la contraseña. Es decir, la suma de [**pwdLastSet para**](/windows/desktop/ADSchema/a-pwdlastset) el usuario y **maxPwdAge** del dominio del usuario.

Este atributo controla si el usuario debe cambiar la contraseña cuando el usuario inicia sesión a continuación. Si [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset) es cero, el valor predeterminado, el usuario debe cambiar la contraseña en el siguiente inicio de sesión. El valor -1 indica que el usuario no tiene que cambiar la contraseña en el siguiente inicio de sesión. El sistema establece este valor en -1 después de que el usuario haya establecido la contraseña.

</dd> <dt>

<span id="sAMAccountType"></span><span id="samaccounttype"></span><span id="SAMACCOUNTTYPE"></span>[**sAMAccountType**](/windows/desktop/ADSchema/a-samaccounttype)
</dt> <dd>

El [**atributo sAMAccountType**](/windows/desktop/ADSchema/a-samaccounttype) especifica un entero que representa el tipo de cuenta. El sistema operativo establece esto cuando se crea el objeto .

</dd> <dt>

<span id="scriptPath"></span><span id="scriptpath"></span><span id="SCRIPTPATH"></span>[**scriptPath**](/windows/desktop/ADSchema/a-scriptpath)
</dt> <dd>

El [**atributo scriptPath**](/windows/desktop/ADSchema/a-scriptpath) especifica la ruta de acceso del script de inicio de sesión del usuario, .cmd, .exe o .bat archivo. La cadena puede ser NULL.

</dd> <dt>

<span id="unicodePwd"></span><span id="unicodepwd"></span><span id="UNICODEPWD"></span>[**unicodePwd**](/windows/desktop/ADSchema/a-unicodepwd)
</dt> <dd>

El [**atributo unicodePwd**](/windows/desktop/ADSchema/a-unicodepwd) es la contraseña del usuario.

Para establecer la contraseña de usuario, use el método [**IADsUser.ChangePassword,**](/windows/desktop/api/iads/nf-iads-iadsuser-changepassword) si el script o la aplicación permiten al usuario cambiar su propia contraseña, o bien el método [**IADsUser.SetPassword,**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) si el script o la aplicación permite que un administrador restablezca una contraseña.

Contraseña del usuario en formato un Windows NT un way (OWF). Windows 2000 usa el Windows NT OWF. Este atributo solo lo usa el sistema operativo. Tenga en cuenta que no puede volver a derivar la contraseña de texto no cifrado del formulario OWF de la contraseña.

</dd> <dt>

<span id="userAccountControl"></span><span id="useraccountcontrol"></span><span id="USERACCOUNTCONTROL"></span>[**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol)
</dt> <dd>

El [**atributo userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) especifica marcas que controlan la contraseña, el bloqueo, la deshabilitación o habilitación, el script y el comportamiento del directorio principal del usuario. Este atributo también contiene una marca que indica el tipo de cuenta del objeto. Normalmente, el objeto de usuario tiene el conjunto UF \_ NORMAL \_ ACCOUNT.

Las marcas siguientes se definen en Lmaccess.h.



| Marca                     | Descripción                                                                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SCRIPT DE \_ UF               | Script de inicio de sesión ejecutado. Este valor debe establecerse para LAN Manager 2.0 o Windows NT.                                                                             |
| UF \_ ACCOUNTDISABLE       | La cuenta de usuario está deshabilitada.                                                                                                                                    |
| SE REQUIERE \_ UF \_ HOMEDIR    | Se requiere el directorio principal. Este valor se omite en Windows NT y Windows 2000.                                                                            |
| UF \_ PASSWD \_ NOTREQD      | No se requiere una contraseña.                                                                                                                                         |
| CAMBIO \_ DE CANT PASSWD \_ DE UF \_ | El usuario no puede cambiar la contraseña.                                                                                                                             |
| BLOQUEO \_ DE UF              | La cuenta está bloqueada actualmente. Este valor se puede borrar para desbloquear una cuenta bloqueada previamente. Este valor no se puede usar para bloquear una cuenta bloqueada previamente. |
| UF \_ DONT \_ EXPIRE \_ PASSWD | Representa la contraseña, que nunca debe expirar en la cuenta.                                                                                               |



 

Las marcas siguientes describen el tipo de cuenta. Solo se puede establecer un valor. No se puede cambiar el tipo de cuenta.



| Marca                            | Descripción                                                                                                                                                                                                                                     |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CUENTA \_ NORMAL DE \_ UF             | Se trata de un tipo de cuenta predeterminado que representa un usuario típico.                                                                                                                                                                                  |
| CUENTA DUPLICADA \_ TEMPORAL \_ DE UF \_    | Se trata de una cuenta para los usuarios cuya cuenta principal está en otro dominio. Esta cuenta proporciona acceso de usuario a este dominio, pero no a ningún dominio que confíe en este dominio. El Administrador de usuarios hace referencia a este tipo de cuenta como una cuenta de usuario local. |
| CUENTA DE CONFIANZA \_ DE ESTACIÓN DE TRABAJO DE \_ \_ UF | Se trata de una cuenta de equipo para un servidor Windows NT Workstation/Windows 2000 Professional o Windows NT Server/Windows 2000 que sea miembro de este dominio.                                                                                     |
| CUENTA DE \_ CONFIANZA \_ DEL SERVIDOR \_ UF      | Se trata de una cuenta de equipo para un Windows de dominio de copia de seguridad de NT que es miembro de este dominio.                                                                                                                                           |
| UF \_ INTERDOMAIN \_ TRUST \_ ACCOUNT | Se trata de una cuenta de permiso para confiar en un Windows NT que confía en otros dominios.                                                                                                                                                            |



 

</dd> <dt>

<span id="userCertificate"></span><span id="usercertificate"></span><span id="USERCERTIFICATE"></span>[**Usercertificate**](/windows/desktop/ADSchema/a-usercertificate)
</dt> <dd>

El [**atributo userCertificate**](/windows/desktop/ADSchema/a-usercertificate) es un atributo de varios valores que contiene los certificados X509v3 codificados con DER emitidos al usuario. Tenga en cuenta que este atributo contiene los certificados de clave pública emitidos a este usuario por Microsoft Certificate Service.

</dd> <dt>

<span id="userSharedFolder"></span><span id="usersharedfolder"></span><span id="USERSHAREDFOLDER"></span>[**userSharedFolder**](/windows/desktop/ADSchema/a-usersharedfolder)
</dt> <dd>

El [**atributo userSharedFolder**](/windows/desktop/ADSchema/a-usersharedfolder) especifica una ruta de acceso UNC a la carpeta de documentos compartidos del usuario. La ruta de acceso debe ser una ruta de acceso UNC de red del directorio del recurso \\ \\ compartido del servidor de \\ \\ formularios. Este valor puede ser una cadena nula.

</dd> <dt>

<span id="userWorkstations"></span><span id="userworkstations"></span><span id="USERWORKSTATIONS"></span>[**userWorkstations**](/windows/desktop/ADSchema/a-userworkstations)
</dt> <dd>

El [**atributo userWorkstations**](/windows/desktop/ADSchema/a-userworkstations) es un atributo de un solo valor que contiene los nombres NetBIOS de las estaciones de trabajo desde las que el usuario puede iniciar sesión. Cada nombre NetBIOS está separado por una coma.

Si no se establece ningún valor, esto indica que no hay ninguna restricción. Para deshabilitar los inicios de sesión de todas las estaciones de trabajo en esta cuenta, establezca el valor \_ UF ACCOUNTDISABLE (definido en Lmaccess.h) en [**el atributo userAccountControl.**](/windows/desktop/ADSchema/a-useraccountcontrol)

</dd> </dl>

 

 
