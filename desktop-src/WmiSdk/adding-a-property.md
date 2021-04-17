---
description: Las propiedades de las clases de WMI describen los datos sobre un objeto administrado.
ms.assetid: 4046bfc7-9528-4737-ad61-bbb8419d0b51
ms.tgt_platform: multiple
title: Agregar una propiedad WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bba8944da155ca250edfed0c6e9160f555ba9551
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716868"
---
# <a name="adding-a-wmi-property"></a>Agregar una propiedad WMI

Las propiedades de las clases de WMI describen los datos sobre un objeto administrado. Por ejemplo, **Handle**, **ProcessId** y **PageFaults** se definen como propiedades de la clase [**de \_ proceso de Win32**](/windows/desktop/CIMWin32Prov/win32-process) y describen aspectos de un proceso del sistema operativo. Para obtener más información, consulte [escribir un proveedor de propiedades](writing-a-property-provider.md).

## <a name="defining-a-property-in-mof"></a>Definir una propiedad en MOF

Una propiedad WMI representa un aspecto o estado en el objeto. En lugar de crear métodos que simplemente obtienen y establecen un valor, puede crear una propiedad. Por ejemplo, la propiedad **NetEnabled** de [**Win32 \_ adaptador de Win32**](/windows/desktop/CIMWin32Prov/win32-networkadapter) muestra si el estado del adaptador está habilitado o deshabilitado. Sin embargo, los métodos [**enable**](/windows/desktop/CIMWin32Prov/enable-method-in-class-win32-networkadapter) y [**Disable**](/windows/desktop/CIMWin32Prov/disable-method-in-class-win32-networkadapter) realizan realmente la acción de cambiar el estado del adaptador.

Una propiedad debe tener un tipo de datos. El tipo de datos del **identificador** de la propiedad [**\_ Process de Win32**](/windows/desktop/CIMWin32Prov/win32-process) es **String** y el tipo de datos de **PageFaults** es **UInt32**. Si una propiedad solo puede tener dos Estados, el tipo de datos de la propiedad normalmente se establece en un **valor booleano**.

La propiedad también puede ser una matriz. Por ejemplo, la propiedad de identificador de seguridad (**SID**) [**de \_ Administrador de confianza de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) es una matriz de bytes (**Uint8**) que contiene el SID. Las propiedades pueden contener objetos incrustados que son referencias a una o más instancias de otra clase WMI. Las propiedades de la lista de control de acceso discrecional **(DACL)** y la lista de control de acceso del sistema **(SACL)** de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor), por ejemplo, son matrices de objetos [**\_ ACE de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) que describen los grupos y las cuentas que tienen acceso. La propiedad **Group** de **Win32 \_ SecurityDescriptor** contiene una referencia a una única instancia de **Administrador de \_ confianza de Win32**. Para obtener más información, vea [incrustar objetos en una clase](embedded-objects.md).

Una propiedad puede tener varios [*calificadores*](gloss-q.md). Estos [calificadores](wmi-qualifiers.md) pueden ser [*modelo de información común (CIM)*](gloss-c.md) o calificadores WMI o pueden ser específicos de determinados tipos de clases, por ejemplo, los calificadores de clase de [contador de rendimiento](qualifiers-specific-to-wmi-performance-classes.md) . Los calificadores especifican algún aspecto de la propiedad, como si es de solo lectura o si no se puede cambiar sin un privilegio específico. Una aplicación que intenta escribir en la propiedad **DACL** de [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor), por ejemplo, requiere los privilegios **SeSecurityPrivilege** y **SeRestorePrivilege**. Para obtener más información, consulte [Agregar un calificador](adding-a-qualifier.md).

Por último, una propiedad debe tener un nombre. Puede asignar un nombre a una propiedad de cualquier elemento dentro de los límites de la práctica de programación estándar. Sin embargo, hay dos excepciones principales. En primer lugar, no puede usar ninguna palabra clave de MOF, como "class", como un nombre de propiedad. En segundo lugar, no puede usar ninguna palabra clave WQL, como "Group", como nombre de propiedad. Para obtener más información sobre las palabras clave MOF y WQL, vea [tipos de datos MOF](mof-data-types.md) y [WQL (SQL para WMI)](wql-sql-for-wmi.md).

En el código de C++ y Managed Object Format (MOF), se declaran las propiedades de una clase al mismo tiempo que se declara la clase.

**Para definir una propiedad**

-   Incluya el tipo de datos de la propiedad, el nombre y un calificador y un valor predeterminado opcional entre las llaves de la descripción de la clase.

    ``` syntax
    class MyClass 
    {
        [key] string   strProp;
        sint32         dwProp1 = 21;
        uint32         dwProp2;
    };
    ```

    La clase MyClass del ejemplo anterior tiene tres propiedades: una cadena de caracteres, un entero con signo de 32 bits y un entero de 32 bits sin signo. A cada propiedad se le asigna un nombre que no distingue mayúsculas de minúsculas y un tipo de datos MOF.

    El calificador de [**clave**](key-qualifier.md) define la propiedad de cadena como la propiedad de clave que identifica de forma única una instancia de la clase. Para obtener más información acerca de los calificadores, vea [Agregar un calificador](adding-a-qualifier.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear una clase](creating-a-class.md)
</dt> </dl>

 

 
