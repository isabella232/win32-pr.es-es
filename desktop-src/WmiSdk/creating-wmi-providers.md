---
description: Los desarrolladores pueden ampliar la infraestructura de WMI mediante el desarrollo de proveedores de WMI.
ms.assetid: 87bc5d10-a5d7-444b-b823-4e1a2d63efb3
ms.tgt_platform: multiple
title: Crear proveedores de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 980d3cd10b7108397a577d54ef93e502fb28d1bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083463"
---
# <a name="creating-wmi-providers"></a>Crear proveedores de WMI

Los desarrolladores pueden ampliar la infraestructura de WMI mediante el desarrollo de proveedores de WMI. Los proveedores WMI son objetos COM que implementan un conjunto especificado de interfaces y, hasta el momento, se implementan siempre en C++. Ahora puede usar lenguajes administrados como C# para implementar proveedores de WMI. La versión 3,5 de .NET Framework presentó el marco de trabajo de extensiones de proveedor WMI que lo hace posible. Para obtener más información sobre la creación de proveedores de WMI con ese marco de trabajo, lea el artículo sobre la [escritura de proveedores de WMI acoplados mediante la extensión de proveedor de WMI.NET 2,0](/previous-versions/dotnet/articles/cc268228(v=msdn.10)).

> [!Note]  
> También puede crear un proveedor mediante la infraestructura de administración de Windows (MI), la versión de la próxima generación de WMI. Para obtener más información, vea [cómo implementar un proveedor de mi](/previous-versions/windows/desktop/wmi_v2/how-to-implement-an-mi-provider).

 

En la tabla siguiente se describe el contenido de esta sección.



| Tema                                                      | Descripción                                                                    |
|------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Proporcionar datos a WMI](providing-data-to-wmi.md)         | Proporciona información general sobre los pasos necesarios para crear un proveedor WMI.         |
| [Desarrollar un proveedor WMI](developing-a-wmi-provider.md) | Describe las tareas que debe realizar al crear varios tipos de proveedores de WMI. |



 

 

 
