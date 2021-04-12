---
title: Crear una partición de directorio de aplicaciones
description: Una partición de directorio de aplicaciones se representa mediante un objeto domainDNS con un valor de atributo instanceType de DS \_ instanceType \_ es el \_ \_ encabezado NC combinado con DS \_ instanceType NC que \_ \_ es \_ grabable.
ms.assetid: 5e90f316-9d67-484d-98b8-0632dd3c2c43
ms.tgt_platform: multiple
keywords:
- Crear una partición de directorio de aplicaciones AD
- Particiones de directorio de aplicaciones AD, crear
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a17471696825179b6e49230b5168abbaf88b8e2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487474"
---
# <a name="creating-an-application-directory-partition"></a>Crear una partición de directorio de aplicaciones

Una partición de directorio de aplicaciones se representa mediante un objeto [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) con un valor de atributo [**instanceType**](/windows/desktop/ADSchema/a-instancetype) de **DS \_ instanceType \_ es el \_ \_ encabezado NC** combinado con **DS \_ instanceType NC que \_ \_ es \_ grabable**. Este objeto **domainDNS** representa la raíz de la partición del directorio de aplicación (encabezado NC) y se denomina de forma similar a una partición de dominio normal, por ejemplo, "DC = DYNAMICDATA, DC = Fabrikam, DC = com", que corresponde a un nombre DNS de "DynamicData.fabrikam.com". Por lo tanto, se puede crear una instancia de una partición de directorio de aplicaciones en cualquier lugar en el que se puedan crear instancias de una partición de dominio. No hay ningún nombre NetBIOS asociado a una partición de directorio de aplicaciones.

Es posible anidar particiones de directorio de aplicaciones, es decir, una partición de directorio de aplicaciones puede tener particiones de directorio de aplicaciones secundarias. Las búsquedas con el ámbito de subárbol con raíz en un encabezado de partición de directorio de aplicaciones generarán referencias de continuación a las particiones de directorio de aplicaciones secundarias.

Una réplica de partición de directorio de aplicaciones solo se puede crear en un controlador de dominio que se ejecute en Windows Server 2003 y versiones posteriores, y solo mientras el rol FSMO Domain-Naming esté contenido en un controlador de dominio de Windows Server 2003 y versiones posteriores. En un bosque mixto con controladores de dominio de Windows Server 2003 y controladores de dominio de nivel inferior (controladores de dominio de Windows 2000 o controladores de dominio principales de Windows NT 4,0), se producirá un error al intentar crear una réplica de partición de directorio de aplicaciones en un controlador de dominio de nivel inferior.

Una partición de directorio de aplicaciones también tiene un objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) correspondiente en el contenedor de particiones de la partición de configuración. La **crossRef** se puede crear manualmente antes de crear el objeto [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) . El objeto **crossRef** creado previamente debe tener los valores de atributo que se muestran en la tabla siguiente o se producirá un error en la creación de la partición. Si el objeto **crossRef** no existe, el servidor de Active Directory creará uno cuando se cree la partición de directorio de aplicaciones.

| Atributo                          | Descripción                                                                                                                               |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot) | Contiene la ruta de acceso DNS del controlador de dominio en el que se creará la partición del directorio de aplicaciones.                               |
| [**habilitado**](/windows/desktop/ADSchema/a-enabled) | Contiene **false**.                                                                                                                       |
| [**nCName**](/windows/desktop/ADSchema/a-ncname)   | Contiene el nombre distintivo de la partición. En el ejemplo anterior, este atributo incluiría "DC = DynamicData, DC = miDominio, DC = com". |



 

**Para crear una nueva partición de directorio de aplicaciones con su primera réplica, realice los pasos siguientes:**

1.  Enlace con el espacio de nombres de la nueva partición y especifique el controlador de dominio que hospedará la partición del directorio de aplicaciones en el ADsPath. Por ejemplo, para crear una partición con un ADsPath de "DC = DynamicData, DC = miDominio, DC = com", el enlace ADsPath sería "LDAP:// <domain controller> /DC = miDominio, DC = com", donde " &lt; controlador &gt; de dominio" es el nombre DNS del controlador de dominio que hospedará la partición.

    La operación de enlace debe especificar las opciones rápida y de delegación. La opción Fast permite que el enlace se realice correctamente incluso si el espacio de nombres no existe. La opción de delegación es necesaria para permitir que el controlador de dominio se ponga en contacto con el titular de la función FSMO de Domain-Naming con las mismas credenciales.

    La versión del sistema del controlador de dominio debe ser el sistema operativo Windows Server 2003 y versiones posteriores.

2.  Cree un objeto [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) con un nombre adecuado para la partición, por ejemplo, "DC = DynamicData", para representar el encabezado de contexto de nomenclatura de la nueva partición. El objeto **domainDNS** debe tener un atributo [**instanceType**](/windows/desktop/ADSchema/a-instancetype) con un valor de 5 (**DS \_ instanceType \_ es \_ NC \_ Head** \| **DS \_ instanceType \_ NC \_ es \_ grabable**). El atributo **instanceType** solo se puede establecer en el momento de la creación porque es un atributo solo del sistema.

Cuando se cree el objeto [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) , el servidor de Active Directory llevará a cabo los pasos siguientes:

1.  Busca un objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) en el contenedor de particiones que tenga un valor de atributo [**NCName**](/windows/desktop/ADSchema/a-ncname) que coincida con el nombre distintivo de la partición y, si se encuentra una coincidencia, modifica el objeto **crossRef** para representar la partición del directorio de aplicaciones. Si no se encuentra un objeto **crossRef** coincidente, el servidor de Active Directory crea un nuevo objeto **crossRef** para representar la partición del directorio de aplicaciones.

    En la tabla siguiente se enumeran los atributos importantes del objeto [**crossRef**](/windows/desktop/ADSchema/c-crossref) .

    | Atributo                                                              | Descripción                                                                                                                                        |
    |------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
    | [**nCName**](/windows/desktop/ADSchema/a-ncname)                                       | Contiene el nombre distintivo de la partición.                                                                                                  |
    | [**dnsRoot**](/windows/desktop/ADSchema/a-dnsroot)                                     | Contiene el nombre DNS de la partición.                                                                                                            |
    | [**msDS-NC-réplica-ubicaciones**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) | El nombre distintivo del objeto [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) del controlador de dominio para la primera réplica se agrega a este atributo. |

    

     

2.  Iniciar una sincronización de la partición de configuración y esperar a que finalice. Esto permite a la aplicación cliente modificar los parámetros de configuración de la partición de directorio de aplicaciones recién creada mientras esté enlazada al mismo controlador de dominio que se usa para crear la partición del directorio de aplicaciones.
3.  Cree el objeto [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) con el **INSTANCETYPE de DS \_ es el \_ \_ \_ encabezado NC** y **DS \_ INSTANCETYPE \_ NC \_ se \_** establecen marcas de escritura en la propiedad [**INSTANCETYPE**](/windows/desktop/ADSchema/a-instancetype) . La propiedad **instanceType** también puede contener otras marcas privadas.
4.  Rellene el atributo [**MS-DS-IS-Master-NC**](/windows/desktop/ADSchema/a-msds-hasmasterncs) del objeto [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa) para el controlador de dominio de destino con el nombre distintivo de la partición de directorio de aplicaciones recién creada.

Cuando se crea la partición del directorio de aplicaciones, o cuando se agrega una nueva réplica de la partición del directorio de aplicaciones y se sincroniza por completo, el servidor de Active Directory registra correctamente la réplica con NetLogon y DNS. Para obtener más información y una lista de los registros SRV registrados, consulte [localizar un servidor host de partición de directorio de aplicaciones](locating-an-application-directory-partition-host-server.md).

Para obtener más información sobre la creación de una partición de directorio de aplicaciones, vea [código de ejemplo para crear una partición de directorio de aplicaciones](example-code-for-creating-an-application-directory-partition.md).

## <a name="locating-the-partitions-container"></a>Buscar el contenedor de particiones

El nombre distintivo del contenedor de particiones se puede encontrar de una de estas dos maneras. El primero es más complicado de realizar, pero siempre proporcionará un resultado preciso:

1.  Enlazar a RootDSE y obtener el atributo **configurationNamingContext** .
2.  Use el atributo **configurationNamingContext** para enlazar con el contenedor de configuración.
3.  Busque en el contenedor de configuración un objeto que sea del tipo [**crossRefContainer**](/windows/desktop/ADSchema/c-crossrefcontainer) .
4.  Obtenga el valor del atributo **distinguishedName** del objeto [**crossRefContainer**](/windows/desktop/ADSchema/c-crossrefcontainer) . Este será el nombre distintivo del contenedor de particiones.

Para obtener más información y un ejemplo de código que muestre este método para buscar el contenedor de particiones, vea la función **GetPartitionsDNSearch** en el [código de ejemplo para buscar el contenedor de particiones](example-code-for-locating-the-partitions-container.md).

El segundo método es más fácil de implementar, pero se basa en el contenedor de particiones que tiene un nombre distintivo relativo determinado. En la actualidad, no es posible cambiar el nombre del contenedor de particiones, pero si se agrega esta funcionalidad en el futuro, el procedimiento que se indica a continuación no funcionará correctamente si se ha cambiado el nombre del contenedor de particiones.

1.  Enlazar a RootDSE y obtener el atributo **configurationNamingContext** .
2.  Combine la cadena "CN = partitions", seguida por el atributo **configurationNamingContext** para formar el nombre distintivo del contenedor de particiones. El nombre distintivo tendrá el formato "CN = partitions <configuration DN> ".

Para obtener más información y un ejemplo de código que muestre este método para buscar el contenedor de particiones, vea la función **GetPartitionsDNManual** en el [código de ejemplo para buscar el contenedor de particiones](example-code-for-locating-the-partitions-container.md).

 

 