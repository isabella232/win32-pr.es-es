---
description: Use esta tabla para crear una instalación de varios paquetes.
ms.assetid: ac1e9c7b-bb83-4e1e-9108-211374c7d878
title: Tabla MsiEmbeddedChainer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1cfcf48f3cf3863f19819b3337a136d2540fa3254067cacc50fcf391256caa5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945060"
---
# <a name="msiembeddedchainer-table"></a>Tabla MsiEmbeddedChainer

Use esta tabla para crear una [instalación de varios paquetes.](multiple-package-installations.md) Cada fila de la tabla MsiEmbeddedChainer hace referencia a una función diferente definida por el usuario que se puede usar para instalar varios paquetes de Windows Installer desde un único paquete. Los [archivos ejecutables](executable-files.md) de las funciones definidas por el usuario se almacenan dentro del Windows Installer.

**[Windows Instalador 4.0 o anterior:](not-supported-in-windows-installer-4-0.md)** No se admite. Esta tabla está disponible a partir de Windows Installer 4.5.

**Windows Server 2008 R2 con el [Servicios de Escritorio remoto](../termserv/terminal-services-portal.md) habilitado:** No se admite. Se produce un error en una instalación de varios paquetes mediante la tabla MsiEmbeddedChainer si el [Servicios de Escritorio remoto](../termserv/terminal-services-portal.md) está habilitado.

Para instalar varios paquetes desde un único paquete, una de las funciones definidas por el usuario enumeradas en la tabla MsiEmbeddedChainer debe tener una instrucción condicional en el campo Condición que se evalúe para ejecutar la acción. Si más de una función tiene una condición que se evalúa como ejecutada, solo se puede ejecutar una función. Este caso es un error y no se puede garantizar qué función se ejecutará. Si la instalación necesita otras acciones personalizadas, se deben crear en la tabla [CustomAction y](customaction-table.md) en las tablas de secuencia.

Las funciones deben unirse a la instalación actual llamando a la función [**MsiJoinTransaction**](/windows/desktop/api/Msi/nf-msi-msijointransaction) y deben llamar a la [**función MsiEndTransaction**](/windows/desktop/api/Msi/nf-msi-msiendtransaction) para confirmar la instalación de varios paquetes. Si las funciones devuelven antes de **llamar a MsiEndTransaction,** el instalador revierte todas las instalaciones.

La tabla MsiEmbeddedChainer tiene las siguientes columnas.



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

Una instrucción condicional para ejecutar la función definida por el usuario. Puede habilitar o deshabilitar las funciones enumeradas en la tabla MsiEmbeddedChainer mediante una transformación que modifique los valores de propiedad evaluados por este campo. Para obtener más información, [vea Using Properties in Conditional Statements](using-properties-in-conditional-statements.md).

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

## <a name="remarks"></a>Comentarios

El Windows programa de instalación no impide que las funciones definidas por el usuario de esta tabla se ejecuten durante el anuncio de la aplicación. Puede usar una instrucción condicional en la columna Condición para evitar que una función se ejecute durante el anuncio.

El Windows de archivos también proporciona un controlador de interfaz de usuario externo no incrustado para compilar una interfaz de usuario enriquecte sobre el paquete Windows Installer. Para obtener más información sobre el uso de un controlador de interfaz de usuario externo con Windows Installer, vea [Monitoring an Installation Using MsiSetExternalUI](monitoring-an-installation-using-msisetexternalui.md).

En [la tabla MsiPackageCertificate se](msipackagecertificate-table.md) enumeran los certificados de firma digital que se usan para comprobar la identidad de los paquetes de instalación que hacen una instalación de varios paquetes. Puede usar esta tabla para reducir el número de veces que la instalación de varios paquetes muestra un mensaje de [*control*](u-gly.md) de cuentas de usuario (UAC) que requiere una respuesta por parte de un administrador.

 

 
