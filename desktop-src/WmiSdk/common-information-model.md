---
description: El Modelo de información común (CIM) es un modelo de datos orientado a los objetos extensible que contiene información acerca de diferentes partes de una empresa.
ms.assetid: 3e619cb7-18a9-40ff-82fe-c10eb5090a93
ms.tgt_platform: multiple
title: Modelo de información común
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e53e4e2dc06e03a1f19b5b47ba0b94d7a866a5e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083075"
---
# <a name="common-information-model"></a>Modelo de información común

El Modelo de información común (CIM) es un modelo de datos orientado a los objetos extensible que contiene información acerca de diferentes partes de una empresa. [CIM](https://www.dmtf.org/standards/cim) es un estándar multiplataforma mantenido por el equipo de administración distribuida ([DMTF](https://www.dmtf.org/)). A través de WMI, un desarrollador puede utilizar CIM para crear clases que representan unidades de disco duro, aplicaciones, enrutadores de red o incluso tecnologías definidas por el usuario, como un acondicionador de aire en red. Al visualizar y modificar una clase CIM, un administrador puede controlar diferentes aspectos de la empresa. Por ejemplo, un administrador podría consultar una instancia de clase CIM que represente una estación de trabajo de sobremesa. A continuación, el administrador podría ejecutar un script para modificar la instancia de la estación de trabajo CIM. WMI traduciría cualquier cambio introducido en la instancia de clase CIM de la estación de trabajo a un cambio en la estación de trabajo real.

CIM es un modelo de programación independiente del lenguaje que utiliza técnicas orientadas a objetos para describir una empresa. Con tres niveles de herencia de elementos primarios y secundarios, CIM puede describir aspectos generales y específicos de una empresa. CIM también utiliza una técnica denominada "Asociación" para vincular diferentes partes del modelo empresarial y utiliza esquemas para distinguir los distintos entornos de administración.

CIM está diseñado para presentar una vista coherente de los objetos lógicos y físicos en un entorno de administración. CIM representa objetos administrados mediante una construcción orientada a objetos denominada "class". Al igual que una clase de C++ o COM, una clase CIM puede incluir propiedades para describir los datos y métodos para describir el comportamiento. Al igual que un conjunto de clases COM, el CIM no está asociado a ninguna plataforma. Sin embargo, WMI incluye una extensión al CIM que describe las plataformas del sistema operativo Microsoft Windows.

CIM define tres niveles de clases:

-   Core

    Las clases principales representan objetos administrados que se aplican a todas las áreas de administración. Estas clases proporcionan un vocabulario básico para analizar y describir sistemas administrados. Las clases [**\_ \_ Parameters**](--parameters.md) y [**\_ \_ SystemSecurity**](--systemsecurity.md) son ejemplos de clases principales.

-   Comunes

    Las clases comunes representan objetos administrados que se aplican a áreas de administración específicas. Sin embargo, las clases comunes son independientes de una implementación o tecnología en particular. Las clases comunes son una extensión de las clases principales. La clase [**CIM \_ UnitaryComputerSystem**](/windows/desktop/CIMWin32Prov/cim-unitarycomputersystem) es un ejemplo de una clase común.

-   Extendido

    Las clases extendidas representan objetos administrados que son adiciones específicas de la tecnología a las clases comunes. Una clase extendida se aplica normalmente a una plataforma concreta, como UNIX o el entorno de Microsoft Win32. La clase de [**Win32 \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) es un ejemplo de una clase extendida.

Un desarrollador puede derivar una clase de otra clase. Una clase derivada representa un caso especial de la clase primaria y hereda todas las propiedades y métodos del elemento primario. Por ejemplo, [**Win32 \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) hereda de [**\_ UnitaryComputerSystem CIM**](/windows/desktop/CIMWin32Prov/cim-unitarycomputersystem). Las relaciones de herencia se pueden determinar mediante la **\_ \_ derivación** de las propiedades del sistema, **\_ \_ Dynasty** y **\_ \_ superclase**. La propiedad del sistema de **\_ \_ derivación** es una matriz de cadenas que enumeran toda la cadena de herencia hasta la clase raíz, incluida en ella, que también se incluye en **\_ \_ Dynasty**. La propiedad sistema de la **\_ \_ superclase** muestra el elemento primario inmediato de la clase actual.

WMI también admite asociaciones. Una asociación es una relación entre dos o más clases WMI diferentes. Por ejemplo, una estación de trabajo en ejecución normalmente tiene un procesador. La clase de asociación WMI [Win32 \_ ComputerSystemProcessor](/windows/desktop/CIMWin32Prov/win32-computersystemprocessor) asocia la clase de estación de trabajo [**Win32 \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) con el [**\_ procesador Win32**](/windows/desktop/CIMWin32Prov/win32-processor)de clase de procesador. Sin embargo, una clase de asociación no tiene que vincular dos clases dependientes. De hecho, el propósito principal de una clase de asociación es mostrar las relaciones entre las clases que no dependen necesariamente entre sí. Para obtener más información, vea [declarar una clase de asociación](declaring-an-association-class.md).

Por último, WMI admite el concepto de esquemas. En el contexto de WMI, un esquema es un grupo de clases que describen un entorno de administración determinado. El kit de desarrollo de software (SDK) de Microsoft Windows usa dos esquemas: el esquema CIM y el esquema de Win32. Los nombres de clase de esquema CIM comienzan con [CIM \_](cimclas.md)y los nombres de clase de esquema Win32 comienzan con [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-provider). El esquema CIM contiene las definiciones de las clases principales y comunes, mientras que el esquema Win32 contiene las definiciones de las clases extendidas que son comunes al entorno de Win32. Sin embargo, un proveedor de terceros puede crear sus propios esquemas para describir los requisitos específicos del proveedor. Dado que los esquemas están diseñados para ser extensiblemente extensibles, un programador siempre puede agregar nuevas clases para describir nuevos objetos administrados en un entorno existente. Sin embargo, para simplificar, la mayoría de los proveedores deciden crear esquemas que heredan propiedades de los esquemas de CIM o Win32.

 

 
