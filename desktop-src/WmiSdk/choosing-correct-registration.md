---
description: WMI admite diferentes modelos de subprocesos en función de cómo esté hospedado el proveedor y el tipo de funcionalidad del proveedor, como clase o propiedad.
ms.assetid: cce3faf5-7bfe-46fe-9205-57398ab9dae9
ms.tgt_platform: multiple
title: Elección del registro correcto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49b66ec0266b5482dcff13a7de05a5bd1414312
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716212"
---
# <a name="choosing-correct-registration"></a>Elección del registro correcto

WMI admite diferentes modelos de subprocesos en función de cómo esté hospedado el proveedor y el tipo de funcionalidad del proveedor, como [clase](writing-a-class-provider.md) o [propiedad](writing-a-property-provider.md). Por ejemplo, los [*proveedores desacoplados*](gloss-d.md) no admiten todos los tipos de funcionalidad de proveedor. Para obtener más información sobre los diferentes modelos de hospedaje y cómo configurarlos, vea [hospedaje y seguridad de proveedores](provider-hosting-and-security.md).

## <a name="in-process-providers"></a>Proveedores de In-Process

Los proveedores en proceso se ejecutan en un proceso de host compartido, Wmiprvse.exe. La mayoría de los tipos de proveedores en proceso utilizan el modelo de contenedor multiproceso (MTA).

El modelo MTA es compatible con los siguientes tipos de funcionalidad de proveedor:

-   [Proveedor de clases](writing-a-class-provider.md)
-   [Proveedor de instancias](writing-an-instance-provider.md)
-   [Proveedor de método](writing-a-method-provider.md)
-   [Proveedor de propiedades](writing-a-property-provider.md)
-   [Proveedor de eventos](writing-an-event-provider.md)
-   [Proveedor de consumidor de eventos](writing-an-event-consumer-provider.md)

El modelo de contenedor uniproceso (STA) es compatible con algunos tipos de funcionalidad de proveedor:

-   [Proveedor de instancias](writing-an-instance-provider.md)
-   [Proveedor de método](writing-a-method-provider.md)
-   [Proveedor de eventos](writing-an-event-provider.md)
-   [Proveedor de consumidor de eventos](writing-an-event-consumer-provider.md)

## <a name="out-of-process-providers"></a>Proveedores fuera de proceso

Los proveedores que se hospedan en un host de servicio compartido diferente admiten la siguiente funcionalidad de proveedor:

-   [Proveedor de clases](writing-a-class-provider.md)
-   [Proveedor de instancias](writing-an-instance-provider.md)
-   [Proveedor de método](writing-a-method-provider.md)
-   [Proveedor de propiedades](writing-a-property-provider.md)
-   [Proveedor de eventos](writing-an-event-provider.md)
-   [Proveedor de consumidor de eventos](writing-an-event-consumer-provider.md)

Para obtener más información sobre los hosts de servicios compartidos, vea [hospedaje y seguridad de proveedores](provider-hosting-and-security.md).

## <a name="decoupled-providers"></a>Proveedores desacoplados

Los proveedores desacoplados se hospedan en una aplicación. Para obtener más información, vea [incorporación de un proveedor en una aplicación](incorporating-a-provider-in-an-application.md). Los proveedores creados con WMI en el .NET Framework están desacoplados. Los proveedores desacoplados admiten la siguiente funcionalidad de proveedor:

-   [Proveedor de instancias](writing-an-instance-provider.md)
-   [Proveedor de método](writing-a-method-provider.md)
-   [Proveedor de eventos](writing-an-event-provider.md)
-   [Proveedor de consumidor de eventos](writing-an-event-consumer-provider.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desarrollar un proveedor WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Hospedaje y seguridad de proveedores](provider-hosting-and-security.md)
</dt> </dl>

 

 



