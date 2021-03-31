---
title: Atributos de seguridad del usuario
description: Además de las propiedades de nomenclatura de los objetos de usuario, por ejemplo, objectGUID, objectSid, CN, distinguishedName, etc., hay otras propiedades de seguridad que se usan para el inicio de sesión, el acceso a la red y el control de acceso.
ms.assetid: eeb16938-4380-4622-804f-6b2ff19aa68d
ms.tgt_platform: multiple
keywords:
- Atributos de seguridad, usar AD
- Atributos de seguridad de usuario AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c51000aefdf9ec0f26406607bd781ac4d87b6106
ms.sourcegitcommit: 25bf66769c2087b1a87d6db5930b604cb57e0f98
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/23/2020
ms.locfileid: "103995710"
---
# <a name="user-security-attributes"></a>Atributos de seguridad del usuario

Además de las propiedades de nomenclatura de los objetos de usuario, por ejemplo, [**objectGUID**](/windows/desktop/ADSchema/a-objectguid), [**objectSid**](/windows/desktop/ADSchema/a-objectsid), [**CN**](/windows/desktop/ADSchema/a-cn), [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname), etc., hay otras propiedades de seguridad que se usan para el inicio de sesión, el acceso a la red y el control de acceso. El sistema de seguridad de Windows 2000 utiliza estas propiedades. Estas propiedades pueden verse y administrarse mediante el complemento Active Directory usuarios y equipos.

<dl> <dt>

<span id="accountExpires"></span><span id="accountexpires"></span><span id="ACCOUNTEXPIRES"></span>[**accountExpires**](/windows/desktop/ADSchema/a-accountexpires)
</dt> <dd>

El atributo [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires) especifica cuándo expira una cuenta. Este valor se almacena como un entero grande que representa el número de intervalos de 100 nanosegundos desde el 1 de enero de 1601 (UTC). Un valor de **TIMEQ \_ Forever** (definido en Lmaccess. h) indica que una cuenta nunca expira.

</dd> <dt>

<span id="altSecurityIdentities"></span><span id="altsecurityidentities"></span><span id="ALTSECURITYIDENTITIES"></span>[**altSecurityIdentities**](/windows/desktop/ADSchema/a-altsecurityidentities)
</dt> <dd>

El atributo [**altSecurityIdentities**](/windows/desktop/ADSchema/a-altsecurityidentities) es un atributo con varios valores que contiene las asignaciones de certificados X. 509 o cuentas de usuario de Kerberos externas a este usuario para la autenticación. Varios paquetes de seguridad, incluido el paquete de autenticación de clave pública y Kerberos, usan estos datos para autenticar a los usuarios cuando presentan la forma alternativa de identificación, como el certificado, el vale de Kerberos de UNIX, etc. Cree un token de Windows 2000 basado en la cuenta de usuario correspondiente para que pueda acceder a los recursos del sistema.

En el caso de los certificados X. 509, los valores deben ser el emisor y los nombres de asunto de los certificados 509v3, emitidos por una entidad de certificación pública externa, que se asignan a la cuenta de usuario usada para buscar una cuenta para la autenticación. El paquete SSL (Schannel) usa la siguiente sintaxis: X509: <somecertinfotype> somecertinfo. Por ejemplo, el valor siguiente especifica el DN del emisor " \<I\> " con el DN "c = US, O = InternetCA, CN = APublicCertificateAuthority" y el DN del firmante " \<S\> " con el DN "c = US, o = Fabrikam, ou = sales, CN = Jeff Smith".


```C++
X509:<I>C=US,O=InternetCA,CN=APublicCertificateAuthority<S>C=US,O=Fabrikam,OU=Sales,CN=Jeff Smith
```



Tenga en cuenta que \<S\> se admiten "" o "" \<I> y " \<S\> ". No se admite el uso de " \<I\> ". Las aplicaciones no deben modificar los valores de " \<I\> " o " \<S\> " porque no se admite la coincidencia de DN parcial.

En el caso de las cuentas de Kerberos externas, los valores deben ser el nombre de la cuenta de Kerberos. El paquete de Kerberos utiliza la sintaxis siguiente: "Kerberos: MITaccountname". Por ejemplo, el siguiente es el valor de una cuenta en Fabrikam.com:


```C++
Kerberos:Jeff.Smith@Fabrikam.com
```



</dd> <dt>

<span id="badPasswordTime"></span><span id="badpasswordtime"></span><span id="BADPASSWORDTIME"></span>[**badPasswordTime**](/windows/desktop/ADSchema/a-badpasswordtime)
</dt> <dd>

Sin replicar. El atributo [**badPasswordTime**](/windows/desktop/ADSchema/a-badpasswordtime) especifica la última vez que el usuario intentó iniciar sesión en la cuenta con una contraseña incorrecta. Este valor se almacena como un entero grande que representa el número de intervalos de 100 nanosegundos desde el 1 de enero de 1601 (UTC). Este atributo se mantiene por separado en cada controlador de dominio del dominio. Un valor de cero significa que se desconoce la última hora de contraseña incorrecta. Para obtener un valor exacto de la última hora de contraseña incorrecta del usuario en el dominio, se deben consultar todos los controladores de dominio del dominio y se debe usar el valor más grande.

</dd> <dt>

<span id="badPwdCount"></span><span id="badpwdcount"></span><span id="BADPWDCOUNT"></span>[**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount)
</dt> <dd>

Sin replicar. El atributo [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount) especifica el número de veces que el usuario intentó iniciar sesión en la cuenta con una contraseña incorrecta. Este atributo se mantiene por separado en cada controlador de dominio del dominio. Un valor de 0 indica que el valor es desconocido. Para obtener un valor preciso para los intentos totales de contraseña incorrecta del usuario en el dominio, se deben consultar todos los controladores de dominio del dominio y se debe usar la suma de los valores.

</dd> <dt>

<span id="codePage"></span><span id="codepage"></span><span id="CODEPAGE"></span>[**737**](/windows/desktop/ADSchema/a-codepage)
</dt> <dd>

El atributo [**CodePage**](/windows/desktop/ADSchema/a-codepage) especifica la página de códigos para el idioma elegido por el usuario. Windows 2000 no usa este valor.

</dd> <dt>

<span id="countryCode"></span><span id="countrycode"></span><span id="COUNTRYCODE"></span>[**País**](/windows/desktop/ADSchema/a-countrycode)
</dt> <dd>

El atributo [**CountryCode**](/windows/desktop/ADSchema/a-countrycode) especifica el código de país o región para el idioma del usuario. Windows 2000 no usa este valor.

</dd> <dt>

<span id="homeDirectory"></span><span id="homedirectory"></span><span id="HOMEDIRECTORY"></span>[**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory)
</dt> <dd>

El atributo [**HomeDirectory**](/windows/desktop/ADSchema/a-homedirectory) especifica la ruta de acceso del directorio principal del usuario. La cadena puede ser null.

Si [**HOMEDRIVE**](/windows/desktop/ADSchema/a-homedrive) está establecido y especifica una letra de unidad, [**HomeDirectory**](/windows/desktop/ADSchema/a-homedirectory) debe ser una ruta de acceso UNC. La ruta de acceso debe ser una ruta de acceso UNC de red con el formato \\ \\ servidor \\ recurso compartido \\ directorio. Este valor puede ser una cadena nula.

Si [**HOMEDRIVE**](/windows/desktop/ADSchema/a-homedrive) no se establece, [**HomeDirectory**](/windows/desktop/ADSchema/a-homedirectory) debe ser una ruta de acceso local, por ejemplo, C: \\ mylocaldir.

</dd> <dt>

<span id="homeDrive"></span><span id="homedrive"></span><span id="HOMEDRIVE"></span>[**homeDrive**](/windows/desktop/ADSchema/a-homedrive)
</dt> <dd>

El atributo [**HOMEDRIVE**](/windows/desktop/ADSchema/a-homedrive) especifica la letra de unidad a la que se va a asignar la ruta de acceso UNC especificada por **HomeDirectory**. La letra de unidad debe especificarse de la forma siguiente:


```C++
<drive letter>:
```



donde " \<drive letter\> " es la letra de la unidad que se va a asignar. Por ejemplo:


```C++
Z:
```



Si no se establece este atributo, el valor de [**HomeDirectory**](/windows/desktop/ADSchema/a-homedirectory) debe ser una ruta de acceso local, por ejemplo, C: \\ mylocaldir.

</dd> <dt>

<span id="lastLogoff"></span><span id="lastlogoff"></span><span id="LASTLOGOFF"></span>[**lastLogoff**](/windows/desktop/ADSchema/a-lastlogoff)
</dt> <dd>

Sin replicar. El atributo [**lastLogoff**](/windows/desktop/ADSchema/a-lastlogoff) especifica cuándo se produjo el último cierre de sesión. Este valor se almacena como un entero grande que representa el número de intervalos de 100 nanosegundos desde el 1 de enero de 1601 (UTC). La parte alta de este entero grande corresponde al miembro **dwHighDateTime** de la estructura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) y la parte baja corresponde al miembro **dwLowDateTime** de la estructura **FILETIME** . Este atributo se mantiene por separado en cada controlador de dominio del dominio. Un valor de cero significa que no se conoce la hora del último cierre de sesión. Para obtener un valor exacto del último cierre de sesión del usuario en el dominio, se debe consultar cada controlador de dominio en el dominio y se debe usar el valor más grande.

</dd> <dt>

<span id="lastLogon"></span><span id="lastlogon"></span><span id="LASTLOGON"></span>[**lastLogon**](/windows/desktop/ADSchema/a-lastlogon)
</dt> <dd>

Sin replicar. El atributo [**lastLogon**](/windows/desktop/ADSchema/a-lastlogon) especifica cuándo se produjo el último inicio de sesión. Este valor se almacena como un entero grande que representa el número de intervalos de 100 nanosegundos desde el 1 de enero de 1601 (UTC). La parte alta de este entero grande corresponde al miembro **dwHighDateTime** de la estructura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) y la parte baja corresponde al miembro **dwLowDateTime** de la estructura **FILETIME** . Este atributo se mantiene por separado en cada controlador de dominio del dominio. Un valor de cero significa que la hora del último inicio de sesión es desconocida. Para obtener un valor preciso para el último inicio de sesión del usuario en el dominio, se deben consultar todos los controladores de dominio del dominio y se debe usar el valor más grande.

</dd> <dt>

<span id="lmPwdHistory"></span><span id="lmpwdhistory"></span><span id="LMPWDHISTORY"></span>[**lmPwdHistory**](/windows/desktop/ADSchema/a-lmpwdhistory)
</dt> <dd>

El atributo [**lmPwdHistory**](/windows/desktop/ADSchema/a-lmpwdhistory) es el historial de contraseñas del usuario en formato unidireccional (OWF) de LAN Manager (LM). LM OWF se usa para la compatibilidad con los clientes de LAN Manager 2. x, Windows 95 y Windows 98. Este atributo solo lo utiliza el sistema operativo. Tenga en cuenta que no puede derivar la contraseña de texto no cifrado de la forma OWF de la contraseña.

</dd> <dt>

<span id="logonCount"></span><span id="logoncount"></span><span id="LOGONCOUNT"></span>[**logonCount**](/windows/desktop/ADSchema/a-logoncount)
</dt> <dd>

Sin replicar. El atributo [**logonCount**](/windows/desktop/ADSchema/a-logoncount) cuenta el número de veces que el usuario intentó iniciar sesión en esta cuenta. Este atributo se mantiene en cada controlador de dominio del dominio. Un valor de 0 indica que el valor es desconocido. Para obtener un valor preciso para el número total de intentos de inicio de sesión correctos del usuario en el dominio, se deben consultar todos los controladores de dominio del dominio y se debe usar la suma de los valores.

</dd> <dt>

<span id="mail"></span><span id="MAIL"></span>[**direcciones**](/windows/desktop/ADSchema/a-mail)
</dt> <dd>

El atributo [**mail**](/windows/desktop/ADSchema/a-mail) es un atributo de un solo valor que contiene la dirección SMTP del usuario, por ejemplo, " jeff@Fabrikam.com ".

</dd> <dt>

<span id="maxStorage"></span><span id="maxstorage"></span><span id="MAXSTORAGE"></span>[**maxStorage**](/windows/desktop/ADSchema/a-maxstorage)
</dt> <dd>

El atributo [**maxStorage**](/windows/desktop/ADSchema/a-maxstorage) especifica la cantidad máxima de espacio en la unidad de disco duro que el usuario puede usar. Use el valor de **User \_ MAXSTORAGE \_ Unlimited** (definido en Lmaccess. h) para usar todo el espacio disponible en disco.

</dd> <dt>

<span id="memberOf"></span><span id="memberof"></span><span id="MEMBEROF"></span>[**memberOf**](/windows/desktop/ADSchema/a-memberof)
</dt> <dd>

El atributo [**memberOf**](/windows/desktop/ADSchema/a-memberof) es un atributo multivalor que contiene grupos de los que el usuario es miembro directo, excepto el grupo principal, que se representa mediante [**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid). La pertenencia a grupos depende del controlador de dominio (DC) del que se recupera este atributo:

-   En un controlador de dominio para el dominio que contiene el usuario, el [**miembro**](/windows/desktop/ADSchema/a-memberof) del usuario está completo con respecto a la pertenencia a los grupos de ese dominio; sin embargo, **memberOf** no contiene la pertenencia del usuario a los grupos locales de dominio y globales de otros dominios.
-   En un servidor de GC, el [**miembro**](/windows/desktop/ADSchema/a-memberof) del usuario está completo con respecto a todas las pertenencias a grupos universales.

Si ambas condiciones se cumplen para el controlador de dominio, ambos conjuntos de datos se incluyen en [**memberOf**](/windows/desktop/ADSchema/a-memberof).

Tenga en cuenta que este atributo muestra los grupos que contienen el usuario en su atributo miembro; no contiene la lista recursiva de predecesoras anidadas. Por ejemplo, si el usuario O es miembro del grupo C y el grupo b y el grupo B estuvieran anidados en el grupo A, el atributo [**memberOf**](/windows/desktop/ADSchema/a-memberof) del usuario O mostraría el grupo C y el grupo b, pero no el grupo a.

Este atributo no se almacena, es un atributo de vínculo de retroceso calculado.

</dd> <dt>

<span id="ntPwdHistory"></span><span id="ntpwdhistory"></span><span id="NTPWDHISTORY"></span>[**ntPwdHistory**](/windows/desktop/ADSchema/a-ntpwdhistory)
</dt> <dd>

El atributo [**ntPwdHistory**](/windows/desktop/ADSchema/a-ntpwdhistory) es el historial de contraseñas del usuario en formato unidireccional (OWF) de Windows NT. Windows 2000 usa las OWF de Windows NT. Este atributo solo lo utiliza el sistema operativo. Tenga en cuenta que no puede volver a derivar la contraseña de texto no cifrado de la forma OWF de la contraseña.

</dd> <dt>

<span id="otherMailbox"></span><span id="othermailbox"></span><span id="OTHERMAILBOX"></span>[**otherMailbox**](/windows/desktop/ADSchema/a-othermailbox)
</dt> <dd>

El atributo [**otherMailbox**](/windows/desktop/ADSchema/a-othermailbox) es un atributo con varios valores que contiene otras direcciones de correo adicionales en un formulario, por ejemplo, "CCMAIL: juanpérez".

</dd> <dt>

<span id="PasswordExpirationDate"></span><span id="passwordexpirationdate"></span><span id="PASSWORDEXPIRATIONDATE"></span>[**PasswordExpirationDate**](/windows/desktop/ADSI/iadsuser-property-methods)
</dt> <dd>

La fecha de expiración de la contraseña no es un atributo del objeto de usuario. Es un valor calculado basado en la suma de [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset) para el usuario y [**maxPwdAge**](/windows/desktop/ADSchema/a-maxpwdage) del dominio del usuario. Para obtener la fecha de expiración de la contraseña, obtenga la propiedad [**IADsUser. PasswordExpirationDate**](/windows/desktop/ADSI/iadsuser-property-methods) . No se puede modificar este atributo para un usuario; en su lugar, establezca la propiedad [**IADsDomain. MaxPasswordAge**](/windows/desktop/ADSI/iadsdomain-property-methods) para cambiar la configuración del dominio.

</dd> <dt>

<span id="primaryGroupID"></span><span id="primarygroupid"></span><span id="PRIMARYGROUPID"></span>[**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid)
</dt> <dd>

El atributo [**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid) es un atributo de un solo valor que contiene el [**primaryGroupToken**](/windows/desktop/ADSchema/a-primarygrouptoken) del grupo que es el grupo primario del objeto. El grupo primario del objeto no se incluye en el atributo [**memberOf**](/windows/desktop/ADSchema/a-memberof) . Por ejemplo, de forma predeterminada, el grupo primario de un objeto de usuario es el **primaryGroupToken** del grupo usuarios del dominio, pero el grupo usuarios del dominio no forma parte del atributo **memberOf** del objeto de usuario.

</dd> <dt>

<span id="profilePath"></span><span id="profilepath"></span><span id="PROFILEPATH"></span>[**profilePath**](/windows/desktop/ADSchema/a-profilepath)
</dt> <dd>

El atributo [**profilePath**](/windows/desktop/ADSchema/a-profilepath) especifica una ruta de acceso al perfil del usuario. Este valor puede ser una cadena nula, una ruta de acceso absoluta local o una ruta de acceso UNC.

</dd> <dt>

<span id="pwdLastSet"></span><span id="pwdlastset"></span><span id="PWDLASTSET"></span>[**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset)
</dt> <dd>

El atributo [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset) especifica cuándo se modificó la contraseña por última vez. Este valor se almacena como un entero grande que representa el número de intervalos de 100 nanosegundos desde el 1 de enero de 1601 (UTC).

El sistema utiliza el valor de este atributo y el atributo [**maxPwdAge**](/windows/desktop/ADSchema/a-maxpwdage) del dominio que contiene el objeto de usuario para calcular la fecha de expiración de la contraseña. Es decir, la suma de [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset) para el usuario y **maxPwdAge** del dominio del usuario.

Este atributo controla si el usuario debe cambiar la contraseña cuando el usuario inicia la sesión siguiente. Si [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset) es cero, el usuario predeterminado debe cambiar la contraseña en el siguiente inicio de sesión. El valor-1 indica que no es necesario que el usuario cambie la contraseña en el siguiente inicio de sesión. El sistema establece este valor en-1 después de que el usuario haya establecido la contraseña.

</dd> <dt>

<span id="sAMAccountType"></span><span id="samaccounttype"></span><span id="SAMACCOUNTTYPE"></span>[**sAMAccountType**](/windows/desktop/ADSchema/a-samaccounttype)
</dt> <dd>

El atributo [**sAMAccountType**](/windows/desktop/ADSchema/a-samaccounttype) especifica un entero que representa el tipo de cuenta. Lo establece el sistema operativo cuando se crea el objeto.

</dd> <dt>

<span id="scriptPath"></span><span id="scriptpath"></span><span id="SCRIPTPATH"></span>[**scriptPath**](/windows/desktop/ADSchema/a-scriptpath)
</dt> <dd>

El atributo [**ScriptPath**](/windows/desktop/ADSchema/a-scriptpath) especifica la ruta de acceso del script de inicio de sesión del usuario,. cmd,. exe o. bat. La cadena puede ser null.

</dd> <dt>

<span id="unicodePwd"></span><span id="unicodepwd"></span><span id="UNICODEPWD"></span>[**unicodePwd**](/windows/desktop/ADSchema/a-unicodepwd)
</dt> <dd>

El atributo [**unicodePwd**](/windows/desktop/ADSchema/a-unicodepwd) es la contraseña del usuario.

Para establecer la contraseña de usuario, use el método [**IADsUser. ChangePassword**](/windows/desktop/api/iads/nf-iads-iadsuser-changepassword) , si el script o la aplicación permiten al usuario cambiar su propia contraseña, o el método [**IADsUser. SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) , si el script o la aplicación permiten al administrador restablecer una contraseña.

Contraseña del usuario en formato unidireccional (OWF) de Windows NT. Windows 2000 usa las OWF de Windows NT. Este atributo solo se usa en el sistema operativo. Tenga en cuenta que no puede volver a derivar la contraseña de texto no cifrado de la forma OWF de la contraseña.

</dd> <dt>

<span id="userAccountControl"></span><span id="useraccountcontrol"></span><span id="USERACCOUNTCONTROL"></span>[**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol)
</dt> <dd>

El atributo [**UserAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) especifica las marcas que controlan la contraseña, el bloqueo, la deshabilitación o la habilitación, el script y el comportamiento del directorio principal del usuario. Este atributo también contiene una marca que indica el tipo de cuenta del objeto. Normalmente, el objeto de usuario tiene \_ \_ establecido el conjunto de cuentas normal.

Las marcas siguientes se definen en Lmaccess. h.



| Marca                     | Descripción                                                                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SCRIPT de fi \_               | El script de inicio de sesión ejecutado. Este valor debe establecerse para LAN Manager 2,0 o Windows NT.                                                                             |
| FI \_ ACCOUNTDISABLE       | La cuenta de usuario está deshabilitada.                                                                                                                                    |
| se \_ requiere fi HOMEDIR \_    | El directorio particular es obligatorio. Este valor se omite en Windows NT y Windows 2000.                                                                            |
| FI \_ passwd \_ NOTREQD      | No se requiere una contraseña.                                                                                                                                         |
| cambio de la \_ insuficiencia de la passwd \_ \_ | El usuario no puede cambiar la contraseña.                                                                                                                             |
| bloqueo de fi \_              | La cuenta está bloqueada actualmente. Este valor se puede borrar para desbloquear una cuenta bloqueada previamente. Este valor no se puede usar para bloquear una cuenta bloqueada previamente. |
| no \_ \_ finalizar la \_ passwd | Representa la contraseña, que nunca debe expirar en la cuenta.                                                                                               |



 

Las marcas siguientes describen el tipo de cuenta. Solo se puede establecer un valor. No se puede cambiar el tipo de cuenta.



| Marca                            | Descripción                                                                                                                                                                                                                                     |
|---------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_cuenta normal de fi \_             | Se trata de un tipo de cuenta predeterminado que representa a un usuario típico.                                                                                                                                                                                  |
| FI \_ - \_ cuenta duplicada temporal \_    | Se trata de una cuenta para usuarios cuya cuenta principal se encuentra en otro dominio. Esta cuenta proporciona acceso de usuario a este dominio, pero no a ningún dominio que confíe en este dominio. El administrador de usuarios hace referencia a este tipo de cuenta como cuenta de usuario local. |
| cuenta de confianza de estación de trabajo de fi \_ \_ \_ | Se trata de una cuenta de equipo para Windows NT Workstation/Windows 2000 Professional o Windows NT Server/Windows 2000 Server que es miembro de este dominio.                                                                                     |
| \_cuenta de \_ confianza de servidor de up \_      | Se trata de una cuenta de equipo para un controlador de dominio de copia de seguridad de Windows NT que es miembro de este dominio.                                                                                                                                           |
| cuenta de confianza entre \_ dominios \_ \_ | Se trata de un permiso para confiar en la cuenta de un dominio de Windows NT que confía en otros dominios.                                                                                                                                                            |



 

</dd> <dt>

<span id="userCertificate"></span><span id="usercertificate"></span><span id="USERCERTIFICATE"></span>[**userCertificate**](/windows/desktop/ADSchema/a-usercertificate)
</dt> <dd>

El atributo [**userCertificate**](/windows/desktop/ADSchema/a-usercertificate) es un atributo con varios valores que contiene los certificados X509v3 con codificación der emitidos para el usuario. Tenga en cuenta que este atributo contiene los certificados de clave pública emitidos para este usuario por el servicio de certificados de Microsoft.

</dd> <dt>

<span id="userSharedFolder"></span><span id="usersharedfolder"></span><span id="USERSHAREDFOLDER"></span>[**userSharedFolder**](/windows/desktop/ADSchema/a-usersharedfolder)
</dt> <dd>

El atributo [**userSharedFolder**](/windows/desktop/ADSchema/a-usersharedfolder) especifica una ruta de acceso UNC a la carpeta de documentos compartidos del usuario. La ruta de acceso debe ser una ruta de acceso UNC de red con el formato \\ \\ servidor \\ recurso compartido \\ directorio. Este valor puede ser una cadena nula.

</dd> <dt>

<span id="userWorkstations"></span><span id="userworkstations"></span><span id="USERWORKSTATIONS"></span>[**userWorkstations**](/windows/desktop/ADSchema/a-userworkstations)
</dt> <dd>

El atributo [**userWorkstations**](/windows/desktop/ADSchema/a-userworkstations) es un atributo de un solo valor que contiene los nombres NetBIOS de las estaciones de trabajo desde las que el usuario puede iniciar sesión. Cada nombre NetBIOS está separado por una coma.

Si no se establece ningún valor, indica que no hay ninguna restricción. Para deshabilitar los inicios de sesión de todas las estaciones de trabajo en esta cuenta, establezca el \_ valor de ACCOUNTDISABLE (definido en Lmaccess. h) en el atributo [**UserAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) .

</dd> </dl>

 

 
