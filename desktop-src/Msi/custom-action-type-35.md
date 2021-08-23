---
description: Los desarrolladores de Windows Installer pueden optar por usar un tipo de acción personalizado 35 cuando las acciones estándar no son suficientes para ejecutar la instalación.
ms.assetid: b88b5f48-5353-4876-9dda-2eeda288fa4b
title: Tipo de acción personalizada 35
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a724fa5a7fc469ea688c64e5935242f088c010da02d963f2f1dc4b05f5eb5e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947973"
---
# <a name="custom-action-type-35"></a>Tipo de acción personalizada 35

Esta acción personalizada establece el directorio de instalación de una cadena de texto con formato. Para obtener más información, [vea Cambiar la ubicación de destino de un directorio.](changing-the-target-location-for-a-directory.md)

## <a name="source"></a>Source

El campo Source de la [tabla CustomAction](customaction-table.md) contiene una clave para la [tabla Directory](directory-table.md). La cadena con formato establece el directorio designado en el campo Destino mediante [**MsiSetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha). Esto establece la ruta de acceso de destino y la propiedad asociada en el valor expandido de la cadena de texto con formato en el campo Destino. No intente cambiar la ubicación de un directorio de destino durante una [instalación de mantenimiento.](maintenance-installation.md) No intente cambiar la ruta de acceso del directorio de destino si algunos componentes que usan esa ruta de acceso ya están instalados para cualquier usuario.

## <a name="type-value"></a>Valor de tipo

Incluya el siguiente valor en la columna Type de la [tabla CustomAction](customaction-table.md) para especificar el tipo numérico básico.



| Constantes                                                              | Hexadecimal | Decimal |
|------------------------------------------------------------------------|-------------|---------|
| **msidbCustomActionTypeTextData**  +  **msidbCustomActionTypeDirectory** | 0x023       | 35      |



 

## <a name="target"></a>Destino

La columna Target de la [tabla CustomAction](customaction-table.md) contiene una cadena de texto con el formato de la funcionalidad especificada en [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) (sin los especificadores de campo numéricos). Los parámetros que se van a reemplazar se incluyen entre corchetes... y pueden ser propiedades, variables de entorno (prefijo %), rutas de acceso de archivo (prefijo) o rutas de acceso de directorio de \[ \] componentes \# (prefijo $). Tenga en cuenta que las rutas de acceso de directorio siempre terminan con un separador de directorios.

## <a name="return-processing-options"></a>Opciones de procesamiento de devolución

La acción personalizada no usa estas opciones.

## <a name="execution-scheduling-options"></a>Opciones de programación de ejecución

Incluya bits de marca opcionales en la columna Tipo de la [tabla CustomAction](customaction-table.md) para especificar las opciones de programación de ejecución. Estas opciones controlan la ejecución múltiple de acciones personalizadas. Para obtener una descripción de las opciones, vea [Opciones de programación de ejecución de acciones personalizadas.](custom-action-execution-scheduling-options.md)

## <a name="in-script-execution-options"></a>In-Script de ejecución

La acción personalizada no usa estas opciones.

## <a name="return-values"></a>Valores devueltos

Vea [Valores devueltos de acciones personalizadas.](custom-action-return-values.md)

## <a name="remarks"></a>Comentarios

Si establece una [propiedad](private-properties.md) privada en la secuencia de interfaz de usuario mediante la creación de una acción personalizada en una de las tablas de secuencia de la interfaz de usuario, esa propiedad no se establece en la secuencia de ejecución. Para establecer la propiedad en la secuencia de ejecución, también debe colocar una acción personalizada en una tabla de secuencia de ejecución. Como alternativa, puede convertir la propiedad en [una propiedad pública](public-properties.md) e incluirla en la propiedad [**SecureCustomProperties**](securecustomproperties.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acciones \_ personalizadas](custom-actions.md)
</dt> <dt>

[Acciones personalizadas de texto con formato](formatted-text-custom-actions.md)
</dt> </dl>

 

 



