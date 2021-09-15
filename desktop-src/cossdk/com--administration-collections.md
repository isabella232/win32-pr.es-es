---
description: Las colecciones de administración de COM+ sirven para almacenar y organizar los datos de configuración almacenados en el catálogo de COM+.
ms.assetid: eed8ca97-39ad-4188-afc6-8670b5073fad
title: Colecciones de administración de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceb49ecd382e5a5a570e3e479714ad905a5eaf5f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465574"
---
# <a name="com-administration-collections"></a>Colecciones de administración de COM+

Las colecciones de administración de COM+ sirven para almacenar y organizar los datos de configuración almacenados en el catálogo de COM+. Las colecciones corresponden a carpetas en el árbol de consola de la herramienta de administración servicios de componentes. Puede acceder a estas colecciones mediante las interfaces y los objetos de administración de COM+.

Para iniciar la administración mediante programación se usan objetos creados a partir de la clase [**COMAdminCatalog,**](comadmincatalog.md) se representan las colecciones del catálogo mediante objetos creados a partir de la clase [**COMAdminCatalogCollection**](comadmincatalogcollection.md) y se representan elementos en colecciones mediante objetos creados a partir de la clase [**COMAdminCatalogObject.**](comadmincatalogobject.md)

Los elementos de una colección determinada exponen un conjunto coherente de propiedades. Por ejemplo, cada elemento de la colección [**Components**](components.md) representa un componente y los elementos de la colección **Components** exponen las mismas propiedades usadas para configurar un componente. Se puede acceder a estas propiedades mediante la [**clase COMAdminCatalogObject.**](comadmincatalogobject.md)

> [!Note]  
> Las propiedades con acceso WriteOnce son ReadWrite mientras se usa el método [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) antes de usar [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) y son ReadOnly después.

 

Para obtener una introducción a la administración mediante programación de COM+, vea [Automatización de la administración de COM+.](automating-com--administration.md)

## <a name="collection-hierarchy"></a>Jerarquía de colecciones

En la ilustración siguiente se muestran las relaciones entre las colecciones. Las colecciones del extremo izquierdo (en cuadros de color blanco y gris) son colecciones de nivel superior, a las que se accede mediante una llamada al método [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-getcollection) de un objeto creado a partir de la clase [**COMAdminCatalog.**](comadmincatalog.md) Solo se puede acceder a las colecciones restantes (en cuadros amarillos) a través de su colección primaria, llamando al método [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) del objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) que representa su elemento primario. Las flechas apuntan desde una colección primaria a sus colecciones secundarias.

![Diagrama que muestra las relaciones entre las colecciones.](images/ab61b0ab-2368-4bd8-9cfc-b7adc5beaca3.png)

Las cuatro colecciones siguientes no se muestran en la ilustración: [**ErrorInfo**](errorinfo.md), [**PropertyInfo**](propertyinfo.md), [**RelatedCollectionInfo**](relatedcollectioninfo.md)y [**Root**](root.md). La **colección ErrorInfo** es un elemento secundario de todas las colecciones de la ilustración, excepto [**InprocServers**](inprocservers.md) y [**WOWInprocServers**](wowinprocservers.md) (en cuadros grises). Las **colecciones PropertyInfo** **y RelatedCollectionInfo** son elementos secundarios de cada colección. La **colección** raíz es una colección de nivel superior que es el elemento primario de todas las demás colecciones de nivel superior. Sin embargo, no es necesario acceder a la colección **raíz** antes de acceder a otras colecciones de nivel superior.

## <a name="comadmin-library"></a>Biblioteca COMAdmin

La biblioteca COMAdmin admite las siguientes colecciones.



| Colección                                                             | Descripción                                                                                                                                           |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ApplicationCluster**](applicationcluster.md)                       | Contiene una lista de los servidores del clúster de aplicaciones.                                                                                            |
| [**ApplicationInstances**](applicationinstances.md)                   | Contiene un objeto para cada instancia de una aplicación COM+ en ejecución.                                                                                   |
| [**Aplicaciones**](applications.md)                                   | Contiene un objeto para cada aplicación COM+ instalada en el equipo local.                                                                         |
| [**Componentes**](components.md)                                       | Contiene un objeto para cada componente de la aplicación con la que está relacionado.                                                                      |
| [**ComputerList**](computerlist.md)                                   | Contiene una lista de los equipos que se encuentran en la **carpeta Equipos** de la herramienta de administración servicios de componentes.                                     |
| [**DCOMProtocols**](dcomprotocols.md)                                 | Contiene una lista de los protocolos que DCOM va a usar. Contiene un objeto para cada protocolo.                                                         |
| [**ErrorInfo**](errorinfo.md)                                         | Recupera información de error extendida con respecto a los métodos que tratan con varios objetos.                                                               |
| [**EventClassesForIID**](eventclassesforiid.md)                       | Recupera información relacionada con las clases de eventos.                                                                                                        |
| [**FilesForImport**](filesforimport.md)                               | Recupera información de su archivo MSI sobre una aplicación que se puede importar.                                                                    |
| [**InprocServers**](inprocservers.md)                                 | Contiene una lista de los servidores en proceso registrados con el sistema. Contiene un objeto para cada componente.                                       |
| [**InterfacesForComponent**](interfacesforcomponent.md)               | Contiene un objeto para cada interfaz expuesta por el componente al que está relacionada la colección.                                                    |
| [**LegacyComponents**](legacycomponents.md)                           | Contiene un objeto para cada componente no configurado de la aplicación con la que está relacionado.                                                         |
| [**LegacyServers**](legacyservers.md)                                 | Idéntico a la [**colección InprocServers,**](inprocservers.md) salvo que esta colección también incluye servidores locales.                           |
| [**LocalComputer**](localcomputer.md)                                 | Contiene un único objeto que contiene información de configuración de nivel de equipo para el equipo al que está accediendo al catálogo.                             |
| [**MethodsForInterface**](methodsforinterface.md)                     | Contiene un objeto para cada método de la interfaz con la que está relacionada la colección.                                                               |
| [**Particiones**](partitions.md)                                       | Se usa para especificar las aplicaciones contenidas en cada partición.                                                                                         |
| [**PartitionUsers**](partitionusers.md)                               | Se usa para especificar los usuarios contenidos en cada partición.                                                                                                |
| [**Propertyinfo**](propertyinfo.md)                                   | Recupera información sobre las propiedades que admite una colección especificada.                                                                      |
| [**PublisherProperties**](publisherproperties.md)                     | Contiene un objeto para cada propiedad del publicador para la colección [**principal SubscriptionsForComponent.**](subscriptionsforcomponent.md)              |
| [**RelatedCollectionInfo**](relatedcollectioninfo.md)                 | Recupera información sobre otras colecciones relacionadas con la colección desde la que se llama.                                                      |
| [**Papeles**](roles.md)                                                 | Contiene un objeto para cada rol asignado a la aplicación con la que está relacionado.                                                                  |
| [**RolesForComponent**](rolesforcomponent.md)                         | Contiene un objeto para cada rol asignado al componente al que está relacionada la colección.                                                        |
| [**RolesForInterface**](rolesforinterface.md)                         | Contiene un objeto para cada rol asignado a la interfaz a la que está relacionada la colección.                                                        |
| [**RolesForMethod**](rolesformethod.md)                               | Contiene un objeto para cada rol asignado al método con el que está relacionada la colección.                                                           |
| [**RolesForPartition**](rolesforpartition.md)                         | Contiene un objeto para cada rol asignado a la partición con la que está relacionada la colección.                                                        |
| [**Raíz**](root.md)                                                   | Contiene las colecciones de nivel superior del catálogo.                                                                                                    |
| [**SubscriberProperties**](subscriberproperties.md)                   | Contiene un objeto para cada propiedad de suscriptor para la colección [**principal SubscriptionsForComponent.**](subscriptionsforcomponent.md)             |
| [**SubscriptionsForComponent**](subscriptionsforcomponent.md)         | Contiene un objeto para cada suscripción de la colección [**de componentes**](components.md) primaria.                                                  |
| [**TransientPublisherProperties**](transientpublisherproperties.md)   | Contiene un objeto para cada propiedad del publicador para la colección [**TransientSubscriptions**](transientsubscriptions.md) primaria.                    |
| [**TransientSubscriberProperties**](transientsubscriberproperties.md) | Contiene un objeto para cada propiedad de suscriptor para la colección [**TransientSubscriptions**](transientsubscriptions.md) primaria.                   |
| [**TransientSubscriptions**](transientsubscriptions.md)               | Contiene un objeto para cada suscripción transitoria.                                                                                                   |
| [**UsersInPartitionRole**](usersinpartitionrole.md)                   | Contiene un objeto para cada usuario del rol de partición con el que está relacionada la colección.                                                            |
| [**UsersInRole**](usersinrole.md)                                     | Contiene un objeto para cada usuario del rol con el que está relacionada la colección.                                                                      |
| [**WOWInprocServers**](wowinprocservers.md)                           | Contiene una lista de los servidores en proceso registrados con el sistema para componentes de 32 bits en equipos de 64 bits.                                       |
| [**WOWLegacyServers**](wowlegacyservers.md)                           | Idéntica a [**la colección LegacyServers,**](legacyservers.md) salvo que esta recopilación se extrae del Registro de 32 bits en equipos de 64 bits. |



 

 

 



