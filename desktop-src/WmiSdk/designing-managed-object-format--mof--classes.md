---
description: Un proveedor WMI consta de un archivo DLL y un archivo Managed Object Format (MOF). El archivo MOF define las clases para las que la implementación del proveedor proporciona datos.
ms.assetid: 20ef6b88-2aaa-4e86-bc4a-bebc34069672
ms.tgt_platform: multiple
title: Diseñar clases de Managed Object Format (MOF)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 201f8c45f7a247fbca5695baa6dd440fc5dc323f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277707"
---
# <a name="designing-managed-object-format-mof-classes"></a>Diseñar clases de Managed Object Format (MOF)

Un [*proveedor WMI*](gloss-p.md) consta de un archivo dll y un archivo Managed Object Format (MOF). El archivo MOF define las clases para las que la implementación del proveedor proporciona datos.

Las definiciones de clases de MOF se compilan mediante la utilidad [**MOFCOMP**](mofcomp.md) y se almacenan en el [*repositorio WMI*](gloss-w.md), también conocido como repositorio modelo de información común (CIM). Una manera menos común de crear clases es a través de los métodos de la [API com para WMI](com-api-for-wmi.md).

> [!Note]  
> Para asegurarse de que todas las definiciones de clase WMI para objetos administrados se restauran en el [*repositorio WMI*](gloss-w.md) si WMI tiene un error y se reinicia, use la instrucción de preprocesador [**\# pragma Recover**](pragma-autorecover.md) en el archivo MOF.

 

En este tema se describen las siguientes secciones:

-   [Definir los objetos que se van a administrar](#defining-the-objects-to-manage)
-   [Definir propiedades o métodos](#defining-properties-or-methods)
-   [Relacionar los objetos entre sí](#relating-objects-to-each-other)
-   [Temas relacionados](#related-topics)

## <a name="defining-the-objects-to-manage"></a>Definir los objetos que se van a administrar

Después de identificar la parte de la empresa que se va a administrar, defina los objetos que desea administrar. La definición debe incluir los datos necesarios y permitirle implementar las reglas de negocios pertinentes de forma precisa. Puede definir objetos en un nivel granular, pero es mejor decidir entre el nivel de detalle contenido en la definición y la necesidad de proporcionar detalles suficientes para ser útil. Los métodos abreviados al principio del proceso pueden ahorrar tiempo, pero pueden provocar más trabajo en el futuro.

El tutorial de CIM en el sitio web del equipo de administración distribuida (DMTF) contiene información excelente sobre el proceso de diseño. Para obtener más información, vea [www.dmtf.org](https://www.dmtf.org/).

Tenga en cuenta los siguientes factores al desarrollar e implementar un diseño de esquema:

-   Calificadores

    Los calificadores proporcionan información sobre cómo describir clases, objetos, propiedades, métodos y parámetros. y se aplican a las definiciones de clase y propiedad. En el código MOF, los calificadores se incluyen entre corchetes y pueden incluir la \[ clave \] o la \[ Asociación \] . Para obtener más información, vea [Agregar un calificador](adding-a-qualifier.md) y [calificadores de WMI](wmi-qualifiers.md).

-   Espacio de nombres

    Un espacio de nombres es una unidad lógica para agrupar clases y objetos, y controlar el ámbito y la visibilidad. Normalmente, un espacio de nombres contiene un conjunto de clases y objetos que representan objetos administrados en un entorno específico. Para obtener más información, vea [Crear jerarquías en WMI](creating-hierarchies-within-wmi.md).

-   Object

    Un objeto modelado podría ser un elemento físico o lógico del esquema. Por ejemplo, puede modelar una unidad de disco físico, como una unidad de disco duro, o un disco lógico que puede ser una partición en un disco físico. Un diseño que usa una clase para modelar una unidad de disco físico y, a continuación, extiende esa clase para modelar un disco lógico es más extensible que uno que intenta crear una clase independiente para cada tipo de disco.

-   Datos

    Los datos pueden ser dinámicos o estáticos. Si los datos son dinámicos, debe crear un proveedor de clases para él.

    Para permitir al usuario modificar los datos, debe determinar si desea o no que una propiedad se pueda escribir directamente o modificar solo mediante un método al que llama el usuario.

## <a name="defining-properties-or-methods"></a>Definir propiedades o métodos

Por lo general, una propiedad de clase WMI es similar a una propiedad de una clase de C++. Si las únicas acciones que implementa el código para el fragmento de datos es obtener el valor o establecer el valor, los datos se deben definir como una propiedad de la clase WMI.

Un método WMI generalmente realiza una acción que cambia el estado de un objeto administrado. Por ejemplo, si la acción es habilitar o deshabilitar la operación de un objeto de hardware, probablemente sea preferible un método para crear una propiedad de lectura y escritura. También puede decidir crear una propiedad que muestre el estado del hardware.

Al crear una clase o una instancia, puede incluir comentarios. Utilice esta técnica para documentar su clase o explicar sus técnicas de programación. Para obtener más información, vea [crear un comentario](creating-a-comment.md). Además, puede agregar datos para calificar el propósito de un objeto de datos. Para obtener más información, consulte [Agregar un calificador](adding-a-qualifier.md).

## <a name="relating-objects-to-each-other"></a>Relacionar los objetos entre sí

Hay dos maneras de relacionar los objetos entre sí: mediante la creación de objetos independientes y un objeto de asociación que los relaciona, o mediante la inserción de un objeto en el otro. CIM no admite objetos incrustados, por lo que para ser compatible con CIM, debe usar el primer método. Sin embargo, WMI admite objetos incrustados, por lo que debe usar cualquier método para representar una relación entre los objetos. Puede encontrar ejemplos de objetos incrustados en las [clases Win32](/windows/desktop/CIMWin32Prov/win32-provider). Por ejemplo, [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) tiene el objeto incrustado [**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace), que tiene otro objeto incrustado, [**Administrador de \_ confianza de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee).

Tenga en cuenta lo siguiente a la hora de decidir cómo representar las relaciones entre objetos:

-   Si una instancia es útil por sí misma, una asociación funciona mejor. Por ejemplo, [**el \_ proceso de Win32**](/windows/desktop/CIMWin32Prov/win32-process) y la [**\_ cuentadeusuario de Win32**](/windows/desktop/CIMWin32Prov/win32-useraccount). Para obtener más información, vea [declarar una clase de asociación](declaring-an-association-class.md).
-   Si una instancia no existe fuera del objeto primario, un objeto incrustado funciona mejor. Por ejemplo, [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) y [**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace). Para obtener más información, vea [incrustar objetos en una clase](embedded-objects.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desarrollar un proveedor WMI](developing-a-wmi-provider.md)
</dt> <dt>

[Proporcionar datos a WMI](providing-data-to-wmi.md)
</dt> <dt>

[Tipos de datos MOF](mof-data-types.md)
</dt> </dl>

 

 
