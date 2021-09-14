---
description: Objeto de puerto del controlador
ms.assetid: 5f94bcdc-93ab-4522-88bd-009a049b5dc9
title: Objeto de puerto del controlador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7547581358bd79212b1093384ce1589e331f6ee0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126890409"
---
# <a name="controller-port-object"></a>Objeto de puerto del controlador

\[A partir Windows 8 y Windows Server 2012, la interfaz COM [del](virtual-disk-service-portal.md) servicio virtual de disco se sustituye por el [Windows Storage API de Administración](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]

Un objeto de puerto de controlador modela un puerto de controlador en un subsistema. Los equipos host pueden escribir y leer desde LUN a través de puertos de controlador. Los puertos del controlador los contienen los controladores de un subsistema. En VDS 1.1 y VDS2.0, cada uno de los puertos de controlador de un subsistema se establece en activo o inactivo en relación con cada uno de los LUN que el subsistema superficie. Un solo puerto de controlador, a continuación, se puede establecer simultáneamente en activo para un LUN e inactivo para otros. Un puerto de controlador que está activo para un LUN determinado asume la responsabilidad de controlar la entrada y la salida del LUN.

Los puertos de controlador activo sirven como uno de los puntos de conexión de las rutas de acceso de MPIO en Canal de fibra proveedores de hardware, en los que se pueden imponer directivas de equilibrio de carga.

Use el [**método IVdsControllerControllerPort::QueryControllerPorts**](/windows/desktop/api/Vds/nf-vds-ivdscontrollercontrollerport-querycontrollerports) para determinar los puertos del controlador contenidos por un controlador específico. Los llamadores pueden obtener un puntero a un puerto de controlador específico seleccionando el objeto de puerto de controlador deseado de la enumeración que devuelve el **método QueryControllerPorts.** Con un objeto de controlador, un autor de la llamada puede establecer el estado del puerto del controlador y consultar sus LUN asociados.

Las propiedades del objeto de controlador incluyen un identificador de objeto, un nombre, un número de serie y el estado del puerto del controlador.

En la tabla siguiente se enumeran las interfaces, enumeraciones y estructuras relacionadas.



| Tipo                                                                                              | Elemento                                                                                               |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| Interfaces que siempre expone este objeto en VDS 1.1 y 2.0 Canal de fibra proveedores | [**IVdsControllerPort**](/windows/desktop/api/Vds/nn-vds-ivdscontrollerport)                                                      |
| Enumeraciones asociadas                                                                           | [**ESTADO DEL PUERTO VDS \_ \_**](/windows/desktop/api/Vds/ne-vds-vds_port_status)                                                          |
| Estructuras asociadas                                                                             | [**VDS \_ PROP \_ DE PUERTO**](/windows/desktop/api/Vds/ns-vds-vds_port_prop) y NOTIFICACIÓN DE [ **\_ PUERTO \_ VDS**](/windows/desktop/api/Vds/ns-vds-vds_port_notification) |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos de proveedor de hardware](hardware-provider-objects.md)
</dt> <dt>

[**IVdsControllerControllerPort::QueryControllerPorts**](/windows/desktop/api/Vds/nf-vds-ivdscontrollercontrollerport-querycontrollerports)
</dt> </dl>

 

 
