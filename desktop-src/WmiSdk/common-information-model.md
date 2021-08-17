---
description: El Modelo de información común (CIM) es un modelo de datos orientado a los objetos extensible que contiene información acerca de diferentes partes de una empresa.
ms.assetid: 3e619cb7-18a9-40ff-82fe-c10eb5090a93
ms.tgt_platform: multiple
title: Modelo de información común
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d095dfb7f05b7637ac027e6ea02eeba2e10e12845670aebd635e50e8c3265fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131647"
---
# <a name="common-information-model"></a>Modelo de información común

El Modelo de información común (CIM) es un modelo de datos orientado a los objetos extensible que contiene información acerca de diferentes partes de una empresa. CIM [es](https://www.dmtf.org/standards/cim) un estándar multiplataforma que mantiene el Grupo de tareas de administración distribuida[(DMTF).](https://www.dmtf.org/) A través de WMI, un desarrollador puede utilizar CIM para crear clases que representan unidades de disco duro, aplicaciones, enrutadores de red o incluso tecnologías definidas por el usuario, como un acondicionador de aire en red. Al visualizar y modificar una clase CIM, un administrador puede controlar diferentes aspectos de la empresa. Por ejemplo, un administrador podría consultar una instancia de clase CIM que represente una estación de trabajo de sobremesa. A continuación, el administrador podría ejecutar un script para modificar la instancia de la estación de trabajo CIM. WMI traduciría cualquier cambio introducido en la instancia de clase CIM de la estación de trabajo a un cambio en la estación de trabajo real.

CIM es un modelo de programación independiente del lenguaje que usa técnicas orientadas a objetos para describir una empresa. Con tres niveles de herencia de elementos primarios y secundarios, el CIM puede describir aspectos generales y específicos de una empresa. Cim también usa una técnica denominada "asociación" para vincular diferentes partes del modelo empresarial y usa esquemas para distinguir distintos entornos de administración.

Cim está diseñado para presentar una vista coherente de objetos lógicos y físicos en un entorno de administración. Cim representa objetos administrados mediante una construcción orientada a objetos denominada "clase". Al igual que una clase C++ o COM, una clase CIM puede incluir propiedades para describir datos y métodos para describir el comportamiento. Al igual que un conjunto de clases COM, cim no está asociado a ninguna plataforma. Sin embargo, WMI incluye una extensión para cim que describe la plataforma de Windows de microsoft.

Cim define tres niveles de clases:

-   Core

    Las clases principales representan objetos administrados que se aplican a todas las áreas de administración. Estas clases proporcionan un vocabulario básico para analizar y describir sistemas administrados. Las [**\_ \_ clases Parameters**](--parameters.md) y [**\_ \_ SystemSecurity**](--systemsecurity.md) son ejemplos de clases principales.

-   Comunes

    Las clases comunes representan objetos administrados que se aplican a áreas de administración específicas. Sin embargo, las clases comunes son independientes de una implementación o tecnología determinadas. Las clases comunes son una extensión de las clases principales. La [**clase \_ CIM UnitaryComputerSystem**](/windows/desktop/CIMWin32Prov/cim-unitarycomputersystem) es un ejemplo de una clase común.

-   Extendido

    Las clases extendidas representan objetos administrados que son adiciones específicas de la tecnología a las clases comunes. Normalmente, una clase extendida se aplica a una plataforma específica, como UNIX o el entorno de Microsoft Win32. La [**clase \_ ComputerSystem de Win32**](/windows/desktop/CIMWin32Prov/win32-computersystem) es un ejemplo de una clase extendida.

Un desarrollador puede derivar una clase de otra clase. Una clase derivada representa un caso especial de la clase primaria y hereda todas las propiedades y métodos del elemento primario. Por ejemplo, [**\_ ComputerSystem de Win32**](/windows/desktop/CIMWin32Prov/win32-computersystem) hereda de [**CIM \_ UnitaryComputerSystem**](/windows/desktop/CIMWin32Prov/cim-unitarycomputersystem). Las relaciones de herencia se pueden determinar mediante las propiedades del sistema **\_ \_ Derivation**, **\_ \_ Inheritance** y **\_ \_ SuperClass**. La **\_ \_ propiedad Del sistema** de derivación es una matriz de cadenas que enumeran toda la cadena de herencia hasta la clase raíz, incluida, que también se incluye en La **\_ \_ herencia**. La propiedad del sistema **\_ \_ SuperClass** muestra el elemento primario inmediato de la clase actual.

WMI también admite asociaciones. Una asociación es una relación entre dos o más clases WMI diferentes. Por ejemplo, una estación de trabajo en ejecución normalmente tiene un procesador. La clase de asociación [WMI Win32 \_ ComputerSystemProcessor](/windows/desktop/CIMWin32Prov/win32-computersystemprocessor) asocia la clase de estación de trabajo [**Win32 \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) con la clase de procesador [**Win32 \_ Processor**](/windows/desktop/CIMWin32Prov/win32-processor). Sin embargo, una clase de asociación no tiene que vincular dos clases dependientes. De hecho, el propósito principal de una clase de asociación es mostrar relaciones entre clases que no dependen necesariamente entre sí. Para obtener más información, vea [Declarar una clase de asociación](declaring-an-association-class.md).

Por último, WMI admite el concepto de esquemas. En el contexto de WMI, un esquema es un grupo de clases que describen un entorno de administración determinado. Microsoft Windows Software Development Kit (SDK) usa dos esquemas: el esquema CIM y el esquema Win32. Los nombres de clase de esquema CIM comienzan [por CIM \_](cimclas.md)y los nombres de clase de esquema Win32 comienzan por [**Win32. \_**](/windows/desktop/CIMWin32Prov/win32-provider) El esquema CIM contiene las definiciones de las clases principales y comunes, mientras que el esquema win32 contiene las definiciones de las clases extendidas que son comunes al entorno win32. Sin embargo, un proveedor externo puede crear sus propios esquemas para describir los requisitos específicos del proveedor. Dado que los esquemas están diseñados para ser infinitamente extensibles, un desarrollador siempre puede agregar nuevas clases para describir nuevos objetos administrados en un entorno existente. Sin embargo, para simplificar, la mayoría de los proveedores eligen crear esquemas que heredan propiedades de los esquemas CIM o Win32.

 

 
