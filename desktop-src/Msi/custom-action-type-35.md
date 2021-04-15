---
description: Los desarrolladores de paquetes de Windows Installer pueden optar por usar un tipo de acción personalizada 35 cuando las acciones estándar no son suficientes para ejecutar la instalación.
ms.assetid: b88b5f48-5353-4876-9dda-2eeda288fa4b
title: Tipo de acción personalizada 35
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8401f26f40ccc7de811ea0d290d556789284680f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669749"
---
# <a name="custom-action-type-35"></a>Tipo de acción personalizada 35

Esta acción personalizada establece el directorio de instalación desde una cadena de texto con formato. Para obtener más información, consulte [cambiar la ubicación de destino de un directorio](changing-the-target-location-for-a-directory.md) .

## <a name="source"></a>Source

El campo de origen de la [tabla CustomAction](customaction-table.md) contiene una clave para la [tabla de directorios](directory-table.md). El directorio designado se establece mediante la cadena con formato en el campo de destino mediante [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha). Esto establece la ruta de acceso de destino y la propiedad asociada en el valor expandido de la cadena de texto con formato en el campo de destino. No intente cambiar la ubicación de un directorio de destino durante una [instalación de mantenimiento](maintenance-installation.md). No intente cambiar la ruta de acceso del directorio de destino si algunos componentes que usan esa ruta de acceso ya están instalados para cualquier usuario.

## <a name="type-value"></a>Valor de tipo

Incluya el siguiente valor en la columna Type de la [tabla CustomAction](customaction-table.md) para especificar el tipo numérico básico.



| Constantes                                                              | Hexadecimal | Decimal |
|------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeTextData**  +  **msidbCustomActionTypeDirectory** | 0x023       | 35      |



 

## <a name="target"></a>Destino

La columna de destino de la [tabla CustomAction](customaction-table.md) contiene una cadena de texto con el formato de la funcionalidad especificada en [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (sin los especificadores de campo numérico). Los parámetros que se van a reemplazar se incluyen entre corchetes \[ ... \] y pueden ser propiedades, variables de entorno (% Prefix), rutas de acceso de archivo ( \# prefijo) o rutas de acceso del directorio de componentes ($ Prefix). Tenga en cuenta que las rutas de acceso de directorio siempre finalizan con un separador de directorios.

## <a name="return-processing-options"></a>Opciones de procesamiento de valores devueltos

La acción personalizada no utiliza estas opciones.

## <a name="execution-scheduling-options"></a>Opciones de programación de ejecución

Incluya los bits de marca opcionales en la columna tipo de la [tabla CustomAction](customaction-table.md) para especificar las opciones de programación de la ejecución. Estas opciones controlan la ejecución múltiple de acciones personalizadas. Para obtener una descripción de las opciones, vea opciones de programación de la [ejecución de acciones personalizadas](custom-action-execution-scheduling-options.md).

## <a name="in-script-execution-options"></a>Opciones de ejecución de In-Script

La acción personalizada no utiliza estas opciones.

## <a name="return-values"></a>Valores devueltos

Vea [valores devueltos de la acción personalizada](custom-action-return-values.md).

## <a name="remarks"></a>Observaciones

Si establece una [propiedad privada](private-properties.md) en la secuencia de la interfaz de usuario mediante la creación de una acción personalizada en una de las tablas de secuencia de la interfaz de usuario, esa propiedad no se establece en la secuencia de ejecución. Para establecer la propiedad en la secuencia de ejecución, también debe colocar una acción personalizada en una tabla de secuencia de ejecución. Como alternativa, puede convertir la propiedad en una [propiedad pública](public-properties.md) e incluirla en la [**propiedad SecureCustomProperties**](securecustomproperties.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[\_Acciones personalizadas](custom-actions.md)
</dt> <dt>

[Acciones personalizadas de texto con formato](formatted-text-custom-actions.md)
</dt> </dl>

 

 



