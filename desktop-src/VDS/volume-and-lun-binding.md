---
description: Enlace de volúmenes y LUN
ms.assetid: ae32b354-799e-4f9b-8989-02bd95968210
title: Enlace de volúmenes y LUN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9f62e599f5b5e457a1ce6dbf6a52524d1b80d1
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/04/2021
ms.locfileid: "104279714"
---
# <a name="volume-and-lun-binding"></a>Enlace de volúmenes y LUN

\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

El enlace es la creación de volúmenes o LUN. Los volúmenes se componen de extensiones de disco y LUN se componen de extensiones de unidad. El enlace selecciona un conjunto de asignaciones para los recursos físicos y se produce dentro de un subsistema, dentro de un paquete o en ambos. Todos los programas de proveedor admiten el enlace parcialmente dirigido a un modelo en el que el autor de la llamada especifica solo los atributos de enlace de interés particular y permite al proveedor elegir el resto. Las operaciones en VDS para los volúmenes de enlace y LUN son similares, pero no idénticas. Por ejemplo, los proveedores de hardware pueden ofrecer opciones de enlace adicionales.

VDS admite los siguientes cinco tipos de enlaces de volumen y LUN para las configuraciones dirigidas parcialmente. (Los proveedores de hardware pueden y admiten muchos otros enlaces).



| Término                                                                                                                                             | Descripción                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="Simple"></span><span id="simple"></span><span id="SIMPLE"></span>Simple<br/>                                                     | Asignación lineal con una y solo una extensión contigua.<br/>                             |
| <span id="Spanned"></span><span id="spanned"></span><span id="SPANNED"></span>Distribuido<br/>                                                 | Asignación lineal con varias extensiones no contiguas en varios discos o unidades.<br/> |
| <span id="Striped"></span><span id="striped"></span><span id="STRIPED"></span>Seccionado<br/>                                                 | Asignación que intercala extensiones de volumen contiguas en varios discos o unidades.<br/> |
| <span id="Mirrored"></span><span id="mirrored"></span><span id="MIRRORED"></span>Reflejada<br/>                                             | Asignación que mantiene dos o más copias de datos idénticas.<br/>                           |
| <span id="Striped_with_parity"></span><span id="striped_with_parity"></span><span id="STRIPED_WITH_PARITY"></span>Seccionado con paridad<br/> | Asignación que distribuye la información de comprobación de paridad en varios discos o unidades.<br/>  |



 

Las construcciones de VDS se reflejan, seccionan y seccionan con enlaces de paridad de más de un miembro. Por ejemplo, un reflejo doble tiene dos miembros. Cada miembro puede ocupar extensiones en más de un disco o unidad. VDS concatena las extensiones para formar el miembro y, a continuación, enlaza el volumen o LUN en los miembros. Un proveedor puede admitir todos los tipos de enlace o cualquier subconjunto. En el modelo de objetos de VDS, cada miembro de un reflejo es un objeto independiente denominado complejo.

De nuevo, los tipos de volumen y LUN son similares, pero no exactos. Para obtener una descripción de los tipos de volumen, consulte el [objeto de volumen](volume-object.md). para los tipos de LUN, consulte el [objeto LUN](lun-object.md). Los tipos de enlace son no tolerantes a errores o tolerantes a errores.

### <a name="non-fault-tolerant-binding"></a>Enlace no tolerante a errores

Los volúmenes y LUN no tolerantes a errores no ofrecen recuperación ante desastres. Si se produce un error en uno de los ejes que contribuye a un volumen o LUN no tolerante a errores, se produce un error en todo el volumen o LUN. En Exchange para el riesgo de datos, los LUN y volúmenes que no son tolerantes a errores ofrecen un rendimiento de entrada/salida que, por lo general, es superior al de los volúmenes y LUN tolerantes a errores. VDS admite los siguientes tres tipos no tolerantes a errores: simple, distribuido y seccionado.

Simple

![Diagrama que muestra un tipo simple sin tolerancia a errores con 2 paquetes y 2 subsistemas.](images/vdssimplelunvol.png)

Distribuido

![Diagrama que muestra un tipo distribuido no tolerante a errores con 1 Pack y 1 subsistema.](images/vdsspanlunvol.png)

Seccionado

![Diagrama que muestra un tipo no tolerante a errores seccionado con 1 Pack y 1 subsistema.](images/vdsstripelunvol.png)

### <a name="fault-tolerant-binding"></a>Enlace tolerante a errores

Los siguientes volúmenes y LUN tolerantes a errores ofrecen recuperación ante desastres. Si se produce un error en uno de los ejes que contribuye a un volumen o LUN tolerante a errores, los datos se pueden recuperar. En Exchange para la seguridad de los datos, el rendimiento de entrada/salida de los volúmenes y LUN tolerantes a errores suele ser inferior al de los volúmenes y LUN que no son tolerantes a errores. VDS admite dos tipos de tolerancia a errores: reflejado y seccionado con paridad.

Reflejado (reflejo triple)

![Diagrama que muestra un tipo de tolerancia a errores de reflejo (reflejo triple).](images/vdsmirrorlunvol.png)

Seccionado con paridad

![Diagrama que muestra un tipo de tolerancia a errores con bandas con paridad.](images/vdsstripeparitylunvol.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general de configuración](configuration.md)
</dt> <dt>

[Objeto de volumen](volume-object.md)
</dt> <dt>

[Objeto LUN](lun-object.md)
</dt> </dl>

 

