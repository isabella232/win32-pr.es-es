---
description: Para crear un proveedor de clases WMI, debe registrar la instancia de Win32Provider que representa al proveedor mediante una instancia \_ \_ de \_ \_ ClassProviderRegistration.
ms.assetid: ed834969-47e9-47df-9db8-c805b2eb71da
ms.tgt_platform: multiple
title: Registro de un proveedor de clases
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f16a28b489f2cfd01163d6b32c9a70c0d8a193a542197795d6d2b40de0e1baef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316487"
---
# <a name="registering-a-class-provider"></a>Registro de un proveedor de clases

Para crear un proveedor de clases WMI, debe registrar la instancia [**\_ \_ de Win32Provider**](--win32provider.md) que representa al proveedor mediante una instancia de [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md). Como objeto COM, el proveedor debe registrarse con el sistema operativo y WMI. En el procedimiento siguiente se da por supuesto que ya ha implementado el proceso de registro como se describe [en Registro de un proveedor](registering-a-provider.md). Si el proveedor almacena la mayoría de los datos en el repositorio WMI y los datos se actualizan solo en la inicialización de WMI, registre la clase como proveedor de clases de inserción. Si los datos que proporciona cambian con frecuencia y el código recupera dinámicamente en cada solicitud de WMI, registre el proveedor como proveedor de clases de extracción.

En el procedimiento siguiente se describe cómo registrar un proveedor de clases de inserción.

**Para registrar un proveedor de clases de inserción**

-   Establezca la **propiedad InteractionType** de la [**\_ \_ instancia classProviderRegistration**](--classproviderregistration.md) en 1.

    La creación de una [**\_ \_ instancia de ClassProviderRegistration**](--classproviderregistration.md) forma parte del proceso de registro.

En el procedimiento siguiente se describe cómo registrar un proveedor de clases de extracción.

**Para registrar un proveedor de clases de extracción**

1.  Cree una instancia de la [**\_ \_ clase Win32Provider**](--win32provider.md) que describa el proveedor.
2.  Cree una instancia de la [**\_ \_ clase ClassProviderRegistration**](--classproviderregistration.md) que describa el conjunto de características del proveedor.

    Dentro de [**\_ \_ la instancia classProviderRegistration:**](--classproviderregistration.md)

    1.  Establezca la **propiedad InteractionType** para indicar si el proveedor es un proveedor de inserción o de extracción.
    2.  Etiquete la clase con los [**calificadores Dynamic**](standard-wmi-qualifiers.md) [**y Provider.**](/windows/desktop/api/Provider/nl-provider-provider)

        El [**calificador**](standard-wmi-qualifiers.md) dinámico indica que WMI debe usar un proveedor para recuperar las instancias de clase. El [**calificador**](/windows/desktop/api/Provider/nl-provider-provider) Provider especifica el nombre del proveedor que WMI debe usar.

    3.  Defina las **propiedades ResultSetQueries**, **ReferencedSetQueries** y **UnsupportedQueries.**

        Estas propiedades de consulta describen información detallada sobre la clase admitida.

Además de describir los distintos métodos admitidos de una clase, la [**\_ \_ clase ClassProviderRegistration**](--classproviderregistration.md) también tiene tres propiedades que describen una serie de consultas. Cuando se usan juntas, estas tres propiedades describen todo el intervalo de clases proporcionado por el proveedor de clases. Cada propiedad de consulta contiene una instrucción SELECT de WQL, denominada "consulta de esquema", para especificar los tipos de clases admitidas. Las consultas de esquema especifican un nombre de clase especial denominado meta \_ class. En la tabla siguiente se enumeran las propiedades de la consulta.



| Propiedad                 | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ResultSetQueries**     | Contiene información sobre el conjunto de resultados que proporciona el proveedor. WMI usa la información para determinar si se debe invocar al proveedor para satisfacer una consulta de una aplicación. Esta propiedad describe el conjunto de todas las clases que el proveedor puede proporcionar o un superconjunto de las clases disponibles, pero nunca un subconjunto. WMI requiere que un proveedor especifique al menos una consulta en esta propiedad.<br/> En el ejemplo siguiente se muestra cómo establecer **ResultSetQueries** cuando un proveedor proporciona una clase de asociación que hace referencia a la [**\_ clase LogicalDisk de Win32.**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)<br/> `SELECT * FROM meta_class WHERE __Class = "Win32_LogicalDisk"`<br/> En el ejemplo siguiente se muestra cómo especificar una consulta general cuando un proveedor proporciona clases que hacen referencia a otras clases desconocidas.<br/> `SELECT * FROM meta_class`<br/> En el ejemplo siguiente se muestra cómo establecer **ResultSetQueries** cuando un proveedor solo proporciona subclases, pero no la clase primaria de una clase determinada.<br/> `SELECT * FROM meta_class WHERE __Dynasty = "MyClass"`<br/> En el ejemplo siguiente se muestra cómo usar la propiedad especial this y establecer ResultSetQueries cuando un proveedor proporciona todas \_ \_ las clases y  subclases.<br/> `SELECT * FROM meta_class WHERE __this ISA "MyClass"`<br/> |
| **ReferencedSetQueries** | Determina si se debe omitir el proveedor en consultas de esquema en las que se solicitan asociaciones y referencias. Los proveedores que pueden proporcionar clases de asociación deben incluir al menos una consulta en su **propiedad ReferencedSetQueries.**<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| **UnsupportedQueries**   | Contiene información sobre el conjunto de resultados que un proveedor de clases no proporciona. WMI usa esta propiedad para restar del conjunto de clases implícito en **ResultSetQueries**. Por ejemplo, un proveedor de clases puede especificar en **ResultSetQueries** compatibilidad con todas las clases derivadas de MyClass y especificar en **UnsupportedQueries** una falta de compatibilidad para una clase derivada determinada.<br/> Cuanto más información pueda registrar un proveedor sobre sus funcionalidades de procesamiento de consultas, más rápido se ejecuta. Escribir una o varias consultas en la propiedad **UnsupportedQueries** es una manera de ser específico y es especialmente importante cuando un proveedor se basa en una clase que no proporciona. Cuando se realiza una solicitud para una clase que aparece en una consulta en la propiedad **UnsupportedQueries,** WMI puede proporcionar la propia clase o invocar un proveedor alternativo para proporcionarla.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

Dado que WMI no admite la cláusula OR, debe crear una consulta independiente para cada clase.

Las consultas siguientes se especifican en **ResultSetQueries** cuando un proveedor de clases proporciona MyClass1, MyClass2 y MyClass3.


```sql
SELECT * FROM meta_class WHERE __Class = "MyClass1"
SELECT * FROM meta_class WHERE __Class = "MyClass2"
SELECT * FROM meta_class WHERE __Class = "MyClass3"
```



Solo los administradores pueden registrar o eliminar un proveedor mediante la creación de una instancia de [**\_ \_ Win32Provider**](--win32provider.md) y [**\_ \_ ClassProviderRegistration**](--classproviderregistration.md).

 

