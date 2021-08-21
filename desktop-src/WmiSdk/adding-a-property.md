---
description: Las propiedades de las clases WMI describen los datos sobre un objeto administrado.
ms.assetid: 4046bfc7-9528-4737-ad61-bbb8419d0b51
ms.tgt_platform: multiple
title: Agregar una propiedad WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97bc05c03556d81920852580300e0b5b02ddb6b68403aa3efd939cf7ec55bb55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118109517"
---
# <a name="adding-a-wmi-property"></a>Agregar una propiedad WMI

Las propiedades de las clases WMI describen los datos sobre un objeto administrado. Por ejemplo, **Handle**, **ProcessId** y **PageFaults** se definen como propiedades de la clase [**Win32 \_ Process**](/windows/desktop/CIMWin32Prov/win32-process) y describen aspectos de un proceso de sistema operativo. Para obtener más información, vea [Escribir un proveedor de propiedades.](writing-a-property-provider.md)

## <a name="defining-a-property-in-mof"></a>Definir una propiedad en MOF

Una propiedad WMI representa un aspecto o estado en el objeto . En lugar de crear métodos que simplemente obtengan y establezcan un valor, puede crear una propiedad . Por ejemplo, la **propiedad NetEnabled** de [**Win32 \_ NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter) muestra si el estado del adaptador está habilitado o deshabilitado. Sin embargo, [**los métodos Enable**](/windows/desktop/CIMWin32Prov/enable-method-in-class-win32-networkadapter) [**y Disable**](/windows/desktop/CIMWin32Prov/disable-method-in-class-win32-networkadapter) realizan realmente la acción de cambiar el estado del adaptador.

Una propiedad debe tener un tipo de datos. El tipo de datos del  identificador de la propiedad Proceso de [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-process) es **cadena** y el tipo de datos **de PageFaults** es **uint32.** Si una propiedad solo puede tener dos estados, el tipo de datos de la propiedad normalmente se establece en **booleano**.

La propiedad también puede ser una matriz. Por ejemplo, la propiedad identificador de seguridad **(SID)** de [**Win32 \_ Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) es una matriz de bytes (**uint8**) que contiene el SID. Las propiedades pueden contener objetos incrustados que son referencias a una o varias instancias de otra clase WMI. Las propiedades de lista de control de acceso discrecional **(DACL)** y lista de control de acceso del sistema **(SACL)** de [**Win32 \_ SecurityDescriptor,**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)por ejemplo, son matrices de objetos ACE de [**Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) que describen los grupos y cuentas que tienen acceso. La **propiedad Group** de **\_ SecurityDescriptor de Win32** contiene una referencia a una única instancia de **Win32 \_ Trustee.** Para obtener más información, [vea Incrustar objetos en una clase](embedded-objects.md).

Una propiedad puede tener varios [*calificadores*](gloss-q.md). Estos calificadores pueden [*ser Modelo de información común (CIM)*](gloss-c.md) o calificadores WMI o pueden ser específicos de [determinados](wmi-qualifiers.md) tipos de clases, por ejemplo, los calificadores de clase [Counter](qualifiers-specific-to-wmi-performance-classes.md) de rendimiento. Los calificadores especifican algún aspecto de la propiedad, como si es de solo lectura o si no se puede cambiar sin un privilegio específico. Una aplicación que intenta escribir en la propiedad [**\_ SECURITYDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)**DACL** de Win32, por ejemplo, requiere los privilegios **SeSecurityPrivilege** y **SeRestorePrivilege.** Para obtener más información, vea [Agregar un calificador](adding-a-qualifier.md).

Por último, una propiedad debe tener un nombre. Puede nombrar cualquier propiedad dentro de los límites de la práctica de programación estándar. Sin embargo, hay dos excepciones principales. En primer lugar, no puede usar ninguna palabra clave MOF, como "class", como nombre de propiedad. En segundo lugar, no puede usar ninguna palabra clave WQL, como "group", como nombre de propiedad. Para obtener más información sobre las palabras clave MOF y WQL, vea Tipos de datos [MOF](mof-data-types.md) y [WQL (SQL para WMI).](wql-sql-for-wmi.md)

Tanto para C++ como Managed Object Format (MOF), se declaran las propiedades de una clase al mismo tiempo que se declara la clase.

**Para definir una propiedad**

-   Incluya el tipo de datos de propiedad, el nombre y un valor predeterminado opcional y un calificador entre las llaves de la descripción de clase.

    ``` syntax
    class MyClass 
    {
        [key] string   strProp;
        sint32         dwProp1 = 21;
        uint32         dwProp2;
    };
    ```

    La clase MyClass del ejemplo anterior tiene tres propiedades: una cadena de caracteres, un entero de 32 bits con signo y un entero de 32 bits sin signo. A cada propiedad se le asigna un nombre sin mayúsculas de minúsculas y un tipo de datos MOF.

    El [**calificador**](key-qualifier.md) Key define la propiedad de cadena como la propiedad de clave que identifica de forma única una instancia de la clase . Para obtener más información sobre los calificadores, vea [Agregar un calificador](adding-a-qualifier.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Crear una clase](creating-a-class.md)
</dt> </dl>

 

 
