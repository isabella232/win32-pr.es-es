---
description: Un proveedor WMI consta de un archivo Managed Object Format (MOF) y un archivo DLL. El archivo MOF define las clases para las que la implementación del proveedor proporciona datos.
ms.assetid: 20ef6b88-2aaa-4e86-bc4a-bebc34069672
ms.tgt_platform: multiple
title: Diseñar clases Managed Object Format (MOF)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 201f8c45f7a247fbca5695baa6dd440fc5dc323f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127575360"
---
# <a name="designing-managed-object-format-mof-classes"></a>Diseñar clases Managed Object Format (MOF)

Un [*proveedor WMI*](gloss-p.md) consta de un archivo Managed Object Format (MOF) y un archivo DLL. El archivo MOF define las clases para las que la implementación del proveedor proporciona datos.

Las definiciones de clase MOF se compilan mediante la utilidad [**mofcomp**](mofcomp.md) y se almacenan en el repositorio [*WMI*](gloss-w.md), también conocido como repositorio Modelo de información común (CIM). Una manera menos común de crear clases es a través de los métodos de la [API COM para WMI.](com-api-for-wmi.md)

> [!Note]  
> Para asegurarse de que todas las definiciones de clase WMI para objetos administrados se restauran en el repositorio [*WMI*](gloss-w.md) si WMI tiene un error y se reinicia, use la instrucción [**\# pragma autorecover**](pragma-autorecover.md) preprocessor en el archivo MOF.

 

En este tema se de abordan las siguientes secciones:

-   [Definir los objetos que se administrarán](#defining-the-objects-to-manage)
-   [Definir propiedades o métodos](#defining-properties-or-methods)
-   [Relacionar objetos entre sí](#relating-objects-to-each-other)
-   [Temas relacionados](#related-topics)

## <a name="defining-the-objects-to-manage"></a>Definir los objetos que se administrarán

Después de identificar la parte de la empresa que se va a administrar, defina los objetos que desea administrar. La definición debe incluir los datos necesarios y le permite implementar las reglas de negocio pertinentes con precisión. Puede definir objetos en un nivel granular, pero es mejor decidir entre el nivel de detalle contenido en la definición y la necesidad de proporcionar suficientes detalles para que sean útiles. Los accesos directos al principio del proceso pueden ahorrar tiempo, pero pueden provocar más trabajo en el futuro.

El tutorial de CIM del sitio web del Grupo de tareas de administración distribuida (DMTF) contiene información excelente sobre el proceso de diseño. Para obtener más información, [vea www.dmtf.org](https://www.dmtf.org/).

Tenga en cuenta los siguientes factores al desarrollar e implementar un diseño de esquema:

-   Calificadores

    Los calificadores proporcionan información sobre cómo describir clases, objetos, propiedades, métodos y parámetros. y se aplican a las definiciones de clase y propiedad. En el código MOF, los calificadores se incluyen entre corchetes y pueden incluir \[ la clave o la \] \[ asociación \] . Para obtener más información, vea [Agregar un calificador y](adding-a-qualifier.md) [calificadores WMI](wmi-qualifiers.md).

-   Espacio de nombres

    Un espacio de nombres es una unidad lógica para agrupar clases y objetos, y controlar el ámbito y la visibilidad. Normalmente, un espacio de nombres contiene un conjunto de clases y objetos que representan objetos administrados en un entorno específico. Para obtener más información, [vea Crear jerarquías dentro de WMI.](creating-hierarchies-within-wmi.md)

-   Object

    Un objeto modelado puede ser un elemento físico o lógico del esquema. Por ejemplo, puede modelar una unidad de disco físico, como una unidad de disco duro, o un disco lógico que puede ser una partición en un disco físico. Un diseño que usa una clase para modelar una unidad de disco físico y, a continuación, extiende esa clase para modelar un disco lógico es más extensible que uno que intenta crear una clase independiente para cada tipo de disco.

-   Datos

    Los datos pueden ser dinámicos o estáticos. Si los datos son dinámicos, debe crear un proveedor de clases para él.

    Para permitir que el usuario modifique los datos, debe determinar si quiere que una propiedad se pueda escribir directamente o modificarse solo mediante un método al que el usuario llama.

## <a name="defining-properties-or-methods"></a>Definir propiedades o métodos

Por lo general, una propiedad de clase WMI es similar a una propiedad de una clase de C++. Si las únicas acciones que implementa el código para el fragmento de datos es obtener el valor o establecer el valor, los datos deben definirse como una propiedad de la clase WMI.

Por lo general, un método WMI realiza una acción que cambia el estado de un objeto administrado. Por ejemplo, si la acción es habilitar o deshabilitar el funcionamiento de un objeto de hardware, es probable que un método sea preferible a crear una propiedad de lectura y escritura. También puede decidir crear una propiedad que muestre el estado del hardware.

Al crear una clase o una instancia de , puede incluir comentarios. Use esta técnica para documentar la clase o explicar las técnicas de programación. Para obtener más información, vea [Crear un comentario](creating-a-comment.md). Además, puede agregar datos para calificar el propósito de un objeto de datos. Para obtener más información, vea [Agregar un calificador](adding-a-qualifier.md).

## <a name="relating-objects-to-each-other"></a>Relacionar objetos entre sí

Hay dos maneras de relacionar objetos entre sí: creando objetos independientes y un objeto de asociación que los relaciona, o insertando un objeto en el otro. CIM no admite objetos incrustados, por lo que para ser compatible con CIM debe usar el primer método. Sin embargo, WMI admite objetos incrustados, por lo que puede usar cualquiera de los métodos para representar una relación entre los objetos . Puede encontrar ejemplos de objetos incrustados en las [clases de Win32](/windows/desktop/CIMWin32Prov/win32-provider). Por ejemplo, [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) tiene el objeto incrustado [**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace), que tiene otro objeto incrustado, [**Win32 \_ Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee).

Tenga en cuenta lo siguiente al decidir cómo representar relaciones entre objetos:

-   Si una instancia es útil por sí misma, una asociación funciona mejor. Por ejemplo, [**Win32 \_ Process y**](/windows/desktop/CIMWin32Prov/win32-process) [**Win32 \_ UserAccount**](/windows/desktop/CIMWin32Prov/win32-useraccount). Para obtener más información, vea [Declarar una clase de asociación](declaring-an-association-class.md).
-   Si una instancia no existe fuera del objeto primario, un objeto incrustado funciona mejor. Por ejemplo, [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) y [**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace). Para obtener más información, [vea Incrustar objetos en una clase](embedded-objects.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desarrollar un proveedor WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Proporcionar datos a WMI](providing-data-to-wmi.md)
</dt> <dt>

[Tipos de datos MOF](mof-data-types.md)
</dt> </dl>

 

 
