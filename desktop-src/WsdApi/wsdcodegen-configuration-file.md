---
description: Describe el archivo de configuración WsdCodeGen.
ms.assetid: 6dc340db-221e-4389-ba76-9f189f91866b
title: Archivo de configuración WsdCodeGen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc9fcb4b10108b2c831ec005abaf7ce5e47904d37cc05b226fb8cfce43c5bb9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855915"
---
# <a name="wsdcodegen-configuration-file"></a>Archivo de configuración WsdCodeGen

Normalmente, la herramienta WsdCodeGen genera un archivo de configuración WsdCodeGen. Puede crear archivos de configuración manualmente, pero la complejidad y la longitud del archivo suelen impedir la codificación manual. Se recomienda encarecidamente usar WsdCodeGen para generar el archivo. Para obtener más información sobre cómo generar archivos de configuración, vea [Using WsdCodeGen](using-wsdcodegen.md) and [WsdCodeGen Command Line Syntax](wsdcodegen-command-line-syntax.md).

Debe inspeccionar el archivo de configuración generado y, si es necesario, modificarlo antes de usarlo para crear código fuente. El archivo de configuración generado por WsdCodeGen suele ser suficiente para la mayoría del desarrollo de cliente.

Para usar el archivo de configuración para el desarrollo del servidor, se requieren algunas modificaciones. Si el hospedaje está habilitado (es decir, si está seleccionado el modo "all" o "host"), modifique el contenido del elemento [**ThisModelMetadata**](thismodelmetadata.md) y sus elementos secundarios según sea necesario. Además, modifique o quite los elementos [**PnPXDeviceCategory**](/windows/desktop/WsdApi/pnpxdevicecategory), [**PnPXHardwareId**](pnpxhardwareid.md)y [**PnPXCompatibleId**](/windows/desktop/WsdApi/pnpxcompatibleid) dentro del elemento **ThisModelMetadata** o los elementos [**Hosted**](hosted.md) según sea necesario.

Un archivo de configuración consta de una secuencia de elementos que [](file.md) proporcionan datos de entrada para la generación de código seguidos de cualquier número de elementos de archivo que describen los archivos que se generarán. Los datos de entrada incluyen algunas propiedades globales y referencias a tipos expresados en WSDL, XSD y ensamblados administrados. El texto y CDATA de **los elementos** de archivo se escriben en los archivos generados sin modificaciones. Otros elementos de **los elementos de** archivo se reemplazan en los archivos generados por código generado.

Los archivos de configuración XML deben seguir algunas reglas generales para que el formato se pueda usar correctamente con la utilidad del generador de código. Estos son:

-   El elemento raíz de cualquier archivo de configuración [**es wsdCodeGen.**](wsdcodegen.md)

-   Los elementos que contienen tipos de datos simples son intercambiables con atributos. Por ejemplo:

    ``` syntax
    <wsdCodeGen>
        <layerNumber>1</layerNumber>
    </wsdCodeGen>
    ```

    equivale a:

    ``` syntax
    <wsdCodeGen layerNumber="1"/>
    ```

-   En general, no hay ninguna restricción en el orden de los elementos. Por ejemplo:

    ``` syntax
    <wsdCodeGen>
        <layerNumber>1</layerNumber>
        <layerPrefix>MEDIA_</layerPrefix>
    </wsdCodeGen>
    ```

    equivale a:

    ``` syntax
    <wsdCodeGen>
        <layerPrefix>MEDIA_</layerPrefix>
        <layerNumber>1</layerNumber>
    </wsdCodeGen>
    ```

    Sin embargo, el generador de código procesa el archivo de configuración en un solo paso y la ordenación tiene cierta relevancia. Por ejemplo, [**los elementos de**](file.md) archivo que generan código relacionado con un tipo de puerto determinado deben producirse después del elemento que indica al generador de código que lea el contrato de tipo de puerto.

Para obtener una lista completa de los elementos usados en los archivos de configuración de WsdCodeGen, vea Referencia XML del archivo [de configuración WsdCodeGen](wsdcodegen-configuration-file-xml-reference.md).

Los archivos de configuración de ejemplo se incluyen con Windows SDK. Para obtener más información, vea [Ejemplos de WSDAPI.](wsdapi-samples.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de WsdCodeGen](about-wsdcodegen.md)
</dt> <dt>

[Ejemplos de WSDAPI](wsdapi-samples.md)
</dt> </dl>

 

 
