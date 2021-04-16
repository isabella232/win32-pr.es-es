---
description: Objeto LUN
ms.assetid: ea22bd6d-4a7a-4674-82e9-08460914ff8e
title: Objeto LUN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad74fa65802adb1439360fb2fcdb423c642ef736
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678447"
---
# <a name="lun-object"></a>Objeto LUN

\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un objeto LUN (número de unidad lógica) modela una unidad lógica de espacio de almacenamiento direccionable creado por un proveedor de hardware y expuesta por un subsistema. Cada LUN incluye al menos un Plex de LUN, que a su vez se compone de extensiones de una o más unidades.

## <a name="lun-types"></a>Tipos de LUN

VDS admite cinco tipos de LUN: simples, distribuidos, seccionados, reflejados y seccionados con paridad. Los LUN simples, distribuidos y seccionados no son tolerantes a errores. los LUN reflejados y de paridad son tolerantes a errores. En el resto de esta sección se describe cada uno de los tipos de LUN de VDS.

-   Un LUN simple es un LUN sin tolerancia a errores que se compone de una única extensión de unidad contigua de una sola unidad. La extensión contigua puede constar de un solo intervalo de bloques o varios intervalos de bloques vinculados entre sí.
-   Un LUN distribuido es un LUN no tolerante a errores que se compone de varias extensiones no contiguas de varias unidades. Los datos se escriben linealmente en cada una de las extensiones de la primera unidad hasta que se rellenan todas las primeras extensiones de unidad y, a continuación, en cada una de las extensiones de la segunda unidad, y así sucesivamente. Los LUN distribuidos proporcionan un uso eficaz del espacio de la unidad en subsistemas que se componen de unidades de distintos tamaños.
-   Un LUN seccionado es un LUN no tolerante a errores compuesto por varias extensiones contiguas intercaladas de varias unidades. Los LUN seccionados usan una configuración de RAID-0, de modo que los datos se "seccionan" cíclicamente en las extensiones de las unidades contribuyentes. Los LUN seccionados funcionan mejor con las unidades del mismo tamaño, modelo y fabricante.
-   Los LUN reflejados son LUN tolerantes a errores que permiten la recuperación ante desastres mediante la duplicación de los datos en varios complejos LUN. Cada complejo de un LUN reflejado contiene una copia de los datos que se almacenan en el Plex original. Cada uno de los Plex reside en una unidad independiente. Todos los datos que se escriben en un LUN reflejado se escriben simultáneamente en cada uno de sus complejos. Si se produce un error en una de las unidades contribuyentes, el Plex de esa unidad deja de estar disponible, pero el sistema continúa funcionando con el Plex o complejos no afectados. Un LUN reflejado puede tener cualquier número de Plex.
-   Los LUN seccionados con paridad son LUN con tolerancia a errores que permiten la recuperación ante desastres mediante la división intermitente de datos de paridad en tres o más unidades. Si se produce un error en una de las unidades contribuyentes, los datos perdidos se pueden volver a crear a partir de los datos y la paridad restantes.

## <a name="lun-creation"></a>Creación de LUN

VDS admite cuatro modelos en los que las aplicaciones pueden crear LUN: explícitamente dirigidas, parcialmente dirigidas, automagic y específicas del proveedor. Todos los proveedores de hardware deben admitir la creación de LUN de forma explícita y parcial, y se recomienda encarecidamente que admitan la creación de LUN de automagic. (La creación de LUN específica del proveedor está fuera del ámbito de esta guía).

La creación de LUN dirigida explícitamente permite al llamador especificar todos los atributos del LUN. La creación de LUN dirigida parcialmente permite al llamador especificar solo los atributos que son de especial interés y, a continuación, permite al proveedor elegir el resto. La creación de LUN de automagic implica que el autor de la llamada solo debe especificar el tipo de LUN y el tamaño junto con un conjunto de "sugerencias automágicas" (preferencias predefinidas para los atributos de LUN) y, a continuación, permitir que el proveedor cree el LUN automáticamente.

## <a name="lun-masking"></a>Enmascaramiento de LUN

VDS admite el desenmascaramiento de LUN para los subsistemas que ofrecen esta funcionalidad. Todos los LUN se muestran en el equipo en el que se ejecuta el proveedor. El desenmascaramiento de LUN permite a un llamador "desenmascarar" los LUN seleccionados en otros equipos de la red. Si se desenmascara un LUN en un equipo, el equipo tiene acceso al LUN. Los equipos para los que se enmascara un LUN no lo hacen.

Un LUN sin máscara expone las interfaces [**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun) y [**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk) al host local. Puede usar **IVdsDisk** para agregar un LUN a un paquete de proveedor de software, crear y quitar volúmenes, asignar Letras de unidad, etc. Para obtener más información acerca de las operaciones realizadas en un disco, consulte el [objeto Disk](disk-object.md).

Una vez que se desenmascara un LUN en un equipo de destino o se enmascara desde un equipo de destino, es posible que la visibilidad del LUN en ese equipo no cambie hasta que se realice un nuevo examen de bus. La aplicación VDS en el equipo de destino inicia el nuevo examen de bus mediante una llamada a [**IVdsService:: reenumerate**](/windows/desktop/api/Vds/nf-vds-ivdsservice-reenumerate). El inicio del nuevo examen de bus es responsabilidad de la aplicación VDS, no del proveedor de hardware.

## <a name="lun-multipathing"></a>Múltiples rutas de LUN

Los proveedores de hardware que admiten e/s de múltiples rutas (MPIO) pueden establecer directivas de equilibrio de carga en rutas de acceso entre un LUN y el host local. Los LUN que admiten esta funcionalidad exponen la interfaz [**IVdsLunMpio**](/windows/desktop/api/Vds/nn-vds-ivdslunmpio) al host local.

## <a name="working-with-luns"></a>Trabajar con LUN

Use el método [**IVdsSubSystem:: CreateLun**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-createlun) para crear un nuevo objeto LUN. Puede consultar los LUN que aparecen en un subsistema específico invocando el método [**QueryLuns**](/windows/desktop/api/Vds/nf-vds-ivdssubsystem-queryluns) , también expuesto por [**IVdsSubSystem**](/windows/desktop/api/Vds/nn-vds-ivdssubsystem). Un llamador puede obtener un puntero a un LUN específico seleccionando el objeto LUN deseado de la enumeración devuelta por **QueryLuns**. Con un objeto LUN, puede establecer el estado de LUN; consultar todos los controladores activos, complejos y sugerencias de automagic; Extienda y reduzca el LUN; Agregar y quitar complejos; establecer máscaras; aplicar sugerencias; y elimine el LUN.

Además de un identificador de objeto, un nombre y un número de serie, las propiedades del objeto LUN incluyen el tipo de LUN, el tamaño, el estado, el estado, el estado de la transición y las marcas; lista de desenmascaramiento; y un valor de prioridad de recompilación.

En la tabla siguiente se enumeran las interfaces, las enumeraciones y las estructuras relacionadas.



| Tipo                                                                                              | Elemento                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces que siempre expone este objeto                                                 | [**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun)                                                                                                                                                                                                                                                                                          |
| Interfaces que siempre expone este objeto en VDS 1,1 y 2,0 Canal de fibra proveedores | [**IVdsLunControllerPorts**](/windows/desktop/api/Vds/nn-vds-ivdsluncontrollerports)                                                                                                                                                                                                                                                            |
| Interfaces que siempre expone este objeto en los proveedores iSCSI de VDS 1,1 y 2,0         | [**IVdsLunIscsi**](/windows/desktop/api/Vds/nn-vds-ivdsluniscsi)                                                                                                                                                                                                                                                                                |
| Interfaces que puede exponer este objeto\*                                                   | [**IVdsMaintenance**](/windows/desktop/api/Vds/nn-vds-ivdsmaintenance), [**IVdsLunMpio**](/windows/desktop/api/Vds/nn-vds-ivdslunmpio), [**IVdsLunNaming**](/windows/desktop/api/Vds/nn-vds-ivdslunnaming)y [**IVdsLunNumber**](/windows/desktop/api/Vds/nn-vds-ivdslunnumber)**windows Server 2008, Windows Vista y Windows Server 2003:** no se admite la interfaz [**IVdsLunNumber**](/windows/desktop/api/Vds/nn-vds-ivdslunnumber) .<br/> |
| Enumeraciones asociadas                                                                           | [**VDS \_ \_Marca de LUN**](/windows/desktop/api/Vds/ne-vds-vds_lun_flag) y [**\_ \_ Estado de LUN de VDS**](/windows/desktop/api/Vds/ne-vds-vds_lun_status), y [**\_ \_ tipo de LUN de VDS**](/windows/desktop/api/Vds/ne-vds-vds_lun_type)                                                                                                                                                                                   |
| Estructuras asociadas                                                                             | [**VDS \_ \_Información de LUN**](/windows/desktop/api/VdsLun/ns-vdslun-vds_lun_information), [**\_ \_ propuesta de LUN de VDS**](/windows/desktop/api/Vds/ns-vds-vds_lun_prop)y [**\_ \_ notificación de LUN de VDS**](/windows/desktop/api/Vds/ns-vds-vds_lun_notification)                                                                                                                                                            |



 

\* Consulte el [objeto de disco](disk-object.md) para obtener una interfaz adicional ([**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk)) que se expone si el LUN no se enmascara como disco en el equipo host local.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos de proveedor de hardware](hardware-provider-objects.md)
</dt> <dt>

[Objeto de paquete](pack-object.md)
</dt> <dt>

[Disk (objeto)](disk-object.md)
</dt> <dt>

[**IVdsLun**](/windows/desktop/api/Vds/nn-vds-ivdslun)
</dt> <dt>

[**IVdsDisk**](/windows/desktop/api/Vds/nn-vds-ivdsdisk)
</dt> <dt>

[Agregar una letra de unidad a un LUN](adding-a-drive-letter-to-a-lun.md)
</dt> </dl>

 

