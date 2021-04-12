---
description: Describe el archivo de configuración WsdCodeGen.
ms.assetid: 6dc340db-221e-4389-ba76-9f189f91866b
title: Archivo de configuración WsdCodeGen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8c252c5361fda411e2b7eca4f906ba92085a552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155797"
---
# <a name="wsdcodegen-configuration-file"></a>Archivo de configuración WsdCodeGen

Normalmente, la herramienta WsdCodeGen genera un archivo de configuración WsdCodeGen. Puede crear archivos de configuración manualmente, pero la complejidad y la longitud del archivo normalmente excluye la codificación manual. Se recomienda usar WsdCodeGen para generar el archivo. Para obtener más información sobre la generación de archivos de configuración, consulte uso de la [Sintaxis de línea de comandos](wsdcodegen-command-line-syntax.md) [WsdCodeGen](using-wsdcodegen.md) y WsdCodeGen.

Debe inspeccionar el archivo de configuración generado y, si es necesario, modificarlo antes de usarlo para crear código fuente. El archivo de configuración generado por WsdCodeGen suele ser suficiente para la mayoría de los desarrollos de cliente.

Para usar el archivo de configuración para el desarrollo del servidor, se requieren algunas modificaciones. Si el hospedaje está habilitado (es decir, si está seleccionado el modo "todo" o "host"), modifique el contenido del elemento [**ThisModelMetadata**](thismodelmetadata.md) y sus elementos secundarios según sea necesario. Además, modifique o quite los elementos [**PnPXDeviceCategory**](/windows/desktop/WsdApi/pnpxdevicecategory), [**PnPXHardwareId**](pnpxhardwareid.md)y [**PnPXCompatibleId**](/windows/desktop/WsdApi/pnpxcompatibleid) dentro del elemento **ThisModelMetadata** o los elementos [**hospedados**](hosted.md) según sea necesario.

Un archivo de configuración consta de una secuencia de elementos que proporcionan datos de entrada para la generación de código seguidos de cualquier número de elementos de [**archivo**](file.md) que describen los archivos que se van a generar. Los datos de entrada incluyen algunas propiedades globales y referencias a los tipos que se expresan en WSDL, XSD y ensamblados administrados. Text y CDATA en los elementos de **archivo** se escriben en los archivos generados sin modificaciones. Otros elementos de los elementos de **archivo** se reemplazan en los archivos generados con código generado.

Los archivos de configuración XML deben seguir algunas reglas generales para tener el formato correcto para su uso con la utilidad generador de código. Dichos componentes son:

-   El elemento raíz de cualquier archivo de configuración es [**wsdCodeGen**](wsdcodegen.md).

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

    Sin embargo, el generador de código procesa el archivo de configuración en un solo paso y la ordenación tiene alguna relevancia. Por ejemplo, los elementos de [**archivo**](file.md) que generan código relacionado con un tipo de Puerto determinado deben aparecer después del elemento que indica al generador de código que lea el contrato de tipo de puerto.

Para obtener una lista completa de los elementos que se usan en los archivos de configuración de WsdCodeGen, consulte [referencia XML del archivo de configuración de WsdCodeGen](wsdcodegen-configuration-file-xml-reference.md).

Los archivos de configuración de ejemplo se incluyen con el Windows SDK. Para obtener más información, vea [ejemplos de WSDAPI](wsdapi-samples.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de WsdCodeGen](about-wsdcodegen.md)
</dt> <dt>

[Ejemplos de WSDAPI](wsdapi-samples.md)
</dt> </dl>

 

 
