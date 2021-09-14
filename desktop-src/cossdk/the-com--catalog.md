---
description: El catálogo de COM+ almacena atributos de aplicación COM+, atributos de clase y atributos de nivel de equipo. Garantiza la coherencia entre estos atributos y proporciona operaciones comunes sobre estos atributos.
ms.assetid: 1838757c-aa8e-4678-8042-207498fb0bbc
title: El catálogo de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad869a6df6a61fc338fe07002512a1de27002788
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361625"
---
# <a name="the-com-catalog"></a>El catálogo de COM+

El catálogo de COM+ almacena atributos de aplicación COM+, atributos de clase y atributos de nivel de equipo. Garantiza la coherencia entre estos atributos y proporciona operaciones comunes sobre estos atributos.

El catálogo de COM+ usa dos almacenes diferentes, como se muestra a continuación:

-   La base de datos de registro de COM+
-   El Windows (**RAÍZ DE CLASES \_ HKEY \_**)

El catálogo presenta una vista lógica unificada de estos dos almacenes y los expone a través de la biblioteca de administración de COM+. Esta biblioteca proporciona, a través de un lenguaje de scripting, toda la funcionalidad de la herramienta administrativa Servicios de componentes.

En el caso de los componentes COM existentes que no requieren ningún servicio COM+ nuevo, la búsqueda se produce en el registro Windows existente. El catálogo de COM+ también usa el registro Windows para el registro de código auxiliar o proxy de interfaz y biblioteca de tipos.

## <a name="split-registration"></a>División del registro

Para los nuevos componentes que ya son componentes COM existentes que se usan en el entorno de servicios (por ejemplo, componentes MTS), el aspecto COM básico del registro se almacena en el registro de Windows y los nuevos servicios y atributos (por ejemplo, componentes en cola) se almacenan en la base de datos de registro com+. Esto se conoce como registro *dividido.*

Cada atributo se almacena en una sola ubicación: el registro Windows o la base de datos de registro com+. Los nuevos componentes COM se registran exclusivamente en la base de datos de registro de COM+, con alguna duplicación en el registro Windows para que las herramientas existentes puedan usarlas.

## <a name="transactional-updates-to-the-catalog"></a>Actualizaciones transaccionales del catálogo

Algunas operaciones en el catálogo se realizan de forma transaccional. Al invocar la biblioteca de administración de COM+ desde un componente transaccional, las actualizaciones de la base de datos de registro de COM+ se realizarán dentro del límite de transacción del componente de llamada.

Sin embargo, no se garantiza que las actualizaciones que implican cambios en otros almacenes (como el sistema de archivos y Windows registro) sean totalmente transaccionales. Una transacción anulada puede dejar estos almacenes en un estado incoherente con los cambios realizados entre sí o en la base de datos de registro de COM+.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear paquetes de instalación para aplicaciones COM+](creating-installation-packages-for-com--applications.md)
</dt> <dt>

[Implementación de Application Proxies](deploying-application-proxies.md)
</dt> <dt>

[La utilidad de replicación COMREPL](the-comrepl-replication-utility.md)
</dt> </dl>

 

 



