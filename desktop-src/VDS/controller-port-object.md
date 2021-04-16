---
description: Objeto de puerto de controlador
ms.assetid: 5f94bcdc-93ab-4522-88bd-009a049b5dc9
title: Objeto de puerto de controlador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7547581358bd79212b1093384ce1589e331f6ee0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696312"
---
# <a name="controller-port-object"></a>Objeto de puerto de controlador

\[A partir de Windows 8 y Windows Server 2012, la interfaz com de [servicio de disco virtual](virtual-disk-service-portal.md) se sustituye por la [API de administración de almacenamiento de Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un objeto de puerto de controlador modela un puerto de controlador en un subsistema. Los equipos host pueden escribir y leer desde LUN a través de puertos de controlador. Los puertos de controlador están incluidos en los controladores de un subsistema. En VDS 1,1 y VDS 2.0, cada uno de los puertos de controlador de un subsistema se establece en activo o inactivo con respecto a cada uno de los LUN que el subsistema Surfaces. Un puerto de un solo controlador, a continuación, se puede establecer simultáneamente en activo para un LUN e inactivo para otros. Un puerto de controlador que está activo para un LUN determinado conlleva la responsabilidad de controlar la entrada y la salida del LUN.

Los puertos de controlador activos sirven como uno de los puntos de conexión de rutas MPIO en Canal de fibra proveedores de hardware, en el que se pueden imponer las directivas de equilibrio de carga.

Use el método [**IVdsControllerControllerPort:: QueryControllerPorts**](/windows/desktop/api/Vds/nf-vds-ivdscontrollercontrollerport-querycontrollerports) para determinar los puertos del controlador contenidos en un controlador específico. Los llamadores pueden obtener un puntero a un puerto de controlador específico seleccionando el objeto de puerto del controlador deseado de la enumeración devuelta por el método **QueryControllerPorts** . Con un objeto de controlador, un llamador puede establecer el estado del puerto del controlador y la consulta para sus LUN asociadas.

Las propiedades de objeto de controlador incluyen un identificador de objeto, un nombre, un número de serie y el estado del puerto del controlador.

En la tabla siguiente se enumeran las interfaces, las enumeraciones y las estructuras relacionadas.



| Tipo                                                                                              | Elemento                                                                                               |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| Interfaces que siempre expone este objeto en VDS 1,1 y 2,0 Canal de fibra proveedores | [**IVdsControllerPort**](/windows/desktop/api/Vds/nn-vds-ivdscontrollerport)                                                      |
| Enumeraciones asociadas                                                                           | [**\_Estado del puerto VDS \_**](/windows/desktop/api/Vds/ne-vds-vds_port_status)                                                          |
| Estructuras asociadas                                                                             | [**VDS \_ \_Expulsión de Puerto**](/windows/desktop/api/Vds/ns-vds-vds_port_prop) y [ **\_ \_ notificación de Puerto VDS**](/windows/desktop/api/Vds/ns-vds-vds_port_notification) |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos de proveedor de hardware](hardware-provider-objects.md)
</dt> <dt>

[**IVdsControllerControllerPort::QueryControllerPorts**](/windows/desktop/api/Vds/nf-vds-ivdscontrollercontrollerport-querycontrollerports)
</dt> </dl>

 

 
