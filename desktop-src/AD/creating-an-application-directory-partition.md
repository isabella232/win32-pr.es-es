---
title: Creación de una partición de directorio de aplicación
description: Una partición de directorio de aplicación se representa mediante un objeto domainDNS con un valor de atributo instanceType de DS INSTANCETYPE IS NC HEAD combinado con \_ \_ \_ \_ DS \_ INSTANCETYPE \_ NC IS \_ \_ WRITEABLE.
ms.assetid: 5e90f316-9d67-484d-98b8-0632dd3c2c43
ms.tgt_platform: multiple
keywords:
- Creación de una partición de directorio de aplicación de AD
- Application Directory Partitions AD , Creating
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c340bac215be62867dcddcda97326c33fc70c458ee242965258cc1ee24cf25f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118020544"
---
# <a name="creating-an-application-directory-partition"></a>Creación de una partición de directorio de aplicación

Una partición de directorio de aplicación se representa mediante un objeto [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) con un valor de atributo [**instanceType**](/windows/desktop/ADSchema/a-instancetype) de **DS \_ INSTANCETYPE \_ IS NC \_ \_ HEAD** combinado con **DS \_ INSTANCETYPE NC IS \_ \_ \_ WRITEABLE**. Este **objeto domainDNS** representa la raíz de partición del directorio de la aplicación (principal nc) y se denomina similar a una partición de dominio normal, por ejemplo, "DC=dynamicdata,DC=fabrikam,DC=com", que corresponde a un nombre DNS de "dynamicdata.fabrikam.com". Por lo tanto, se puede crear una instancia de una partición de directorio de aplicación en cualquier lugar en el que se pueda crear una instancia de una partición de dominio. No hay ningún nombre NetBIOS asociado a una partición de directorio de aplicación.

Es posible anidar particiones de directorio de aplicación, es decir, una partición de directorio de aplicación puede tener particiones de directorio de aplicación secundarias. Las búsquedas con el ámbito de subárbol con raíz en un responsable de partición de directorio de aplicación generarán referencias de continuación a las particiones de directorio de aplicación secundarias.

Una réplica de partición de directorio de aplicación solo se puede crear en un controlador de dominio que se ejecuta en Windows Server 2003 y versiones posteriores y solo mientras el rol FSMO de Domain-Naming está en manos de un controlador de dominio de Windows Server 2003 y versiones posteriores. En un bosque mixto que tiene controladores de dominio de Windows Server 2003 y controladores de dominio de nivel inferior (Windows 2000 controladores de dominio o controladores de dominio principales de Windows NT 4.0), se producirá un error al intentar crear una réplica de partición de directorio de aplicación en un controlador de dominio de nivel inferior.

Una partición de directorio de aplicación también tiene un [**objeto crossRef**](/windows/desktop/ADSchema/c-crossref) correspondiente en el contenedor Partitions de la partición de configuración. CrossRef **se** puede crear manualmente antes de crear el [**objeto domainDNS.**](/windows/desktop/ADSchema/c-domaindns) El objeto **crossRef** creado previamente debe tener los valores de atributo que se muestran en la tabla siguiente o se producirá un error en la creación de la partición. Si el **objeto crossRef** no existe, el Active Directory creará uno cuando se cree la partición del directorio de la aplicación.

| Atributo                          | Descripción                                                                                                                               |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot) | Contiene la ruta de acceso DNS del controlador de dominio en el que se creará la partición del directorio de la aplicación.                               |
| [**habilitado**](/windows/desktop/ADSchema/a-enabled) | Contiene **FALSE.**                                                                                                                       |
| [**nCName**](/windows/desktop/ADSchema/a-ncname)   | Contiene el nombre distintivo de la partición. En el ejemplo anterior, este atributo contendrá "DC=dynamicdata,DC=mydomain,DC=com". |



 

**Para crear una nueva partición de directorio de aplicación con su primera réplica, realice los pasos siguientes**

1.  Enlace al espacio de nombres de la nueva partición, especificando el controlador de dominio que hospedará la partición del directorio de la aplicación en ADsPath. Por ejemplo, para crear una partición con un ADsPath de "DC=dynamicdata,DC=mydomain,DC=com", el enlace ADsPath sería "LDAP:// <domain controller> /DC=mydomain,DC=com", donde " controlador de dominio " es el nombre DNS del controlador de dominio que hospedará la &lt; &gt; partición.

    La operación de enlace debe especificar las opciones rápida y de delegación. La opción rápida permite que el enlace se haga correctamente incluso si el espacio de nombres no existe. La opción de delegación es necesaria para permitir que el controlador de dominio se pondrá en contacto con el Domain-Naming de roles de FSMO con las mismas credenciales.

    La versión del sistema del controlador de dominio debe Windows sistema operativo Server 2003 y versiones posteriores.

2.  Cree un [**objeto domainDNS**](/windows/desktop/ADSchema/c-domaindns) con un nombre adecuado para la partición, por ejemplo, "DC=dynamicdata", para representar el responsable del contexto de nomenclatura de la nueva partición. El **objeto domainDNS** debe tener un atributo [**instanceType**](/windows/desktop/ADSchema/a-instancetype) con un valor de 5 **(DS \_ INSTANCETYPE IS NC \_ \_ \_ HEAD** \| **DS \_ INSTANCETYPE NC IS \_ \_ \_ WRITEABLE**). El **atributo instanceType** solo se puede establecer en el momento de la creación porque es un atributo solo del sistema.

Cuando se crea el objeto [**domainDNS,**](/windows/desktop/ADSchema/c-domaindns) Active Directory servidor realizará los pasos siguientes:

1.  Busca un objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) en el contenedor Partitions que tenga un valor de atributo [**nCName**](/windows/desktop/ADSchema/a-ncname) que coincida con el nombre distintivo de la partición y, si se encuentra una coincidencia, modifica el objeto **crossRef** para representar la partición del directorio de la aplicación. Si no se encuentra **un objeto crossRef** correspondiente, el servidor Active Directory crea un nuevo objeto **crossRef** para representar la partición del directorio de la aplicación.

    En la tabla siguiente se enumeran los atributos importantes del [**objeto crossRef.**](/windows/desktop/ADSchema/c-crossref)

    | Atributo                                                              | Descripción                                                                                                                                        |
    |------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
    | [**nCName**](/windows/desktop/ADSchema/a-ncname)                                       | Contiene el nombre distintivo de la partición.                                                                                                  |
    | [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot)                                     | Contiene el nombre DNS de la partición.                                                                                                            |
    | [**msDS-NC-Replica-Locations**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) | El nombre distintivo del objeto [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) del controlador de dominio para la primera réplica se agrega a este atributo. |

    

     

2.  Inicie una sincronización de la partición de configuración y espere a que finalice. Esto permite a la aplicación cliente modificar los parámetros de configuración de la partición de directorio de aplicación recién creada mientras se enlaza al mismo controlador de dominio que se usa para crear la partición del directorio de la aplicación.
3.  Cree el [**objeto domainDNS**](/windows/desktop/ADSchema/c-domaindns) con las marcas **DS \_ INSTANCETYPE \_ IS NC \_ \_ HEAD** y **DS \_ INSTANCETYPE NC IS \_ \_ \_ WRITEABLE** establecidas en la [**propiedad instanceType.**](/windows/desktop/ADSchema/a-instancetype) La **propiedad instanceType** también puede contener otras marcas privadas.
4.  Rellene el [**atributo ms-DS-Has-Master-NCs**](/windows/desktop/ADSchema/a-msds-hasmasterncs) del objeto [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) para el controlador de dominio de destino con el nombre distintivo de la partición de directorio de aplicación recién creada.

Cuando se crea la partición del directorio de la aplicación o cuando se agrega una nueva réplica de la partición del directorio de la aplicación y se sincroniza completamente, el servidor de Active Directory registra correctamente la réplica con NetLogon y DNS. Para obtener más información y una lista de los registros SRV registrados, vea Buscar un servidor host de [partición de directorio de aplicación](locating-an-application-directory-partition-host-server.md).

Para obtener más información sobre cómo crear una partición de directorio de aplicación, vea [Ejemplo de código para crear una partición de directorio de aplicación.](example-code-for-creating-an-application-directory-partition.md)

## <a name="locating-the-partitions-container"></a>Buscar el contenedor de particiones

El nombre distintivo del contenedor Partitions se puede encontrar de una de estas dos maneras. El primero es más complicado de realizar, pero siempre proporcionará un resultado preciso:

1.  Enlace a RootDSE y obtenga el **atributo configurationNamingContext.**
2.  Use el **atributo configurationNamingContext** para enlazar con el contenedor de configuración.
3.  Busque en el contenedor de configuración un objeto que sea del [**tipo crossRefContainer.**](/windows/desktop/ADSchema/c-crossrefcontainer)
4.  Obtenga el **valor del atributo distinguishedName** del [**objeto crossRefContainer.**](/windows/desktop/ADSchema/c-crossrefcontainer) Este será el nombre distintivo del contenedor Partitions.

Para obtener más información y un ejemplo de código que muestra este método para buscar el contenedor Partitions, vea la función **GetPartitionsDNSearch** en Example [Code for Locating the Partitions Container](example-code-for-locating-the-partitions-container.md).

El segundo método es más fácil de implementar, pero se basa en que el contenedor Partitions tiene un nombre distintivo relativo determinado. Actualmente no es posible cambiar el nombre del contenedor Particiones, pero si esta funcionalidad se agrega en el futuro, el procedimiento siguiente no funcionará correctamente si se ha cambiado el nombre del contenedor Partitions.

1.  Enlace a RootDSE y obtenga el **atributo configurationNamingContext.**
2.  Combine la cadena "CN=Partitions", seguida del atributo **configurationNamingContext** para formar el nombre distintivo del contenedor Partitions. El nombre distintivo tendrá el formato "CN=Partitions, <configuration DN> ".

Para obtener más información y un ejemplo de código que muestra este método para buscar el contenedor Partitions, vea la función **GetPartitionsDNManual** en Código de ejemplo para buscar el contenedor [de particiones](example-code-for-locating-the-partitions-container.md).

 

 