---
description: WMI admite diferentes modelos de subprocesamiento en función de cómo se hospeda el proveedor y del tipo de funcionalidad del proveedor, como Clase o Propiedad.
ms.assetid: cce3faf5-7bfe-46fe-9205-57398ab9dae9
ms.tgt_platform: multiple
title: Elección del registro correcto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f3e9a252e9013e828f5dc2c6e4c7228919d0834d0edb3da5f699cbe0306a38d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131807"
---
# <a name="choosing-correct-registration"></a>Elección del registro correcto

WMI admite diferentes modelos de subprocesamiento en función de cómo se hospeda el proveedor y del tipo de funcionalidad del proveedor, como [Clase](writing-a-class-provider.md) o [Propiedad](writing-a-property-provider.md). Por ejemplo, [*los proveedores desacoplados*](gloss-d.md) no admiten todos los tipos de funcionalidad del proveedor. Para obtener más información sobre los diferentes modelos de hospedaje y cómo configurarlos, vea [Provider Hosting and Security](provider-hosting-and-security.md).

## <a name="in-process-providers"></a>In-Process proveedores

Los proveedores en proceso se ejecutan en un proceso de host compartido, Wmiprvse.exe. La mayoría de los tipos de proveedor en proceso usan el modelo de apartamento multiproceso (MTA).

El modelo MTA es compatible con los siguientes tipos de funcionalidad de proveedor:

-   [Proveedor de clases](writing-a-class-provider.md)
-   [Proveedor de instancias](writing-an-instance-provider.md)
-   [Proveedor de métodos](writing-a-method-provider.md)
-   [Proveedor de propiedades](writing-a-property-provider.md)
-   [Proveedor de eventos](writing-an-event-provider.md)
-   [Proveedor de consumidores de eventos](writing-an-event-consumer-provider.md)

El modelo de apartamento de un solo subproceso (STA) es compatible con algunos tipos de funcionalidad del proveedor:

-   [Proveedor de instancias](writing-an-instance-provider.md)
-   [Proveedor de métodos](writing-a-method-provider.md)
-   [Proveedor de eventos](writing-an-event-provider.md)
-   [Proveedor de consumidores de eventos](writing-an-event-consumer-provider.md)

## <a name="out-of-process-providers"></a>Proveedores fuera de proceso

Los proveedores que se hospedan en otro host de servicio compartido admiten la siguiente funcionalidad de proveedor:

-   [Proveedor de clases](writing-a-class-provider.md)
-   [Proveedor de instancias](writing-an-instance-provider.md)
-   [Proveedor de métodos](writing-a-method-provider.md)
-   [Proveedor de propiedades](writing-a-property-provider.md)
-   [Proveedor de eventos](writing-an-event-provider.md)
-   [Proveedor de consumidores de eventos](writing-an-event-consumer-provider.md)

Para obtener más información sobre los hosts de servicio compartidos, vea [Provider Hosting and Security](provider-hosting-and-security.md).

## <a name="decoupled-providers"></a>Proveedores desacoplados

Los proveedores desacoplados se hospedan en una aplicación. Para obtener más información, vea [Incorporación de un proveedor en una aplicación](incorporating-a-provider-in-an-application.md). Los proveedores creados mediante WMI en .NET Framework se desacoplan. Los proveedores desacoplados admiten la siguiente funcionalidad de proveedor:

-   [Proveedor de instancias](writing-an-instance-provider.md)
-   [Proveedor de métodos](writing-a-method-provider.md)
-   [Proveedor de eventos](writing-an-event-provider.md)
-   [Proveedor de consumidores de eventos](writing-an-event-consumer-provider.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desarrollar un proveedor WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Hospedaje y seguridad del proveedor](provider-hosting-and-security.md)
</dt> </dl>

 

 



