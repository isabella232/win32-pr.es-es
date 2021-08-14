---
description: Objeto LUN
ms.assetid: ea22bd6d-4a7a-4674-82e9-08460914ff8e
title: Objeto LUN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d315e33b8d253e346b42b01f86a85379aadace73e517a169cc653214a9c674d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118347496"
---
# <a name="lun-object"></a>Objeto LUN

\[A partir Windows 8 y Windows Server 2012, la interfaz COM del servicio [virtual](virtual-disk-service-portal.md) de disco se sustituye por [el Windows Storage API de Administración](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un objeto LUN (número de unidad lógica) modela una unidad lógica de espacio de almacenamiento direccionable creado por un proveedor de hardware y que un subsistema ha presentado. Cada LUN consta de al menos un plex LUN, que a su vez se compone de extensiones de una o varias unidades.

## <a name="lun-types"></a>Tipos de LUN

VDS admite cinco tipos de LUN: simple, con intervalos, seccionado, reflejado y seccionado con paridad. Los LUN simples, con intervalos y seccionados no son tolerantes a errores; los LUN reflejados y paridad son tolerantes a errores. En el resto de esta sección se describe cada uno de los tipos de LUN vds.

-   Un LUN simple es un LUN no tolerante a errores que se forma de una sola extensión de unidad contigua desde una sola unidad. La extensión contigua puede estar formada por un único intervalo de bloques o varios intervalos de bloques vinculados entre sí.
-   Un LUN abarcado es un LUN no tolerante a errores que se conste de varias extensiones desconcertadas de varias unidades. Los datos se escriben linealmente en cada una de las extensiones de la primera unidad hasta que se rellenan todas las extensiones de la primera unidad y, a continuación, en cada una de las extensiones de la segunda unidad, y así sucesivamente. Los LUN abarcados proporcionan un uso eficaz del espacio de unidad en subsistemas que constan de unidades de varios tamaños.
-   Un LUN seccionado es un LUN tolerante a errores que se forma de varias extensiones contiguas intercaladas de varias unidades. Los LUN seccionados usan una configuración RAID-0, de modo que los datos se "seccionan" cíclicamente en las extensiones de las unidades que contribuyen. Los LUN seccionados funcionan mejor con unidades del mismo tamaño, modelo y fabricante.
-   Los LUN reflejados son LUN tolerantes a errores que proporcionan recuperación ante desastres mediante la duplicación de los datos en varios plexos LUN. Cada plex de un LUN reflejado contiene una copia de los datos almacenados en el plex original. Cada uno de los plexos reside en una unidad independiente. Todos los datos que se escriben en un LUN reflejado se escriben simultáneamente en cada uno de sus plexos. Si se producirá un error en una de las unidades que contribuyen, el plex de esa unidad deja de estar disponible, pero el sistema sigue funcionando con los plex o plex no afectados. Un LUN reflejado puede tener cualquier número de plexos.
-   Los LUN seccionados con paridad son LUN tolerantes a errores que proporcionan recuperación ante desastres mediante la seccionación intermitente de datos de paridad en tres o más unidades. Si se producirá un error en una de las unidades que contribuyen, los datos perdidos se pueden volver a crear a partir de los datos restantes y la paridad.

## <a name="lun-creation"></a>Creación de LUN

VDS admite cuatro modelos mediante los que las aplicaciones pueden crear LUN: dirigidos explícitamente, dirigidos parcialmente, automagic y específicos del proveedor. Todos los proveedores de hardware deben admitir la creación de LUN dirigidos explícita y parcialmente, y se recomienda encarecidamente que admitan la creación automática de LUN. (La creación de LUN específica del proveedor está fuera del ámbito de esta guía).

La creación de LUN dirigida explícitamente permite al autor de la llamada especificar todos los atributos del LUN. La creación de LUN dirigida parcialmente permite al autor de la llamada especificar solo los atributos que son de especial interés y, a continuación, permite al proveedor elegir el resto. La creación de LUN de Automagic implica permitir que el autor de la llamada simplemente especifique el tipo y el tamaño de LUN junto con un conjunto de "sugerencias de automagic" (preferencias predefinidas para los atributos LUN) y, a continuación, permitir que el proveedor cree el LUN automáticamente.

## <a name="lun-masking"></a>Enmascaramiento de LUN

VDS admite la desenmascaración de LUN para subsistemas que ofrecen esta funcionalidad. Todos los LUN se encuentran en el equipo en el que se ejecuta el proveedor. La desenmascaramiento de LUN permite que un autor de la llamada "desenmascare" los LUN seleccionados en otros equipos de la red. Si desenmascara un LUN en un equipo, el equipo tiene acceso al LUN. Los equipos para los que se enmascara un LUN no lo hacen.

Un LUN sin máscara expone las interfaces [**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun) e [**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk) al host local. Puede usar **IVdsDisk** para agregar un LUN a un paquete de proveedor de software, crear y quitar volúmenes, asignar letras de unidad, y así sucesivamente. Para obtener más información sobre las operaciones realizadas en un disco, vea el [objeto de disco](disk-object.md).

Una vez que un LUN se desenmascara en una máquina de destino o se enmascara desde una máquina de destino, es posible que la visibilidad del LUN en esa máquina no cambie hasta que se vuelva a examinar un bus. La aplicación VDS de la máquina de destino inicia el nuevo análisis del bus mediante una llamada a [**IVdsService::Reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate). El inicio del nuevo análisis del bus es responsabilidad de la aplicación VDS, no del proveedor de hardware.

## <a name="lun-multipathing"></a>Múltiples rutas de LUN

Los proveedores de hardware que admiten E/S de múltiples rutas (MPIO) pueden establecer directivas de equilibrio de carga en las rutas de acceso entre un LUN y el host local. Los LUN que admiten esta funcionalidad exponen la [**interfaz IVdsLunMpio**](/windows/desktop/api/Vds/nn-vds-ivdslunmpio) al host local.

## <a name="working-with-luns"></a>Trabajar con LUN

Use el [**método IVdsSubSystem::CreateLun**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-createlun) para crear un nuevo objeto LUN. Puede consultar los LUN que expone un subsistema específico invocando el método [**QueryLuns,**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-queryluns) también expuesto por [**IVdsSubSystem**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem). Un llamador puede obtener un puntero a un LUN específico seleccionando el objeto LUN deseado de la enumeración devuelta por **QueryLuns**. Con un objeto LUN, puede establecer el estado de LUN; consulta de todos los controladores activos, plexos y sugerencias de automagic; ampliar y reducir el LUN; agregar y quitar plexos; set masks; aplicar sugerencias; y eliminar el LUN.

Además de un identificador de objeto, un nombre y un número de serie, las propiedades del objeto LUN incluyen el tipo lun, el tamaño, el estado, el estado, el estado de transición y las marcas. una lista de desenmascaramiento; y una configuración de prioridad de recompilación.

En la tabla siguiente se enumeran las interfaces, enumeraciones y estructuras relacionadas.



| Tipo                                                                                              | Elemento                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que siempre expone este objeto                                                 | [**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun)                                                                                                                                                                                                                                                                                          |
| Interfaces que siempre expone este objeto en VDS 1.1 y 2.0 Canal de fibra proveedores | [**IVdsLunControllerPorts**](/windows/desktop/api/Vds/nn-vds-ivdsluncontrollerports)                                                                                                                                                                                                                                                            |
| Interfaces que siempre expone este objeto en proveedores de iSCSI VDS 1.1 y 2.0         | [**IVdsLunIscsi**](/windows/desktop/api/Vds/nn-vds-ivdsluniscsi)                                                                                                                                                                                                                                                                                |
| Interfaces que puede exponer este objeto\*                                                   | [**IVdsMaintenance,**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance) [**IVdsLunMpio,**](/windows/desktop/api/Vds/nn-vds-ivdslunmpio) [**IVdsLunNaming**](/windows/desktop/api/Vds/nn-vds-ivdslunnaming)e [**IVdsLunNumber**](/windows/desktop/api/Vds/nn-vds-ivdslunnumber)**Windows Server 2008, Windows Vista y Windows Server 2003:** no se admite la interfaz [**IVdsLunNumber.**](/windows/desktop/api/Vds/nn-vds-ivdslunnumber)<br/> |
| Enumeraciones asociadas                                                                           | [**VDS \_ LUN \_ FLAG y**](/windows/desktop/api/Vds/ne-vds-vds_lun_flag) [**VDS LUN \_ \_ STATUS**](/windows/desktop/api/Vds/ne-vds-vds_lun_status)y [**VDS LUN \_ \_ TYPE**](/windows/desktop/api/Vds/ne-vds-vds_lun_type)                                                                                                                                                                                   |
| Estructuras asociadas                                                                             | [**VDS \_ INFORMACIÓN \_ DE LUN,**](/windows/desktop/api/VdsLun/ns-vdslun-vds_lun_information) [**PROP DE LUN \_ \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_lun_prop)y [**NOTIFICACIÓN DE LUN \_ VDS \_**](/windows/desktop/api/Vds/ns-vds-vds_lun_notification)                                                                                                                                                            |



 

\* Consulte [Disk Object (Objeto](disk-object.md) de disco) para obtener una interfaz adicional [**(IVdsDisk)**](/windows/desktop/api/Vds/nn-vds-ivdsdisk)que se expone si el LUN se desenmascara como un disco en el equipo host local.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos de proveedor de hardware](hardware-provider-objects.md)
</dt> <dt>

[Pack (objeto)](pack-object.md)
</dt> <dt>

[Objeto de disco](disk-object.md)
</dt> <dt>

[**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun)
</dt> <dt>

[**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk)
</dt> <dt>

[Agregar una letra de unidad a un LUN](adding-a-drive-letter-to-a-lun.md)
</dt> </dl>

 

