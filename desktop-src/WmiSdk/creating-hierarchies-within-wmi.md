---
description: Espacio de nombres WMI es un objeto de programación que define el ámbito de un conjunto de clases e instancias. Las clases de proveedor WMI deben definirse dentro de un espacio de nombres.
ms.assetid: a00f26e6-bb81-45bc-a530-9346a074bb3c
ms.tgt_platform: multiple
title: Crear jerarquías dentro de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a2649fb764c1710613b27e1c9bbe518dd4cb8d02215df935ddccb59c9d7e922
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119568785"
---
# <a name="creating-hierarchies-within-wmi"></a>Crear jerarquías dentro de WMI

[*Espacio de nombres WMI*](gloss-n.md) es un objeto de programación que define el ámbito de un conjunto de clases e instancias. Las clases de proveedor WMI deben definirse dentro de un espacio de nombres.

Los espacios de nombres describen diferentes entornos administrados, como el entorno de SMS. Dado que las clases e instancias de un esquema definen los componentes de un entorno administrado, cada nuevo esquema requiere un nuevo espacio de nombres. Por ejemplo, el espacio de nombres cimv2 raíz contiene las clases e instancias definidas en el esquema Win32, así como las clases Modelo de información común (CIM) primarias de las que hereda el esquema \\ Win32. El grupo de tareas de administración distribuida[(DMTF)](https://www.dmtf.org/home)define las clases CIM .

> [!Note]  
> Para asegurarse de que todas las definiciones de clase WMI para objetos administrados se restauran en el repositorio [*WMI*](gloss-w.md) si WMI tiene un error y se reinicia, use la instrucción de preprocesador [**\# pragma autorecover**](pragma-autorecover.md) en el archivo [*Managed Object Format (MOF).*](gloss-m.md)

 

WMI define un espacio de nombres como una instancia de la clase del sistema [**\_ \_ Namespace**](--namespace.md) o cualquier clase que se derive de **\_ \_ Namespace**. La **\_ \_ clase del** sistema Namespace tiene una sola propiedad denominada **Name**, que debe ser única dentro del ámbito del espacio de nombres primario. La **propiedad Name** también debe contener una cadena que comience por una letra. Todos los demás caracteres de la cadena pueden ser letras, dígitos o caracteres de subrayado. Todos los caracteres no tienen en cuenta las mayúsculas y minúsculas.

Además de determinar el nombre único de un espacio de nombres secundario, el espacio de nombres WMI primario puede proteger las instancias estáticas de las clases frente a modificaciones accidentales por parte de otros proveedores. Por ejemplo, puede que le resulte conveniente anidar un nuevo espacio de nombres en un espacio de nombres existente para otro proveedor. Sin embargo, el proveedor original puede intentar actualizar todas las instancias de clase para que coincidan con un nuevo esquema. Al hacerlo, el proveedor original puede eliminar todos los elementos secundarios de un espacio de nombres. Aunque puede ser una acción adecuada para el espacio de nombres de destino, puede afectar a las instancias de clase no relacionadas de un espacio de nombres secundario (es decir, a sus propias clases de proveedor).

Por lo tanto, se recomienda crear y registrar el espacio de nombres como independiente de los espacios de nombres que no se controlan directamente. Esto es especialmente cierto si las clases se derivan solo de clases CIM generales u otras clases de su empresa. El espacio de nombres puede estar en el **espacio de nombres** raíz, como el siguiente:

**Root/myCompany/myProduct**

Por el contrario, si la nueva clase deriva de la clase de otro proveedor, es posible que tenga que almacenar la clase en un subso espacio de nombres de ese proveedor. Tenga en cuenta que esto expone la nueva clase a la eliminación accidental por parte del proveedor original.

WMI proporciona varias maneras diferentes de crear un espacio de nombres:

-   [Crear un espacio de nombres secundario con código MOF](creating-a-child-namespace-with-mof-code.md)
-   [Crear un espacio de nombres relacionado con código MOF](creating-a-sibling-namespace-with-mof-code.md)
-   [Creación de un espacio de nombres con la API WMI](creating-a-namespace-with-the-wmi-api.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Diseñar clases Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



