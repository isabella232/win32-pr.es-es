---
description: El catálogo de COM+ almacena los atributos de la aplicación COM+, los atributos de clase y los atributos de nivel de equipo. Garantiza la coherencia entre estos atributos y proporciona operaciones comunes sobre estos atributos.
ms.assetid: 1838757c-aa8e-4678-8042-207498fb0bbc
title: El catálogo de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad869a6df6a61fc338fe07002512a1de27002788
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666171"
---
# <a name="the-com-catalog"></a>El catálogo de COM+

El catálogo de COM+ almacena los atributos de la aplicación COM+, los atributos de clase y los atributos de nivel de equipo. Garantiza la coherencia entre estos atributos y proporciona operaciones comunes sobre estos atributos.

El catálogo de COM+ utiliza dos almacenes diferentes, como se indica a continuación:

-   La base de datos de registro de COM+
-   El registro de Windows **( \_ clases HKEY \_ raíz**)

El catálogo presenta una vista lógica y unificada de estos dos almacenes y los expone a través de la biblioteca de administración de COM+. Esta biblioteca proporciona, a través de un lenguaje de scripting, toda la funcionalidad de la herramienta administrativa Servicios de componentes.

En el caso de los componentes COM existentes que no requieren ningún servicio COM+ nuevo, la búsqueda se produce en el registro de Windows existente. El catálogo de COM+ también utiliza el registro de Windows para la biblioteca de tipos y el registro de código auxiliar y proxy de interfaz.

## <a name="split-registration"></a>Dividir registro

En el caso de los componentes nuevos que ya son componentes COM existentes que se usan en el entorno de servicios (por ejemplo, componentes MTS), el aspecto COM básico del registro se almacena en el registro de Windows y los nuevos servicios y atributos (por ejemplo, los componentes en cola) se almacenan en la base de datos de registro de COM+. Esto se conoce como *registro dividido*.

Cada atributo se almacena en una sola ubicación: el registro de Windows o la base de datos de registro de COM+. Los nuevos componentes COM se registran exclusivamente en la base de datos de registro de COM+, con algunas duplicaciones en el registro de Windows para que las herramientas existentes puedan utilizarlos.

## <a name="transactional-updates-to-the-catalog"></a>Actualizaciones transaccionales en el catálogo

Algunas operaciones en el catálogo se realizan de manera transaccional. Al invocar la biblioteca de administración de COM+ desde un componente transaccional, las actualizaciones de la base de datos de registro de COM+ se realizarán dentro del límite de la transacción del componente que realiza la llamada.

Sin embargo, no se garantiza que las actualizaciones que implican cambios en otros almacenes (como el sistema de archivos y el registro de Windows) sean completamente transaccionales. Una transacción anulada puede dejar estos almacenes en un estado incoherente con los cambios realizados en otro o en la base de datos de registro de COM+.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear paquetes de instalación para aplicaciones COM+](creating-installation-packages-for-com--applications.md)
</dt> <dt>

[Implementación de servidores proxy de aplicación](deploying-application-proxies.md)
</dt> <dt>

[La utilidad de replicación COMREPL](the-comrepl-replication-utility.md)
</dt> </dl>

 

 



