---
description: Use esta tabla para crear una instalación de varios paquetes.
ms.assetid: ac1e9c7b-bb83-4e1e-9108-211374c7d878
title: Tabla MsiEmbeddedChainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 902a33bce5d3a0aff3d2797fce94e5d272b61271
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666883"
---
# <a name="msiembeddedchainer-table"></a>Tabla MsiEmbeddedChainer

Use esta tabla para crear una [instalación de varios paquetes](multiple-package-installations.md). Cada fila de la tabla MsiEmbeddedChainer hace referencia a una función definida por el usuario diferente que se puede usar para instalar varios paquetes de Windows Installer desde un único paquete. Los [archivos ejecutables](executable-files.md) para las funciones definidas por el usuario se almacenan dentro del paquete Windows Installer.

**[Windows Installer 4,0 o una versión anterior](not-supported-in-windows-installer-4-0.md):** No compatible. Esta tabla está disponible a partir de Windows Installer 4,5.

**Windows Server 2008 R2 con el rol de [servicios de escritorio remoto](../termserv/terminal-services-portal.md) habilitado:** No compatible. Se produce un error en una instalación de varios paquetes mediante la tabla MsiEmbeddedChainer si está habilitado el rol [servicios de escritorio remoto](../termserv/terminal-services-portal.md) .

Para instalar varios paquetes desde un único paquete, una de las funciones definidas por el usuario enumeradas en la tabla MsiEmbeddedChainer debe tener una instrucción condicional en el campo condición que se evalúe para ejecutar la acción. Si hay más de una función que tiene una condición que se evalúa como de ejecución, solo se puede ejecutar una función. Este caso es un error y no se puede garantizar qué función se ejecutará. Si la instalación necesita otras acciones personalizadas, estas deben crearse en las tablas de tabla y de secuencia de [CustomAction](customaction-table.md) .

Las funciones deben unirse a la instalación actual llamando a la función [**MsiJoinTransaction**](/windows/desktop/api/Msi/nf-msi-msijointransaction) y deben llamar a la función [**MsiEndTransaction**](/windows/desktop/api/Msi/nf-msi-msiendtransaction) para confirmar la instalación de varios paquetes. Si las funciones devuelven antes de llamar a **MsiEndTransaction**, el instalador revierte todas las instalaciones.

La tabla MsiEmbeddedChainer tiene las columnas siguientes.



| Columna             | Tipo                             | Clave | Nullable |
|--------------------|----------------------------------|-----|----------|
| MsiEmbeddedChainer | [Identificador](identifier.md)     | Y   | N        |
| Condición          | [Condition](condition.md)       | N   | Y        |
| CommandLine        | [Formatea](formatted.md)       | N   | Y        |
| Source             | [CustomSource](customsource.md) | N   | N        |
| Tipo               | [Entero](integer.md)           | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="MsiEmbeddedChainer"></span><span id="msiembeddedchainer"></span><span id="MSIEMBEDDEDCHAINER"></span>MsiEmbeddedChainer
</dt> <dd>

La clave principal de la tabla. Este valor es un identificador único para la función definida por el usuario que describe esta fila.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Cumple
</dt> <dd>

Instrucción condicional para ejecutar la función definida por el usuario. Puede habilitar o deshabilitar las funciones enumeradas en la tabla MsiEmbeddedChainer mediante una transformación que modifica los valores de propiedad evaluados por este campo. Para obtener más información, vea [usar propiedades en instrucciones condicionales](using-properties-in-conditional-statements.md).

</dd> <dt>

<span id="CommandLine"></span><span id="commandline"></span><span id="COMMANDLINE"></span>CommandLine
</dt> <dd>

El valor de este campo es una parte de la cadena de línea de comandos que se pasa al archivo ejecutable identificado en la columna de origen. El instalador anexa el valor de este campo al identificador de transacción para generar la línea de comandos. Si el valor de esta columna es null, la línea de comandos solo se compone del identificador de la transacción.

</dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Fuentes
</dt> <dd>

Ubicación del archivo ejecutable para la función definida por el usuario. Si el valor de la columna Type es 2, esta columna puede contener una clave externa en la [tabla binaria](binary-table.md). Si el valor de la columna Type es 18, esta columna puede contener una clave externa en la [tabla File](file-table.md). Si el valor de la columna Type es 50, esta columna puede contener una clave externa en la [tabla de propiedades](property-table.md).

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Automáticamente
</dt> <dd>

Las funciones enumeradas en la tabla MsiEmbeddedChainer se describen mediante los siguientes tipos numéricos de acción personalizada. Esta columna solo puede contener los valores de los tres tipos numéricos siguientes: se omite cualquier otra combinación de marcas de acción personalizadas.



| Tipo de acción personalizada                                 | Marcas de acción personalizadas                                                | Hexadecimal | Decimal |
|----------------------------------------------------|--------------------------------------------------------------------|-------------|---------|
| [Tipo de acción personalizada 2](custom-action-type-2.md)   | **msidbCustomActionTypeExe**  +  **msidbCustomActionTypeBinaryData** | 0x002       | 2       |
| [Tipo de acción personalizada 18](custom-action-type-18.md) | **msidbCustomActionTypeExe**  +  **msidbCustomActionTypeSourceFile** | 0x012       | 18      |
| [Tipo de acción personalizada 50](custom-action-type-50.md) | **msidbCustomActionTypeExe**  +  **msidbCustomActionTypeProperty**   | 0x032       | 50      |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

El Windows Installer no evita que se ejecuten las funciones definidas por el usuario en esta tabla durante el anuncio de la aplicación. Puede usar una instrucción condicional en la columna condición para evitar que una función se ejecute durante el anuncio.

El Windows Installer también proporciona un controlador de interfaz de usuario externa no incrustado para compilar una interfaz de usuario enriquecida sobre el paquete de Windows Installer. Para obtener más información sobre el uso de un controlador de interfaz de usuario externo con el Windows Installer, vea [supervisar una instalación mediante MsiSetExternalUI](monitoring-an-installation-using-msisetexternalui.md).

En la [tabla MsiPackageCertificate](msipackagecertificate-table.md) se muestran los certificados de firma digital que se usan para comprobar la identidad de los paquetes de instalación que realizan una instalación de varios paquetes. Puede usar esta tabla para reducir el número de veces que la instalación de varios paquetes muestra un mensaje de [*control de cuentas de usuario*](u-gly.md) (UAC) que requiere una respuesta por parte de un administrador.

 

 
