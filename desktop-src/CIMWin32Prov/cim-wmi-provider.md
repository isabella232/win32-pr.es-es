---
description: Estas clases de WMI se declaran en CimWin32. mof.
ms.assetid: 53122499-1CC0-4B48-AEA1-B70B7BBC3A99
ms.tgt_platform: multiple
title: Proveedor WMI de CIM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a3249549e0915f51b6a9a6f2386c18ba695919a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538482"
---
# <a name="cim-wmi-provider"></a>Proveedor WMI de CIM

Estas clases de WMI se declaran en CimWin32. mof.

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[**Acción de CIM \_**](cim-action.md)
</dt> <dd>

Una clase de [**\_ acción CIM**](cim-action.md) es una operación que forma parte de un proceso para crear un elemento de software en su estado siguiente o para eliminar el elemento de software en el estado actual.

</dd> <dt>

[**\_ACTIONSEQUENCE CIM**](cim-actionsequence.md)
</dt> <dd>

La [**Asociación \_ ActionSequence de CIM**](cim-actionsequence.md) define una serie de operaciones que transfieren el elemento de software (al que hace referencia la Asociación [**\_ SoftwareElementActions de CIM**](cim-softwareelementactions.md) ) al siguiente estado o quita el elemento de software de su estado actual.

</dd> <dt>

[**\_ACTSASSPARE CIM**](cim-actsasspare.md)
</dt> <dd>

La [**Asociación \_ ActsAsSpare de CIM**](cim-actsasspare.md) indica qué elementos pueden ser repuestos o reemplazar otros elementos agregados. Una reserva puede funcionar en modo de "espera activa" como se especifica en cada elemento.

</dd> <dt>

[**\_ADJACENTSLOTS CIM**](cim-adjacentslots.md)
</dt> <dd>

La [**Asociación \_ AdjacentSlots de CIM**](cim-adjacentslots.md) describe el diseño de las ranuras en una placa de hospedaje o en una tarjeta de adaptador. La información, como la distancia entre las ranuras y si están "compartidas" (si se ha rellenado una, no se puede usar la otra ranura), se transmite como propiedades de asociación.

</dd> <dt>

[**\_AGGREGATEPEXTENT CIM**](cim-aggregatepextent.md)
</dt> <dd>

La clase [**CIM \_ AggregatePExtent**](cim-aggregatepextent.md) proporciona información de resumen sobre los bloques lógicos direccionables, que están en el mismo grupo de redundancia de almacenamiento y se encuentran en el mismo medio físico.

</dd> <dt>

[**\_AGGREGATEPSEXTENT CIM**](cim-aggregatepsextent.md)
</dt> <dd>

La clase [**CIM \_ AggregatePSExtent**](cim-aggregatepsextent.md) define el número de bloques lógicos direccionables en un único dispositivo de almacenamiento, excluidos los bloques lógicos asignados como datos de comprobación. Si se definen conjuntos de volúmenes, los bloques lógicos se incluyen en un único conjunto de volúmenes. Se trata de una agrupación alternativa para [**CIM \_ ProtectedSpaceExtent**](cim-protectedspaceextent.md), cuando solo se necesita información de resumen o cuando se usa la configuración automática.

</dd> <dt>

[**\_AGGREGATEREDUNDANCYCOMPONENT CIM**](cim-aggregateredundancycomponent.md)
</dt> <dd>

La clase [**CIM \_ AggregateRedundancyComponent**](cim-aggregateredundancycomponent.md) describe la extensión física agregada en un grupo de redundancia de almacenamiento.

</dd> <dt>

[**\_ALARMDEVICE CIM**](cim-alarmdevice.md)
</dt> <dd>

La [**clase \_ AlarmDevice de CIM**](cim-alarmdevice.md) es un dispositivo de alarma que emite indicaciones auditivas o visibles relacionadas con una situación problemática.

</dd> <dt>

[**\_ALLOCATEDRESOURCE CIM**](cim-allocatedresource.md)
</dt> <dd>

La clase [**CIM \_ AllocatedResource**](cim-allocatedresource.md) representa una asociación entre dispositivos lógicos y recursos del sistema e indica que el recurso está asignado al dispositivo.

</dd> <dt>

[**\_APPLICATIONSYSTEM CIM**](cim-applicationsystem.md)
</dt> <dd>

La clase [**CIM \_ ApplicationSystem**](cim-applicationsystem.md) representa una aplicación o un sistema de software que admite una determinada función empresarial que se puede administrar como una unidad independiente. Este tipo de sistema se puede descomponer en sus componentes funcionales mediante la clase [**CIM \_ SoftwareFeature**](cim-softwarefeature.md) . Las características de software de una aplicación o un sistema de software en particular se encuentran mediante la Asociación [**\_ ApplicationSystemSoftwareFeature de CIM**](cim-applicationsystemsoftwarefeature.md) .

</dd> <dt>

[**\_APPLICATIONSYSTEMSOFTWAREFEATURE CIM**](cim-applicationsystemsoftwarefeature.md)
</dt> <dd>

La clase [**CIM \_ ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) representa una asociación que identifica las características de software que componen un sistema de aplicación determinado. Las características de software se pueden incluir en diferentes productos.

</dd> <dt>

[**\_ASSOCIATEDALARM CIM**](cim-associatedalarm.md)
</dt> <dd>

La [**dependencia \_ AssociatedAlarm de CIM**](cim-associatedalarm.md) asocia una alarma a un dispositivo lógico.

</dd> <dt>

[**\_ASSOCIATEDBATTERY CIM**](cim-associatedbattery.md)
</dt> <dd>

La [**dependencia \_ AssociatedBattery de CIM**](cim-associatedbattery.md) asocia una batería a un dispositivo lógico. Utilice esta asociación para modelar baterías individuales que componen un sistema de alimentación ininterrumpida (SAI).

</dd> <dt>

[**\_ASSOCIATEDCOOLING CIM**](cim-associatedcooling.md)
</dt> <dd>

La [**Asociación \_ AssociatedCooling de CIM**](cim-associatedcooling.md) indica si los ventiladores u otros dispositivos de refrigeración son específicos de un dispositivo (en lugar de proporcionar la refrigeración del gabinete o del contenedor).

</dd> <dt>

[**\_ASSOCIATEDMEMORY CIM**](cim-associatedmemory.md)
</dt> <dd>

La [**clase \_ AssociateMemory de CIM**](cim-associatedmemory.md) asocia la memoria instalada o asociada, como la memoria caché con un dispositivo lógico.

</dd> <dt>

[**\_ASSOCIATEDPROCESSORMEMORY CIM**](cim-associatedprocessormemory.md)
</dt> <dd>

La [**clase \_ AssociatedProcessorMemory de CIM**](cim-associatedprocessormemory.md) asocia el procesador y la memoria del sistema, o la memoria caché de un procesador.

</dd> <dt>

[**\_ASSOCIATEDSENSOR CIM**](cim-associatedsensor.md)
</dt> <dd>

La [**clase \_ AssociatedSensor de CIM**](cim-associatedsensor.md) asocia un sensor instalado a un dispositivo lógico. El sensor mide las propiedades críticas de entrada y salida, y puede incluirse con el dispositivo o instalarse cerca.

</dd> <dt>

[**\_ASSOCIATEDSUPPLYCURRENTSENSOR CIM**](cim-associatedsupplycurrentsensor.md)
</dt> <dd>

La [**clase \_ AssociatedSupplyCurrentSensor de CIM**](cim-associatedsupplycurrentsensor.md) asocia una fuente de alimentación con un sensor actual (amperaje) que supervisa la frecuencia de entrada.

</dd> <dt>

[**\_ASSOCIATEDSUPPLYVOLTAGESENSOR CIM**](cim-associatedsupplyvoltagesensor.md)
</dt> <dd>

Asocia una fuente de alimentación a un sensor de voltaje que supervisa su voltaje de entrada.

</dd> <dt>

[**\_BasedOn CIM**](cim-basedon.md)
</dt> <dd>

La [**clase \_ basada en CIM**](cim-basedon.md) representa una asociación que describe cómo se pueden ensamblar las extensiones de almacenamiento de las extensiones de nivel inferior. Por ejemplo, las extensiones físicas incluyen extensiones de espacio protegido. Por lo tanto, los conjuntos de volúmenes se ensamblan a partir de una o más extensiones de espacio físico o protegido. La memoria caché se puede definir de forma independiente y realizada en un elemento físico, o bien se puede basar en extensiones de almacenamiento volátiles o no volátiles.

</dd> <dt>

[**\_Batería CIM**](cim-battery.md)
</dt> <dd>

La clase de [**\_ batería CIM**](cim-battery.md) representa las capacidades y la administración del dispositivo lógico de batería. Esta clase se aplica a las baterías de los sistemas portátiles y a otras baterías internas y externas.

</dd> <dt>

[**\_BINARYSENSOR CIM**](cim-binarysensor.md)
</dt> <dd>

La clase [**CIM \_ BinarySensor**](cim-binarysensor.md) proporciona una salida booleana. Las propiedades **CurrentState** y **PossibleStates** se agregaron para el sensor, por lo que la subclase **CIM \_ BinarySensor** ya no es necesaria, aunque se conserva por compatibilidad con versiones anteriores. Se puede crear un sensor binario creando una instancia de un sensor con dos Estados posibles.

</dd> <dt>

[**\_BIOSELEMENT CIM**](cim-bioselement.md)
</dt> <dd>

La clase [**CIM \_ BIOSElement**](cim-bioselement.md) representa el software de bajo nivel que se carga en el almacenamiento no volátil y que se usa para iniciar y configurar un sistema de equipo.

</dd> <dt>

[**\_BIOSFEATURE CIM**](cim-biosfeature.md)
</dt> <dd>

representa las capacidades del software de bajo nivel que se usa para iniciar y configurar un sistema de equipo.

</dd> <dt>

[**\_BIOSFEATUREBIOSELEMENTS CIM**](cim-biosfeaturebioselements.md)
</dt> <dd>

La [**clase \_ BIOSFeatureBIOSElements de CIM**](cim-biosfeaturebioselements.md) asocia una característica de BIOS y sus elementos de BIOS agregados.

</dd> <dt>

[**\_BIOSLOADEDINNV CIM**](cim-biosloadedinnv.md)
</dt> <dd>

La clase [**CIM \_ BIOSLoadedInNV**](cim-biosloadedinnv.md) asocia un elemento BIOS y el almacenamiento no volátil en el que se carga.

</dd> <dt>

[**\_BOOTOSFROMFS CIM**](cim-bootosfromfs.md)
</dt> <dd>

La [**clase \_ BootOSFromFS de CIM**](cim-bootosfromfs.md) asocia el sistema operativo y los sistemas de archivos desde los que se carga el sistema operativo. La asociación es de varios a varios; un sistema operativo distribuido puede depender de varios sistemas de archivos para que se carguen correctamente y por completo.

</dd> <dt>

[**\_BOOTSAP CIM**](cim-bootsap.md)
</dt> <dd>

La clase [**CIM \_ BootSAP**](cim-bootsap.md) representa los puntos de acceso de un servicio de arranque.

</dd> <dt>

[**\_BOOTSERVICE CIM**](cim-bootservice.md)
</dt> <dd>

La clase [**CIM \_ BootService**](cim-bootservice.md) representa la funcionalidad proporcionada por un dispositivo o software, o por una red, para cargar un sistema operativo en un sistema de equipo unitario.

</dd> <dt>

[**\_BOOTSERVICEACCESSBYSAP CIM**](cim-bootserviceaccessbysap.md)
</dt> <dd>

La [**clase \_ BootServiceAccessBySAP de CIM**](cim-bootserviceaccessbysap.md) asocia un servicio de arranque y sus puntos de acceso.

</dd> <dt>

[**\_CACHEMEMORY CIM**](cim-cachememory.md)
</dt> <dd>

La clase [**CIM \_ CacheMemory**](cim-cachememory.md) define las capacidades y la administración de la memoria caché.

</dd> <dt>

[**\_Tarjeta CIM**](cim-card.md)
</dt> <dd>

La clase de [**\_ tarjeta CIM**](cim-card.md) representa un tipo de contenedor físico que se puede conectar a otra tarjeta o panel de hospedaje, o es en sí mismo una placa de hospedaje o placa base en un chasis. Esta clase incluye cualquier paquete capaz de llevar señales y proporcionar un punto de montaje para los componentes físicos, como chips u otros paquetes físicos, como otras tarjetas.

</dd> <dt>

[**\_CARDINSLOT CIM**](cim-cardinslot.md)
</dt> <dd>

La clase [**CIM \_ CardInSlot**](cim-cardinslot.md) asocia una tarjeta de adaptador con el contenedor en el que se inserta.

</dd> <dt>

[**\_CARDONCARD CIM**](cim-cardoncard.md)
</dt> <dd>

La [**Asociación \_ CardOnCard de CIM**](cim-cardoncard.md) describe las relaciones de las tarjetas que se pueden conectar a las motherboards/placas base, daughtercards de un adaptador o tarjetas que admiten módulos especiales de tipo tarjeta.

</dd> <dt>

[**\_CDROMDRIVE CIM**](cim-cdromdrive.md)
</dt> <dd>

La clase [**CIM \_ CDROMDrive**](cim-cdromdrive.md) representa una unidad de CD-ROM del equipo.

</dd> <dt>

[**\_Chasis CIM**](cim-chassis.md)
</dt> <dd>

La clase del [**\_ chasis CIM**](cim-chassis.md) representa los elementos físicos que contienen otros elementos y proporcionan funcionalidad definible, como un escritorio, un nodo de procesamiento, un SAI, un almacenamiento en disco o en cinta, o una combinación de estos.

</dd> <dt>

[**\_CHASSISINRACK CIM**](cim-chassisinrack.md)
</dt> <dd>

La [**Asociación \_ ChassisInRack de CIM**](cim-chassisinrack.md) representa la relación "que contiene" entre un bastidor y un chasis que contiene.

</dd> <dt>

[**Comprobación de CIM \_**](cim-check.md)
</dt> <dd>

La clase de [**\_ comprobación CIM**](cim-check.md) representa una condición o característica que se espera que sea verdadera en un entorno definido o en el ámbito de una instancia de una clase de [**\_ ComputerSystem de CIM**](cim-computersystem.md) . Las comprobaciones asociadas a un elemento de software determinado se organizan en uno de dos grupos mediante la propiedad **Phase** de la Asociación [**\_ SoftwareElementChecks de CIM**](cim-softwareelementchecks.md) .

</dd> <dt>

[**\_Chip CIM**](cim-chip.md)
</dt> <dd>

La clase de [**\_ chip CIM**](cim-chip.md) representa el tipo de hardware de circuito integrado, incluidos Asics, procesadores, chips de memoria, etc.

</dd> <dt>

[**\_CLUSTERINGSAP CIM**](cim-clusteringsap.md)
</dt> <dd>

La clase [**CIM \_ ClusteringSAP**](cim-clusteringsap.md) representa los puntos de acceso de un servicio de agrupación en clústeres.

</dd> <dt>

[**\_CLUSTERINGSERVICE CIM**](cim-clusteringservice.md)
</dt> <dd>

La clase [**CIM \_ ClusteringService**](cim-clusteringservice.md) representa la funcionalidad proporcionada por un clúster. Por ejemplo, la funcionalidad de conmutación por error se puede modelar como un servicio de un clúster de conmutación por error.

</dd> <dt>

[**\_CLUSTERSERVICEACCESSBYSAP CIM**](cim-clusterserviceaccessbysap.md)
</dt> <dd>

La clase [**CIM \_ ClusterServiceAccessBySAP**](cim-clusterserviceaccessbysap.md) representa la relación entre un servicio de agrupación en clústeres y sus puntos de acceso.

</dd> <dt>

[**\_COLLECTEDCOLLECTIONS CIM**](cim-collectedcollections.md)
</dt> <dd>

La [**clase \_ CollectedCollections de CIM**](cim-collectedcollections.md) es una asociación de agregación que representa una colección de elementos del sistema administrados (MSE) contenidos en una colección de MSEs.

</dd> <dt>

[**\_COLLECTEDMSES CIM**](cim-collectedmses.md)
</dt> <dd>

La clase de asociación [**CIM \_ CollectedMSEs**](cim-collectedmses.md) representa los miembros del objeto de agrupación, una clase [**CollectionOfMSEs**](cim-collectionofmses.md) .

</dd> <dt>

[**CollectionOfMSEs de CIM \_**](cim-collectionofmses.md)
</dt> <dd>

El objeto [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) permite la agrupación de objetos [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md) con el fin de asociar configuraciones y configuraciones. Es abstracto requerir más definición y perfeccionamiento semántico en las subclases.

</dd> <dt>

[**\_COLLECTIONOFSENSORS CIM**](cim-collectionofsensors.md)
</dt> <dd>

La [**Asociación \_ CollectionOfSensors de CIM**](cim-collectionofsensors.md) representa los sensores binarios que componen el sensor de múltiples Estados.

</dd> <dt>

[**\_COLLECTIONSETTING CIM**](cim-collectionsetting.md)
</dt> <dd>

La clase [**CIM \_ CollectionSetting**](cim-collectionsetting.md) representa la asociación entre un [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) y la clase de configuración definida para ellos.

</dd> <dt>

[**\_COMPATIBLEPRODUCT CIM**](cim-compatibleproduct.md)
</dt> <dd>

La clase [**CIM \_ CompatibleProduct**](cim-compatibleproduct.md) representa una asociación entre productos que indica si dos productos a los que se hace referencia son interoperables, por ejemplo, si se pueden instalar juntos o si puede ser el contenedor físico del otro, etc.

</dd> <dt>

[**\_Componente CIM**](cim-component.md)
</dt> <dd>

La Asociación de [**\_ componentes CIM**](cim-component.md) representa las partes de una relación entre MSEs.

</dd> <dt>

[**ComputerSystem de CIM \_**](cim-computersystem.md)
</dt> <dd>

Una clase de [**\_ ComputerSystem de CIM**](cim-computersystem.md) representa una colección especial de instancias de los [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md) . Esta colección proporciona funciones de equipo y actúa como un punto de agregación para asociar uno o varios de los siguientes elementos: sistema de archivos, sistema operativo, procesador y memoria (almacenamiento volátil y no volátil). Esta clase se deriva del [**\_ Sistema CIM**](cim-system.md).

</dd> <dt>

[**\_COMPUTERSYSTEMDMA CIM**](cim-computersystemdma.md)
</dt> <dd>

La clase [**CIM \_ ComputerSystemDMA**](cim-computersystemdma.md) representa una asociación entre un equipo y sus canales de acceso directo a memoria (DMA) disponibles.

</dd> <dt>

[**\_COMPUTERSYSTEMIRQ CIM**](cim-computersystemirq.md)
</dt> <dd>

La clase [**CIM \_ ComputerSystemIRQ**](cim-computersystemirq.md) representa una asociación entre un equipo y sus líneas de solicitud de interrupción (IRQ) disponibles.

</dd> <dt>

[**\_COMPUTERSYSTEMMAPPEDIO CIM**](cim-computersystemmappedio.md)
</dt> <dd>

La clase [**CIM \_ ComputerSystemMappedIO**](cim-computersystemmappedio.md) representa una asociación entre un equipo y sus puertos de e/s asignados a memoria disponibles.

</dd> <dt>

[**\_COMPUTERSYSTEMPACKAGE CIM**](cim-computersystempackage.md)
</dt> <dd>

La clase [**CIM \_ ComputerSystemPackage**](cim-computersystempackage.md) representa una asociación que define explícitamente la relación entre los sistemas de equipos unitarios y uno o varios paquetes físicos. La asociación es similar a la forma en que los dispositivos lógicos se encontraban en los elementos físicos.

</dd> <dt>

[**\_COMPUTERSYSTEMRESOURCE CIM**](cim-computersystemresource.md)
</dt> <dd>

La clase [**CIM \_ ComputerSystemResource**](cim-computersystemresource.md) representa una asociación entre un equipo y sus recursos del sistema disponibles.

</dd> <dt>

[**Configuración de CIM \_**](cim-configuration.md)
</dt> <dd>

El objeto de [**\_ configuración de CIM**](cim-configuration.md) permite agrupar los conjuntos de parámetros (definidos en objetos de [**\_ configuración de CIM**](cim-setting.md) ) y las dependencias de uno o más elementos del sistema administrados.

</dd> <dt>

[**\_Connected de CIM**](cim-connectedto.md)
</dt> <dd>

La clase de [**CIM \_ Connected**](cim-connectedto.md) representa una asociación que indica que dos o más conectores físicos están conectados.

</dd> <dt>

[**\_CONNECTORONPACKAGE CIM**](cim-connectoronpackage.md)
</dt> <dd>

La clase [**CIM \_ ConnectorOnPackage**](cim-connectoronpackage.md) representa una asociación que hace explícita la relación de contención entre los conectores y los paquetes. Los paquetes físicos contienen conectores y otros elementos físicos.

</dd> <dt>

[**\_Contenedor CIM**](cim-container.md)
</dt> <dd>

La clase de [**\_ contenedor CIM**](cim-container.md) representa una asociación entre un elemento contenido y un elemento físico contenedor. Un objeto contenedor debe ser un paquete físico.

</dd> <dt>

[**\_CONTROLLEDBY CIM**](cim-controlledby.md)
</dt> <dd>

La relación de [**\_ ControlledBy de CIM**](cim-controlledby.md) indica los dispositivos a los que se puede acceder o a los que se accede mediante el dispositivo lógico del controlador.

</dd> <dt>

[**\_Controlador CIM**](cim-controller.md)
</dt> <dd>

La clase de [**\_ controlador CIM**](cim-controller.md) es una clase primaria para agrupar dispositivos varios relacionados con el control. Algunos ejemplos de controladores son controladores SCSI, controladores USB y controladores serie.

</dd> <dt>

[**\_COOLINGDEVICE CIM**](cim-coolingdevice.md)
</dt> <dd>

La clase [**CIM \_ CoolingDevice**](cim-coolingdevice.md) representa las capacidades y la administración de dispositivos de enfriamiento.

</dd> <dt>

[**\_COPYFILEACTION CIM**](cim-copyfileaction.md)
</dt> <dd>

La clase [**CIM \_ CopyFileAction**](cim-copyfileaction.md) representa el traslado o la copia de archivos de un sistema informático a una nueva ubicación.

</dd> <dt>

[**\_CREATEDIRECTORYACTION CIM**](cim-createdirectoryaction.md)
</dt> <dd>

La clase [**CIM \_ CreateDirectoryAction**](cim-createdirectoryaction.md) crea directorios vacíos para que los elementos de software se instalen de forma local.

</dd> <dt>

[**\_CURRENTSENSOR CIM**](cim-currentsensor.md)
</dt> <dd>

La [**clase \_ CurrentSensor de CIM**](cim-currentsensor.md) existe para la compatibilidad con versiones anteriores con las definiciones de esquema CIM anteriores.

</dd> <dt>

[**\_Archivo de archivos CIM**](cim-datafile.md)
</dt> <dd>

La clase de [**\_ archivo**](cim-datafile.md) de datos CIM representa una colección con nombre de datos o código ejecutable. Solo se devolverán las instancias de los archivos de los discos fijos locales

</dd> <dt>

[**Dependencia de CIM \_**](cim-dependency.md)
</dt> <dd>

La clase de [**\_ dependencia CIM**](cim-dependency.md) representa una asociación que establece relaciones de dependencia entre objetos.

</dd> <dt>

[**\_DEPENDENCYCONTEXT CIM**](cim-dependencycontext.md)
</dt> <dd>

La [**relación \_ DependencyContext de CIM**](cim-dependencycontext.md) asocia una clase de [**\_ dependencia CIM**](cim-dependency.md) a uno o más objetos de [**\_ configuración de CIM**](cim-configuration.md) . Por ejemplo, las dependencias de un equipo pueden cambiar en función de la red a la que está conectado el sistema.

</dd> <dt>

[**\_DESKTOPMONITOR CIM**](cim-desktopmonitor.md)
</dt> <dd>

La clase [**CIM \_ DesktopMonitor**](cim-desktopmonitor.md) representa las capacidades y la administración del dispositivo lógico monitor de escritorio (CRT).

</dd> <dt>

[**\_DEVICEACCESSEDBYFILE CIM**](cim-deviceaccessedbyfile.md)
</dt> <dd>

La clase de asociación [**CIM \_ DeviceAccessedByFile**](cim-deviceaccessedbyfile.md) especifica el dispositivo lógico al que se tiene acceso mediante la clase [**\_ DeviceFile CIM**](cim-devicefile.md) a la que se hace referencia.

</dd> <dt>

[**DeviceConnection de CIM \_**](cim-deviceconnection.md)
</dt> <dd>

La clase de Asociación de [**CIM \_ DeviceConnection**](cim-deviceconnection.md) representa dos o más dispositivos conectados.

</dd> <dt>

[**\_DEVICEERRORCOUNTS CIM**](cim-deviceerrorcounts.md)
</dt> <dd>

La clase [**CIM \_ DeviceErrorCounts**](cim-deviceerrorcounts.md) es una clase estadística que contiene contadores relacionados con errores para un dispositivo lógico. Los tipos de errores se definen mediante CCITt (REC X. 733) e ISO (IEC 10164-4).

</dd> <dt>

[**\_DEVICEFILE CIM**](cim-devicefile.md)
</dt> <dd>

La clase [**CIM \_ DeviceFile**](cim-devicefile.md) representa un tipo de archivo lógico, que representa un dispositivo. Esta Convención es útil para los sistemas operativos que administran dispositivos mediante un modelo de e/s de secuencia de bytes. El dispositivo lógico asociado a este archivo se especifica mediante la relación [**\_ DeviceAccessedByFile de CIM**](cim-deviceaccessedbyfile.md) .

</dd> <dt>

[**\_DEVICESAPIMPLEMENTATION CIM**](cim-devicesapimplementation.md)
</dt> <dd>

La clase [**CIM \_ DeviceSAPImplementation**](cim-devicesapimplementation.md) representa una asociación entre un punto de acceso de servicio (SAP) y cómo se implementa. Cuando muchos dispositivos lógicos están asociados a un SAP, los elementos funcionan conjuntamente para proporcionar el punto de acceso. Si existen implementaciones diferentes de un SAP, cada implementación da como resultado la creación de instancias individuales del objeto SAP.

</dd> <dt>

[**\_DEVICESERVICEIMPLEMENTATION CIM**](cim-deviceserviceimplementation.md)
</dt> <dd>

La clase [**CIM \_ DeviceServiceImplementation**](cim-deviceserviceimplementation.md) representa una asociación entre un servicio y cómo se implementa. Cuando hay varios dispositivos asociados a un servicio, los elementos funcionan conjuntamente para proporcionar el servicio. Si existen implementaciones diferentes de un servicio, cada implementación tiene como resultado la creación de instancias individuales del objeto de servicio.

</dd> <dt>

[**\_DEVICESOFTWARE CIM**](cim-devicesoftware.md)
</dt> <dd>

La [**relación \_ DeviceSoftware de CIM**](cim-devicesoftware.md) identifica el software que está asociado a un dispositivo, como controladores, software de la aplicación o de configuración, o firmware.

</dd> <dt>

[**\_Directorio CIM**](cim-directory.md)
</dt> <dd>

La clase de [**\_ directorio CIM**](cim-directory.md) representa un tipo de archivo que agrupa lógicamente los archivos de datos que contiene y proporciona información de la ruta de acceso para los archivos agrupados.

</dd> <dt>

[**\_DIRECTORYACTION CIM**](cim-directoryaction.md)
</dt> <dd>

La clase abstracta [**\_ DirectoryAction de CIM**](cim-directoryaction.md) administra los directorios. La clase [**CIM \_ CreateDirectoryAction**](cim-createdirectoryaction.md) controla la creación de directorios y la eliminación del directorio se controla mediante la clase [**\_ RemoveDirectoryAction de CIM**](cim-removedirectoryaction.md) .

</dd> <dt>

[**\_DIRECTORYCONTAINSFILE CIM**](cim-directorycontainsfile.md)
</dt> <dd>

La clase [**CIM \_ DirectoryContainsFile**](cim-directorycontainsfile.md) representa una asociación entre un directorio y los archivos contenidos en ese directorio.

</dd> <dt>

[**\_DIRECTORYSPECIFICATION CIM**](cim-directoryspecification.md)
</dt> <dd>

La clase [**CIM \_ DirectorySpecification**](cim-directoryspecification.md) captura la estructura de directorios principal de un elemento de software. Esta clase se usa para organizar los archivos de un elemento de software en unidades administrables que se pueden reubicar en un sistema informático.

</dd> <dt>

[**\_DIRECTORYSPECIFICATIONFILE CIM**](cim-directoryspecificationfile.md)
</dt> <dd>

La [**Asociación \_ DirectorySpecificationFile de CIM**](cim-directoryspecificationfile.md) representa el directorio que contiene el archivo especificado al hacer referencia a la clase [**\_ DirectorySpecification de CIM**](cim-directoryspecification.md) .

</dd> <dt>

[**\_DISCRETESENSOR CIM**](cim-discretesensor.md)
</dt> <dd>

La clase [**CIM \_ DiscreteSensor**](cim-discretesensor.md) tiene un conjunto de valores de cadena válidos que puede notificar. Los valores se enumeran en la propiedad **PossibleValues** del sensor. Un sensor discreto siempre tiene una lectura actual que corresponde a uno de los valores enumerados.

</dd> <dt>

[**\_DISKDRIVE CIM**](cim-diskdrive.md)
</dt> <dd>

La clase [**CIM \_ DiskDrive**](cim-diskdrive.md) representa una unidad de disco física tal como la muestra el sistema operativo. Las características de la unidad de disco se corresponden con las características lógicas y de administración de la unidad, y en algunos casos, es posible que no reflejen las características físicas del dispositivo. Una interfaz a una unidad física es miembro de esta clase. Sin embargo, un objeto basado en otro dispositivo lógico no es miembro de esta clase.

</dd> <dt>

[**\_DISKETTEDRIVE CIM**](cim-diskettedrive.md)
</dt> <dd>

La clase [**CIM \_ DisketteDrive**](cim-diskettedrive.md) representa las capacidades y la administración de una unidad de disquete.

</dd> <dt>

[**\_DISKPARTITION CIM**](cim-diskpartition.md)
</dt> <dd>

La clase [**CIM \_ DiskPartition**](cim-diskpartition.md) representa un intervalo contiguo de bloques lógicos que el sistema operativo identifica mediante el tipo de la partición y los campos de subtipo. Las particiones de disco deben realizarse directamente mediante medios físicos (indicados por la Asociación [**\_ RealizesDiskPartition de CIM**](cim-realizesdiskpartition.md) ) o basados en volúmenes de almacenamiento.

</dd> <dt>

[**\_DISKSPACECHECK CIM**](cim-diskspacecheck.md)
</dt> <dd>

La [**clase \_ DiskSpaceCheck de CIM**](cim-diskspacecheck.md) comprueba la cantidad de espacio en disco disponible del sistema y lo especifica en la propiedad **AvailableDiskSpace** . Los detalles se comparan con el valor de la propiedad **AvailableSpace** del objeto de sistema de [**\_ archivos CIM**](cim-filesystem.md) que está asociado al objeto [**\_ ComputerSystem de CIM**](cim-computersystem.md) , que describe el entorno del sistema. Cuando el valor de la propiedad **AvailableSpace** es mayor o igual que el valor especificado en la propiedad **AvailableDiskSpace** , se cumple la condición.

</dd> <dt>

[**Presentación de CIM \_**](cim-display.md)
</dt> <dd>

La clase de [**\_ presentación CIM**](cim-display.md) es una clase primaria para agrupar dispositivos de pantalla varios.

</dd> <dt>

[**DMA de CIM \_**](cim-dma.md)
</dt> <dd>

La clase de [**\_ DMA de CIM**](cim-dma.md) representa el acceso directo a memoria (DMA) de la arquitectura del equipo.

</dd> <dt>

[**CIM \_ acoplado**](cim-docked.md)
</dt> <dd>

La [**Asociación \_ acoplada CIM**](cim-docked.md) representa la relación entre dos chasis. Por ejemplo, un portátil (un tipo de chasis) se puede acoplar en una estación de acoplamiento (otro tipo de chasis). Esta relación típica se describe explícitamente.

</dd> <dt>

[**\_ELEMENTCAPACITY CIM**](cim-elementcapacity.md)
</dt> <dd>

La [**clase \_ ElementCapacity de CIM**](cim-elementcapacity.md) asocia un objeto [**\_ PhysicalCapacity de CIM**](cim-physicalcapacity.md) con uno o más elementos físicos. Asocia una descripción de los requisitos de hardware mínimos y máximos (o las capacidades) a los elementos físicos que se describen.

</dd> <dt>

[**\_ELEMENTCONFIGURATION CIM**](cim-elementconfiguration.md)
</dt> <dd>

La [**Asociación \_ ElementConfiguration de CIM**](cim-elementconfiguration.md) relaciona un objeto de [**\_ configuración de CIM**](cim-configuration.md) con uno o más elementos del sistema administrados. El objeto de **\_ configuración de CIM** representa un comportamiento determinado o un estado funcional deseado para el [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md)asociado.

</dd> <dt>

[**\_ELEMENTSETTING CIM**](cim-elementsetting.md)
</dt> <dd>

La clase [**CIM \_ ElementSetting**](cim-elementsetting.md) representa la asociación entre los elementos del sistema administrados y la clase de configuración definida para ellos.

</dd> <dt>

[**\_ELEMENTSLINKED CIM**](cim-elementslinked.md)
</dt> <dd>

La [**Asociación \_ ElementsLinked de CIM**](cim-elementslinked.md) representa los elementos físicos que están cableados juntos por un vínculo físico.

</dd> <dt>

[**\_ERRORCOUNTERSFORDEVICE CIM**](cim-errorcountersfordevice.md)
</dt> <dd>

La clase [**CIM \_ ErrorCountersForDevice**](cim-errorcountersfordevice.md) asocia la clase [**\_ DeviceErrorCounts de CIM**](cim-deviceerrorcounts.md) al dispositivo lógico al que se aplica.

</dd> <dt>

[**\_EXECUTEPROGRAM CIM**](cim-executeprogram.md)
</dt> <dd>

La clase [**CIM \_ ExecuteProgram**](cim-executeprogram.md) representa los archivos que se pueden ejecutar en el sistema donde está instalado el elemento de software.

</dd> <dt>

[**Exportación de CIM \_**](cim-export.md)
</dt> <dd>

La clase de [**\_ exportación CIM**](cim-export.md) representa una asociación entre un sistema de archivos local y sus directorios, que indican que los directorios especificados están disponibles para su montaje. Al exportar un sistema de archivos completo, el directorio debe hacer referencia al directorio superior del sistema de archivos.

</dd> <dt>

[**\_EXTRACAPACITYGROUP CIM**](cim-extracapacitygroup.md)
</dt> <dd>

La clase [**CIM \_ ExtraCapacityGroup**](cim-extracapacitygroup.md) se deriva de un grupo de redundancia que indica que los elementos agregados tienen más capacidad o capacidad de la necesaria. Un ejemplo de este tipo de redundancia es la instalación de fuentes de alimentación N + 1 o ventiladores en un sistema.

</dd> <dt>

[**\_Ventilador CIM**](cim-fan.md)
</dt> <dd>

La clase del [**\_ ventilador CIM**](cim-fan.md) representa las capacidades y la administración de un dispositivo de refrigeración de ventilador.

</dd> <dt>

[**\_FILEACTION CIM**](cim-fileaction.md)
</dt> <dd>

La clase [**CIM \_ FileAction**](cim-fileaction.md) permite al autor ubicar los archivos que ya existen en el equipo de un usuario y, a continuación, trasladarlos o copiarlos a una nueva ubicación.

</dd> <dt>

[**\_FILESPECIFICATION CIM**](cim-filespecification.md)
</dt> <dd>

La clase [**CIM \_ FileSpecification**](cim-filespecification.md) representa un archivo que está activado o desactivado en el sistema. El archivo se encuentra en el directorio identificado por la [**Asociación \_ DirectorySpecificationFile de CIM**](cim-directoryspecificationfile.md) . El método [**Invoke**](invoke-method-in-class-cim-filespecification.md) usa la información para comprobar la existencia del archivo. Tenga en cuenta que las propiedades con un valor **null** no se comprueban.

</dd> <dt>

[**\_FILESTORAGE CIM**](cim-filestorage.md)
</dt> <dd>

La [**Asociación \_ FileStorage de CIM**](cim-filestorage.md) vincula el sistema de archivos y los archivos lógicos que se dirigen a través del sistema de archivos.

</dd> <dt>

[**\_Sistema de archivos CIM**](cim-filesystem.md)
</dt> <dd>

La clase de sistema de archivos [**CIM \_**](cim-filesystem.md) representa un archivo o un conjunto de datos local de un equipo o montado de forma remota desde un servidor de archivos.

</dd> <dt>

[**\_FLATPANEL CIM**](cim-flatpanel.md)
</dt> <dd>

La clase [**CIM \_ FlatPanel**](cim-flatpanel.md) representa las capacidades y la administración del dispositivo lógico de panel plano.

</dd> <dt>

[**\_FROMDIRECTORYACTION CIM**](cim-fromdirectoryaction.md)
</dt> <dd>

La [**Asociación \_ FromDirectoryAction de CIM**](cim-fromdirectoryaction.md) identifica el directorio de origen para la acción de archivo. Cuando se usa esta asociación, se supone que el directorio de origen fue creado por una acción anterior. Esta asociación no puede existir con una asociación [**\_ FromDirectorySpecification de CIM**](cim-fromdirectoryspecification.md) ; una acción de archivo solo puede incluir un único directorio de origen.

</dd> <dt>

[**\_FROMDIRECTORYSPECIFICATION CIM**](cim-fromdirectoryspecification.md)
</dt> <dd>

La [**Asociación \_ FromDirectorySpecification de CIM**](cim-fromdirectoryspecification.md) identifica el directorio de origen para la acción de archivo. Cuando se usa esta asociación, se supone que el directorio de origen ya existe. Esta asociación no puede existir con una asociación [**\_ FromDirectoryAction de CIM**](cim-fromdirectoryaction.md) ; una acción de archivo solo puede incluir un único directorio de origen.

</dd> <dt>

[**FRU de CIM \_**](cim-fru.md)
</dt> <dd>

La clase [**CIM \_ FRU**](cim-fru.md) representa una colección definida por el proveedor de productos y elementos físicos que están asociados a una unidad reemplazable en campo (FRU) para admitir, mantener o actualizar un producto en la ubicación del cliente.

</dd> <dt>

[**\_FRUINCLUDESPRODUCT CIM**](cim-fruincludesproduct.md)
</dt> <dd>

La clase [**CIM \_ FRUIncludesProduct**](cim-fruincludesproduct.md) indica que una unidad reemplazable en campo (FRU) puede estar formada por otros productos.

</dd> <dt>

[**\_FRUPHYSICALELEMENTS CIM**](cim-fruphysicalelements.md)
</dt> <dd>

La clase [**CIM \_ FRUPhysicalElements**](cim-fruphysicalelements.md) representa los elementos físicos que componen una unidad reemplazable en campo (FRU).

</dd> <dt>

[**\_HEATPIPE CIM**](cim-heatpipe.md)
</dt> <dd>

La clase [**CIM \_ HeatPipe**](cim-heatpipe.md) representa las capacidades y la administración de un dispositivo de refrigeración de canalización térmica.

</dd> <dt>

[**\_HOSTEDACCESSPOINT CIM**](cim-hostedaccesspoint.md)
</dt> <dd>

La clase [**CIM \_ HostedAccessPoint**](cim-hostedaccesspoint.md) representa una asociación entre un punto de acceso de servicio (SAP) y el sistema en el que se proporciona. Cada sistema puede hospedar muchos SAP.

</dd> <dt>

[**\_HOSTEDBOOTSAP CIM**](cim-hostedbootsap.md)
</dt> <dd>

La clase [**CIM \_ HostedBootSAP**](cim-hostedbootsap.md) define el sistema de equipo unitario de hospedaje para una clase [**\_ BootSAP de CIM**](cim-bootsap.md) . Puesto que esta relación se subclase de [**\_ HostedAccessPoint de CIM**](cim-hostedaccesspoint.md), hereda el esquema de ámbito y de nomenclatura definido para [**\_ punto de CIM**](cim-serviceaccesspoint.md), donde un punto de acceso se pospone a su sistema de hospedaje. En este caso, **\_ BootSAP CIM** debe diferir a su [**clase \_ UnitaryComputerSystem CIM**](cim-unitarycomputersystem.md) de hospedaje.

</dd> <dt>

[**\_HOSTEDBOOTSERVICE CIM**](cim-hostedbootservice.md)
</dt> <dd>

La [**clase \_ HostedBootService de CIM**](cim-hostedbootservice.md) asocia un sistema de hospedaje y un servicio de arranque. Puesto que esta relación se ha subclase de [**CIM \_ HostedService**](cim-hostedservice.md), hereda el esquema de ámbito y de nomenclatura definido para el servicio, donde un servicio se pospone a su sistema de hospedaje.

</dd> <dt>

[**\_HOSTEDFILESYSTEM CIM**](cim-hostedfilesystem.md)
</dt> <dd>

La [**Asociación \_ HostedFileSystem de CIM**](cim-hostedfilesystem.md) representa un vínculo entre el equipo y el sistema de archivos hospedado en el sistema del equipo.

</dd> <dt>

[**\_HOSTEDJOBDESTINATION CIM**](cim-hostedjobdestination.md)
</dt> <dd>

La clase [**CIM \_ HostedJobDestination**](cim-hostedjobdestination.md) representa una asociación entre un destino de trabajo y el sistema en el que reside. Un sistema puede hospedar muchas colas de trabajos. Los destinos del trabajo se aplazan al sistema de hospedaje.

</dd> <dt>

[**HostedService de CIM \_**](cim-hostedservice.md)
</dt> <dd>

La clase [**CIM \_ HostedService**](cim-hostedservice.md) representa una asociación entre un servicio y el sistema en el que reside la funcionalidad. Un sistema puede hospedar muchos servicios, que aplazan el sistema de hospedaje. El modelo no representa servicios hospedados en varios sistemas.

</dd> <dt>

[**\_INFRAREDCONTROLLER CIM**](cim-infraredcontroller.md)
</dt> <dd>

La clase [**CIM \_ InfraredController**](cim-infraredcontroller.md) representa las capacidades y la administración de un controlador de infrarrojos.

</dd> <dt>

[**\_Instalado CIM**](cim-installedos.md)
</dt> <dd>

La clase de Asociación de [**CIM \_ instalados**](cim-installedos.md) representa un vínculo entre el equipo y el sistema operativo instalado. Un sistema operativo se instala cuando está en la extensión de almacenamiento de un sistema (por ejemplo, se copia en una unidad de disco o se descarga en memoria).

</dd> <dt>

[**\_INSTALLEDSOFTWAREELEMENT CIM**](cim-installedsoftwareelement.md)
</dt> <dd>

La [**clase \_ InstalledSoftwareElement de CIM**](cim-installedsoftwareelement.md) asocia un equipo con un elemento de software instalado.

</dd> <dt>

[**\_IRQ CIM**](cim-irq.md)
</dt> <dd>

La clase de [**\_ IRQ CIM**](cim-irq.md) representa una línea de solicitud de interrupción (IRQ) de arquitectura Intel.

</dd> <dt>

[**Trabajo de CIM \_**](cim-job.md)
</dt> <dd>

La clase de [**\_ trabajo CIM**](cim-job.md) representa una unidad de trabajo para un sistema, como un trabajo de impresión. Un trabajo es distinto de un proceso porque se puede programar un trabajo.

</dd> <dt>

[**\_JOBDESTINATION CIM**](cim-jobdestination.md)
</dt> <dd>

La clase [**CIM \_ JobDestination**](cim-jobdestination.md) representa dónde se envía un trabajo para su procesamiento. Puede hacer referencia a una cola que contiene cero o más trabajos, como una cola de impresión que contiene los trabajos de impresión. Los destinos del trabajo se hospedan en sistemas, de forma similar a la manera en que los servicios se hospedan en los sistemas.

</dd> <dt>

[**\_JOBDESTINATIONJOBS CIM**](cim-jobdestinationjobs.md)
</dt> <dd>

La [**Asociación \_ JobDestinationJobs de CIM**](cim-jobdestinationjobs.md) describe dónde se envía un trabajo para su procesamiento (es decir, a qué destino del trabajo).

</dd> <dt>

[**\_Teclado CIM**](cim-keyboard.md)
</dt> <dd>

La clase de [**\_ teclado CIM**](cim-keyboard.md) representa las capacidades y la administración del dispositivo lógico del teclado.

</dd> <dt>

[**\_LINKHASCONNECTOR CIM**](cim-linkhasconnector.md)
</dt> <dd>

La [**clase \_ LinkHasConnector de CIM**](cim-linkhasconnector.md) asocia los cables y los vínculos usados como conectores físicos, que conectan los elementos físicos. Esta asociación define explícitamente la relación de los conectores para [**\_ PhysicalLink CIM**](cim-physicallink.md).

</dd> <dt>

[**\_LOCALFILESYSTEM CIM**](cim-localfilesystem.md)
</dt> <dd>

La clase [**CIM \_ LocalFileSystem**](cim-localfilesystem.md) representa el almacén de archivos controlado por un sistema informático a través de medios locales (por ejemplo, acceso directo al controlador de dispositivo). El almacén de archivos se puede administrar directamente mediante el sistema del equipo, sin necesidad de que otro equipo actúe como servidor de archivos. Sin embargo, para un sistema de archivos en clúster, el sistema de archivos es local y, por lo tanto, se pospone al clúster.

</dd> <dt>

[**Ubicación de CIM \_**](cim-location.md)
</dt> <dd>

La clase de [**\_ Ubicación CIM**](cim-location.md) representa la posición y la dirección de un elemento físico.

</dd> <dt>

[**LogicalDevice de CIM \_**](cim-logicaldevice.md)
</dt> <dd>

La clase de [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) representa una entidad de hardware que puede o no ser realizada en el hardware físico.

</dd> <dt>

[**LogicalDisk de CIM \_**](cim-logicaldisk.md)
</dt> <dd>

La clase de [**\_ LogicalDisk de CIM**](cim-logicaldisk.md) representa un intervalo contiguo de bloques lógicos que un sistema de archivos identifica mediante el campo de **DeviceID** (clave) del disco. Por ejemplo, en un entorno de Windows, el campo **DeviceID** contiene una letra de unidad; en un entorno de UNIX, contiene la ruta de acceso; y en un entorno de NetWare, contiene el nombre del volumen.

</dd> <dt>

[**\_LOGICALDISKBASEDONPARTITION CIM**](cim-logicaldiskbasedonpartition.md)
</dt> <dd>

La [**clase \_ LogicalDiskBasedOnPartition de CIM**](cim-logicaldiskbasedonpartition.md) asocia un disco lógico a la partición de disco en la que reside.

</dd> <dt>

[**\_LOGICALDISKBASEDONVOLUMESET CIM**](cim-logicaldiskbasedonvolumeset.md)
</dt> <dd>

La [**Asociación \_ LogicalDiskBasedOnVolumeSet de CIM**](cim-logicaldiskbasedonvolumeset.md) relaciona los discos lógicos con el volumen en el que se encuentran. Los discos lógicos pueden basarse en un único volumen (por ejemplo, expuesto por un administrador de volumen de software) o una partición de disco.

</dd> <dt>

[**\_LOGICALELEMENT CIM**](cim-logicalelement.md)
</dt> <dd>

La clase [**CIM \_ LogicalElement**](cim-logicalelement.md) es la clase base para todos los componentes del sistema que representan componentes del sistema abstractos, como perfiles, procesos o capacidades del sistema, en forma de dispositivos lógicos.

</dd> <dt>

[**\_LOGICALFILE CIM**](cim-logicalfile.md)
</dt> <dd>

La clase [**CIM \_ LogicalFile**](cim-logicalfile.md) representa una colección con nombre de datos, que puede ser código ejecutable, que se encuentra en un sistema de archivos en una extensión de almacenamiento.

</dd> <dt>

[**\_LOGICALIDENTITY CIM**](cim-logicalidentity.md)
</dt> <dd>

La clase [**CIM \_ LogicalIdentity**](cim-logicalidentity.md) es una asociación abstracta y genérica que indica que dos elementos lógicos representan distintos aspectos de la misma entidad subyacente.

</dd> <dt>

[**\_MAGNETOOPTICALDRIVE CIM**](cim-magnetoopticaldrive.md)
</dt> <dd>

La clase [**CIM \_ MagnetoOpticalDrive**](cim-magnetoopticaldrive.md) representa las capacidades y la administración de una unidad magneto-óptica, un subtipo del dispositivo de acceso a medios.

</dd> <dt>

[**ManagedSystemElement de CIM \_**](cim-managedsystemelement.md)
</dt> <dd>

La clase del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md) es la clase base para la jerarquía de elementos del sistema. Cualquier componente del sistema distinguible es un candidato para la inclusión en esta clase.

</dd> <dt>

[**\_MANAGEMENTCONTROLLER CIM**](cim-managementcontroller.md)
</dt> <dd>

La [**clase \_ ManagementController de CIM**](cim-managementcontroller.md) se relaciona con las capacidades y la administración de un controlador de administración.

</dd> <dt>

[**\_MEDIAACCESSDEVICE CIM**](cim-mediaaccessdevice.md)
</dt> <dd>

La clase [**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md) representa la capacidad de obtener acceso a uno o más medios y, a continuación, utilizar los medios para almacenar y recuperar datos.

</dd> <dt>

[**\_MEDIAPRESENT CIM**](cim-mediapresent.md)
</dt> <dd>

La [**Asociación \_ MediaPresent de CIM**](cim-mediapresent.md) describe una relación en la que se debe tener acceso a una extensión de almacenamiento a través de un dispositivo de acceso a medios.

</dd> <dt>

[**Memoria de CIM \_**](cim-memory.md)
</dt> <dd>

La clase de [**\_ memoria CIM**](cim-memory.md) representa las capacidades y la administración de los dispositivos lógicos relacionados con la memoria.

</dd> <dt>

[**\_MEMORYCAPACITY CIM**](cim-memorycapacity.md)
</dt> <dd>

La clase [**CIM \_ MemoryCapacity**](cim-memorycapacity.md) representa la memoria que se puede instalar en un elemento físico y sus configuraciones mínima y máxima. La información sobre la memoria que está instalada actualmente y los requisitos mínimos y máximos de un elemento se encuentra en las instancias de la clase [**\_ PhysicalMemory de CIM**](cim-physicalmemory.md) .

</dd> <dt>

[**\_MEMORYCHECK CIM**](cim-memorycheck.md)
</dt> <dd>

La clase [**CIM \_ MemoryCheck**](cim-memorycheck.md) especifica una condición para la cantidad mínima de memoria que debe estar disponible en un sistema.

</dd> <dt>

[**\_MEMORYMAPPEDIO CIM**](cim-memorymappedio.md)
</dt> <dd>

La clase [**CIM \_ MemoryMappedIO**](cim-memorymappedio.md) representa la arquitectura de equipo de e/s asignada a la memoria. Esta clase trata los recursos de memoria y de e/s de puerto.

</dd> <dt>

[**\_MEMORYONCARD CIM**](cim-memoryoncard.md)
</dt> <dd>

La [**clase \_ MemoryOnCard de CIM**](cim-memoryoncard.md) asocia la memoria física que se encuentra en los paneles de hospedaje, las tarjetas de adaptador, etc. Esta asociación define explícitamente la relación de memoria con las tarjetas.

</dd> <dt>

[**\_MEMORYWITHMEDIA CIM**](cim-memorywithmedia.md)
</dt> <dd>

La [**clase \_ MemoryWithMedia de CIM**](cim-memorywithmedia.md) asocia la memoria física con un medio físico y su cartucho. La memoria proporciona identificación de medios y almacena datos específicos del usuario.

</dd> <dt>

[**\_MODIFYSETTINGACTION CIM**](cim-modifysettingaction.md)
</dt> <dd>

La clase [**CIM \_ ModifySettingAction**](cim-modifysettingaction.md) representa la información para modificar un archivo de configuración concreto, para una entrada específica, con un valor específico.

</dd> <dt>

[**\_MONITORRESOLUTION CIM**](cim-monitorresolution.md)
</dt> <dd>

La clase [**CIM \_ MonitorResolution**](cim-monitorresolution.md) representa la relación entre las resoluciones horizontal y vertical, y la frecuencia de actualización y el modo de recorrido de un monitor de escritorio. Los valores se especifican en el objeto de controlador de vídeo.

</dd> <dt>

[**\_MONITORSETTING CIM**](cim-monitorsetting.md)
</dt> <dd>

La [**clase \_ MonitorSetting de CIM**](cim-monitorsetting.md) asocia la resolución del monitor con el monitor de escritorio al que se aplica.

</dd> <dt>

[**Montaje de CIM \_**](cim-mount.md)
</dt> <dd>

La clase de [**\_ montaje CIM**](cim-mount.md) representa una asociación entre un sistema de archivos y un directorio al que está asociado.

</dd> <dt>

[**\_MULTISTATESENSOR CIM**](cim-multistatesensor.md)
</dt> <dd>

La clase [**CIM \_ MultiStateSensor**](cim-multistatesensor.md) representa un conjunto de varios miembros de sensores binarios donde cada sensor binario informa de un resultado booleano.

</dd> <dt>

[**Adaptador de la CIM \_**](cim-networkadapter.md)
</dt> <dd>

La [**clase \_ CIM**](cim-networkadapter.md) Networking es una clase abstracta que define los conceptos generales de hardware de red (por ejemplo, la dirección permanente o la velocidad de funcionamiento). La información se transmite mediante la Asociación [**\_ DeviceSAPImplementation de CIM**](cim-devicesapimplementation.md) .

</dd> <dt>

[**NFS de CIM \_**](cim-nfs.md)
</dt> <dd>

La clase de [**\_ NFS de CIM**](cim-nfs.md) representa un sistema de archivos remoto que se monta mediante el protocolo Network File System (NFS), desde un equipo.

</dd> <dt>

[**\_NONVOLATILESTORAGE CIM**](cim-nonvolatilestorage.md)
</dt> <dd>

La clase [**CIM \_ NonVolatileStorage**](cim-nonvolatilestorage.md) representa las capacidades y la administración de almacenamiento no volátil. La memoria no volátil incluye de forma nativa el almacenamiento en Flash y ROM.

</dd> <dt>

[**NumericSensor de CIM \_**](cim-numericsensor.md)
</dt> <dd>

La clase [**CIM \_ NumericSensor**](cim-numericsensor.md) representa un sensor numérico que devuelve lecturas numéricas y, opcionalmente, admite valores de umbral.

</dd> <dt>

[**OperatingSystem de CIM \_**](cim-operatingsystem.md)
</dt> <dd>

La clase [**CIM \_ OperatingSystem**](cim-operatingsystem.md) representa un sistema operativo del equipo, que se compone de software y firmware que hace que el hardware del equipo sea utilizable.

</dd> <dt>

[**\_OPERATINGSYSTEMSOFTWAREFEATURE CIM**](cim-operatingsystemsoftwarefeature.md)
</dt> <dd>

La clase [**CIM \_ OperatingSystemSoftwareFeature**](cim-operatingsystemsoftwarefeature.md) representa las características de software que componen el sistema operativo.

</dd> <dt>

[**\_OSPROCESS CIM**](cim-osprocess.md)
</dt> <dd>

La [**clase \_ OSProcess de CIM**](cim-osprocess.md) asocia el sistema operativo y uno o más procesos que se ejecutan en el contexto del sistema operativo.

</dd> <dt>

[**\_OSVERSIONCHECK CIM**](cim-osversioncheck.md)
</dt> <dd>

La clase [**CIM \_ OSVersionCheck**](cim-osversioncheck.md) especifica las versiones del sistema operativo que pueden admitir un elemento de software.

</dd> <dt>

[**\_PACKAGEALARM CIM**](cim-packagealarm.md)
</dt> <dd>

La [**Asociación \_ PackageAlarm de CIM**](/windows/desktop/SecCrypto/extendedproperties-newenum) representa la relación en la que un dispositivo de alarma se instala como parte de un paquete. La instalación de indica problemas con el entorno del paquete, su estado de seguridad o su estado general.

</dd> <dt>

[**\_PACKAGECOOLING CIM**](cim-packagecooling.md)
</dt> <dd>

La [**Asociación \_ PackageCooling de CIM**](cim-packagecooling.md) representa la relación en la que se instala un dispositivo de enfriamiento en un paquete, como un chasis o un bastidor, para ayudar con la refrigeración del paquete.

</dd> <dt>

[**\_PACKAGEDCOMPONENT CIM**](cim-packagedcomponent.md)
</dt> <dd>

La [**Asociación \_ PackagedComponent de CIM**](cim-packagedcomponent.md) representa una relación explícita en la que un componente normalmente está contenido en un paquete físico, como un chasis o una tarjeta.

</dd> <dt>

[**\_PACKAGEINCHASSIS CIM**](cim-packageinchassis.md)
</dt> <dd>

La [**Asociación \_ PackageInChassis de CIM**](cim-packageinchassis.md) representa la relación en la que un chasis puede contener otros paquetes, como otros chasis y tarjetas.

</dd> <dt>

[**\_PACKAGEINSLOT CIM**](cim-packageinslot.md)
</dt> <dd>

La [**Asociación \_ PackageInSlot de CIM**](cim-packageinslot.md) representa la relación entre las tarjetas de dispositivo y el chasis en el que se montan.

</dd> <dt>

[**\_PACKAGETEMPSENSOR CIM**](cim-packagetempsensor.md)
</dt> <dd>

La [**Asociación \_ PackageTempSensor de CIM**](cim-packagetempsensor.md) representa la relación en la que un sensor de temperatura se instala a menudo en un paquete, como un chasis o un bastidor, para supervisar el entorno del paquete.

</dd> <dt>

[**\_PARALLELCONTROLLER CIM**](cim-parallelcontroller.md)
</dt> <dd>

La [**Asociación \_ ParallelController de CIM**](cim-parallelcontroller.md) se relaciona con las capacidades y la administración del dispositivo lógico de puerto paralelo.

</dd> <dt>

[**\_PARTICIPATESINSET CIM**](cim-participatesinset.md)
</dt> <dd>

La clase [**CIM \_ ParticipatesInSet**](cim-participatesinset.md) identifica los elementos físicos que se deben reemplazar juntos.

</dd> <dt>

[**\_PCICONTROLLER CIM**](cim-pcicontroller.md)
</dt> <dd>

La clase [**CIM \_ PCIController**](cim-pcicontroller.md) representa las propiedades y la administración de un controlador PCI. Las propiedades de esta clase y sus subclases se definen en las diversas especificaciones de PCI publicadas por PCI SIG.

</dd> <dt>

[**\_PCMCIACONTROLLER CIM**](cim-pcmciacontroller.md)
</dt> <dd>

La clase [**CIM \_ PCMCIAController**](cim-pcmciacontroller.md) representa las capacidades y la administración de un controlador de la Asociación Internacional de tarjetas de memoria (PCMCIA) del equipo.

</dd> <dt>

[**\_PCVIDEOCONTROLLER CIM**](cim-pcvideocontroller.md)
</dt> <dd>

El [**\_ PCVideoController CIM**](cim-pcvideocontroller.md) representa las capacidades y la administración de un controlador de vídeo de equipo personal, un subtipo de controlador de vídeo.

</dd> <dt>

[**\_PEXTENTREDUNDANCYCOMPONENT CIM**](cim-pextentredundancycomponent.md)
</dt> <dd>

La clase [**CIM \_ PExtentRedundancyComponent**](cim-pextentredundancycomponent.md) representa las extensiones físicas que participan en un grupo de redundancia de almacenamiento.

</dd> <dt>

[**\_PHYSICALCAPACITY CIM**](cim-physicalcapacity.md)
</dt> <dd>

La clase [**CIM \_ PhysicalCapacity**](cim-physicalcapacity.md) es una clase abstracta que representa los requisitos mínimo y máximo de un elemento físico y su capacidad para admitir distintos tipos de hardware. Por ejemplo, los requisitos de memoria mínima y máxima se pueden modelar como una subclase de **\_ PhysicalCapacity de CIM**.

</dd> <dt>

[**\_PHYSICALCOMPONENT CIM**](cim-physicalcomponent.md)
</dt> <dd>

La clase [**CIM \_ PhysicalComponent**](cim-physicalcomponent.md) representa un componente de bajo nivel o básico dentro de un paquete. Un elemento físico que no es un vínculo, conector o paquete es un descendiente (o miembro) de esta clase.

</dd> <dt>

[**\_PHYSICALCONNECTOR CIM**](cim-physicalconnector.md)
</dt> <dd>

La clase [**CIM \_ PhysicalConnector**](cim-physicalconnector.md) representa cualquier elemento físico que se utiliza para conectarse a otros elementos. Cualquier objeto que pueda conectarse y transmitir señales o potencia entre dos o más elementos físicos es un descendiente (o miembro) de esta clase.

</dd> <dt>

[**\_PHYSICALELEMENT CIM**](cim-physicalelement.md)
</dt> <dd>

Las subclases [**\_ PhysicalElement de CIM**](cim-physicalelement.md) definen cualquier componente de un sistema que tenga una identidad física distinta. Las instancias de esta clase se pueden definir en términos de etiquetas que se pueden adjuntar físicamente al objeto.

</dd> <dt>

[**\_PHYSICALELEMENTLOCATION CIM**](cim-physicalelementlocation.md)
</dt> <dd>

La [**clase \_ PhysicalElementLocation de CIM**](cim-physicalelementlocation.md) asocia un elemento físico a un objeto de [**\_ Ubicación CIM**](cim-location.md) para fines de inventario o de reemplazo.

</dd> <dt>

[**\_PHYSICALEXTENT CIM**](cim-physicalextent.md)
</dt> <dd>

La clase [**CIM \_ PhysicalExtent**](cim-physicalextent.md) representa una implementación RAID de SCC. Define las direcciones de bloque direccionables consecutivas en un único dispositivo de almacenamiento que se tratan como una única extensión de almacenamiento en la misma clase [**\_ StorageRedundancyGroup de CIM**](cim-storageredundancygroup.md) . Una alternativa, cuando se utiliza la configuración automática, es crear una instancia de la [**clase \_ AggregatePExtent de CIM**](cim-aggregatepextent.md) o extenderla.

</dd> <dt>

[**\_PHYSICALFRAME CIM**](cim-physicalframe.md)
</dt> <dd>

La clase [**CIM \_ PhysicalFrame**](cim-physicalframe.md) es una clase primaria de bastidores, chasis y otros alojamientos de fotogramas, tal y como se definen en las clases de extensión. En esta clase primaria se incluyen propiedades como **VisibleAlarm** y **AudibleAlarm**, y datos relacionados con las infracciones de seguridad.

</dd> <dt>

[**\_PHYSICALLINK CIM**](cim-physicallink.md)
</dt> <dd>

La clase [**CIM \_ PhysicalLink**](cim-physicallink.md) representa el cableado de los elementos físicos.

</dd> <dt>

[**\_PHYSICALMEDIA CIM**](cim-physicalmedia.md)
</dt> <dd>

La clase [**CIM \_ PhysicalMedia**](cim-physicalmedia.md) representa los tipos de documentación y el medio de almacenamiento, como cintas, CD-ROM, etc.

</dd> <dt>

[**\_PHYSICALMEMORY CIM**](cim-physicalmemory.md)
</dt> <dd>

La clase [**CIM \_ PhysicalMemory**](cim-physicalmemory.md) representa dispositivos de memoria de bajo nivel, como SIMM, DIMM, chips de memoria sin procesar, etc.

</dd> <dt>

[**\_PHYSICALPACKAGE CIM**](cim-physicalpackage.md)
</dt> <dd>

La clase [**CIM \_ PhysicalPackage**](cim-physicalpackage.md) representa los elementos físicos que contienen u hospedan otros componentes. Algunos ejemplos son un alojamiento en bastidor o una tarjeta adaptadora.

</dd> <dt>

[**\_POINTINGDEVICE CIM**](cim-pointingdevice.md)
</dt> <dd>

La clase [**CIM \_ PointingDevice**](cim-pointingdevice.md) representa un dispositivo que apunta a las regiones de la pantalla. Cualquier dispositivo que manipula un puntero, o apunta a regiones de una presentación visual, es un miembro de esta clase. Por ejemplo, un mouse, un lápiz, un teclado táctil o una tableta.

</dd> <dt>

[**\_POTSMODEM CIM**](cim-potsmodem.md)
</dt> <dd>

La clase [**CIM \_ POTSModem**](cim-potsmodem.md) representa un dispositivo que traduce los datos binarios en modulaciones de onda para la transmisión basada en sonido mediante la conexión a la red de sistema telefónico anterior (POTS).

</dd> <dt>

[**Sistema \_ CIM**](cim-powersupply.md)
</dt> <dd>

La clase de energía [**CIM \_**](cim-powersupply.md) representa las capacidades y la administración del dispositivo lógico de fuente de alimentación.

</dd> <dt>

[**\_Impresora CIM**](cim-printer.md)
</dt> <dd>

La clase de [**\_ impresora CIM**](cim-printer.md) representa las capacidades y la administración del dispositivo lógico de impresora.

</dd> <dt>

[**\_Proceso CIM**](cim-process.md)
</dt> <dd>

La clase de [**\_ proceso CIM**](cim-process.md) representa una única instancia de un programa en ejecución. Un usuario suele ver un proceso como una aplicación o una tarea.

</dd> <dt>

[**\_PROCESSEXECUTABLE CIM**](cim-processexecutable.md)
</dt> <dd>

La clase [**CIM \_ ProcessExecutable**](cim-processexecutable.md) representa un vínculo entre un proceso y un archivo de datos e indica que el archivo participa en la ejecución del proceso.

</dd> <dt>

[**\_Procesador CIM**](cim-processor.md)
</dt> <dd>

La clase de [**\_ procesador de CIM**](cim-processor.md) representa las capacidades y la administración del dispositivo lógico del procesador.

</dd> <dt>

[**\_PROCESSTHREAD CIM**](cim-processthread.md)
</dt> <dd>

La clase [**CIM \_ ProcessThread**](cim-processthread.md) representa un vínculo entre un proceso y los subprocesos que se ejecutan en el contexto del proceso.

</dd> <dt>

[**\_Producto CIM**](cim-product.md)
</dt> <dd>

La clase de [**\_ producto CIM**](cim-product.md) es una clase concreta que representa una colección de elementos físicos, características de software y otros productos, adquiridos como una unidad. La adquisición implica un acuerdo entre el proveedor y el consumidor, que puede tener implicaciones en las licencias, el soporte técnico y la garantía del producto.

</dd> <dt>

[**\_PRODUCTFRU CIM**](cim-productfru.md)
</dt> <dd>

La clase [**CIM \_ ProductFRU**](cim-productfru.md) representa una asociación entre el producto y una unidad reemplazable en campo (FRU), que proporciona información acerca de los componentes de producto que se han reemplazado o se han sustituido.

</dd> <dt>

[**\_PRODUCTPARENTCHILD CIM**](cim-productparentchild.md)
</dt> <dd>

La [**Asociación \_ ProductParentChild de CIM**](cim-productparentchild.md) define una jerarquía de elementos primarios y secundarios entre productos. Por ejemplo, un producto puede estar incluido en otros productos.

</dd> <dt>

[**\_PRODUCTPHYSICALELEMENTS CIM**](cim-productphysicalelements.md)
</dt> <dd>

La clase [**CIM \_ ProductPhysicalElements**](cim-productphysicalelements.md) representa los elementos físicos que componen un producto.

</dd> <dt>

[**\_PRODUCTPRODUCTDEPENDENCY CIM**](cim-productproductdependency.md)
</dt> <dd>

La clase [**CIM \_ ProductProductDependency**](cim-productproductdependency.md) representa una asociación entre dos productos, lo que indica que se debe instalar o ausente un para que el otro funcione. Es conceptualmente equivalente a la Asociación [**\_ ServiceServiceDependency de CIM**](cim-serviceservicedependency.md) .

</dd> <dt>

[**\_PRODUCTSOFTWAREFEATURES CIM**](cim-productsoftwarefeatures.md)
</dt> <dd>

La [**Asociación \_ ProductSoftwareFeatures de CIM**](cim-productsoftwarefeatures.md) identifica las características de software para un producto determinado.

</dd> <dt>

[**\_PRODUCTSUPPORT CIM**](cim-productsupport.md)
</dt> <dd>

La clase [**CIM \_ ProductSupport**](cim-productsupport.md) representa una asociación entre el producto y el acceso de soporte que muestra cómo se obtiene la compatibilidad con el producto. Hay varios tipos de soporte técnico disponibles para un producto; el mismo objeto de soporte técnico puede proporcionar asistencia para varios productos.

</dd> <dt>

[**ProtectedSpaceExtent de CIM \_**](cim-protectedspaceextent.md)
</dt> <dd>

La clase [**CIM \_ ProtectedSpaceExtent**](cim-protectedspaceextent.md) representa direcciones de bloques lógicos direccionables, que se tratan como una única extensión de almacenamiento, pero se encuentran en una única extensión física.

</dd> <dt>

[**\_PSEXTENTBASEDONPEXTENT CIM**](cim-psextentbasedonpextent.md)
</dt> <dd>

La [**clase \_ PSExtentBasedOnPExtent de CIM**](cim-psextentbasedonpextent.md) asocia las extensiones de espacio protegidas basadas en una extensión física.

</dd> <dt>

[**\_Bastidor CIM**](cim-rack.md)
</dt> <dd>

La clase de [**\_ bastidor CIM**](cim-rack.md) representa un bastidor (una trama física o un alojamiento) en el que se almacena el chasis. Normalmente, un bastidor representa el alojamiento; todos los componentes que funcionan están empaquetados en el chasis.

</dd> <dt>

[**Contrataciones \_ de CIM**](cim-realizes.md)
</dt> <dd>

La clase [**CIM \_ Observations**](cim-realizes.md) representa la asociación que define la asignación entre un dispositivo lógico y el componente físico que implementa el dispositivo.

</dd> <dt>

[**\_REALIZESAGGREGATEPEXTENT CIM**](cim-realizesaggregatepextent.md)
</dt> <dd>

La [**Asociación \_ RealizesAggregatePExtent de CIM**](cim-realizesaggregatepextent.md) representa la relación en la que se realiza la clase [**\_ AggregatePExtent de CIM**](cim-aggregatepextent.md) en un medio físico.

</dd> <dt>

[**\_REALIZESDISKPARTITION CIM**](cim-realizesdiskpartition.md)
</dt> <dd>

La clase [**CIM \_ RealizesDiskPartition**](cim-realizesdiskpartition.md) representa una partición de disco en un medio físico que modela la creación de particiones en una unidad SCSI o IDE sin procesar.

</dd> <dt>

[**\_REALIZESPEXTENT CIM**](cim-realizespextent.md)
</dt> <dd>

La [**Asociación \_ RealizesPExtent de CIM**](cim-realizespextent.md) representa la relación en la que se realizan las extensiones físicas en un medio físico. Además, se especifica la dirección inicial de la extensión física en el medio físico.

</dd> <dt>

[**\_REBOOTACTION CIM**](cim-rebootaction.md)
</dt> <dd>

La [**clase \_ RebootAction de CIM**](cim-rebootaction.md) provoca un reinicio del sistema en el que está instalado el elemento de software.

</dd> <dt>

[**\_REDUNDANCYCOMPONENT CIM**](cim-redundancycomponent.md)
</dt> <dd>

La clase [**CIM \_ RedundancyComponent**](cim-redundancycomponent.md) asocia un grupo de redundancia compuesto por elementos del sistema administrados e indica que, juntos, los elementos proporcionan redundancia. Todos los elementos agregados en un grupo de redundancia deben ser instancias de la misma clase de objeto.

</dd> <dt>

[**\_REDUNDANCYGROUP CIM**](cim-redundancygroup.md)
</dt> <dd>

La clase [**CIM \_ RedundancyGroup**](cim-redundancygroup.md) representa una colección de elementos del sistema administrados, que indica que los componentes agregados, juntos, proporcionan redundancia. Todos los elementos agregados en un grupo de redundancia deben ser instancias de la misma clase de objeto.

</dd> <dt>

[**\_Refrigeración CIM**](cim-refrigeration.md)
</dt> <dd>

La clase de [**\_ refrigeración CIM**](cim-refrigeration.md) representa las capacidades y la administración de un dispositivo de enfriamiento de refrigeración.

</dd> <dt>

[**\_RELATEDSTATISTICS CIM**](cim-relatedstatistics.md)
</dt> <dd>

La [**Asociación \_ RelatedStatistics de CIM**](cim-relatedstatistics.md) representa jerarquías y dependencias de las clases de [**\_ StatisticalInformation CIM**](cim-statisticalinformation.md) relacionadas.

</dd> <dt>

[**\_REMOTEFILESYSTEM CIM**](cim-remotefilesystem.md)
</dt> <dd>

La clase [**CIM \_ RemoteFileSystem**](cim-remotefilesystem.md) representa un sistema de archivos remoto al que se tiene acceso por medio de un servicio relacionado con la red. En este caso, el almacén de archivos está hospedado en un equipo, que actúa como servidor de archivos.

</dd> <dt>

[**\_REMOVEDIRECTORYACTION CIM**](cim-removedirectoryaction.md)
</dt> <dd>

La [**clase \_ RemoveDirectoryAction de CIM**](cim-removedirectoryaction.md) quita los directorios de los elementos de software.

</dd> <dt>

[**\_REMOVEFILEACTION CIM**](cim-removefileaction.md)
</dt> <dd>

La [**clase \_ RemoveFileAction de CIM**](cim-removefileaction.md) desinstala los archivos.

</dd> <dt>

[**\_REPLACEMENTSET CIM**](cim-replacementset.md)
</dt> <dd>

La clase [**CIM \_ ReplacementSet**](cim-replacementset.md) agrega elementos físicos que se deben reemplazar juntos. Por ejemplo, al reemplazar una tarjeta de memoria, los chips de memoria de componente también se pueden quitar y reemplazar. O bien, esta asociación se puede usar para reemplazar o actualizar un conjunto de chips de memoria.

</dd> <dt>

[**\_RESIDESONEXTENT CIM**](cim-residesonextent.md)
</dt> <dd>

La clase [**CIM \_ ResidesOnExtent**](cim-residesonextent.md) representa una asociación entre un sistema de archivos y la extensión de almacenamiento donde se encuentra. Normalmente, un sistema de archivos reside en un disco lógico.

</dd> <dt>

[**Ejecución de CIM \_**](cim-runningos.md)
</dt> <dd>

La clase [**CIM \_ Runnings**](cim-runningos.md) representa el sistema operativo que se está ejecutando actualmente. Como máximo, un sistema operativo puede ejecutarse en cualquier momento en un sistema informático; es posible que no se haya iniciado el equipo o que el sistema operativo sea desconocido.

</dd> <dt>

[**\_SAPSAPDEPENDENCY CIM**](cim-sapsapdependency.md)
</dt> <dd>

La [**clase \_ SAPSAPDependency de CIM**](cim-sapsapdependency.md) es una asociación entre dos puntos de acceso de servicio (SAP), que indica que el segundo SAP es necesario para que el primer SAP se conecte con su servicio.

</dd> <dt>

[**\_Escáner CIM**](cim-scanner.md)
</dt> <dd>

El [**\_ analizador de CIM**](cim-scanner.md) representa las capacidades y la administración del dispositivo lógico del escáner.

</dd> <dt>

[**\_SCSICONTROLLER CIM**](cim-scsicontroller.md)
</dt> <dd>

La clase [**CIM \_ SCSIController**](cim-scsicontroller.md) representa las capacidades y la administración del dispositivo lógico SCSI Controller.

</dd> <dt>

[**\_SCSIINTERFACE CIM**](cim-scsiinterface.md)
</dt> <dd>

representa una relación de [**\_ ControlledBy de CIM**](cim-controlledby.md) que indica a qué dispositivos se tiene acceso a través de una controladora SCSI y las características de acceso.

</dd> <dt>

[**\_Sensor CIM**](cim-sensor.md)
</dt> <dd>

La clase de [**\_ sensor CIM**](cim-sensor.md) representa un dispositivo de hardware capaz de medir las características de una propiedad física (por ejemplo, las características de temperatura o voltaje de un sistema de equipo unitario).

</dd> <dt>

[**\_SERIALCONTROLLER CIM**](cim-serialcontroller.md)
</dt> <dd>

La clase [**CIM \_ SerialController**](cim-serialcontroller.md) representa las capacidades y la administración del dispositivo lógico de puerto serie.

</dd> <dt>

[**\_SERIALINTERFACE CIM**](cim-serialinterface.md)
</dt> <dd>

La clase [**CIM \_ SerialInterface**](cim-serialinterface.md) representa una relación [**\_ ControlledBy de CIM**](cim-controlledby.md) que indica a qué dispositivos se tiene acceso a través del controlador serie y las características del acceso.

</dd> <dt>

[**\_Servicio CIM**](cim-service.md)
</dt> <dd>

La clase de [**\_ servicio CIM**](cim-service.md) representa un elemento lógico que contiene información para representar y administrar la funcionalidad proporcionada por una característica de dispositivo o software. Un servicio es un objeto de uso general para configurar y administrar la implementación de la funcionalidad. no es la propia funcionalidad.

</dd> <dt>

[**\_SERVICEACCESSBYSAP CIM**](cim-serviceaccessbysap.md)
</dt> <dd>

La clase de asociación [**CIM \_ ServiceAccessBySAP**](cim-serviceaccessbysap.md) representa los puntos de acceso de un servicio. Por ejemplo, se puede tener acceso a una impresora a través de los puntos de acceso de servicio (SAP, Macintosh o Windows), que pueden hospedarse en sistemas diferentes.

</dd> <dt>

[**\_Punto CIM**](cim-serviceaccesspoint.md)
</dt> <dd>

La clase [**CIM \_ punto**](cim-serviceaccesspoint.md) representa la capacidad de usar o invocar un servicio. Los puntos de acceso representan servicios que están disponibles para su uso por parte de otras entidades.

</dd> <dt>

[**\_SERVICESAPDEPENDENCY CIM**](cim-servicesapdependency.md)
</dt> <dd>

La clase [**CIM \_ ServiceSAPDependency**](cim-servicesapdependency.md) representa una asociación entre un servicio y un punto de acceso de servicio (SAP), que indica que el servicio utiliza el SAP al que se hace referencia para proporcionar su funcionalidad.

</dd> <dt>

[**\_SERVICESERVICEDEPENDENCY CIM**](cim-serviceservicedependency.md)
</dt> <dd>

La clase [**CIM \_ ServiceServiceDependency**](cim-serviceservicedependency.md) representa una asociación entre dos servicios.

</dd> <dt>

[**Configuración de CIM \_**](cim-setting.md)
</dt> <dd>

La clase de [**\_ configuración CIM**](cim-setting.md) representa parámetros operativos y relacionados con la configuración de uno o más elementos del sistema administrados.

</dd> <dt>

[**\_SETTINGCHECK CIM**](cim-settingcheck.md)
</dt> <dd>

La clase [**CIM \_ SettingCheck**](cim-settingcheck.md) especifica la información necesaria para comprobar un archivo de configuración determinado para una entrada específica que contiene un valor igual al valor especificado. Se supone que todas las comparaciones no distinguen mayúsculas de minúsculas.

</dd> <dt>

[**\_SETTINGCONTEXT CIM**](cim-settingcontext.md)
</dt> <dd>

La [**clase \_ SettingContext de CIM**](cim-settingcontext.md) asocia objetos de configuración con objetos de configuración.

</dd> <dt>

[**\_Ranura CIM**](cim-slot.md)
</dt> <dd>

La clase de [**\_ ranura CIM**](cim-slot.md) representa los conectores en los que se insertan los paquetes.

</dd> <dt>

[**\_SLOTINSLOT CIM**](cim-slotinslot.md)
</dt> <dd>

La [**relación \_ SlotInSlot de CIM**](cim-slotinslot.md) representa la capacidad de un adaptador especial de extender la estructura de ranura existente para habilitar la conexión de tarjetas que, de lo contrario, no es compatible con un marco o un panel de hospedaje.

</dd> <dt>

[**\_SOFTWAREELEMENT CIM**](cim-softwareelement.md)
</dt> <dd>

La [**clase \_ SoftwareElement de CIM**](cim-softwareelement.md) descompone un [**objeto \_ SoftwareFeature de CIM**](cim-softwarefeature.md) en un conjunto de elementos que se pueden administrar o implementar individualmente para una plataforma determinada. La plataforma de un elemento de software está identificada de forma exclusiva por su sistema operativo y la arquitectura de hardware subyacente.

</dd> <dt>

[**\_SOFTWAREELEMENTACTIONS CIM**](cim-softwareelementactions.md)
</dt> <dd>

La [**Asociación \_ SoftwareElementActions de CIM**](cim-softwareelementactions.md) identifica las acciones de un elemento de software.

</dd> <dt>

[**\_SOFTWAREELEMENTCHECKS CIM**](cim-softwareelementchecks.md)
</dt> <dd>

La clase de asociación [**CIM \_ SoftwareElementChecks**](cim-softwareelementchecks.md) relaciona un elemento de software con información de condición o ubicación que una característica puede necesitar.

</dd> <dt>

[**\_SOFTWAREELEMENTVERSIONCHECK CIM**](cim-softwareelementversioncheck.md)
</dt> <dd>

La clase [**CIM \_ SoftwareElementVersionCheck**](cim-softwareelementversioncheck.md) representa un tipo de elemento de software que debe existir en el entorno.

</dd> <dt>

[**\_SOFTWAREFEATURE CIM**](cim-softwarefeature.md)
</dt> <dd>

La clase [**CIM \_ SoftwareFeature**](cim-softwarefeature.md) representa una función o funcionalidad determinada de un sistema de aplicaciones o productos.

</dd> <dt>

[**\_SOFTWAREFEATURESAPIMPLEMENTATION CIM**](cim-softwarefeaturesapimplementation.md)
</dt> <dd>

La clase [**CIM \_ SoftwareFeatureSAPImplementation**](cim-softwarefeaturesapimplementation.md) representa una asociación entre un punto de acceso al servicio (SAP) y cómo se implementa en el software.

</dd> <dt>

[**\_SOFTWAREFEATURESERVICEIMPLEMENTATION CIM**](cim-softwarefeatureserviceimplementation.md)
</dt> <dd>

La clase [**CIM \_ SoftwareFeatureServiceImplementation**](cim-softwarefeatureserviceimplementation.md) representa una asociación entre un servicio y cómo se implementa en el software.

</dd> <dt>

[**\_SOFTWAREFEATURESOFTWAREELEMENTS CIM**](cim-softwarefeaturesoftwareelements.md)
</dt> <dd>

La [**Asociación \_ SoftwareFeatureSoftwareElements de CIM**](cim-softwarefeaturesoftwareelements.md) identifica los elementos de software que componen una característica de software específica.

</dd> <dt>

[**\_SPAREGROUP CIM**](cim-sparegroup.md)
</dt> <dd>

La clase [**CIM \_ SpareGroup**](cim-sparegroup.md) se deriva de la clase [**\_ RedundancyGroup de CIM**](cim-redundancygroup.md) e indica que uno o varios de los elementos agregados se pueden retener.

</dd> <dt>

[**\_STATISTICALINFORMATION CIM**](cim-statisticalinformation.md)
</dt> <dd>

La clase [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md) es una clase raíz para la colección arbitraria de datos estadísticos o métricas aplicables a uno o varios elementos del sistema administrados.

</dd> <dt>

[**Estadísticas de CIM \_**](cim-statistics.md)
</dt> <dd>

La clase de [**\_ estadísticas CIM**](cim-statistics.md) representa una asociación que relaciona los elementos del sistema administrados con los grupos estadísticos que se aplican a ellos.

</dd> <dt>

[**\_STORAGEDEFECT CIM**](cim-storagedefect.md)
</dt> <dd>

La agregación [**\_ StorageDefect de CIM**](cim-storagedefect.md) recopila los errores de almacenamiento para una extensión de almacenamiento.

</dd> <dt>

[**\_STORAGEERROR CIM**](cim-storageerror.md)
</dt> <dd>

La clase [**CIM \_ StorageError**](cim-storageerror.md) representa bloques de medios o espacio de memoria que se asignan sin usar debido a errores. La clave de la clase es la propiedad **StartingAddress** de los bytes con error.

</dd> <dt>

[**\_STORAGEEXTENT CIM**](cim-storageextent.md)
</dt> <dd>

La clase [**CIM \_ StorageExtent**](cim-storageextent.md) representa las capacidades y la administración de los distintos medios que existen para almacenar datos y permitir la recuperación de datos. Esta clase primaria puede representar los distintos componentes de RAID (hardware o software) o una extensión lógica sin procesar sobre medios físicos.

</dd> <dt>

[**\_STORAGEREDUNDANCYGROUP CIM**](cim-storageredundancygroup.md)
</dt> <dd>

La clase [**CIM \_ StorageRedundancyGroup**](cim-storageredundancygroup.md) representa información de redundancia relacionada con el almacenamiento masivo.

</dd> <dt>

[**\_SUPPORTACCESS CIM**](cim-supportaccess.md)
</dt> <dd>

La clase [**CIM \_ SupportAccess**](cim-supportaccess.md) define cómo obtener ayuda para un producto.

</dd> <dt>

[**\_SWAPSPACECHECK CIM**](cim-swapspacecheck.md)
</dt> <dd>

La clase [**CIM \_ SwapSpaceCheck**](cim-swapspacecheck.md) especifica la cantidad de espacio de intercambio que debe estar disponible en el sistema.

</dd> <dt>

[**\_Sistema CIM**](cim-system.md)
</dt> <dd>

La [**clase \_ del sistema CIM**](cim-system.md) agrega un conjunto enumerable de elementos del sistema administrados. La agregación funciona como un todo funcional. Dentro de cualquier subclase del sistema, existe una lista bien definida de las clases de elementos del sistema administradas cuyas instancias deben agregarse.

</dd> <dt>

[**\_SYSTEMCOMPONENT CIM**](cim-systemcomponent.md)
</dt> <dd>

una clase de asociación Modelo de información común (CIM) que establece relaciones entre un sistema y los elementos del sistema administrados en los que se compone.

</dd> <dt>

[**\_SYSTEMDEVICE CIM**](cim-systemdevice.md)
</dt> <dd>

La [**Asociación \_ SystemDevice de CIM**](cim-systemdevice.md) representa una relación explícita en la que un sistema puede agregar dispositivos lógicos.

</dd> <dt>

[**\_SYSTEMRESOURCE CIM**](cim-systemresource.md)
</dt> <dd>

La clase [**CIM \_ SystemResource**](cim-systemresource.md) representa una entidad administrada por BIOS o un sistema operativo que está disponible para su uso por software y dispositivos lógicos.

</dd> <dt>

[**\_Tacómetro CIM**](cim-tachometer.md)
</dt> <dd>

La clase de [**\_ tacómetro CIM**](cim-tachometer.md) existe para la compatibilidad con versiones anteriores con definiciones de esquema CIM anteriores.

</dd> <dt>

[**CIM \_ TapeDrive**](cim-tapedrive.md)
</dt> <dd>

La clase [**CIM \_ TapeDrive**](cim-tapedrive.md) representa una unidad de cinta en el sistema. Las unidades de cinta se distinguen principalmente en que solo se puede tener acceso a ellas de forma secuencial.

</dd> <dt>

[**\_TEMPERATURESENSOR CIM**](cim-temperaturesensor.md)
</dt> <dd>

La [**clase \_ TemperatureSensor de CIM**](cim-temperaturesensor.md) existe por compatibilidad con versiones anteriores de definiciones de esquema CIM.

</dd> <dt>

[**Subproceso CIM \_**](cim-thread.md)
</dt> <dd>

La clase de [**\_ subproceso CIM**](cim-thread.md) representa la capacidad de ejecutar unidades de un proceso o una tarea, en paralelo. Un proceso puede tener muchos subprocesos, cada uno de los cuales es débil para el proceso.

</dd> <dt>

[**\_TODIRECTORYACTION CIM**](cim-todirectoryaction.md)
</dt> <dd>

La [**Asociación \_ ToDirectoryAction de CIM**](cim-todirectoryaction.md) identifica el directorio de destino de la acción de archivo.

</dd> <dt>

[**\_TODIRECTORYSPECIFICATION CIM**](cim-todirectoryspecification.md)
</dt> <dd>

La [**Asociación \_ ToDirectorySpecification de CIM**](cim-todirectoryspecification.md) identifica el directorio de destino de la acción de archivo.

</dd> <dt>

[**\_UNINTERRUPTIBLEPOWERSUPPLY CIM**](cim-uninterruptiblepowersupply.md)
</dt> <dd>

La clase [**CIM \_ UninterruptiblePowerSupply**](cim-uninterruptiblepowersupply.md) representa las capacidades y la administración de un sistema de alimentación ininterrumpida (SAI).

</dd> <dt>

[**\_UNITARYCOMPUTERSYSTEM CIM**](cim-unitarycomputersystem.md)
</dt> <dd>

La clase [**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md) representa un equipo de escritorio, móvil, de red, servidor u otro tipo de sistema de un solo nodo.

</dd> <dt>

[**\_USBCONTROLLER CIM**](cim-usbcontroller.md)
</dt> <dd>

La clase [**CIM \_ USBController**](cim-usbcontroller.md) representa las capacidades y la administración de una controladora USB.

</dd> <dt>

[**\_USBCONTROLLERHASHUB CIM**](cim-usbcontrollerhashub.md)
</dt> <dd>

La clase [**CIM \_ USBControllerHasHub**](cim-usbcontrollerhashub.md) define los concentradores que son inferiores al controlador USB.

</dd> <dt>

[**\_USBDEVICE CIM**](cim-usbdevice.md)
</dt> <dd>

La clase [**CIM \_ USBDevice**](cim-usbdevice.md) representa las características de administración de un dispositivo USB.

</dd> <dt>

[**USBHub de CIM \_**](cim-usbhub.md)
</dt> <dd>

La clase de [**\_ USBHub de CIM**](cim-usbhub.md) representa las capacidades y la administración de un concentrador USB.

</dd> <dt>

[**\_USERDEVICE CIM**](cim-userdevice.md)
</dt> <dd>

La clase [**CIM \_ UserDevice**](cim-userdevice.md) es una clase primaria de la que otras clases, como [**el \_ teclado CIM**](cim-keyboard.md) o [**\_ DesktopMonitor CIM**](cim-desktopmonitor.md), descienden. Los dispositivos de usuario son dispositivos lógicos que permiten al usuario del equipo escribir, ver o oír datos.

</dd> <dt>

[**\_VERSIONCOMPATIBILITYCHECK CIM**](cim-versioncompatibilitycheck.md)
</dt> <dd>

La clase [**CIM \_ VersionCompatibilityCheck**](cim-versioncompatibilitycheck.md) especifica si se permite crear el siguiente estado de un elemento de software.

</dd> <dt>

[**\_VIDEOBIOSELEMENT CIM**](cim-videobioselement.md)
</dt> <dd>

La clase [**CIM \_ VideoBIOSElement**](cim-videobioselement.md) representa el software de bajo nivel que se carga en el almacenamiento no volátil y se usa para configurar y tener acceso al controlador de vídeo de un equipo y mostrarlo.

</dd> <dt>

[**\_VIDEOBIOSFEATURE CIM**](cim-videobiosfeature.md)
</dt> <dd>

La clase [**CIM \_ VideoBIOSFeature**](cim-videobiosfeature.md) representa las capacidades del software de bajo nivel que se usa para configurar y tener acceso al controlador de vídeo de un equipo y mostrarlo.

</dd> <dt>

[**\_VIDEOBIOSFEATUREVIDEOBIOSELEMENTS CIM**](cim-videobiosfeaturevideobioselements.md)
</dt> <dd>

La [**clase \_ VideoBIOSFeatureVideoBIOSElements de CIM**](cim-videobiosfeaturevideobioselements.md) asocia una característica de BIOS de vídeo y sus elementos de BIOS de vídeo agregados.

</dd> <dt>

[**\_Videocontroladora CIM**](cim-videocontroller.md)
</dt> <dd>

La clase de [**\_ videocontroladora CIM**](cim-videocontroller.md) representa las capacidades y la administración del controlador de vídeo.

</dd> <dt>

[**\_VIDEOCONTROLLERRESOLUTION CIM**](cim-videocontrollerresolution.md)
</dt> <dd>

La clase [**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) representa los distintos modos de vídeo que puede admitir un controlador de vídeo.

</dd> <dt>

[**Videoconfiguración de CIM \_**](cim-videosetting.md)
</dt> <dd>

La clase de [**\_ videoconfiguración de CIM**](cim-videosetting.md) asocia el objeto de configuración [**\_ VideoControllerResolution de CIM**](cim-videocontrollerresolution.md) con el controlador al que se aplica.

</dd> <dt>

[**\_VOLATILESTORAGE CIM**](cim-volatilestorage.md)
</dt> <dd>

La clase [**CIM \_ VolatileStorage**](cim-volatilestorage.md) representa las capacidades y la administración del almacenamiento volátil.

</dd> <dt>

[**\_VOLTAGESENSOR CIM**](cim-voltagesensor.md)
</dt> <dd>

La [**clase \_ VoltageSensor de CIM**](cim-voltagesensor.md) existe para la compatibilidad con versiones anteriores con las definiciones de esquema CIM anteriores. Con las adiciones al [**\_ sensor CIM**](cim-sensor.md) y las clases de [**CIM \_ NumericSensor**](cim-numericsensor.md) en la versión 2,2, ya no es necesario.

</dd> <dt>

[**\_VOLUMESET CIM**](cim-volumeset.md)
</dt> <dd>

La clase [**CIM \_ VolumeSet**](cim-volumeset.md) representa un intervalo contiguo de bloques lógicos que se presentan al entorno operativo para leer y escribir datos de usuario.

</dd> <dt>

[**\_WORMDRIVE CIM**](cim-wormdrive.md)
</dt> <dd>

La clase [**CIM \_ WORMDrive**](cim-wormdrive.md) representa las capacidades y la administración de una unidad Worm, un subtipo del dispositivo de acceso a medios.

</dd> </dl>

 

 
