---
title: Crear y eliminar objetos en Active Directory Domain Services
description: El procedimiento utilizado para crear y eliminar objetos mediante programación en Active Directory Domain Services depende de la tecnología de programación utilizada.
ms.assetid: 13f83aea-ad39-4737-af3c-24316a31046d
ms.tgt_platform: multiple
keywords:
- Crear y eliminar objetos Active Directory Active Directory
- Active Directory Domain Services Active Directory, usar la creación y eliminación de objetos
- objetos Active Directory, crear y eliminar objetos de Active Directory Domain Services
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11d3e85ef3c356978faeab059e3969bb657185bd
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487471"
---
# <a name="creating-and-deleting-objects-in-active-directory-domain-services"></a>Crear y eliminar objetos en Active Directory Domain Services

El procedimiento utilizado para crear y eliminar objetos mediante programación en Active Directory Domain Services depende de la tecnología de programación utilizada. Para obtener más información acerca de la creación y eliminación de objetos en Active Directory Domain Services con una tecnología de programación específica, vea los temas que se muestran en la tabla siguiente.



| Tecnología de programación                                                                       | Para obtener más información                                                            |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Interfaces de servicio de Active Directory](/windows/desktop/ADSI/active-directory-service-interfaces-adsi)         | [Crear y eliminar objetos](/windows/desktop/ADSI/creating-and-deleting-objects)             |
| [Protocolo ligero de acceso a directorio](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) | [Modificar una entrada de directorio](/previous-versions/windows/desktop/ldap/modifying-a-directory-entry)                 |
| [System.DirectoryServices](/dotnet/api/system.directoryservices) | [Crear, eliminar, cambiar el nombre y trasladar objetos](https://msdn.microsoft.com/library/ms180850(v=VS.80).aspx) |



 

## <a name="creating-an-object"></a>Creación de un objeto

En general, los únicos atributos necesarios para crear un objeto son los atributos **CN** y **objectClass** . Sin embargo, la creación de un objeto no tiene por qué convertirlo en un objeto funcional. Ciertos tipos de objetos, como usuarios y grupos, tienen atributos adicionales necesarios para que funcionen. Para obtener más información sobre la creación de tipos de objetos específicos, vea [crear un usuario](creating-a-user.md) y [crear grupos en un dominio](creating-groups-in-a-domain.md).

**Windows Server 2003:** Cuando se crea un objeto de la clase de [**usuario**](/windows/desktop/ADSchema/c-user), [**Grupo**](/windows/desktop/ADSchema/c-group)o [**equipo**](/windows/desktop/ADSchema/c-computer) en un controlador de dominio que se ejecuta en WWindows Server 2003 o posterior, el controlador de dominio establece automáticamente el atributo [**samAccountName**](/windows/desktop/ADSchema/a-samaccountname) para el objeto en una cadena única, si no se especifica ninguno.

## <a name="deleting-an-object"></a>Eliminar un objeto

El servidor de Active Directory realiza las siguientes acciones cuando se elimina un objeto:

-   El atributo **IsDeleted** del objeto eliminado se establece en **true**. Los objetos con un valor de atributo **IsDeleted** establecido en **true** se denominan [*marcadores de exclusión*](/previous-versions/windows/desktop/legacy/ms681941(v=vs.85)).
-   El objeto eliminado se mueve al contenedor objetos eliminados para su contexto de nomenclatura. Si la propiedad **systemFlags** del objeto contiene la marca 0x02000000, el objeto no se mueve al contenedor de objetos eliminados. Para obtener más información sobre cómo enlazar y enumerar el contenido del contenedor de objetos eliminados, vea [recuperar objetos eliminados](retrieving-deleted-objects.md).
-   El contenedor de objetos eliminados es plano, por lo que todos los objetos se encuentran en el mismo nivel dentro del contenedor de objetos eliminados. Por lo tanto, se cambia el nombre distintivo relativo del objeto eliminado para asegurarse de que el nombre es único en el contenedor de objetos eliminados. Si el nombre original tiene más de 75 caracteres, se trunca a 75 caracteres. A continuación, se agregan los siguientes nombres al nuevo nombre:
    1.  Un carácter 0x0A
    2.  La cadena "DEL:"
    3.  La forma de cadena de un GUID único, como "947e3228-70c9-4311-8b7a-e5c9b5bd4432"

    Un ejemplo de un nombre de objeto eliminado es:
    ```C++
    Jeff Smith\0ADEL:947e3228-70c9-4311-8b7a-e5c9b5bd4432
    ```

    

-   La mayoría de los valores de atributo del objeto eliminado se quitan. Los siguientes atributos se conservan automáticamente:

    -   **attributeID**
    -   **attributeSyntax**
    -   **Distintivo**
    -   **dNReferenceUpdate**
    -   **flatName**
    -   **governsID**
    -   **groupType**
    -   **instanceType**
    -   **lDAPDisplayName**
    -   **legacyExchangeDN**
    -   **mS-DS-CreatorSID**
    -   **mSMQOwnerID**
    -   **name**
    -   **nCName**
    -   **objectClass**
    -   **GUID**
    -   **objectSid**
    -   **oMSyntax**
    -   **proxiedObjectName**
    -   **replPropertyMetaData**
    -   **Atributo**
    -   **securityIdentifier**
    -   **subClassOf**
    -   **systemFlags**
    -   **trustAttributes**
    -   **trustDirection**
    -   **trustPartner**
    -   **trustType**
    -   **userAccountControl**
    -   **uSNChanged**
    -   **uSNCreated**
    -   **whenCreated**

    También se conservan otros atributos que tienen un valor de atributo **searchFlags** que contiene 0x00000008.

    Los siguientes valores de atributo siempre se quitan de un objeto eliminado:

    -   **objectCategory**
    -   **samAccountType**

-   El descriptor de seguridad del objeto eliminado se conserva y las entradas de control de acceso heredables no se propagan. El descriptor de seguridad se conserva tal cual en el momento en que se elimina el objeto.
-   Los vínculos a y desde el objeto eliminado se borran. Esto se realiza en segundo plano después de que se elimine el objeto. Si el objeto eliminado se restaura antes de que se borren todos los vínculos, se recibirá un error.
-   Si el objeto se elimina en un controlador de dominio de Windows Server 2003, el atributo **lastKnownParent** del objeto eliminado se establece en el nombre distintivo del contenedor donde estaba incluido el objeto cuando se eliminó.

El objeto eliminado permanece en el contenedor de objetos eliminados durante un período de tiempo conocido como duración del objeto de *desecho*. De forma predeterminada, la duración del desecho es de 60 días, pero el administrador del sistema puede cambiar este valor. Cuando expira la duración del objeto de desecho, el objeto se quita de forma permanente del servicio de directorio. Para evitar que se produzca una operación de eliminación, una aplicación debe realizar sincronizaciones incrementales con más frecuencia que la duración del desecho.

Windows Server 2003 agrega la capacidad de restaurar objetos eliminados. Para obtener más información acerca de la restauración de objetos eliminados, consulte restauración de [objetos eliminados](restoring-deleted-objects.md).

Cuando se elimina un elemento, no se puede modificar ninguno de los atributos del objeto. En Windows Server 2003, es posible modificar el descriptor de seguridad (el atributo **ntSecurityDescriptor** ) de un objeto eliminado. Esto se hace para permitir la restauración de objetos cuando la persona que restaura el objeto no tiene permisos de escritura en los atributos obligatorios. Para actualizar el descriptor de seguridad en un objeto eliminado, el autor de la llamada debe tener el derecho de acceso de control "reanimar desecho" en el contexto de nomenclatura, además de la **\_ DAC de escritura** normal y el acceso de **\_ propietario de escritura** . Incluso si el descriptor de seguridad es restrictivo, el administrador puede asumir primero la propiedad del objeto, suponiendo que el Administrador tenga el privilegio de **\_ nombre de \_ propiedad \_ se toma** y, a continuación, modificar el descriptor de seguridad. Para ello, use la función [**LDAP \_ Modify \_ ext \_ s**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_ext_s) con el [**servidor LDAP \_ Mostrar control de \_ \_ \_ OID eliminado**](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid) . La lista de modificación debe contener un solo reemplazo de atributo para el atributo **ntSecurityDescriptor** .

 

 