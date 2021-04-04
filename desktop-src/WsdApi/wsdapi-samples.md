---
description: Hay dos ejemplos de WSDAPI incluidos en el Windows SDK para Windows Server 2008.
ms.assetid: 156b79ef-1f05-4ef1-9df9-81fe81c73ca7
title: Ejemplos de WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed088c43f9617da062d5e4fb4f0343f74e3bcbc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812368"
---
# <a name="wsdapi-samples"></a>Ejemplos de WSDAPI

Hay dos ejemplos de WSDAPI incluidos en el Windows SDK para Windows Server 2008. El código fuente de los ejemplos se puede encontrar en <Windows SDK Install Folder> \\ ejemplos \\ Web \\ WSDAPI. Esta versión del SDK está disponible en el [centro de descarga](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf). Los ejemplos no están disponibles en el SDK de Windows Vista.

El ejemplo stock quote (que se encuentra en <Windows SDK Install Folder> \\ Samples \\ Web \\ WSDAPI \\ StockQuote) muestra un servicio con funcionalidad básica de mensajería. El ejemplo de servicio de archivo ( <Windows SDK Install Folder> \\ que se encuentra en ejemplos \\ Web \\ WSDAPI \\ FileService) muestra un servicio con funcionalidad avanzada, como mensajería asincrónica, datos adjuntos y eventos.

Ambos ejemplos incluyen los siguientes tipos de archivos.

-   Archivos WSDL que contienen las descripciones del servicio.
-   [Archivos de configuración de WsdCodeGen](wsdcodegen-configuration-file.md) que se usan para generar código WSDAPI.
-   Archivos de encabezado y código fuente de C++ generados.
-   Archivos de implementación de cliente y servicio.
-   Archivos de proyecto y de solución de Visual Studio.

Ambos ejemplos implementan hosts de dispositivo ([**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost)), proxy de dispositivo ([**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy)) y proxy de servicio ([**IWSDServiceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdserviceproxy)). Además, el ejemplo de servicio de archivo muestra el uso de mensajería asincrónica ([**IWSDAsyncCallback**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasynccallback), [**IWSDAsyncResult**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasyncresult)), datos adjuntos ([**IWSDInboundAttachment**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdinboundattachment), [**IWSDOutboundAttachment**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdoutboundattachment)) y eventos.

Los archivos FileServiceContract. vcproj y StockQuoteContract. vcproj incluidos con los ejemplos llaman a [WsdCodeGen](web-services-for-devices-code-generator.md) para generar el encabezado y los archivos de código fuente de C++ a partir del archivo WSDL especificado en el archivo de configuración de WsdCodeGen. Esto significa que, si se cambia el archivo de configuración WSDL o WsdCodeGen de ejemplo y se vuelve a generar el proyecto de ejemplo, WsdCodeGen genera automáticamente nuevos archivos de encabezado y de origen que reflejan los cambios. Este es el método preferido para compilar aplicaciones de WSDAPI. Normalmente, se llama a WsdCodeGen desde la línea de comandos. Abra el \* archivo. vcproj pertinente para ver las llamadas de la línea de comandos de WsdCodeGen de ejemplo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desarrollo de aplicaciones WSD en Windows](wsd-application-development-on-windows.md)
</dt> </dl>

 

 



