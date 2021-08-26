---
description: En esta sección se describen las funciones de la API Windows Installer pueden llamar a las propiedades del flujo de información de resumen. Para obtener más información sobre el flujo de información de resumen y cómo funciona con las bases de datos, vea Acerca de la secuencia de información de resumen.
ms.assetid: 2c22fe52-52a9-4e3f-9482-b5e41b91b3ae
title: Uso del flujo de información de resumen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a90d6be9586ab6adc469f14fea71dc1325cb19107bd8ddc634a3d0b4463c490
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996045"
---
# <a name="using-the-summary-information-stream"></a>Uso del flujo de información de resumen

En esta sección se describen las funciones de la API Windows Installer pueden llamar a las propiedades del flujo de información de resumen. Para obtener más información sobre el flujo de información de resumen y cómo funciona con las bases de datos, vea Acerca de [la secuencia de información de resumen](about-the-summary-information-stream.md).

-   Es importante recordar que el instalador contiene diferentes tipos de bases de datos y algunas propiedades del flujo de información de resumen tienen significados diferentes con bases de datos diferentes. Para obtener más información, [vea Resumen de descripciones de propiedades](summary-property-descriptions.md).
-   Cuando se abre una base de datos como salida de otra base de datos, el flujo de información de resumen de la base de datos de salida es realmente un reflejo de solo lectura de la base de datos original y, por tanto, no se puede cambiar. Además, no se conservará con la base de datos. Para crear o modificar la información de resumen de la base de datos de salida, debe cerrarse y volver a abrirse.

En los pasos siguientes se describe cómo usar las funciones de flujo de información de resumen:

**Para usar las propiedades de flujo de información de resumen**

1.  Obtenga un identificador para la base de datos que contiene el flujo de información de resumen llamando a la [**función MsiGetSummaryInformation.**](/windows/desktop/api/Msiquery/nf-msiquery-msigetsummaryinformationa)
2.  Llame a [**la función MsiSummaryInfoGetPropertyCount**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertycount) para obtener el número de propiedades existentes.
3.  Llame a [**la función MsiSummaryInfoGetProperty para**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya) ver una única propiedad de información de resumen.
4.  Llame a [**la función MsiSummaryInfoSetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfosetpropertya) para establecer una sola propiedad.
5.  Llame a [**la función MsiSummaryInfoPersist**](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfopersist) para guardar la propiedad de información de resumen.
6.  Llame a [**la función MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) para crear la información de resumen de una transformación existente.

[Orca.exe](orca-exe.md) y [Msiinfo.exe](msiinfo-exe.md) son herramientas que se pueden usar para editar o mostrar el flujo de información de resumen de una base de datos. Estas herramientas solo están disponibles en los componentes Windows [SDK para desarrolladores Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

También se puede acceder al flujo de información de resumen mediante los métodos y propiedades siguientes de la interfaz de automatización Windows instalador de [.](automation-interface.md)

-   [**SummaryInfo.Property**](summaryinfo-summaryinfo.md)
-   [**SummaryInfo.PropertyCount**](summaryinfo-propertycount.md)
-   [**SummaryInfo.Persist**](summaryinfo-persist.md)
-   [**Installer.SummaryInformation**](installer-summaryinformation.md)
-   [**Database.SummaryInformation**](database-summaryinformation.md)
-   [**Database.CreateTransformSummaryInfo**](database-createtransformsummaryinfo.md)

El archivo vbscript WiSumInf.vbs se proporciona en los componentes del SDK de [Windows para Windows desarrolladores del instalador de .](platform-sdk-components-for-windows-installer-developers.md) Este script de ejemplo se puede usar para administrar el flujo de información de resumen de un Windows Installer. Para obtener más información sobre WiSumInf.vbs, vea [Administrar información de resumen](manage-summary-information.md).

 

 



