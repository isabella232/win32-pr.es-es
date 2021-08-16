---
description: Enlace de volúmenes y LUN
ms.assetid: ae32b354-799e-4f9b-8989-02bd95968210
title: Enlace de volúmenes y LUN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91014241014793b601c15c64ec19e5a2b1d153c71ba617cead54a5d68cf978b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125573"
---
# <a name="volume-and-lun-binding"></a>Enlace de volúmenes y LUN

\[A partir Windows 8 y Windows Server 2012, la interfaz COM del servicio [virtual](virtual-disk-service-portal.md) de disco se sustituye por [el Windows Storage API de Administración](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

El enlace es la creación de volúmenes o LUN. Los volúmenes constan de extensiones de disco y LUN que constan de extensiones de unidad. El enlace selecciona para un conjunto de asignaciones a recursos físicos y se produce dentro de un subsistema, dentro de un paquete o ambos. Todos los programas de proveedor admiten el enlace dirigido parcialmente a un modelo en el que el autor de la llamada especifica solo los atributos de enlace de especial interés y permite al proveedor elegir el resto. Las operaciones en VDS para volúmenes de enlace y LUN son similares, pero no idénticas. Por ejemplo, los proveedores de hardware pueden ofrecer opciones de enlace adicionales.

VDS admite los cinco tipos de enlace de volumen y LUN siguientes para configuraciones dirigidas parcialmente. (Los proveedores de hardware pueden y admiten muchos otros enlaces).



| Término                                                                                                                                             | Descripción                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="Simple"></span><span id="simple"></span><span id="SIMPLE"></span>Simple<br/>                                                     | Asignación lineal con una sola extensión contigua.<br/>                             |
| <span id="Spanned"></span><span id="spanned"></span><span id="SPANNED"></span>Atravesado<br/>                                                 | Asignación lineal con varias extensiones no persistentes en varios discos o unidades.<br/> |
| <span id="Striped"></span><span id="striped"></span><span id="STRIPED"></span>Rayas<br/>                                                 | Asignación que intercala extensiones de volumen contiguas en varios discos o unidades.<br/> |
| <span id="Mirrored"></span><span id="mirrored"></span><span id="MIRRORED"></span>Espejada<br/>                                             | Asignación que mantiene dos o más copias de datos idénticas.<br/>                           |
| <span id="Striped_with_parity"></span><span id="striped_with_parity"></span><span id="STRIPED_WITH_PARITY"></span>Seccionados con paridad<br/> | Asignación que distribuye la información de comprobación de paridad entre varios discos o unidades.<br/>  |



 

VDS crea construcciones reflejadas, seccionadas y seccionadas con enlaces de paridad de más de un miembro. Por ejemplo, un reflejo de dos vías tiene dos miembros. Cada miembro puede ocupar extensiones en más de un disco o unidad. VDS concatena las extensiones para formar el miembro y, a continuación, enlaza el volumen o LUN en los miembros. Un proveedor puede admitir todos los tipos de enlace o cualquier subconjunto. En el modelo de objetos VDS, cada miembro de un reflejo es un objeto independiente denominado plex.

De nuevo, los tipos de volumen y LUN son similares, pero no exactos. Para obtener una descripción de los tipos de volumen, vea [el objeto Volume](volume-object.md); Para los tipos lun, vea el [objeto LUN](lun-object.md). Los tipos de enlace no son tolerantes a errores o tolerantes a errores.

### <a name="non-fault-tolerant-binding"></a>Enlace no tolerante a errores

Los volúmenes y LUN no tolerantes a errores no ofrecen recuperación ante desastres. Si se produce un error en uno de los ejes que contribuye a un volumen no tolerante a errores o LUN, se produce un error en todo el volumen o LUN. A cambio del riesgo para los datos, los volúmenes y LUN no tolerantes a errores ofrecen un rendimiento de entrada y salida que suele ser superior al de los volúmenes y LUN tolerantes a errores. VDS admite los tres tipos siguientes que no son tolerantes a errores: simple, con intervalos y seccionados.

Simple

![Diagrama que muestra un tipo simple no tolerante a errores con 2 paquetes y 2 subsistemas.](images/vdssimplelunvol.png)

Distribuido

![Diagrama que muestra un tipo no tolerante a errores abarcado con 1 Pack y 1 Subsystem.](images/vdsspanlunvol.png)

Seccionado

![Diagrama que muestra un tipo no tolerante a errores seccionado con 1 Pack y 1 Subsystem.](images/vdsstripelunvol.png)

### <a name="fault-tolerant-binding"></a>Enlace tolerante a errores

Los siguientes volúmenes tolerantes a errores y LUN ofrecen recuperación ante desastres. Si se produce un error en uno de los ejes que contribuye a un volumen tolerante a errores o LUN, se pueden recuperar los datos. A cambio de la seguridad de los datos, el rendimiento de entrada y salida de volúmenes tolerantes a errores y LUN suele ser inferior al de los volúmenes y LUN no tolerantes a errores. VDS admite dos tipos tolerantes a errores: reflejados y seccionados con paridad.

Reflejado (reflejo triple)

![Diagrama que muestra un tipo tolerante a errores reflejado (reflejo de 3 vías).](images/vdsmirrorlunvol.png)

Seccionados con paridad

![Diagrama que muestra un tipo seccionado con tolerancia a errores de paridad.](images/vdsstripeparitylunvol.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Información general sobre la configuración](configuration.md)
</dt> <dt>

[Objeto Volume](volume-object.md)
</dt> <dt>

[Objeto LUN](lun-object.md)
</dt> </dl>

 

