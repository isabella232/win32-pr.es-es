---
description: En esta sección se describen las funciones de la API de Windows Installer pueden llamar a las propiedades de la secuencia de información de resumen. Para obtener más información sobre el flujo de información de Resumen y cómo funciona con las bases de datos, vea acerca de la secuencia de información de resumen.
ms.assetid: 2c22fe52-52a9-4e3f-9482-b5e41b91b3ae
title: Usar el flujo de información de Resumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de3ece9ad336b1a88d343b859fd3881b23246c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104002012"
---
# <a name="using-the-summary-information-stream"></a>Usar el flujo de información de Resumen

En esta sección se describen las funciones de la API de Windows Installer pueden llamar a las propiedades de la secuencia de información de resumen. Para obtener más información sobre el flujo de información de Resumen y cómo funciona con las bases de datos, vea [acerca de la secuencia de información de Resumen](about-the-summary-information-stream.md).

-   Es importante recordar que el instalador contiene diferentes tipos de bases de datos y que algunas propiedades de la secuencia de información de Resumen tienen diferentes significados con distintas bases de datos. Para obtener más información, vea [descripciones de propiedades de Resumen](summary-property-descriptions.md).
-   Cuando una base de datos se abre como la salida de otra base de datos, la secuencia de información de Resumen de la base de datos de salida es realmente un reflejo de solo lectura de la base de datos original y, por tanto, no se puede cambiar. Además, no se conservará con la base de datos. Para crear o modificar la información de Resumen de la base de datos de salida, se debe cerrar y volver a abrir.

En los pasos siguientes se describe cómo utilizar las funciones de flujo de información de Resumen:

**Para usar las propiedades de la secuencia de información de Resumen**

1.  Obtener un identificador para la base de datos que contiene la secuencia de información de Resumen mediante una llamada a la función [**MsiGetSummaryInformation**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa) .
2.  Llame a la función [**MsiSummaryInfoGetPropertyCount**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertycount) para obtener el número de propiedades existentes.
3.  Llame a la función [**MsiSummaryInfoGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya) para ver una única propiedad de información de resumen.
4.  Llamar a la función [**MsiSummaryInfoSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfosetpropertya) para establecer una propiedad única
5.  Llame a la función [**MsiSummaryInfoPersist**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfopersist) para guardar la propiedad de información de resumen.
6.  Llame a la función [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) para crear la información de Resumen de una transformación existente.

[Orca.exe](orca-exe.md) y [Msiinfo.exe](msiinfo-exe.md) son herramientas que se pueden usar para editar o mostrar el flujo de información de Resumen de una base de datos. Estas herramientas solo están disponibles en los [componentes de Windows SDK para los desarrolladores de Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

También se puede tener acceso al flujo de información de Resumen mediante los siguientes métodos y propiedades de la [interfaz de automatización](automation-interface.md)de Windows Installer.

-   [**SummaryInfo. Property**](summaryinfo-summaryinfo.md)
-   [**SummaryInfo. PropertyCount**](summaryinfo-propertycount.md)
-   [**SummaryInfo. Persist**](summaryinfo-persist.md)
-   [**Instalador. SummaryInformation**](installer-summaryinformation.md)
-   [**Base de datos. SummaryInformation**](database-summaryinformation.md)
-   [**Base de datos. CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md)

El WiSumInf.vbs de archivos de VBScript se proporciona en los [componentes de Windows SDK para Windows Installer desarrolladores](platform-sdk-components-for-windows-installer-developers.md). Este script de ejemplo se puede usar para administrar la secuencia de información de Resumen de un paquete de Windows Installer. Para obtener más información acerca de WiSumInf.vbs, vea [administrar información de Resumen](manage-summary-information.md).

 

 



