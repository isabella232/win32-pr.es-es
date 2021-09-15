---
description: Una aplicación de administración que usa el proveedor del Registro del sistema puede definir clases con propiedades que representan datos del Registro para claves concretas y, a continuación, almacena las clases en el repositorio WMI.
ms.assetid: e8707a3d-a393-4be0-9e86-297f0af15d99
ms.tgt_platform: multiple
title: Definir clases para el proveedor del Registro del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ebce4867559398722182b7b77ae02bc31c070b8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127467280"
---
# <a name="defining-classes-for-the-system-registry-provider"></a>Definir clases para el proveedor del Registro del sistema

Una aplicación de administración que usa el proveedor del Registro del sistema puede definir clases con propiedades que representan datos del Registro para claves concretas y, a continuación, almacena las clases en el repositorio WMI. La mayoría de los procesos para definir una clase para el registro del sistema es idéntico a definir cualquier otra clase. Sin embargo, el proveedor del Registro del sistema requiere que se usen calificadores y tipos de datos específicos.

En el procedimiento siguiente se describe cómo definir una clase para el proveedor del Registro del sistema.

**Para definir una clase para el proveedor del Registro del sistema**

1.  Cree la clase como lo haría con cualquier otra clase.

    Para obtener más información, vea [Crear una clase](creating-a-class.md).

2.  Asigne los tipos de datos del Registro adecuados a los tipos WMI adecuados.

    El proveedor del Registro del sistema asigna los tipos de datos del Registro a tipos de datos WMI específicos. Para obtener más información, vea [Asignar un tipo de datos del Registro a un tipo de datos WMI](mapping-a-registry-data-type-to-a-wmi-data-type.md).

3.  Use los calificadores necesarios para definir la ubicación del proveedor del Registro y la ubicación de la clave del Registro adecuada.

    El proveedor del Registro del sistema usa tres calificadores para definir la ubicación de varias clases, proveedores y entradas del Registro. Para obtener más información, vea [Definir una clase del Registro con calificadores](defining-a-registry-class-with-qualifiers.md).

 

 



