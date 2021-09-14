---
description: Use esta tabla para crear una instalación de varios paquetes.
ms.assetid: ac1e9c7b-bb83-4e1e-9108-211374c7d878
title: Tabla MsiEmbeddedChainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 902a33bce5d3a0aff3d2797fce94e5d272b61271
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071862"
---
# <a name="msiembeddedchainer-table"></a>Tabla MsiEmbeddedChainer

Use esta tabla para crear una [instalación de varios paquetes.](multiple-package-installations.md) Cada fila de la tabla MsiEmbeddedChainer hace referencia a una función diferente definida por el usuario que se puede usar para instalar varios paquetes de Windows Installer desde un único paquete. Los [archivos ejecutables](executable-files.md) para las funciones definidas por el usuario se almacenan dentro del paquete Windows Installer.

**[Windows Instalador 4.0 o anterior:](not-supported-in-windows-installer-4-0.md)** No se admite. Esta tabla está disponible a partir de Windows Installer 4.5.

**Windows Server 2008 R2 con el [Servicios de Escritorio remoto](../termserv/terminal-services-portal.md) habilitado:** No se admite. Se produce un error en una instalación de varios paquetes mediante la tabla MsiEmbeddedChainer [si el Servicios de Escritorio remoto](../termserv/terminal-services-portal.md) rol está habilitado.

Para instalar varios paquetes desde un único paquete, una de las funciones definidas por el usuario enumeradas en la tabla MsiEmbeddedChainer debe tener una instrucción condicional en el campo Condición que se evalúe para ejecutar la acción. Si más de una función tiene una condición que se evalúa como ejecutada, solo se puede ejecutar una función. Este caso es un error y no se puede garantizar qué función se ejecutará. Si la instalación necesita otras acciones personalizadas, estas se deben crear en las tablas de tabla y secuencia [CustomAction.](customaction-table.md)

Las funciones deben unirse a la instalación actual llamando a la función [**MsiJoinTransaction**](/windows/desktop/api/Msi/nf-msi-msijointransaction) y deben llamar a la [**función MsiEndTransaction**](/windows/desktop/api/Msi/nf-msi-msiendtransaction) para confirmar la instalación de varios paquetes. Si las funciones devuelven antes de **llamar a MsiEndTransaction,** el instalador revierte todas las instalaciones.

La tabla MsiEmbeddedChainer tiene las columnas siguientes.



| Columna             | Tipo                             | Clave | Nullable |
|--------------------|----------------------------------|-----|----------|
| MsiEmbeddedChainer | [Identificador](identifier.md)     | Y   | N        |
| Condición          | [Condition](condition.md)       | N   | Y        |
| CommandLine        | [Formato](formatted.md)       | N   | Y        |
| Source             | [CustomSource](customsource.md) | N   | N        |
| Tipo               | [Entero](integer.md)           | N   | N        |



 

## <a name="columns"></a>Columnas

<dl> <dt>

<span id="MsiEmbeddedChainer"></span><span id="msiembeddedchainer"></span><span id="MSIEMBEDDEDCHAINER"></span>MsiEmbeddedChainer
</dt> <dd>

Clave principal de la tabla. Este valor es un identificador único para la función definida por el usuario descrita por esta fila.

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condición
</dt> <dd>

Una instrucción condicional para ejecutar la función definida por el usuario. Puede habilitar o deshabilitar las funciones enumeradas en la tabla MsiEmbeddedChainer mediante una transformación que modifica los valores de propiedad evaluados por este campo. Para obtener más información, [vea Using Properties in Conditional Statements](using-properties-in-conditional-statements.md).

</dd> <dt>

<span id="CommandLine"></span><span id="commandline"></span><span id="COMMANDLINE"></span>Commandline
</dt> <dd>

El valor de este campo forma parte de la cadena de línea de comandos que se pasa al archivo ejecutable identificado en la columna Origen. El instalador anexa el valor de este campo al identificador de transacción para generar la línea de comandos. Si el valor de esta columna es NULL, la línea de comandos consta solo del identificador de transacción.

</dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Fuente
</dt> <dd>

Ubicación del archivo ejecutable para la función definida por el usuario. Si el valor de la columna Tipo es 2, esta columna puede contener una clave externa en la [tabla binaria](binary-table.md). Si el valor de la columna Tipo es 18, esta columna puede contener una clave externa en la [tabla File](file-table.md). Si el valor de la columna Tipo es 50, esta columna puede contener una clave externa en la [tabla Property](property-table.md).

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Tipo
</dt> <dd>

Las funciones enumeradas en la tabla MsiEmbeddedChainer se describen mediante los siguientes tipos numéricos de acción personalizada. Esta columna solo puede contener los valores de los tres tipos numéricos siguientes; se omite cualquier otra combinación de marcas de acción personalizadas.



| Tipo de acción personalizada                                 | Marcas de acción personalizadas                                                | Hexadecimal | Decimal |
|----------------------------------------------------|--------------------------------------------------------------------|-------------|---------|
| [Tipo de acción personalizada 2](custom-action-type-2.md)   | **msidbCustomActionTypeExe**  +  **msidbCustomActionTypeBinaryData** | 0x002       | 2       |
| [Tipo de acción personalizada 18](custom-action-type-18.md) | **msidbCustomActionTypeExe**  +  **msidbCustomActionTypeSourceFile** | 0x012       | 18      |
| [Tipo de acción personalizada 50](custom-action-type-50.md) | **msidbCustomActionTypeExe**  +  **msidbCustomActionTypeProperty**   | 0x032       | 50      |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

El Windows no impide que las funciones definidas por el usuario de esta tabla se ejecuten durante el anuncio de la aplicación. Puede usar una instrucción condicional en la columna Condición para evitar que una función se ejecute durante el anuncio.

El instalador Windows también proporciona un controlador de interfaz de usuario externo no incrustado para compilar una interfaz de usuario enriqueceda sobre el paquete Windows Installer. Para obtener más información sobre el uso de un controlador de interfaz de usuario externo con el instalador Windows, vea Supervisar una instalación mediante [MsiSetExternalUI](monitoring-an-installation-using-msisetexternalui.md).

En [la tabla MsiPackageCertificate se](msipackagecertificate-table.md) enumeran los certificados de firma digital que se usan para comprobar la identidad de los paquetes de instalación que hacen una instalación de varios paquetes. Puede usar esta tabla para reducir el número de veces que la instalación de varios paquetes muestra un mensaje de [*Control*](u-gly.md) de cuentas de usuario (UAC) que requiere una respuesta por parte de un administrador.

 

 
