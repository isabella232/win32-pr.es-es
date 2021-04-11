---
description: El espacio de nombres WMI es un objeto de programación que define el ámbito de un conjunto de clases e instancias. Las clases del proveedor de WMI se deben definir dentro de un espacio de nombres.
ms.assetid: a00f26e6-bb81-45bc-a530-9346a074bb3c
ms.tgt_platform: multiple
title: Crear jerarquías en WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5743c8da8c40fc0419a96a8ec9c65e7e112573a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276266"
---
# <a name="creating-hierarchies-within-wmi"></a>Crear jerarquías en WMI

El [*espacio de nombres WMI*](gloss-n.md) es un objeto de programación que define el ámbito de un conjunto de clases e instancias. Las clases del proveedor de WMI se deben definir dentro de un espacio de nombres.

Los espacios de nombres describen diferentes entornos administrados, como el entorno de SMS. Dado que las clases y las instancias de un esquema definen los componentes de un entorno administrado, cada esquema nuevo requiere un espacio de nombres nuevo. Por ejemplo, el \\ espacio de nombres root cimv2 contiene las clases e instancias definidas en el esquema de Win32, así como las clases de modelo de información común primario (CIM) de las que hereda el esquema de Win32. Las clases CIM están definidas por el equipo de tareas de administración distribuida ([DMTF](https://www.dmtf.org/home)).

> [!Note]  
> Para asegurarse de que todas las definiciones de clases de WMI para objetos administrados se restauran en el [*repositorio de WMI*](gloss-w.md) si WMI tiene un error y se reinicia, use la instrucción de preprocesador [**\# pragma autocover**](pragma-autorecover.md) en el archivo [*Managed Object Format (MOF)*](gloss-m.md) .

 

WMI define un espacio de nombres como una instancia de la clase de sistema de [**\_ \_ espacio de nombres**](--namespace.md) o cualquier clase que derive de un espacio de **\_ \_ nombres**. La clase de sistema de **\_ \_ espacio de nombres** tiene una propiedad única denominada **Name**, que debe ser única dentro del ámbito del espacio de nombres primario. La propiedad **Name** también debe contener una cadena que empiece por una letra. Todos los demás caracteres de la cadena pueden ser letras, dígitos o caracteres de subrayado. Todos los caracteres no distinguen mayúsculas de minúsculas.

Además de determinar el nombre único de un espacio de nombres secundario, el espacio de nombres WMI primario puede proteger las instancias estáticas de las clases frente a modificaciones accidentales de otros proveedores. Por ejemplo, puede que le resulte conveniente anidar un nuevo espacio de nombres en un espacio de nombres existente para otro proveedor. Sin embargo, el proveedor original puede intentar actualizar todas las instancias de clase para que coincida con un nuevo esquema. Al hacerlo, el proveedor original puede eliminar todos los subelementos secundarios de un espacio de nombres. Aunque puede ser una acción adecuada para el espacio de nombres de destino, puede afectar a las instancias de clase no relacionadas en un espacio de nombres secundario (es decir, sus propias clases de proveedor).

Por lo tanto, se recomienda crear y registrar el espacio de nombres como independiente de los espacios de nombres que no controle directamente. Esto es especialmente cierto si las clases solo se derivan de clases CIM generales u otras clases de la empresa. El espacio de nombres puede estar en el espacio de nombres **raíz** , como el siguiente:

**Root/mycompany/mi producto**

En cambio, si la nueva clase se deriva de la clase de otro proveedor, puede que necesite almacenar la clase en un subespacio de nombres de ese proveedor. Tenga en cuenta que esto expone la nueva clase a la eliminación accidental por parte del proveedor original.

WMI proporciona varias maneras diferentes de crear un espacio de nombres:

-   [Crear un espacio de nombres secundario con código MOF](creating-a-child-namespace-with-mof-code.md)
-   [Crear un espacio de nombres relacionado con código MOF](creating-a-sibling-namespace-with-mof-code.md)
-   [Crear un espacio de nombres con la API de WMI](creating-a-namespace-with-the-wmi-api.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Diseñar clases de Managed Object Format (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



