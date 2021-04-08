---
description: Para crear un proveedor de clase WMI, debe registrar la \_ \_ instancia de Win32Provider que representa el proveedor mediante una instancia de \_ \_ ClassProviderRegistration.
ms.assetid: ed834969-47e9-47df-9db8-c805b2eb71da
ms.tgt_platform: multiple
title: Registrar un proveedor de clases
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bc15893e654f96f8c4e476219389a1f8f2c464a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001545"
---
# <a name="registering-a-class-provider"></a>Registrar un proveedor de clases

Para crear un proveedor de clase WMI, debe registrar la instancia de [**\_ \_ Win32Provider**](--win32provider.md) que representa el proveedor mediante una instancia de [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md). Como objeto COM, el proveedor debe registrarse en el sistema operativo y en WMI. En el procedimiento siguiente se supone que ya ha implementado el proceso de registro como se describe en [registrar un proveedor](registering-a-provider.md). Si el proveedor almacena la mayoría de los datos en el repositorio WMI y los datos se actualizan solo en la inicialización de WMI, registre la clase como un proveedor de clase de inserciones. Si los datos que va a proporcionar cambian con frecuencia y el código lo recupera dinámicamente en cada solicitud de WMI, registre el proveedor como un proveedor de clase de extracción.

En el procedimiento siguiente se describe cómo registrar un proveedor de clase de inserciones.

**Para registrar un proveedor de clase de inserciones**

-   Establezca la propiedad **InteractionType** de la instancia de [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md) en 1.

    La creación de una instancia de [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md) forma parte del proceso de registro.

En el procedimiento siguiente se describe cómo registrar un proveedor de clase de extracción.

**Para registrar un proveedor de clase de extracción**

1.  Cree una instancia de la clase [**\_ \_ Win32Provider**](--win32provider.md) que describa el proveedor.
2.  Cree una instancia de la clase [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md) que describa el conjunto de características del proveedor.

    Dentro de la instancia de [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md) :

    1.  Establezca la propiedad **InteractionType** para indicar si el proveedor es un proveedor de inserción o de extracción.
    2.  Etiquete la clase con los calificadores de [**proveedor**](/windows/desktop/api/Provider/nl-provider-provider) y [**dinámicos**](standard-wmi-qualifiers.md) .

        El calificador [**dinámico**](standard-wmi-qualifiers.md) indica que WMI debe utilizar un proveedor para recuperar las instancias de clase. El calificador de [**proveedor**](/windows/desktop/api/Provider/nl-provider-provider) especifica el nombre del proveedor que debe usar WMI.

    3.  Defina las propiedades **ResultSetQueries**, **ReferencedSetQueries** y **UnsupportedQueries** .

        Estas propiedades de consulta describen información detallada sobre la clase admitida.

Además de describir los distintos métodos admitidos de una clase, la clase [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md) también tiene tres propiedades que describen una serie de consultas. Cuando se usan juntas, estas tres propiedades describen el intervalo completo de clases proporcionadas por el proveedor de clases. Cada propiedad de consulta contiene una instrucción SELECT de WQL, denominada "consulta de esquema", para especificar los tipos de clases admitidas. Las consultas de esquema especifican un nombre de clase especial denominado meta \_ Class. En la tabla siguiente se enumeran las propiedades de la consulta.



| Propiedad                 | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ResultSetQueries**     | Contiene información sobre el conjunto de resultados que proporciona el proveedor. WMI utiliza la información para determinar si se debe invocar al proveedor para satisfacer una consulta de una aplicación. Esta propiedad describe el conjunto de todas las clases que el proveedor puede proporcionar o un supraconjunto de las clases disponibles, pero nunca un subconjunto. WMI requiere que un proveedor especifique al menos una consulta en esta propiedad.<br/> En el ejemplo siguiente se muestra cómo establecer **ResultSetQueries** cuando un proveedor proporciona una clase de asociación que hace referencia a la clase [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .<br/> `SELECT * FROM meta_class WHERE __Class = "Win32_LogicalDisk"`<br/> En el ejemplo siguiente se muestra cómo especificar una consulta general cuando un proveedor suministra clases que hacen referencia a otras clases desconocidas.<br/> `SELECT * FROM meta_class`<br/> En el ejemplo siguiente se muestra cómo establecer **ResultSetQueries** cuando un proveedor solo suministra subclases, pero no la clase primaria de una clase determinada.<br/> `SELECT * FROM meta_class WHERE __Dynasty = "MyClass"`<br/> En el ejemplo siguiente se muestra cómo usar la \_ \_ propiedad especial this y establecer **ResultSetQueries** cuando un proveedor proporciona todas las clases y subclases.<br/> `SELECT * FROM meta_class WHERE __this ISA "MyClass"`<br/> |
| **ReferencedSetQueries** | Determina si se omitirá el proveedor en las consultas de esquema en las que se solicitan las asociaciones y referencias. Los proveedores que pueden proporcionar clases de asociación deben incluir al menos una consulta en su propiedad **ReferencedSetQueries** .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **UnsupportedQueries**   | Contiene información sobre el conjunto de resultados que no proporciona un proveedor de clases. WMI usa esta propiedad para restar del conjunto de clases implícitas por **ResultSetQueries**. Por ejemplo, un proveedor de clase puede especificar en la compatibilidad con **ResultSetQueries** para todas las clases derivadas de MyClass y especificar en **UnsupportedQueries** una falta de compatibilidad con una clase derivada determinada.<br/> Cuanto más información pueda registrar un proveedor sobre sus capacidades de procesamiento de consultas, más rápido se ejecutará. Escribir una o más consultas en la propiedad **UnsupportedQueries** es una forma de ser específica y es especialmente importante cuando un proveedor se basa en una clase que no proporciona. Cuando se realiza una solicitud de una clase que aparece en una consulta en la propiedad **UnsupportedQueries** , WMI puede proporcionar la propia clase o invocar a un proveedor alternativo para proporcionarla.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

Dado que WMI no admite la cláusula OR, debe crear una consulta independiente para cada clase.

Las siguientes consultas se especifican en **ResultSetQueries** cuando un proveedor de clases proporciona myclass1, MyClass2 y MyClass3.


```sql
SELECT * FROM meta_class WHERE __Class = "MyClass1"
SELECT * FROM meta_class WHERE __Class = "MyClass2"
SELECT * FROM meta_class WHERE __Class = "MyClass3"
```



Solo los administradores pueden registrar o eliminar un proveedor mediante la creación de una instancia de [**\_ \_ Win32Provider**](--win32provider.md) y [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md).

 

