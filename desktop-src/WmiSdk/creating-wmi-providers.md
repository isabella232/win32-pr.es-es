---
description: Los desarrolladores pueden ampliar la infraestructura wmi mediante el desarrollo de proveedores WMI.
ms.assetid: 87bc5d10-a5d7-444b-b823-4e1a2d63efb3
ms.tgt_platform: multiple
title: Creación de proveedores WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40cb15b911cb549e28e3536da0a9da31de8df1d6f395ede5f9c9176d21239abc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679745"
---
# <a name="creating-wmi-providers"></a>Creación de proveedores WMI

Los desarrolladores pueden ampliar la infraestructura wmi mediante el desarrollo de proveedores WMI. Los proveedores WMI son objetos COM que implementan un conjunto especificado de interfaces y, hasta hace poco, siempre se implementaban en C++. Ahora puede usar lenguajes administrados como C# para implementar proveedores WMI. La versión 3.5 de .NET Framework introdujo el marco de extensiones del proveedor WMI que lo hace posible. Para obtener más información sobre cómo crear proveedores WMI mediante ese marco, lea el artículo Escritura de proveedores WMI acoplados mediante WMI.NET [Provider Extension 2.0](/previous-versions/dotnet/articles/cc268228(v=msdn.10)).

> [!Note]  
> También puede crear un proveedor mediante Windows Management Infrastructure (MI), la versión de próxima generación de WMI. Para obtener más información, [vea How to Implement an MI Provider](/previous-versions/windows/desktop/wmi_v2/how-to-implement-an-mi-provider).

 

En la tabla siguiente se describe el contenido de esta sección.



| Tema                                                      | Descripción                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Proporcionar datos a WMI](providing-data-to-wmi.md)         | Proporciona información general sobre los pasos necesarios para crear un proveedor WMI.         |
| [Desarrollar un proveedor WMI](developing-a-wmi-provider.md) | Describe las tareas que debe realizar al crear varios tipos de proveedores WMI. |



 

 

 
