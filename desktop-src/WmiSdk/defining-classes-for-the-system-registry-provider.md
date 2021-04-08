---
description: Una aplicación de administración que utiliza el proveedor del registro del sistema puede definir clases con propiedades que representan los datos del registro para claves concretas y, a continuación, almacena las clases en el repositorio WMI.
ms.assetid: e8707a3d-a393-4be0-9e86-297f0af15d99
ms.tgt_platform: multiple
title: Definir clases para el proveedor del registro del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ebce4867559398722182b7b77ae02bc31c070b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002516"
---
# <a name="defining-classes-for-the-system-registry-provider"></a>Definir clases para el proveedor del registro del sistema

Una aplicación de administración que utiliza el proveedor del registro del sistema puede definir clases con propiedades que representan los datos del registro para claves concretas y, a continuación, almacena las clases en el repositorio WMI. La mayoría de los procesos para definir una clase para el registro del sistema son idénticos a la definición de cualquier otra clase. Sin embargo, el proveedor del registro del sistema requiere que se utilicen tipos de datos y calificadores específicos.

En el procedimiento siguiente se describe cómo definir una clase para el proveedor del registro del sistema.

**Para definir una clase para el proveedor del registro del sistema**

1.  Cree la clase como lo haría con cualquier otra clase.

    Para obtener más información, vea [crear una clase](creating-a-class.md).

2.  Asigne los tipos de datos del registro adecuados a los tipos de WMI adecuados.

    El proveedor del registro del sistema asigna los tipos de datos del registro a tipos de datos WMI específicos. Para obtener más información, vea [asignar un tipo de datos del registro a un tipo de datos de WMI](mapping-a-registry-data-type-to-a-wmi-data-type.md).

3.  Use los calificadores necesarios para definir la ubicación del proveedor del registro y la ubicación de la clave del registro adecuada.

    El proveedor del registro del sistema usa tres calificadores para definir la ubicación de varias clases, proveedores y entradas del registro. Para obtener más información, vea [definir una clase de registro con calificadores](defining-a-registry-class-with-qualifiers.md).

 

 



