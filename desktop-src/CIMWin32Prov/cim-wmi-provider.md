---
description: Estas clases WMI se declaran en CimWin32.mof.
ms.assetid: 53122499-1CC0-4B48-AEA1-B70B7BBC3A99
ms.tgt_platform: multiple
title: Proveedor WMI cim
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acb9a01e0771645cf6101171ce870be593181cb61d6118e627b9bf96b61994be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118420344"
---
# <a name="cim-wmi-provider"></a>Proveedor WMI cim

Estas clases WMI se declaran en CimWin32.mof.

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[**Acción \_ cim**](cim-action.md)
</dt> <dd>

Una [**\_ clase de acción CIM**](cim-action.md) es una operación que forma parte de un proceso para crear un elemento de software en su siguiente estado o para eliminar el elemento de software en el estado actual.

</dd> <dt>

[**CIM \_ ActionSequence**](cim-actionsequence.md)
</dt> <dd>

La [**asociación \_ ActionSequence**](cim-actionsequence.md) de CIM define una serie de operaciones que hacen la transición del elemento de software (al que hace referencia la asociación [**CIM \_ SoftwareElementActions)**](cim-softwareelementactions.md) a su siguiente estado, o quita el elemento de software de su estado actual.

</dd> <dt>

[**CIM \_ ActsAsSpare**](cim-actsasspare.md)
</dt> <dd>

La [**\_ asociación Cim ActsAsSpare**](cim-actsasspare.md) indica qué elementos se pueden ahorrar o reemplazar otros elementos agregados. Una reserva puede funcionar en modo de "espera activa" tal y como se especifica elemento por elemento.

</dd> <dt>

[**CIM \_ AdjacentSlots**](cim-adjacentslots.md)
</dt> <dd>

La [**\_ asociación CIM AdjacentSlots**](cim-adjacentslots.md) describe el diseño de ranuras en una tarjeta de hospedaje o adaptador. La información, como la distancia entre las ranuras y si se "comparten" (si se rellena una, no se puede usar la otra ranura), se transmite como propiedades de asociación.

</dd> <dt>

[**Agregado \_ de CIMPExtent**](cim-aggregatepextent.md)
</dt> <dd>

La [**clase \_ AggregatePExtent**](cim-aggregatepextent.md) de CIM proporciona información de resumen sobre los bloques lógicos direccionables, que se encuentran en el mismo grupo de redundancia de almacenamiento y se encuentran en el mismo medio físico.

</dd> <dt>

[**Agregado \_ DE CIMPSExtent**](cim-aggregatepsextent.md)
</dt> <dd>

La [**clase \_ AggregatePSExtent**](cim-aggregatepsextent.md) de CIM define el número de bloques lógicos direccionables en un único dispositivo de almacenamiento, excepto los bloques lógicos asignados como datos de comprobación. Si se definen conjuntos de volúmenes, los bloques lógicos se incluyen dentro de un único conjunto de volúmenes. Se trata de una agrupación alternativa para [**CIM \_ ProtectedSpaceExtent,**](cim-protectedspaceextent.md)cuando solo se necesita información de resumen o cuando se usa la configuración automática.

</dd> <dt>

[**\_AggregateRedundancyComponent de CIM**](cim-aggregateredundancycomponent.md)
</dt> <dd>

La [**clase \_ AggregateRedundancyComponent de CIM**](cim-aggregateredundancycomponent.md) describe la extensión física agregada en un grupo de redundancia de almacenamiento.

</dd> <dt>

[**CIM \_ AlarmDevice**](cim-alarmdevice.md)
</dt> <dd>

La [**clase CIM \_ AlarmDevice**](cim-alarmdevice.md) es un dispositivo de alarma que emite indicaciones visibles o acústicas relacionadas con una situación de problema.

</dd> <dt>

[**CIM \_ AllocatedResource**](cim-allocatedresource.md)
</dt> <dd>

La [**clase \_ AllocatedResource**](cim-allocatedresource.md) de CIM representa una asociación entre los dispositivos lógicos y los recursos del sistema e indica que el recurso está asignado al dispositivo.

</dd> <dt>

[**Sistema \_ de aplicaciones CIM**](cim-applicationsystem.md)
</dt> <dd>

La [**clase \_ Cim ApplicationSystem**](cim-applicationsystem.md) representa una aplicación o un sistema de software que admite una función empresarial determinada que se puede administrar como una unidad independiente. Este sistema se puede descomponer en sus componentes funcionales mediante la [**clase \_ CIM SoftwareFeature.**](cim-softwarefeature.md) Las características de software para una aplicación o sistema de software determinados se encuentran mediante la asociación [**\_ CIM ApplicationSystemSoftwareFeature.**](cim-applicationsystemsoftwarefeature.md)

</dd> <dt>

[**CIM \_ ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md)
</dt> <dd>

La [**clase \_ Cim ApplicationSystemSoftwareFeature**](cim-applicationsystemsoftwarefeature.md) representa una asociación que identifica las características de software que constituye un sistema de aplicación determinado. Las características de software se pueden incluir en distintos productos.

</dd> <dt>

[**CIM \_ AssociatedAlarm**](cim-associatedalarm.md)
</dt> <dd>

La [**dependencia \_ AssociatedAlarm de CIM**](cim-associatedalarm.md) asocia una alarma a un dispositivo lógico.

</dd> <dt>

[**CIM \_ AssociatedBattery**](cim-associatedbattery.md)
</dt> <dd>

La [**dependencia \_ AssociatedBattery de CIM**](cim-associatedbattery.md) asocia una batería a un dispositivo lógico. Use esta asociación para modelar baterías individuales que conste de una fuente de alimentación ininterrumpida (UPS).

</dd> <dt>

[**CIM \_ Associated Cooling**](cim-associatedcooling.md)
</dt> <dd>

La [**\_ asociación Associated Cooling**](cim-associatedcooling.md) de CIM indica cuándo los ventiladores u otros dispositivos de refrigeración son específicos de un dispositivo (en lugar de proporcionar refrigeración del gabinete o del gabinete).

</dd> <dt>

[**CIM \_ AssociatedMemory**](cim-associatedmemory.md)
</dt> <dd>

La [**clase \_ AssociateMemory**](cim-associatedmemory.md) de CIM asocia la memoria instalada o asociada, como la memoria caché con un dispositivo lógico.

</dd> <dt>

[**CIM \_ AssociatedProcessorMemory**](cim-associatedprocessormemory.md)
</dt> <dd>

La [**clase \_ AssociatedProcessorMemory**](cim-associatedprocessormemory.md) de CIM asocia el procesador y la memoria del sistema, o la memoria caché de un procesador.

</dd> <dt>

[**CIM \_ AssociatedSensor**](cim-associatedsensor.md)
</dt> <dd>

La [**clase \_ AssociatedSensor de CIM**](cim-associatedsensor.md) asocia un sensor instalado a un dispositivo lógico. El sensor mide las propiedades críticas de entrada y salida, y se puede incluir con el dispositivo o instalarse cerca.

</dd> <dt>

[**CIM \_ AssociatedSupplyCurrentSensor**](cim-associatedsupplycurrentsensor.md)
</dt> <dd>

La [**clase \_ AssociatedSupplyCurrentSensor de CIM**](cim-associatedsupplycurrentsensor.md) asocia una fuente de alimentación a un sensor actual (amperage) que supervisa su frecuencia de entrada.

</dd> <dt>

[**CIM \_ AssociatedSupplyVoltageSensor**](cim-associatedsupplyvoltagesensor.md)
</dt> <dd>

Asocia una fuente de alimentación a un sensor de voltaje que supervisa su voltaje de entrada.

</dd> <dt>

[**CIM \_ BasedOn**](cim-basedon.md)
</dt> <dd>

La [**clase \_ BasedOn**](cim-basedon.md) de CIM representa una asociación que describe cómo se pueden ensamblar extensiones de almacenamiento desde extensiones de nivel inferior. Por ejemplo, las extensiones físicas incluyen extensiones de espacio protegido. Por lo tanto, los conjuntos de volúmenes se ensamblan a partir de una o varias extensiones de espacio físico o protegido. La memoria caché se puede definir de forma independiente y realizarse en un elemento físico, o puede basarse en extensiones de almacenamiento volátiles o no volátiles.

</dd> <dt>

[**Batería \_ CIM**](cim-battery.md)
</dt> <dd>

La [**clase \_ Battery cim**](cim-battery.md) representa las funcionalidades y la administración del dispositivo lógico de la batería. Esta clase se aplica a baterías en sistemas portátiles y otras baterías internas y externas.

</dd> <dt>

[**CIM \_ BinarySensor**](cim-binarysensor.md)
</dt> <dd>

La [**clase \_ BinarySensor de CIM**](cim-binarysensor.md) proporciona una salida booleana. Las **propiedades CurrentState** y **PossibleStates** se agregaron para la sensoración, lo que hace que la subclase **\_ BinarySensor** de CIM ya no sea necesaria, aunque se conserva por compatibilidad con versiones anteriores. Se puede crear un sensor binario mediante la creación de instancias de un sensor con dos estados posibles.

</dd> <dt>

[**CIM \_ BIOSElement**](cim-bioselement.md)
</dt> <dd>

La [**clase \_ CIM BIOSElement**](cim-bioselement.md) representa el software de bajo nivel que se carga en el almacenamiento no volátil y se usa para iniciar y configurar un sistema informático.

</dd> <dt>

[**CIM \_ BIOSFeature**](cim-biosfeature.md)
</dt> <dd>

representa las funcionalidades del software de bajo nivel que se usa para iniciar y configurar un sistema informático.

</dd> <dt>

[**CIM \_ BIOSFeatureBIOSElements**](cim-biosfeaturebioselements.md)
</dt> <dd>

La [**clase \_ CIM BIOSFeatureBIOSElements**](cim-biosfeaturebioselements.md) asocia una característica BIOS y sus elementos BIOS agregados.

</dd> <dt>

[**CIM \_ BIOSLoadedInNV**](cim-biosloadedinnv.md)
</dt> <dd>

La [**clase \_ CIM BIOSLoadedInNV**](cim-biosloadedinnv.md) asocia un elemento BIOS y el almacenamiento no volátil en el que se carga.

</dd> <dt>

[**CIM \_ BootOSFromFS**](cim-bootosfromfs.md)
</dt> <dd>

La [**clase \_ CIM BootOSFromFS**](cim-bootosfromfs.md) asocia el sistema operativo y los sistemas de archivos desde los que se carga el sistema operativo. La asociación es de varios a varios; un sistema operativo distribuido puede depender de varios sistemas de archivos para cargarse correcta y completamente.

</dd> <dt>

[**CIM \_ BootSAP**](cim-bootsap.md)
</dt> <dd>

La [**clase \_ BOOTSAP de CIM**](cim-bootsap.md) representa los puntos de acceso de un servicio de arranque.

</dd> <dt>

[**CIM \_ BootService**](cim-bootservice.md)
</dt> <dd>

La [**clase CIM \_ BootService**](cim-bootservice.md) representa la funcionalidad proporcionada por un dispositivo o software, o por una red, para cargar un sistema operativo en un sistema informático unitario.

</dd> <dt>

[**CIM \_ BootServiceAccessBySAP**](cim-bootserviceaccessbysap.md)
</dt> <dd>

La [**clase CIM \_ BootServiceAccessBySAP**](cim-bootserviceaccessbysap.md) asocia un servicio de arranque y sus puntos de acceso.

</dd> <dt>

[**CIM \_ CacheMemory**](cim-cachememory.md)
</dt> <dd>

La [**clase \_ Cim CacheMemory**](cim-cachememory.md) define las funcionalidades y la administración de la memoria caché.

</dd> <dt>

[**Tarjeta \_ CIM**](cim-card.md)
</dt> <dd>

La [**clase \_ cim card**](cim-card.md) representa un tipo de contenedor físico que se puede conectar a otra tarjeta o placa de hospedaje, o bien es en sí una placa de hospedaje o placa base en un chasis. Esta clase incluye cualquier paquete capaz de transportar señales y proporcionar un punto de montaje para componentes físicos, como chips u otros paquetes físicos, como otras tarjetas.

</dd> <dt>

[**CIM \_ CardInSlot**](cim-cardinslot.md)
</dt> <dd>

La [**clase \_ CIM CardInSlot**](cim-cardinslot.md) asocia una tarjeta adaptadora con el contenedor en el que se inserta.

</dd> <dt>

[**CIM \_ CardOnCard**](cim-cardoncard.md)
</dt> <dd>

La [**asociación \_ CardOnCard**](cim-cardoncard.md) de CIM describe las relaciones sobre las tarjetas que se pueden conectar a placa base o placa base, tarjetas de presentación de un adaptador o tarjetas que admiten módulos especiales de tipo tarjeta.

</dd> <dt>

[**CIM \_ CDROMDrive**](cim-cdromdrive.md)
</dt> <dd>

La [**clase CIM \_ CDROMDrive**](cim-cdromdrive.md) representa una unidad de CD-ROM en el equipo.

</dd> <dt>

[**Chasis \_ CIM**](cim-chassis.md)
</dt> <dd>

La clase CIM Chassis representa los elementos [**\_ físicos**](cim-chassis.md) que incluyen otros elementos y proporcionan una funcionalidad definible, como un escritorio, un nodo de procesamiento, un UPS, almacenamiento en disco o cinta, o una combinación de estos.

</dd> <dt>

[**Chasis \_ CIMInRack**](cim-chassisinrack.md)
</dt> <dd>

La [**\_ asociación CIM ChassisInRack**](cim-chassisinrack.md) representa la relación "que contiene" entre un bastidor y un chasis que contiene.

</dd> <dt>

[**Comprobación de \_ CIM**](cim-check.md)
</dt> <dd>

La [**clase \_ CHECK**](cim-check.md) de CIM representa una condición o característica que se espera que sea verdadera en un entorno definido o con ámbito por una instancia de una clase [**\_ ComputerSystem de CIM.**](cim-computersystem.md) Las comprobaciones asociadas a un elemento de software determinado se organizan en uno de dos grupos mediante la **propiedad Phase** de la asociación [**CIM \_ SoftwareElementChecks.**](cim-softwareelementchecks.md)

</dd> <dt>

[**CIM \_ Chip**](cim-chip.md)
</dt> <dd>

La [**clase CIM \_ Chip**](cim-chip.md) representa el tipo de hardware de circuito integrado, incluidos LOS ASIC, procesadores, chips de memoria, entre otros.

</dd> <dt>

[**Clústeres \_ CIMSAP**](cim-clusteringsap.md)
</dt> <dd>

La [**clase CIM \_ ClusteringSAP**](cim-clusteringsap.md) representa los puntos de acceso de un servicio de agrupación en clústeres.

</dd> <dt>

[**CIM \_ ClusteringService**](cim-clusteringservice.md)
</dt> <dd>

La [**clase CIM \_ ClusteringService**](cim-clusteringservice.md) representa la funcionalidad proporcionada por un clúster. Por ejemplo, la funcionalidad de conmutación por error se puede modelar como un servicio de un clúster de conmutación por error.

</dd> <dt>

[**CIM \_ ClusterServiceAccessBySAP**](cim-clusterserviceaccessbysap.md)
</dt> <dd>

La [**clase \_ CLUSTERServiceAccessBySAP**](cim-clusterserviceaccessbysap.md) de CIM representa la relación entre un servicio de agrupación en clústeres y sus puntos de acceso.

</dd> <dt>

[**Recopilaciones \_ de CIMCollections**](cim-collectedcollections.md)
</dt> <dd>

La [**clase \_ CollectedCollections**](cim-collectedcollections.md) de CIM es una asociación de agregación que representa una colección de elementos de sistema administrados (MSE) contenida en una colección de MSE.

</dd> <dt>

[**CIM \_ CollectedMSEs**](cim-collectedmses.md)
</dt> <dd>

La [**clase \_ de asociación CollectedMSEs**](cim-collectedmses.md) de CIM representa los miembros del objeto de agrupación, [**una clase CollectionOfMSEs.**](cim-collectionofmses.md)

</dd> <dt>

[**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md)
</dt> <dd>

El [**objeto \_ CollectionOfMSEs**](cim-collectionofmses.md) de CIM permite la agrupación de objetos [**\_ ManagedSystemElement**](cim-managedsystemelement.md) de CIM con el fin de asociar configuraciones y configuraciones. Es abstracto requerir más definición y perfeccionamiento semántico en subclases.

</dd> <dt>

[**CIM \_ CollectionOfSensors**](cim-collectionofsensors.md)
</dt> <dd>

La [**\_ asociación CIM CollectionOfSensors**](cim-collectionofsensors.md) representa los sensores binarios que representan el sensor multiestado.

</dd> <dt>

[**CIM \_ CollectionSetting**](cim-collectionsetting.md)
</dt> <dd>

La [**clase \_ CollectionSetting de CIM**](cim-collectionsetting.md) representa la asociación entre una colección [**\_ CIMOfMSE**](cim-collectionofmses.md) y la clase de configuración definida para ellos.

</dd> <dt>

[**CIM \_ CompatibleProduct**](cim-compatibleproduct.md)
</dt> <dd>

La [**clase \_ CompatibleProduct**](cim-compatibleproduct.md) de CIM representa una asociación entre productos que indica si dos productos a los que se hace referencia son interoperables, como si se pueden instalar juntos, o si uno puede ser el contenedor físico para el otro, y así sucesivamente.

</dd> <dt>

[**Componente \_ CIM**](cim-component.md)
</dt> <dd>

La [**\_ asociación del**](cim-component.md) componente CIM representa las partes de una relación entre los MSE.

</dd> <dt>

[**CIM \_ ComputerSystem**](cim-computersystem.md)
</dt> <dd>

Una [**clase \_ ComputerSystem de CIM**](cim-computersystem.md) representa una colección especial de instancias [**\_ managedSystemElement de CIM.**](cim-managedsystemelement.md) Esta colección proporciona funcionalidades de equipo y sirve como punto de agregación para asociar uno o varios de los siguientes elementos: sistema de archivos, sistema operativo, procesador y memoria (almacenamiento volátil y no volátil). Esta clase se deriva del sistema [**CIM \_**](cim-system.md).

</dd> <dt>

[**Equipo \_ CIMSystemDMA**](cim-computersystemdma.md)
</dt> <dd>

La [**clase CIM \_ ComputerSystemDMA**](cim-computersystemdma.md) representa una asociación entre un sistema informático y sus canales de acceso directo a memoria (DMA) disponibles.

</dd> <dt>

[**Equipo \_ CIMSystemIRQ**](cim-computersystemirq.md)
</dt> <dd>

La [**clase CIM \_ ComputerSystemIRQ representa**](cim-computersystemirq.md) una asociación entre un sistema informático y sus líneas de solicitud de interrupción (IRQ) disponibles.

</dd> <dt>

[**Equipo \_ CIMSystemMappedIO**](cim-computersystemmappedio.md)
</dt> <dd>

La [**clase CIM \_ ComputerSystemMappedIO representa**](cim-computersystemmappedio.md) una asociación entre un sistema informático y sus puertos de E/S asignados a memoria disponibles.

</dd> <dt>

[**EQUIPO \_ CIMSystemPackage**](cim-computersystempackage.md)
</dt> <dd>

La [**clase CIM \_ ComputerSystemPackage representa**](cim-computersystempackage.md) una asociación que define explícitamente la relación entre los sistemas de equipos unitarios y uno o varios paquetes físicos. La asociación es similar a la forma en que los elementos físicos realizan los dispositivos lógicos.

</dd> <dt>

[**CIM \_ ComputerSystemResource**](cim-computersystemresource.md)
</dt> <dd>

La [**clase CIM \_ ComputerSystemResource**](cim-computersystemresource.md) representa una asociación entre un sistema informático y sus recursos del sistema disponibles.

</dd> <dt>

[**Configuración de \_ CIM**](cim-configuration.md)
</dt> <dd>

El [**objeto de \_ configuración CIM**](cim-configuration.md) permite la agrupación de conjuntos de parámetros (definidos en objetos de configuración [**de CIM) \_**](cim-setting.md) y dependencias para uno o varios elementos del sistema administrados.

</dd> <dt>

[**CIM \_ ConnectedTo**](cim-connectedto.md)
</dt> <dd>

La [**clase \_ ConnectedTo**](cim-connectedto.md) de CIM representa una asociación que indica que hay dos o más conectores físicos conectados.

</dd> <dt>

[**Conector \_ CIMOnPackage**](cim-connectoronpackage.md)
</dt> <dd>

La [**clase \_ CIM ConnectorOnPackage**](cim-connectoronpackage.md) representa una asociación que hace explícita la relación de contención entre conectores y paquetes. Los paquetes físicos contienen conectores, así como otros elementos físicos.

</dd> <dt>

[**Contenedor \_ CIM**](cim-container.md)
</dt> <dd>

La [**clase \_ contenedora CIM**](cim-container.md) representa una asociación entre un elemento contenido y un elemento físico contenedor. Un objeto que contiene debe ser un paquete físico.

</dd> <dt>

[**CIM \_ ControlledBy**](cim-controlledby.md)
</dt> <dd>

La [**relación \_ CIM ControlledBy**](cim-controlledby.md) indica qué dispositivos son controlados por el dispositivo lógico del controlador o a los que se accede a través de ellos.

</dd> <dt>

[**Controlador \_ CIM**](cim-controller.md)
</dt> <dd>

La [**clase \_ cim controller**](cim-controller.md) es una clase primaria para agrupar dispositivos varios relacionados con el control. Algunos ejemplos de controladores son controladores SCSI, controladores USB y controladores serie.

</dd> <dt>

[**REFRIGERACIÓN \_ CIMDispositivo**](cim-coolingdevice.md)
</dt> <dd>

La [**clase \_ CoolingDevice de CIM**](cim-coolingdevice.md) representa las funciones y la administración de los dispositivos de refrigeración.

</dd> <dt>

[**CopyFileAction de CIM \_**](cim-copyfileaction.md)
</dt> <dd>

La [**clase \_ CopyFileAction de CIM**](cim-copyfileaction.md) representa mover o copiar archivos desde un sistema informático a una nueva ubicación.

</dd> <dt>

[**CreateDirectoryAction de CIM \_**](cim-createdirectoryaction.md)
</dt> <dd>

La [**clase \_ CreateDirectoryAction de CIM**](cim-createdirectoryaction.md) crea directorios vacíos para que los elementos de software se instalen localmente.

</dd> <dt>

[**CIM \_ CurrentSensor**](cim-currentsensor.md)
</dt> <dd>

La [**clase \_ CurrentSensor de CIM**](cim-currentsensor.md) existe por compatibilidad con versiones anteriores con las definiciones de esquema CIM anteriores.

</dd> <dt>

[**Archivo de datos CIM \_**](cim-datafile.md)
</dt> <dd>

La [**clase \_ DataFile**](cim-datafile.md) de CIM representa una colección con nombre de datos o código ejecutable. Solo se devolverán instancias de archivos en discos fijos locales

</dd> <dt>

[**Dependencia \_ cim**](cim-dependency.md)
</dt> <dd>

La [**clase \_ de dependencia**](cim-dependency.md) CIM representa una asociación que establece relaciones de dependencia entre objetos .

</dd> <dt>

[**DependencyContext de CIM \_**](cim-dependencycontext.md)
</dt> <dd>

La [**relación \_ dependencyContext de CIM**](cim-dependencycontext.md) asocia una clase de dependencia [**\_ CIM**](cim-dependency.md) con uno o varios objetos [**de configuración \_ de CIM.**](cim-configuration.md) Por ejemplo, las dependencias de un sistema informático pueden cambiar en función de la red a la que está asociado el sistema.

</dd> <dt>

[**CIM \_ DesktopMonitor**](cim-desktopmonitor.md)
</dt> <dd>

La [**clase CIM \_ DesktopMonitor**](cim-desktopmonitor.md) representa las funciones y la administración del dispositivo lógico del monitor de escritorio (CRT).

</dd> <dt>

[**Dispositivo \_ CIMAccessedByFile**](cim-deviceaccessedbyfile.md)
</dt> <dd>

La [**clase \_ de asociación DeviceAccessedByFile**](cim-deviceaccessedbyfile.md) de CIM especifica el dispositivo lógico al que se accede mediante la clase [**\_ DeviceFile DE CIM**](cim-devicefile.md) a la que se hace referencia.

</dd> <dt>

[**CIM \_ DeviceConnection**](cim-deviceconnection.md)
</dt> <dd>

La [**clase de \_ asociación DeviceConnection**](cim-deviceconnection.md) de CIM representa dos o más dispositivos conectados.

</dd> <dt>

[**CIM \_ DeviceErrorCounts**](cim-deviceerrorcounts.md)
</dt> <dd>

La [**clase \_ DeviceErrorCounts**](cim-deviceerrorcounts.md) de CIM es una clase estadística que contiene contadores relacionados con errores para un dispositivo lógico. Los tipos de errores se definen mediante CCITT (Rec X.733) e ISO (IEC 10164-4).

</dd> <dt>

[**CIM \_ DeviceFile**](cim-devicefile.md)
</dt> <dd>

La [**clase \_ DeviceFile**](cim-devicefile.md) de CIM representa un tipo de archivo lógico, que representa un dispositivo. Esta convención es útil para los sistemas operativos que administran dispositivos mediante un modelo de E/S de secuencia de bytes. El dispositivo lógico asociado a este archivo se especifica mediante la relación [**\_ DeviceAccessedByFile**](cim-deviceaccessedbyfile.md) de CIM.

</dd> <dt>

[**Dispositivos \_ CIMSAPImplementation**](cim-devicesapimplementation.md)
</dt> <dd>

La [**clase \_ Cim DeviceSAPImplementation**](cim-devicesapimplementation.md) representa una asociación entre un punto de acceso de servicio (SAP) y cómo se implementa. Cuando muchos dispositivos lógicos están asociados a un SAP, los elementos funcionan juntos para proporcionar el punto de acceso. Si existen implementaciones diferentes de un SAP, cada implementación produce instancias individuales del objeto SAP.

</dd> <dt>

[**CIM \_ DeviceServiceImplementation**](cim-deviceserviceimplementation.md)
</dt> <dd>

La [**clase \_ DeviceServiceImplementation**](cim-deviceserviceimplementation.md) de CIM representa una asociación entre un servicio y cómo se implementa. Cuando varios dispositivos están asociados a un servicio, los elementos funcionan juntos para proporcionar el servicio. Si existen implementaciones diferentes de un servicio, cada implementación produce instancias individuales del objeto de servicio.

</dd> <dt>

[**CIM \_ DeviceSoftware**](cim-devicesoftware.md)
</dt> <dd>

La [**relación \_ dispositivo CIMSoftware**](cim-devicesoftware.md) identifica el software asociado a un dispositivo, como controladores, software de configuración o de aplicación, o firmware.

</dd> <dt>

[**Directorio \_ CIM**](cim-directory.md)
</dt> <dd>

La [**clase \_ Cim Directory**](cim-directory.md) representa un tipo de archivo que agrupa lógicamente los archivos de datos que contiene y proporciona información de ruta de acceso para los archivos agrupados.

</dd> <dt>

[**CIM \_ DirectoryAction**](cim-directoryaction.md)
</dt> <dd>

La [**clase \_ abstracta DirectoryAction**](cim-directoryaction.md) de CIM administra directorios. La creación de directorios se controla mediante la clase [**\_ CreateDirectoryAction**](cim-createdirectoryaction.md) de CIM y la eliminación de directorios se controla mediante la [**\_ clase RemoveDirectoryAction de CIM.**](cim-removedirectoryaction.md)

</dd> <dt>

[**CIM \_ DirectoryContainsFile**](cim-directorycontainsfile.md)
</dt> <dd>

La [**clase CIM \_ DirectoryContainsFile**](cim-directorycontainsfile.md) representa una asociación entre un directorio y los archivos contenidos en ese directorio.

</dd> <dt>

[**CIM \_ DirectorySpecification**](cim-directoryspecification.md)
</dt> <dd>

La [**clase CIM \_ DirectorySpecification**](cim-directoryspecification.md) captura la estructura de directorios principal de un elemento de software. Esta clase se usa para organizar los archivos de un elemento de software en unidades administrables que se pueden reubicar en un sistema informático.

</dd> <dt>

[**CIM \_ DirectorySpecificationFile**](cim-directoryspecificationfile.md)
</dt> <dd>

La [**\_ asociación Cim DirectorySpecificationFile**](cim-directoryspecificationfile.md) representa el directorio que contiene el archivo especificado haciendo referencia a la [**clase \_ DirectorySpecification de CIM.**](cim-directoryspecification.md)

</dd> <dt>

[**CIM \_ DiscreteSensor**](cim-discretesensor.md)
</dt> <dd>

La [**clase CIM \_ DiscreteSensor**](cim-discretesensor.md) tiene un conjunto de valores de cadena legales que puede notificar. Los valores se enumeran en la propiedad **PossibleValues del** sensor. Un sensor discreto siempre tiene una lectura actual que corresponde a uno de los valores enumerados.

</dd> <dt>

[**CIM \_ DiskDrive**](cim-diskdrive.md)
</dt> <dd>

La [**clase \_ CIM DiskDrive**](cim-diskdrive.md) representa una unidad de disco física tal como la ve el sistema operativo. Las características de la unidad de disco corresponden a las características lógicas y de administración de la unidad y, en algunos casos, pueden no reflejar las características físicas del dispositivo. Una interfaz a una unidad física es miembro de esta clase. Sin embargo, un objeto basado en otro dispositivo lógico no es miembro de esta clase.

</dd> <dt>

[**CIM \_ DisketteDrive**](cim-diskettedrive.md)
</dt> <dd>

La [**clase CIM \_ DisketteDrive representa**](cim-diskettedrive.md) las funciones y la administración de una unidad diskette.

</dd> <dt>

[**CIM \_ DiskPartition**](cim-diskpartition.md)
</dt> <dd>

La [**clase \_ CIM DiskPartition**](cim-diskpartition.md) representa un intervalo contiguo de bloques lógicos que el sistema operativo puede identificar mediante los campos de tipo y subtipo de la partición. Las particiones de disco deben realizarse directamente mediante medios físicos (indicados por la asociación [**CIM \_ RealizesDiskPartition)**](cim-realizesdiskpartition.md) o se deben crear en volúmenes de almacenamiento.

</dd> <dt>

[**CIM \_ DiskSpaceCheck**](cim-diskspacecheck.md)
</dt> <dd>

La [**clase CIM \_ DiskSpaceCheck**](cim-diskspacecheck.md) comprueba la cantidad de espacio disponible en disco del sistema y la especifica en la **propiedad AvailableDiskSpace.** Los detalles se comparan con el valor de la propiedad **AvailableSpace** del objeto [**\_ FileSystem cim**](cim-filesystem.md) asociado al objeto [**\_ ComputerSystem de CIM,**](cim-computersystem.md) que describe el entorno del sistema. Cuando el valor de la **propiedad AvailableSpace** es mayor o igual que el valor especificado en la **propiedad AvailableDiskSpace,** se cumple la condición.

</dd> <dt>

[**Visualización de \_ CIM**](cim-display.md)
</dt> <dd>

La [**clase Cim \_ Display**](cim-display.md) es una clase primaria para agrupar dispositivos de visualización varios.

</dd> <dt>

[**CIM \_ DMA**](cim-dma.md)
</dt> <dd>

La [**clase CIM \_ DMA representa**](cim-dma.md) el acceso directo a memoria (DMA) de la arquitectura del equipo.

</dd> <dt>

[**CIM \_ acoplado**](cim-docked.md)
</dt> <dd>

La [**\_ asociación acoplada cim**](cim-docked.md) representa la relación entre dos chasis. Por ejemplo, un portátil (un tipo de chasis) se puede acoplar en una estación de acoplamiento (otro tipo de chasis). Esta relación típica se describe explícitamente.

</dd> <dt>

[**CIM \_ ElementCapacity**](cim-elementcapacity.md)
</dt> <dd>

La [**clase \_ ElementCapacity de CIM**](cim-elementcapacity.md) asocia un objeto [**\_ PhysicalCapacity**](cim-physicalcapacity.md) de CIM con uno o varios elementos físicos. Asocia una descripción de los requisitos mínimos y máximos de hardware (o funcionalidades) a los elementos físicos que se describen.

</dd> <dt>

[**CIM \_ ElementConfiguration**](cim-elementconfiguration.md)
</dt> <dd>

La [**\_ asociación ElementConfiguration**](cim-elementconfiguration.md) de CIM relaciona un [**objeto de configuración \_ de CIM**](cim-configuration.md) con uno o varios elementos del sistema administrados. El **objeto \_ de configuración** cim representa un comportamiento determinado o un estado funcional deseado para el elemento [**\_ ManagedSystemElement de CIM asociado.**](cim-managedsystemelement.md)

</dd> <dt>

[**CIM \_ ElementSetting**](cim-elementsetting.md)
</dt> <dd>

La [**clase \_ ElementSetting de CIM**](cim-elementsetting.md) representa la asociación entre los elementos del sistema administrados y la clase de configuración definida para ellos.

</dd> <dt>

[**Elementos \_ CIMLinked**](cim-elementslinked.md)
</dt> <dd>

La [**\_ asociación elementos CIMLinked**](cim-elementslinked.md) representa elementos físicos que se cablen juntos mediante un vínculo físico.

</dd> <dt>

[**\_Error cimCountersForDevice**](cim-errorcountersfordevice.md)
</dt> <dd>

La [**clase CIM \_ ErrorCountersForDevice**](cim-errorcountersfordevice.md) asocia la clase [**\_ DeviceErrorCounts de CIM**](cim-deviceerrorcounts.md) al dispositivo lógico al que se aplica.

</dd> <dt>

[**ExecuteProgram de CIM \_**](cim-executeprogram.md)
</dt> <dd>

La [**clase \_ ExecuteProgram de CIM**](cim-executeprogram.md) representa los archivos que se pueden ejecutar en el sistema donde está instalado el elemento de software.

</dd> <dt>

[**Exportación de CIM \_**](cim-export.md)
</dt> <dd>

La [**clase CIM \_ Export**](cim-export.md) representa una asociación entre un sistema de archivos local y sus directorios, lo que indica que los directorios especificados están disponibles para el montaje. Al exportar un sistema de archivos completo, el directorio debe hacer referencia al directorio más alto del sistema de archivos.

</dd> <dt>

[**CIM \_ ExtraCapacityGroup**](cim-extracapacitygroup.md)
</dt> <dd>

La [**clase \_ CIM ExtraCapacityGroup**](cim-extracapacitygroup.md) se deriva de un grupo de redundancia que indica que los elementos agregados tienen más capacidad o capacidad de la necesaria. Un ejemplo de este tipo de redundancia es la instalación de fuentes de alimentación N+1 o ventiladores en un sistema.

</dd> <dt>

[**Ventilador \_ CIM**](cim-fan.md)
</dt> <dd>

La [**clase de \_ ventilador CIM**](cim-fan.md) representa las funciones y la administración de un dispositivo de refrigeración de ventilador.

</dd> <dt>

[**CIM \_ FileAction**](cim-fileaction.md)
</dt> <dd>

La [**clase \_ FileAction**](cim-fileaction.md) de CIM permite al autor buscar archivos que ya existen en el equipo de un usuario y, a continuación, mover o copiar esos archivos en una nueva ubicación.

</dd> <dt>

[**CIM \_ FileSpecification**](cim-filespecification.md)
</dt> <dd>

La [**clase \_ CIM FileSpecification**](cim-filespecification.md) representa un archivo que está en o fuera del sistema. El archivo se encuentra en el directorio identificado por la [**asociación CIM \_ DirectorySpecificationFile.**](cim-directoryspecificationfile.md) El [**método Invoke**](invoke-method-in-class-cim-filespecification.md) usa la información para comprobar la existencia del archivo. Tenga en cuenta que no se **comprueban las propiedades con** un valor NULL.

</dd> <dt>

[**CIM \_ FileStorage**](cim-filestorage.md)
</dt> <dd>

La [**\_ asociación CIM FileStorage**](cim-filestorage.md) vincula el sistema de archivos y los archivos lógicos que se abordan a través del sistema de archivos.

</dd> <dt>

[**\_Sistema de archivos CIM**](cim-filesystem.md)
</dt> <dd>

La [**clase CIM \_ FileSystem**](cim-filesystem.md) representa un archivo o un conjunto de datos local en un sistema informático o montado de forma remota desde un servidor de archivos.

</dd> <dt>

[**CIM \_ FlatPanel**](cim-flatpanel.md)
</dt> <dd>

La [**clase \_ FlatPanel cim**](cim-flatpanel.md) representa las funciones y la administración del dispositivo lógico de panel plano.

</dd> <dt>

[**CIM \_ FromDirectoryAction**](cim-fromdirectoryaction.md)
</dt> <dd>

La [**\_ asociación FromDirectoryAction de CIM**](cim-fromdirectoryaction.md) identifica el directorio de origen para la acción de archivo. Cuando se usa esta asociación, se supone que una acción anterior creó el directorio de origen. Esta asociación no puede existir con una [**asociación \_ FromDirectorySpecification**](cim-fromdirectoryspecification.md) de CIM; una acción de archivo solo puede implicar un único directorio de origen.

</dd> <dt>

[**CIM \_ FromDirectorySpecification**](cim-fromdirectoryspecification.md)
</dt> <dd>

La [**\_ asociación FromDirectorySpecification**](cim-fromdirectoryspecification.md) de CIM identifica el directorio de origen para la acción de archivo. Cuando se usa esta asociación, se supone que el directorio de origen ya existe. Esta asociación no puede existir con una [**asociación \_ FromDirectoryAction de CIM;**](cim-fromdirectoryaction.md) una acción de archivo solo puede implicar un único directorio de origen.

</dd> <dt>

[**CIM \_ FRU**](cim-fru.md)
</dt> <dd>

La [**clase \_ FRU cim**](cim-fru.md) representa una colección definida por el proveedor de productos y elementos físicos que están asociados a una unidad reemplazable de campo (FRU) para admitir, mantener o actualizar un producto en la ubicación del cliente.

</dd> <dt>

[**CIM \_ FRUIncludesProduct**](cim-fruincludesproduct.md)
</dt> <dd>

La [**clase \_ CIM FRUIncludesProduct**](cim-fruincludesproduct.md) indica que una unidad reemplazable de campo (FRU) puede estar compuesta de otros productos.

</dd> <dt>

[**CIM \_ FRUPhysicalElements**](cim-fruphysicalelements.md)
</dt> <dd>

La [**clase \_ FRUPhysicalElements**](cim-fruphysicalelements.md) de CIM representa los elementos físicos que representan una unidad reemplazable de campo (FRU).

</dd> <dt>

[**CIM \_ HeatPipe**](cim-heatpipe.md)
</dt> <dd>

La [**clase CIM \_ HeatPipe**](cim-heatpipe.md) representa las funciones y la administración de un dispositivo de refrigeración por canalización de calor.

</dd> <dt>

[**CIM \_ HostedAccessPoint**](cim-hostedaccesspoint.md)
</dt> <dd>

La [**clase \_ HostedAccessPoint de CIM**](cim-hostedaccesspoint.md) representa una asociación entre un punto de acceso de servicio (SAP) y el sistema en el que se proporciona. Cada sistema puede hospedar muchos SAP.

</dd> <dt>

[**CIM \_ HostedBootSAP**](cim-hostedbootsap.md)
</dt> <dd>

La [**clase \_ HostedBootSAP**](cim-hostedbootsap.md) de CIM define el sistema de equipo unitario de hospedaje para una [**clase \_ BootSAP de CIM.**](cim-bootsap.md) Puesto que esta relación se subclasifica de [**CIM \_ HostedAccessPoint**](cim-hostedaccesspoint.md), hereda el esquema de ámbito y nomenclatura definido para [**CIM \_ ServiceAccessPoint,**](cim-serviceaccesspoint.md)donde un punto de acceso se aplaza a su sistema de hospedaje. En este caso, **CIM \_ BootSAP** debe aplazar a su clase [**\_ UnitaryComputerSystem**](cim-unitarycomputersystem.md) de CIM de hospedaje.

</dd> <dt>

[**CIM \_ HostedBootService**](cim-hostedbootservice.md)
</dt> <dd>

La [**clase \_ HostedBootService de CIM**](cim-hostedbootservice.md) asocia un sistema de hospedaje y un servicio de arranque. Puesto que esta relación se subclasifica de [**CIM \_ HostedService**](cim-hostedservice.md), hereda el esquema de ámbito y nomenclatura definido para el servicio, donde un servicio se aplaza a su sistema de hospedaje.

</dd> <dt>

[**CIM \_ HostedFileSystem**](cim-hostedfilesystem.md)
</dt> <dd>

La [**\_ asociación CIM HostedFileSystem**](cim-hostedfilesystem.md) representa un vínculo entre el sistema de equipos y el sistema de archivos hospedado en el sistema de equipos.

</dd> <dt>

[**CIM \_ HostedJobDestination**](cim-hostedjobdestination.md)
</dt> <dd>

La [**clase \_ HostedJobDestination**](cim-hostedjobdestination.md) de CIM representa una asociación entre un destino de trabajo y el sistema en el que reside. Un sistema puede hospedar muchas colas de trabajos. Los destinos de trabajo se aplazan al sistema de hospedaje.

</dd> <dt>

[**CIM \_ HostedService**](cim-hostedservice.md)
</dt> <dd>

La [**clase \_ HostedService**](cim-hostedservice.md) de CIM representa una asociación entre un servicio y el sistema en el que reside la funcionalidad. Un sistema puede hospedar muchos servicios, que se aplazan al sistema de hospedaje. El modelo no representa los servicios hospedados en varios sistemas.

</dd> <dt>

[**Cim \_ Descontrolador Descontrolador**](cim-infraredcontroller.md)
</dt> <dd>

La [**clase \_ CIMController representa**](cim-infraredcontroller.md) las funcionalidades y la administración de un controlador de vuelos.

</dd> <dt>

[**CIM \_ instalado OS**](cim-installedos.md)
</dt> <dd>

La [**clase \_ de asociación CIM InstalledOS**](cim-installedos.md) representa un vínculo entre el sistema informático y el sistema operativo instalado. Un sistema operativo se instala cuando se encuentra en la extensión de almacenamiento de un sistema informático (por ejemplo, se copia en una unidad de disco o se descarga en la memoria).

</dd> <dt>

[**CIM \_ InstalledSoftwareElement**](cim-installedsoftwareelement.md)
</dt> <dd>

La [**clase \_ CIM InstalledSoftwareElement**](cim-installedsoftwareelement.md) asocia un sistema informático con un elemento de software instalado.

</dd> <dt>

[**CIM \_ IRQ**](cim-irq.md)
</dt> <dd>

La [**clase \_ CIM IRQ**](cim-irq.md) representa una línea de solicitud de interrupción (IRQ) de la arquitectura Intel.

</dd> <dt>

[**Trabajo \_ cim**](cim-job.md)
</dt> <dd>

La [**clase Job \_ de CIM**](cim-job.md) representa una unidad de trabajo para un sistema, como un trabajo de impresión. Un trabajo es distinto de un proceso porque se puede programar un trabajo.

</dd> <dt>

[**CIM \_ JobDestination**](cim-jobdestination.md)
</dt> <dd>

La [**clase \_ Cim JobDestination**](cim-jobdestination.md) representa dónde se envía un trabajo para su procesamiento. Puede hacer referencia a una cola que contiene cero o más trabajos, como una cola de impresión que contiene trabajos de impresión. Los destinos de trabajo se hospedan en sistemas, de forma similar a la forma en que los servicios se hospedan en sistemas.

</dd> <dt>

[**CIM \_ JobDestinationJobs**](cim-jobdestinationjobs.md)
</dt> <dd>

La [**\_ asociación CIM JobDestinationJobs**](cim-jobdestinationjobs.md) describe dónde se envía un trabajo para su procesamiento (es decir, a qué destino de trabajo).

</dd> <dt>

[**Teclado \_ CIM**](cim-keyboard.md)
</dt> <dd>

La [**clase CIM \_ Keyboard**](cim-keyboard.md) representa las funciones y la administración del dispositivo lógico de teclado.

</dd> <dt>

[**CIM \_ LinkHasConnector**](cim-linkhasconnector.md)
</dt> <dd>

La [**clase CIM \_ LinkHasConnector**](cim-linkhasconnector.md) asocia los cables y vínculos que se usan como conectores físicos, que conectan los elementos físicos. Esta asociación define explícitamente la relación de los conectores para [**CIM \_ PhysicalLink**](cim-physicallink.md).

</dd> <dt>

[**CIM \_ LocalFileSystem**](cim-localfilesystem.md)
</dt> <dd>

La [**clase CIM \_ LocalFileSystem representa**](cim-localfilesystem.md) el almacén de archivos controlado por un sistema informático a través de medios locales (por ejemplo, acceso directo al controlador de dispositivo). El sistema de equipos puede administrar el almacén de archivos directamente, sin necesidad de que otro equipo actúe como servidor de archivos. Sin embargo, para un sistema de archivos en clúster, el sistema de archivos es local y, por lo tanto, se aplaza al clúster.

</dd> <dt>

[**Ubicación \_ cim**](cim-location.md)
</dt> <dd>

La [**clase \_ CIM Location**](cim-location.md) representa la posición y la dirección de un elemento físico.

</dd> <dt>

[**\_Dispositivo lógico CIM**](cim-logicaldevice.md)
</dt> <dd>

La [**clase \_ LOGICALDevice de CIM**](cim-logicaldevice.md) representa una entidad de hardware que puede o no realizarse en hardware físico.

</dd> <dt>

[**\_Disco lógico CIM**](cim-logicaldisk.md)
</dt> <dd>

La [**clase \_ Cim LogicalDisk**](cim-logicaldisk.md) representa un intervalo contiguo de bloques lógicos que un sistema de archivos puede identificar a través del campo **DeviceID** (clave) del disco. Por ejemplo, en un entorno Windows, el **campo DeviceID** contiene una letra de unidad; en un UNIX de acceso, contiene la ruta de acceso; y en un entorno de NetWare, contiene el nombre del volumen.

</dd> <dt>

[**CIM \_ LogicalDiskBasedOnPartition**](cim-logicaldiskbasedonpartition.md)
</dt> <dd>

La [**clase \_ Cim LogicalDiskBasedOnPartition**](cim-logicaldiskbasedonpartition.md) asocia un disco lógico a la partición de disco en la que reside.

</dd> <dt>

[**CIM \_ LogicalDiskBasedOnVolumeSet**](cim-logicaldiskbasedonvolumeset.md)
</dt> <dd>

La [**\_ asociación CIM LogicalDiskBasedOnVolumeSet**](cim-logicaldiskbasedonvolumeset.md) relaciona los discos lógicos con el volumen en el que se encuentran. Los discos lógicos se pueden basar en un único volumen (por ejemplo, expuesto por un administrador de volúmenes de software) o en una partición de disco.

</dd> <dt>

[**Elemento \_ lógico CIM**](cim-logicalelement.md)
</dt> <dd>

La [**clase \_ LogicalElement**](cim-logicalelement.md) de CIM es la clase base para todos los componentes del sistema que representan componentes abstractos del sistema, como perfiles, procesos o funcionalidades del sistema, en forma de dispositivos lógicos.

</dd> <dt>

[**CIM \_ LogicalFile**](cim-logicalfile.md)
</dt> <dd>

La [**clase \_ Cim LogicalFile**](cim-logicalfile.md) representa una colección con nombre de datos, que puede ser código ejecutable, que se encuentra en un sistema de archivos en una extensión de almacenamiento.

</dd> <dt>

[**CIM \_ LogicalIdentity**](cim-logicalidentity.md)
</dt> <dd>

La [**clase \_ LogicalIdentity**](cim-logicalidentity.md) de CIM es una asociación abstracta y genérica que indica que dos elementos lógicos representan aspectos diferentes de la misma entidad subyacente.

</dd> <dt>

[**CIM \_ MagnetoOpticalDrive**](cim-magnetoopticaldrive.md)
</dt> <dd>

La [**clase \_ Cim MagnetoOpticalDrive representa**](cim-magnetoopticaldrive.md) las funcionalidades y la administración de una unidad magneto-óptica, un subtipo del dispositivo de acceso multimedia.

</dd> <dt>

[**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md)
</dt> <dd>

La [**clase \_ ManagedSystemElement de CIM**](cim-managedsystemelement.md) es la clase base para la jerarquía de elementos del sistema. Cualquier componente distintivo del sistema es un candidato para su inclusión en esta clase.

</dd> <dt>

[**CIM \_ ManagementController**](cim-managementcontroller.md)
</dt> <dd>

La [**clase CIM \_ ManagementController**](cim-managementcontroller.md) se relaciona con las funcionalidades y la administración de un controlador de administración.

</dd> <dt>

[**CIM \_ MediaAccessDevice**](cim-mediaaccessdevice.md)
</dt> <dd>

La [**clase \_ Cim MediaAccessDevice**](cim-mediaaccessdevice.md) representa la capacidad de acceder a uno o varios medios y, a continuación, usar los medios para almacenar y recuperar datos.

</dd> <dt>

[**CIM \_ MediaPresent**](cim-mediapresent.md)
</dt> <dd>

La [**\_ asociación CIM MediaPresent**](cim-mediapresent.md) describe una relación en la que se debe tener acceso a una extensión de almacenamiento a través de un dispositivo de acceso multimedia.

</dd> <dt>

[**Memoria \_ CIM**](cim-memory.md)
</dt> <dd>

La [**clase de \_ memoria CIM**](cim-memory.md) representa las funcionalidades y la administración de dispositivos lógicos relacionados con la memoria.

</dd> <dt>

[**MemoryCapacity de CIM \_**](cim-memorycapacity.md)
</dt> <dd>

La [**clase \_ MemoryCapacity de CIM**](cim-memorycapacity.md) representa la memoria que se puede instalar en un elemento físico y sus configuraciones mínima y máxima. La información sobre la memoria que está instalada actualmente y los requisitos mínimos y máximos de un elemento se encuentran en instancias de la clase [**\_ PhysicalMemory de CIM.**](cim-physicalmemory.md)

</dd> <dt>

[**Comprobación de memoria de CIM \_**](cim-memorycheck.md)
</dt> <dd>

La [**clase \_ MemoryCheck**](cim-memorycheck.md) de CIM especifica una condición para la cantidad mínima de memoria que debe estar disponible en un sistema.

</dd> <dt>

[**CIM \_ MemoryMappedIO**](cim-memorymappedio.md)
</dt> <dd>

La [**clase \_ CIM MemoryMappedIO representa**](cim-memorymappedio.md) la E/S asignada a memoria de la arquitectura del equipo. Esta clase direcciona los recursos de E/S de puerto y memoria.

</dd> <dt>

[**MemoryOnCard de CIM \_**](cim-memoryoncard.md)
</dt> <dd>

La [**clase \_ MemoryOnCard de CIM**](cim-memoryoncard.md) asocia la memoria física ubicada en paneles de hospedaje, tarjetas adaptadoras, y así sucesivamente. Esta asociación define explícitamente la relación de memoria con las tarjetas.

</dd> <dt>

[**CIM \_ MemoryWithMedia**](cim-memorywithmedia.md)
</dt> <dd>

La [**clase \_ CIM MemoryWithMedia**](cim-memorywithmedia.md) asocia la memoria física a un medio físico y su tratamiento. La memoria proporciona identificación de medios y almacena datos específicos del usuario.

</dd> <dt>

[**CIM \_ ModifySettingAction**](cim-modifysettingaction.md)
</dt> <dd>

La [**clase \_ CIM ModifySettingAction**](cim-modifysettingaction.md) representa la información para modificar un archivo de configuración específico, para una entrada específica, con un valor específico.

</dd> <dt>

[**Monitor \_ CIMResolution**](cim-monitorresolution.md)
</dt> <dd>

La [**clase \_ MonitorResolution de CIM**](cim-monitorresolution.md) representa la relación entre las resoluciones horizontales y verticales y la frecuencia de actualización y el modo de examen de un monitor de escritorio. Los valores se especifican en el objeto de controlador de vídeo.

</dd> <dt>

[**CIM \_ MonitorSetting**](cim-monitorsetting.md)
</dt> <dd>

La [**clase \_ Cim MonitorSetting**](cim-monitorsetting.md) asocia la resolución del monitor con el monitor de escritorio al que se aplica.

</dd> <dt>

[**Montaje de \_ CIM**](cim-mount.md)
</dt> <dd>

La [**clase \_ CIM Mount**](cim-mount.md) representa una asociación entre un sistema de archivos y un directorio al que está asociado.

</dd> <dt>

[**CIM \_ MultiStateSensor**](cim-multistatesensor.md)
</dt> <dd>

La [**clase \_ CIM MultiStateSensor representa**](cim-multistatesensor.md) un conjunto de varios miembros de sensores binarios donde cada sensor binario notifica un resultado booleano.

</dd> <dt>

[**CIM \_ NetworkAdapter**](cim-networkadapter.md)
</dt> <dd>

La [**clase \_ Cim NetworkAdapter**](cim-networkadapter.md) es una clase abstracta que define conceptos generales de hardware de red (por ejemplo, dirección permanente o velocidad de funcionamiento). La información se transmite mediante la asociación [**\_ CIM DeviceSAPImplementation.**](cim-devicesapimplementation.md)

</dd> <dt>

[**CIM \_ NFS**](cim-nfs.md)
</dt> <dd>

La [**clase \_ CIM NFS**](cim-nfs.md) representa un sistema de archivos remoto que se monta, mediante el protocolo del sistema de archivos de red (NFS), desde un sistema informático.

</dd> <dt>

[**CIM \_ NonVolatileStorage**](cim-nonvolatilestorage.md)
</dt> <dd>

La [**clase CIM \_ NonVolatileStorage**](cim-nonvolatilestorage.md) representa las funcionalidades y la administración del almacenamiento no volátil. La memoria no volátil incluye de forma nativa almacenamiento flash y ROM.

</dd> <dt>

[**CIM \_ NumericSensor**](cim-numericsensor.md)
</dt> <dd>

La [**clase \_ NumericSensor de CIM**](cim-numericsensor.md) representa un sensor numérico que devuelve lecturas numéricas y, opcionalmente, admite la configuración de umbrales.

</dd> <dt>

[**Sistema operativo CIM \_**](cim-operatingsystem.md)
</dt> <dd>

La [**clase \_ CIM OperatingSystem**](cim-operatingsystem.md) representa un sistema operativo de equipo, que se constituye en software y firmware que hacen que el hardware de un sistema informático sea utilizable.

</dd> <dt>

[**CIM \_ OperatingSystemSoftwareFeature**](cim-operatingsystemsoftwarefeature.md)
</dt> <dd>

La [**clase CIM \_ OperatingSystemSoftwareFeature**](cim-operatingsystemsoftwarefeature.md) representa las características de software que constituye el sistema operativo.

</dd> <dt>

[**CIM \_ OSProcess**](cim-osprocess.md)
</dt> <dd>

La [**clase \_ CIM OSProcess**](cim-osprocess.md) asocia el sistema operativo y uno o varios procesos que se ejecutan en el contexto del sistema operativo.

</dd> <dt>

[**CIM \_ OSVersionCheck**](cim-osversioncheck.md)
</dt> <dd>

La [**clase CIM \_ OSVersionCheck**](cim-osversioncheck.md) especifica las versiones del sistema operativo que pueden admitir un elemento de software.

</dd> <dt>

[**CIM \_ PackageAlarm**](cim-packagealarm.md)
</dt> <dd>

La [**\_ asociación Cim PackageAlarm**](/windows/desktop/SecCrypto/extendedproperties-newenum) representa la relación en la que se instala un dispositivo de alarma como parte de un paquete. La instalación indica problemas con el entorno del paquete: su estado de seguridad o su estado general.

</dd> <dt>

[**Cim \_ Package (Paquete CIM)Package (Paquete CIM)**](cim-packagecooling.md)
</dt> <dd>

La [**asociación \_ CIM Package Cooling**](cim-packagecooling.md) representa la relación en la que se instala un dispositivo de refrigeración en un paquete, como un chasis o bastidor, para ayudar con la refrigeración del paquete.

</dd> <dt>

[**CIM \_ PackagedComponent**](cim-packagedcomponent.md)
</dt> <dd>

La [**\_ asociación CIM PackagedComponent**](cim-packagedcomponent.md) representa una relación explícita en la que un componente suele estar contenido por un paquete físico, como un chasis o una tarjeta.

</dd> <dt>

[**Paquete \_ CIMInChassis**](cim-packageinchassis.md)
</dt> <dd>

La [**\_ asociación Cim PackageInChassis**](cim-packageinchassis.md) representa la relación en la que un chasis puede contener otros paquetes, como otros chasis y tarjetas.

</dd> <dt>

[**Paquete \_ CIMInSlot**](cim-packageinslot.md)
</dt> <dd>

La [**\_ asociación Cim PackageInSlot**](cim-packageinslot.md) representa la relación entre las tarjetas de dispositivo y el chasis en el que se montan.

</dd> <dt>

[**CIM \_ PackageTempSensor**](cim-packagetempsensor.md)
</dt> <dd>

La [**asociación \_ CIM PackageTempSensor**](cim-packagetempsensor.md) representa la relación en la que a menudo se instala un sensor de temperatura en un paquete, como un chasis o un bastidor, para supervisar el entorno del paquete.

</dd> <dt>

[**CIM \_ ParallelController**](cim-parallelcontroller.md)
</dt> <dd>

La [**\_ asociación de CIM ParallelController**](cim-parallelcontroller.md) se relaciona con las funcionalidades y la administración del dispositivo lógico de puerto paralelo.

</dd> <dt>

[**CIM \_ ParticipaInSet**](cim-participatesinset.md)
</dt> <dd>

La [**clase CIM \_ ParticipatesInSet**](cim-participatesinset.md) identifica los elementos físicos que se deben reemplazar juntos.

</dd> <dt>

[**CIM \_ PCIController**](cim-pcicontroller.md)
</dt> <dd>

La [**clase \_ CIM PCIController**](cim-pcicontroller.md) representa las propiedades y la administración de un controlador PCI. Las propiedades de esta clase y sus subclases se definen en las distintas especificaciones de PCI publicadas por PCI SIG.

</dd> <dt>

[**CIM \_ PCMCIAController**](cim-pcmciacontroller.md)
</dt> <dd>

La [**clase \_ CIM PCMCIAController representa**](cim-pcmciacontroller.md) las funciones y la administración de un controlador de asociación internacional de tarjetas de memoria de equipo personal (PCMCIA).

</dd> <dt>

[**CIM \_ PCVideoController**](cim-pcvideocontroller.md)
</dt> <dd>

CIM [**\_ PCVideoController representa**](cim-pcvideocontroller.md) las funciones y la administración de un controlador de vídeo de equipo personal, un subtipo de un controlador de vídeo.

</dd> <dt>

[**CIM \_ PExtentRedundancyComponent**](cim-pextentredundancycomponent.md)
</dt> <dd>

La [**clase CIM \_ PExtentRedundancyComponent**](cim-pextentredundancycomponent.md) representa las extensiones físicas que participan en un grupo de redundancia de almacenamiento.

</dd> <dt>

[**CIM \_ PhysicalCapacity**](cim-physicalcapacity.md)
</dt> <dd>

La [**clase \_ Cim PhysicalCapacity**](cim-physicalcapacity.md) es una clase abstracta que representa los requisitos mínimos y máximos de un elemento físico y su capacidad para admitir distintos tipos de hardware. Por ejemplo, los requisitos mínimos y máximos de memoria se pueden modelar como una subclase de **CIM \_ PhysicalCapacity**.

</dd> <dt>

[**CIM \_ PhysicalComponent**](cim-physicalcomponent.md)
</dt> <dd>

La [**clase \_ PhysicalComponent de CIM**](cim-physicalcomponent.md) representa un componente básico o de bajo nivel dentro de un paquete. Un elemento físico que no es un vínculo, conector o paquete es un descendiente (o miembro) de esta clase.

</dd> <dt>

[**CIM \_ PhysicalConnector**](cim-physicalconnector.md)
</dt> <dd>

La [**clase \_ CIM PhysicalConnector**](cim-physicalconnector.md) representa cualquier elemento físico que se usa para conectarse a otros elementos. Cualquier objeto que pueda conectarse y transmitir señales o potencia entre dos o más elementos físicos es un descendiente (o miembro) de esta clase.

</dd> <dt>

[**Elemento \_ físico CIM**](cim-physicalelement.md)
</dt> <dd>

Las [**subclases \_ PhysicalElement**](cim-physicalelement.md) de CIM definen cualquier componente de un sistema que tenga una identidad física distinta. Las instancias de esta clase se pueden definir en términos de etiquetas que se pueden adjuntar físicamente al objeto .

</dd> <dt>

[**CIM \_ PhysicalElementLocation**](cim-physicalelementlocation.md)
</dt> <dd>

La [**clase \_ CIM PhysicalElementLocation**](cim-physicalelementlocation.md) asocia un elemento físico a un objeto [**Cim \_ Location**](cim-location.md) con fines de inventario o reemplazo.

</dd> <dt>

[**CIM \_ PhysicalExtent**](cim-physicalextent.md)
</dt> <dd>

La [**clase \_ CIM PhysicalExtent**](cim-physicalextent.md) representa una implementación de SCC RAID. Define las direcciones de bloque direccionable consecutivas en un único dispositivo de almacenamiento que se tratan como una sola extensión de almacenamiento en la misma clase [**\_ CIM StorageRedundancyGroup.**](cim-storageredundancygroup.md) Una alternativa, cuando se usa la configuración automática, es crear instancias de la clase [**\_ AggregatePExtent**](cim-aggregatepextent.md) de CIM o ampliarla.

</dd> <dt>

[**CIM \_ PhysicalFrame**](cim-physicalframe.md)
</dt> <dd>

La [**clase \_ PhysicalFrame**](cim-physicalframe.md) cim es una clase primaria de bastidor, chasis y otros gabinetes de marco, tal como se definen en las clases de extensión. En esta clase primaria se incluyen propiedades como **VisibleAlarm** y **AudibleAlarm,** así como datos relacionados con infracciones de seguridad.

</dd> <dt>

[**CIM \_ PhysicalLink**](cim-physicallink.md)
</dt> <dd>

La [**clase \_ CIM PhysicalLink**](cim-physicallink.md) representa el cableado de elementos físicos.

</dd> <dt>

[**CIM \_ PhysicalMedia**](cim-physicalmedia.md)
</dt> <dd>

La [**clase \_ PhysicalMedia**](cim-physicalmedia.md) de CIM representa tipos de documentación y medio de almacenamiento, como cintas, ROMs de CD, entre otros.

</dd> <dt>

[**CIM \_ PhysicalMemory**](cim-physicalmemory.md)
</dt> <dd>

La [**clase \_ Cim PhysicalMemory**](cim-physicalmemory.md) representa dispositivos de memoria de bajo nivel, como SIMMS, DIMM, chips de memoria sin procesar, entre otros.

</dd> <dt>

[**CIM \_ PhysicalPackage**](cim-physicalpackage.md)
</dt> <dd>

La [**clase \_ PhysicalPackage**](cim-physicalpackage.md) de CIM representa elementos físicos que contienen u hospedan otros componentes. Algunos ejemplos son un gabinete de bastidor o una tarjeta adaptadora.

</dd> <dt>

[**CIM \_ PointingDevice**](cim-pointingdevice.md)
</dt> <dd>

La [**clase CIM \_ PointingDevice**](cim-pointingdevice.md) representa un dispositivo que apunta a regiones de la pantalla. Cualquier dispositivo que manipula un puntero o apunta a regiones en una pantalla visual es miembro de esta clase. Por ejemplo, un mouse, un lápiz óptico, un panel táctil o una tableta.

</dd> <dt>

[**CIM \_ POTSModem**](cim-potsmodem.md)
</dt> <dd>

La [**clase \_ CIM POTSModem**](cim-potsmodem.md) representa un dispositivo que traduce los datos binarios en transmisiones de onda para la transmisión basada en sonido mediante la conexión a la red del Sistema de teléfono antiguo sin formato (POTS).

</dd> <dt>

[**CIM \_ PowerSupply**](cim-powersupply.md)
</dt> <dd>

La [**clase CIM \_ PowerSupply**](cim-powersupply.md) representa las funcionalidades y la administración del dispositivo lógico de la fuente de alimentación.

</dd> <dt>

[**Impresora \_ CIM**](cim-printer.md)
</dt> <dd>

La [**clase \_ CIM Printer**](cim-printer.md) representa las funcionalidades y la administración del dispositivo lógico de impresora.

</dd> <dt>

[**Proceso \_ CIM**](cim-process.md)
</dt> <dd>

La [**clase \_ Cim Process**](cim-process.md) representa una única instancia de un programa en ejecución. Normalmente, un usuario ve un proceso como una aplicación o tarea.

</dd> <dt>

[**Proceso \_ CIMExecutable**](cim-processexecutable.md)
</dt> <dd>

La [**clase CIM \_ ProcessExecutable**](cim-processexecutable.md) representa un vínculo entre un proceso y un archivo de datos, e indica que el archivo participa en la ejecución del proceso.

</dd> <dt>

[**Procesador \_ CIM**](cim-processor.md)
</dt> <dd>

La [**clase \_ procesador CIM**](cim-processor.md) representa las funcionalidades y la administración del dispositivo lógico del procesador.

</dd> <dt>

[**CIM \_ ProcessThread**](cim-processthread.md)
</dt> <dd>

La [**clase Cim \_ ProcessThread**](cim-processthread.md) representa un vínculo entre un proceso y los subprocesos que se ejecutan en el contexto del proceso.

</dd> <dt>

[**Producto \_ CIM**](cim-product.md)
</dt> <dd>

La [**clase \_ Cim Product**](cim-product.md) es una clase concreta que representa una colección de elementos físicos, características de software y otros productos adquiridos como una unidad. La adquisición implica un acuerdo entre el proveedor y el consumidor, lo que puede tener implicaciones en las licencias de productos, el soporte técnico y la garantía.

</dd> <dt>

[**CIM \_ ProductFRU**](cim-productfru.md)
</dt> <dd>

La [**clase \_ CIM ProductFRU**](cim-productfru.md) representa una asociación entre el producto y una unidad reemplazable de campo (FRU), que proporciona información sobre los componentes del producto que se han reemplazado o se están reemplazando.

</dd> <dt>

[**CIM \_ ProductParentChild**](cim-productparentchild.md)
</dt> <dd>

La [**\_ asociación CIM ProductParentChild**](cim-productparentchild.md) define una jerarquía de elementos primarios y secundarios entre los productos. Por ejemplo, un producto puede estar empaquetado con otros productos.

</dd> <dt>

[**CIM \_ ProductPhysicalElements**](cim-productphysicalelements.md)
</dt> <dd>

La [**clase \_ CIM ProductPhysicalElements**](cim-productphysicalelements.md) representa los elementos físicos que constituye un producto.

</dd> <dt>

[**CIM \_ ProductProductDependency**](cim-productproductdependency.md)
</dt> <dd>

La [**clase \_ CIM ProductProductDependency**](cim-productproductdependency.md) representa una asociación entre dos productos, lo que indica que uno debe estar instalado o ausente para que el otro funcione. Esto es conceptualmente equivalente a la [**\_ asociación ServiceServiceDependency**](cim-serviceservicedependency.md) de CIM.

</dd> <dt>

[**Producto \_ CIMSoftwareFeatures**](cim-productsoftwarefeatures.md)
</dt> <dd>

La [**\_ asociación CIM ProductSoftwareFeatures**](cim-productsoftwarefeatures.md) identifica las características de software de un producto determinado.

</dd> <dt>

[**CIM \_ ProductSupport**](cim-productsupport.md)
</dt> <dd>

La [**clase \_ CIM ProductSupport**](cim-productsupport.md) representa una asociación entre el producto y el acceso de soporte técnico que transmite cómo se obtiene el soporte técnico para el producto. Hay varios tipos de soporte técnico disponibles para un producto; el mismo objeto de soporte técnico puede proporcionar asistencia para varios productos.

</dd> <dt>

[**CIM \_ ProtectedSpaceExtent**](cim-protectedspaceextent.md)
</dt> <dd>

La [**clase \_ CIM ProtectedSpaceExtent**](cim-protectedspaceextent.md) representa direcciones de bloque lógico direccionables, que se tratan como una sola extensión de almacenamiento, pero se encuentran en una sola extensión física.

</dd> <dt>

[**CIM \_ PSExtentBasedOnPExtent**](cim-psextentbasedonpextent.md)
</dt> <dd>

La [**clase \_ CIM PSExtentBasedOnPExtent**](cim-psextentbasedonpextent.md) asocia extensiones de espacio protegido basadas en una extensión física.

</dd> <dt>

[**Bastidor \_ CIM**](cim-rack.md)
</dt> <dd>

La [**clase CIM \_ Rack**](cim-rack.md) representa un bastidor (un bastidor físico o un gabinete) en el que se almacena el chasis. Normalmente, un bastidor representa el gabinete; todos los componentes en funcionamiento se empaquetan en el chasis.

</dd> <dt>

[**CIM \_ se da cuenta**](cim-realizes.md)
</dt> <dd>

La [**clase CIM \_ Realizes**](cim-realizes.md) representa la asociación que define la asignación entre un dispositivo lógico y el componente físico que implementa el dispositivo.

</dd> <dt>

[**CIM \_ se da cuenta deAggregatePExtent**](cim-realizesaggregatepextent.md)
</dt> <dd>

La [**\_ asociación CIM RealizesAggregatePExtent**](cim-realizesaggregatepextent.md) representa la relación en la que la clase [**\_ AggregatePExtent**](cim-aggregatepextent.md) de CIM se realiza en un medio físico.

</dd> <dt>

[**CIM \_ RealizesDiskPartition**](cim-realizesdiskpartition.md)
</dt> <dd>

La [**clase CIM \_ RealizesDiskPartition**](cim-realizesdiskpartition.md) representa una partición de disco en un medio físico que modela la creación de particiones en una unidad SCSI o IDE sin procesar.

</dd> <dt>

[**CIM \_ realizaPExtent**](cim-realizespextent.md)
</dt> <dd>

La [**\_ asociación CIM RealizesPExtent**](cim-realizespextent.md) representa la relación en la que las extensiones físicas se realizan en un medio físico. Además, se especifica la dirección inicial de la extensión física en el medio físico.

</dd> <dt>

[**RebootAction de CIM \_**](cim-rebootaction.md)
</dt> <dd>

La [**clase \_ RebootAction de CIM**](cim-rebootaction.md) provoca un reinicio del sistema donde está instalado el elemento de software.

</dd> <dt>

[**Redundancia \_ de CIMComponent**](cim-redundancycomponent.md)
</dt> <dd>

La [**clase \_ RedundancyComponent de CIM**](cim-redundancycomponent.md) asocia un grupo de redundancia compuesto de elementos del sistema administrados e indica que, juntos, los elementos proporcionan redundancia. Todos los elementos agregados en un grupo de redundancia deben ser instancias de la misma clase de objeto.

</dd> <dt>

[**CIM \_ RedundancyGroup**](cim-redundancygroup.md)
</dt> <dd>

La [**clase \_ Cim RedundancyGroup**](cim-redundancygroup.md) representa una colección de elementos del sistema administrados, lo que indica que los componentes agregados, juntos, proporcionan redundancia. Todos los elementos agregados en un grupo de redundancia deben ser instancias de la misma clase de objeto.

</dd> <dt>

[**Refrigeración \_ CIM**](cim-refrigeration.md)
</dt> <dd>

La [**clase CIM \_ Refrigeration**](cim-refrigeration.md) representa las funciones y la administración de un dispositivo de refrigeración.

</dd> <dt>

[**CIM \_ RelatedStatistics**](cim-relatedstatistics.md)
</dt> <dd>

La [**\_ asociación RelatedStatistics de CIM**](cim-relatedstatistics.md) representa jerarquías y dependencias de las clases [**\_ statisticalInformation de CIM**](cim-statisticalinformation.md) relacionadas.

</dd> <dt>

[**CIM \_ RemoteFileSystem**](cim-remotefilesystem.md)
</dt> <dd>

La [**clase \_ RemoteFileSystem de CIM**](cim-remotefilesystem.md) representa un sistema de archivos remoto al que se accede mediante un servicio relacionado con la red. En este caso, el almacén de archivos está hospedado por un equipo, que actúa como un servidor de archivos.

</dd> <dt>

[**RemoveDirectoryAction de CIM \_**](cim-removedirectoryaction.md)
</dt> <dd>

La [**clase \_ RemoveDirectoryAction de CIM**](cim-removedirectoryaction.md) quita los directorios de los elementos de software.

</dd> <dt>

[**RemoveFileAction de CIM \_**](cim-removefileaction.md)
</dt> <dd>

La [**clase \_ RemoveFileAction**](cim-removefileaction.md) de CIM desinstala los archivos.

</dd> <dt>

[**CIM \_ ReplacementSet**](cim-replacementset.md)
</dt> <dd>

La [**clase CIM \_ ReplacementSet**](cim-replacementset.md) agrega elementos físicos que se deben reemplazar juntos. Por ejemplo, al reemplazar una tarjeta de memoria, también se pueden quitar y reemplazar los chips de memoria del componente. O bien, esta asociación se puede usar para reemplazar o actualizar un conjunto de chips de memoria.

</dd> <dt>

[**CIM \_ ResidesOnExtent**](cim-residesonextent.md)
</dt> <dd>

La [**clase CIM \_ ResidesOnExtent representa**](cim-residesonextent.md) una asociación entre un sistema de archivos y la extensión de almacenamiento donde se encuentra. Normalmente, un sistema de archivos reside en un disco lógico.

</dd> <dt>

[**CIM \_ en ejecución de OS**](cim-runningos.md)
</dt> <dd>

La [**clase \_ RunningOS de CIM**](cim-runningos.md) representa el sistema operativo que se está ejecutando actualmente. Como máximo, un sistema operativo se puede ejecutar en cualquier momento en un sistema informático; es posible que el sistema del equipo no esté arrancado actualmente o que su sistema operativo sea desconocido.

</dd> <dt>

[**CIM \_ SAPSAPDependency**](cim-sapsapdependency.md)
</dt> <dd>

La [**clase \_ SAPSAPDependency**](cim-sapsapdependency.md) de CIM es una asociación entre dos puntos de acceso de servicio (SAP), lo que indica que el segundo SAP es necesario para que el primer SAP se conecte con su servicio.

</dd> <dt>

[**Escáner \_ CIM**](cim-scanner.md)
</dt> <dd>

El [**escáner CIM \_ representa**](cim-scanner.md) las funcionalidades y la administración del dispositivo lógico del analizador.

</dd> <dt>

[**CIM \_ SCSIController**](cim-scsicontroller.md)
</dt> <dd>

La [**clase \_ CIM SCSIController**](cim-scsicontroller.md) representa las funciones y la administración del dispositivo lógico del controlador SCSI.

</dd> <dt>

[**CIM \_ SCSIInterface**](cim-scsiinterface.md)
</dt> <dd>

representa una [**relación \_ ControlledBy de CIM**](cim-controlledby.md) que indica a qué dispositivos se accede a través de un controlador SCSI y las características de acceso.

</dd> <dt>

[**CIM \_ Sensor**](cim-sensor.md)
</dt> <dd>

La [**clase \_ sensor CIM**](cim-sensor.md) representa un dispositivo de hardware capaz de medir las características de una propiedad física (por ejemplo, las características de temperatura o voltaje de un sistema informático unitario).

</dd> <dt>

[**CIM \_ SerialController**](cim-serialcontroller.md)
</dt> <dd>

La [**clase \_ SerialController de CIM**](cim-serialcontroller.md) representa las funciones y la administración del dispositivo lógico del puerto serie.

</dd> <dt>

[**CIM \_ SerialInterface**](cim-serialinterface.md)
</dt> <dd>

La [**clase Cim \_ SerialInterface**](cim-serialinterface.md) representa una relación [**\_ ControlledBy**](cim-controlledby.md) de CIM que indica a qué dispositivos se accede a través del controlador serie y las características del acceso.

</dd> <dt>

[**Servicio \_ CIM**](cim-service.md)
</dt> <dd>

La [**clase de \_ servicio CIM**](cim-service.md) representa un elemento lógico que contiene información para representar y administrar la funcionalidad proporcionada por una característica de dispositivo o software. Un servicio es un objeto de uso general para configurar y administrar la implementación de la funcionalidad. no es la propia funcionalidad.

</dd> <dt>

[**Servicio \_ CIMAccessBySAP**](cim-serviceaccessbysap.md)
</dt> <dd>

La [**clase de asociación CIM \_ ServiceAccessBySAP**](cim-serviceaccessbysap.md) representa los puntos de acceso de un servicio. Por ejemplo, NetWare, Macintosh o Windows service access points (SAP) pueden acceder a una impresora, que se hospedan potencialmente en sistemas diferentes.

</dd> <dt>

[**Servicio \_ CIMAccessPoint**](cim-serviceaccesspoint.md)
</dt> <dd>

La [**clase CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md) representa la capacidad de usar o invocar un servicio. Los puntos de acceso representan servicios que están disponibles para su uso por otras entidades.

</dd> <dt>

[**CIM \_ ServiceSAPDependency**](cim-servicesapdependency.md)
</dt> <dd>

La [**clase CIM \_ ServiceSAPDependency**](cim-servicesapdependency.md) representa una asociación entre un servicio y un punto de acceso de servicio (SAP), lo que indica que el servicio utiliza la SAP a la que se hace referencia para proporcionar su funcionalidad.

</dd> <dt>

[**CIM \_ ServiceServiceDependency**](cim-serviceservicedependency.md)
</dt> <dd>

La [**clase CIM \_ ServiceServiceDependency**](cim-serviceservicedependency.md) representa una asociación entre dos servicios.

</dd> <dt>

[**Configuración de CIM \_**](cim-setting.md)
</dt> <dd>

La [**clase CIM \_ Setting**](cim-setting.md) representa parámetros operativos y relacionados con la configuración para uno o varios elementos del sistema administrados.

</dd> <dt>

[**CIM \_ SettingCheck**](cim-settingcheck.md)
</dt> <dd>

La [**clase CIM \_ SettingCheck**](cim-settingcheck.md) especifica la información necesaria para comprobar un archivo de configuración determinado para una entrada específica que contiene un valor igual al valor especificado. Se supone que todas las comparaciones no tienen en cuenta mayúsculas de minúsculas.

</dd> <dt>

[**CIM \_ SettingContext**](cim-settingcontext.md)
</dt> <dd>

La [**clase \_ SettingContext de CIM**](cim-settingcontext.md) asocia los objetos de configuración a los objetos de configuración.

</dd> <dt>

[**Ranura \_ CIM**](cim-slot.md)
</dt> <dd>

La [**clase de \_ ranura CIM**](cim-slot.md) representa los conectores en los que se insertan los paquetes.

</dd> <dt>

[**CIM \_ SlotInSlot**](cim-slotinslot.md)
</dt> <dd>

La [**relación \_ cim slotInSlot**](cim-slotinslot.md) representa la capacidad de un adaptador especial para ampliar la estructura de ranuras existente para permitir que las tarjetas incompatibles de otro modo se conecten a un marco o a una placa de hospedaje.

</dd> <dt>

[**CIM \_ SoftwareElement**](cim-softwareelement.md)
</dt> <dd>

La [**clase \_ CIM SoftwareElement**](cim-softwareelement.md) descompone un objeto [**CIM \_ SoftwareFeature**](cim-softwarefeature.md) en un conjunto de elementos administrables o implementables individualmente para una plataforma determinada. La plataforma de un elemento de software se identifica de forma única por su arquitectura de hardware y sistema operativo subyacentes.

</dd> <dt>

[**CIM \_ SoftwareElementActions**](cim-softwareelementactions.md)
</dt> <dd>

La [**\_ asociación CIM SoftwareElementActions**](cim-softwareelementactions.md) identifica las acciones de un elemento de software.

</dd> <dt>

[**CIM \_ SoftwareElementChecks**](cim-softwareelementchecks.md)
</dt> <dd>

La [**clase \_ de asociación CIM SoftwareElementChecks**](cim-softwareelementchecks.md) relaciona un elemento de software con la información de condición o ubicación que puede requerir una característica.

</dd> <dt>

[**CIM \_ SoftwareElementVersionCheck**](cim-softwareelementversioncheck.md)
</dt> <dd>

La [**\_ clase CIM SoftwareElementVersionCheck**](cim-softwareelementversioncheck.md) representa un tipo de elemento de software que debe existir en el entorno.

</dd> <dt>

[**CIM \_ SoftwareFeature**](cim-softwarefeature.md)
</dt> <dd>

La [**clase \_ CIM SoftwareFeature**](cim-softwarefeature.md) representa una función o funcionalidad determinadas de un producto o sistema de aplicación.

</dd> <dt>

[**CIM \_ SoftwareFeatureSAPImplementation**](cim-softwarefeaturesapimplementation.md)
</dt> <dd>

La [**clase \_ CIM SoftwareFeatureSAPImplementation**](cim-softwarefeaturesapimplementation.md) representa una asociación entre un punto de acceso de servicio (SAP) y cómo se implementa en el software.

</dd> <dt>

[**CIM \_ SoftwareFeatureServiceImplementation**](cim-softwarefeatureserviceimplementation.md)
</dt> <dd>

La [**\_ clase CIM SoftwareFeatureServiceImplementation**](cim-softwarefeatureserviceimplementation.md) representa una asociación entre un servicio y cómo se implementa en el software.

</dd> <dt>

[**CIM \_ SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md)
</dt> <dd>

La [**\_ asociación CIM SoftwareFeatureSoftwareElements**](cim-softwarefeaturesoftwareelements.md) identifica los elementos de software que son una característica de software específica.

</dd> <dt>

[**CIM \_ SpareGroup**](cim-sparegroup.md)
</dt> <dd>

La [**clase \_ CIM SpareGroup**](cim-sparegroup.md) se deriva de la clase [**Cim \_ RedundancyGroup**](cim-redundancygroup.md) e indica que se pueden ahorrar uno o varios de los elementos agregados.

</dd> <dt>

[**CIM \_ StatisticalInformation**](cim-statisticalinformation.md)
</dt> <dd>

La [**clase \_ StatisticalInformation**](cim-statisticalinformation.md) de CIM es una clase raíz para la colección arbitraria de datos estadísticos o métricas aplicables a uno o varios elementos del sistema administrados.

</dd> <dt>

[**Estadísticas de CIM \_**](cim-statistics.md)
</dt> <dd>

La [**clase CIM \_ Statistics**](cim-statistics.md) representa una asociación que relaciona los elementos administrados del sistema con los grupos estadísticos que se les aplican.

</dd> <dt>

[**CIM \_ StorageDefect**](cim-storagedefect.md)
</dt> <dd>

La [**\_ agregación StorageDefect de CIM**](cim-storagedefect.md) recopila los errores de almacenamiento de una extensión de almacenamiento.

</dd> <dt>

[**CIM \_ StorageError**](cim-storageerror.md)
</dt> <dd>

La [**clase \_ StorageError de CIM**](cim-storageerror.md) representa bloques de espacio de memoria o multimedia que están asignados fuera de uso debido a errores. La clave de la clase es la **propiedad StartingAddress** de los bytes en error.

</dd> <dt>

[**CIM \_ StorageExtent**](cim-storageextent.md)
</dt> <dd>

La [**clase \_ StorageExtent de CIM**](cim-storageextent.md) representa las funciones y la administración de los distintos medios que existen para almacenar datos y permitir la recuperación de datos. Esta clase primaria puede representar los distintos componentes de RAID (hardware o software) o una extensión lógica sin procesar sobre los medios físicos.

</dd> <dt>

[**CIM \_ StorageRedundancyGroup**](cim-storageredundancygroup.md)
</dt> <dd>

La [**clase CIM \_ StorageRedundancyGroup representa**](cim-storageredundancygroup.md) información de redundancia masiva relacionada con el almacenamiento.

</dd> <dt>

[**Compatibilidad \_ de CIMAcceso**](cim-supportaccess.md)
</dt> <dd>

La [**clase \_ SupportAccess**](cim-supportaccess.md) de CIM define cómo obtener ayuda para un producto.

</dd> <dt>

[**SWAPSpaceCheck de CIM \_**](cim-swapspacecheck.md)
</dt> <dd>

La [**clase \_ SWAPSpaceCheck**](cim-swapspacecheck.md) de CIM especifica la cantidad de espacio de intercambio que debe estar disponible en el sistema.

</dd> <dt>

[**Sistema \_ CIM**](cim-system.md)
</dt> <dd>

La [**clase \_ cim system**](cim-system.md) agrega un conjunto enumerable de elementos del sistema administrados. La agregación funciona como un conjunto funcional. Dentro de cualquier subclase concreta del sistema, hay una lista bien definida de clases de elementos del sistema administrado cuyas instancias se deben agregar.

</dd> <dt>

[**CIM \_ SystemComponent**](cim-systemcomponent.md)
</dt> <dd>

una Modelo de información común de asociación (CIM) que establece relaciones entre un sistema y los elementos del sistema administrados de los que se compone.

</dd> <dt>

[**SISTEMA \_ CIMDispositivo**](cim-systemdevice.md)
</dt> <dd>

La [**\_ asociación SystemDevice**](cim-systemdevice.md) de CIM representa una relación explícita en la que un sistema puede agregar dispositivos lógicos.

</dd> <dt>

[**CIM \_ SystemResource**](cim-systemresource.md)
</dt> <dd>

La [**clase \_ SystemResource**](cim-systemresource.md) de CIM representa una entidad administrada por BIOS o un sistema operativo que está disponible para su uso por software y dispositivos lógicos.

</dd> <dt>

[**CIM \_ Tachometer**](cim-tachometer.md)
</dt> <dd>

La [**clase \_ CIM Tachometer**](cim-tachometer.md) existe por compatibilidad con versiones anteriores con definiciones de esquema CIM anteriores.

</dd> <dt>

[**CIM \_ TapeDrive**](cim-tapedrive.md)
</dt> <dd>

La [**clase \_ TapeDrive de CIM**](cim-tapedrive.md) representa una unidad de cinta en el sistema. Las unidades de cinta se distinguen principalmente en que solo se puede acceder a ellas secuencialmente.

</dd> <dt>

[**CIM \_ TemperatureSensor**](cim-temperaturesensor.md)
</dt> <dd>

La [**clase CIM \_ TemperatureSensor**](cim-temperaturesensor.md) existe por compatibilidad con versiones anteriores con definiciones de esquema CIM anteriores.

</dd> <dt>

[**Subproceso \_ CIM**](cim-thread.md)
</dt> <dd>

La [**clase de \_ subproceso CIM**](cim-thread.md) representa la capacidad de ejecutar unidades de un proceso o tarea, en paralelo. Un proceso puede tener muchos subprocesos, cada uno de los cuales es débil para el proceso.

</dd> <dt>

[**CIM \_ ToDirectoryAction**](cim-todirectoryaction.md)
</dt> <dd>

La [**\_ asociación Cim ToDirectoryAction**](cim-todirectoryaction.md) identifica el directorio de destino para la acción de archivo.

</dd> <dt>

[**CIM \_ ToDirectorySpecification**](cim-todirectoryspecification.md)
</dt> <dd>

La [**\_ asociación Cim ToDirectorySpecification**](cim-todirectoryspecification.md) identifica el directorio de destino para la acción de archivo.

</dd> <dt>

[**CIM \_ UninterruptiblePowerSupply**](cim-uninterruptiblepowersupply.md)
</dt> <dd>

La [**clase CIM \_ UninterruptiblePowerSupply**](cim-uninterruptiblepowersupply.md) representa las funciones y la administración de una fuente de alimentación ininterrumpida (UPS).

</dd> <dt>

[**CIM \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md)
</dt> <dd>

La [**clase \_ UnitaryComputerSystem**](cim-unitarycomputersystem.md) de CIM representa un equipo de escritorio, móvil, equipo de red, servidor u otro tipo de sistema de equipo de nodo único.

</dd> <dt>

[**CIM \_ USBController**](cim-usbcontroller.md)
</dt> <dd>

La [**clase \_ CIM USBController**](cim-usbcontroller.md) representa las funciones y la administración de un controlador USB.

</dd> <dt>

[**CIM \_ USBControllerHasHub**](cim-usbcontrollerhashub.md)
</dt> <dd>

La [**clase \_ CIM USBControllerHasHub**](cim-usbcontrollerhashub.md) define los concentradores que están en la bajada del controlador USB.

</dd> <dt>

[**CIM \_ USBDevice**](cim-usbdevice.md)
</dt> <dd>

La [**clase \_ CIM USBDevice**](cim-usbdevice.md) representa las características de administración de un dispositivo USB.

</dd> <dt>

[**CIM \_ USBHub**](cim-usbhub.md)
</dt> <dd>

La [**clase \_ CIM USBHub**](cim-usbhub.md) representa las funcionalidades y la administración de un concentrador USB.

</dd> <dt>

[**CIM \_ UserDevice**](cim-userdevice.md)
</dt> <dd>

La [**clase \_ UserDevice**](cim-userdevice.md) de CIM es una clase primaria de la que descienden otras clases, como [**CIM \_ Keyboard**](cim-keyboard.md) o [**CIM \_ DesktopMonitor.**](cim-desktopmonitor.md) Los dispositivos de usuario son dispositivos lógicos que permiten al usuario de un sistema informático introducir, ver o escuchar datos.

</dd> <dt>

[**CIM \_ VersionCompatibilityCheck**](cim-versioncompatibilitycheck.md)
</dt> <dd>

La [**clase CIM \_ VersionCompatibilityCheck**](cim-versioncompatibilitycheck.md) especifica si está permitido crear el siguiente estado de un elemento de software.

</dd> <dt>

[**CIM \_ VideoBIOSElement**](cim-videobioselement.md)
</dt> <dd>

La [**clase \_ CIM VideoBIOSElement**](cim-videobioselement.md) representa el software de bajo nivel que se carga en el almacenamiento no volátil y se usa para configurar y acceder al controlador de vídeo y la pantalla de un sistema informático.

</dd> <dt>

[**\_Vídeo CIMBIOSFeature**](cim-videobiosfeature.md)
</dt> <dd>

La [**clase \_ CIM VideoBIOSFeature**](cim-videobiosfeature.md) representa las funciones del software de bajo nivel que se usa para configurar y acceder al controlador de vídeo y la pantalla de un sistema informático.

</dd> <dt>

[**Vídeo \_ CIMBIOSFeatureVideoBIOSElements**](cim-videobiosfeaturevideobioselements.md)
</dt> <dd>

La [**clase CIM \_ VideoBIOSFeatureVideoBIOSElements**](cim-videobiosfeaturevideobioselements.md) asocia una característica bios de vídeo y sus elementos bios de vídeo agregados.

</dd> <dt>

[**CIM \_ VideoController**](cim-videocontroller.md)
</dt> <dd>

La [**clase \_ CIM VideoController**](cim-videocontroller.md) representa las funciones y la administración del controlador de vídeo.

</dd> <dt>

[**CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md)
</dt> <dd>

La [**clase CIM \_ VideoControllerResolution**](cim-videocontrollerresolution.md) representa los distintos modos de vídeo que puede admitir un controlador de vídeo.

</dd> <dt>

[**CIM \_ VideoSetting**](cim-videosetting.md)
</dt> <dd>

La [**clase \_ CIM VideoSetting**](cim-videosetting.md) asocia el objeto de configuración [**\_ VideoControllerResolution**](cim-videocontrollerresolution.md) de CIM con el controlador al que se aplica.

</dd> <dt>

[**CIM \_ VolatileStorage**](cim-volatilestorage.md)
</dt> <dd>

La [**clase \_ VOLATILEStorage de CIM**](cim-volatilestorage.md) representa las funciones y la administración del almacenamiento volátil.

</dd> <dt>

[**CIM \_ VoltageSensor**](cim-voltagesensor.md)
</dt> <dd>

La [**clase CIM \_ VoltageSensor existe**](cim-voltagesensor.md) por compatibilidad con versiones anteriores con las definiciones de esquema CIM anteriores. Con las adiciones a las [**clases \_ CIM Sensor**](cim-sensor.md) y CIM [**\_ NumericSensor**](cim-numericsensor.md) en la versión 2.2, ya no es necesario.

</dd> <dt>

[**CIM \_ VolumeSet**](cim-volumeset.md)
</dt> <dd>

La [**clase CIM \_ VolumeSet**](cim-volumeset.md) representa un intervalo contiguo de bloques lógicos presentados al entorno operativo para leer y escribir datos de usuario.

</dd> <dt>

[**CIM \_ WORMDrive**](cim-wormdrive.md)
</dt> <dd>

La [**clase \_ WORMDrive de CIM**](cim-wormdrive.md) representa las funciones y la administración de una unidad WORM, un subtipo del dispositivo de acceso multimedia.

</dd> </dl>

 

 
