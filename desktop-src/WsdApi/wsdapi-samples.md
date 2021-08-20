---
description: Hay dos ejemplos de WSDAPI incluidos con el SDK Windows para Windows Server 2008.
ms.assetid: 156b79ef-1f05-4ef1-9df9-81fe81c73ca7
title: Ejemplos de WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06cf4c1ff36195e667c55d9fb5206c0cee2afcf15d1bad7f0139911b3f702a37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117919962"
---
# <a name="wsdapi-samples"></a>Ejemplos de WSDAPI

Hay dos ejemplos de WSDAPI incluidos con el SDK Windows para Windows Server 2008. El código fuente de los ejemplos se puede encontrar en <Windows SDK Install Folder> \\ Samples Web \\ \\ WSDAPI (Ejemplos de WSDAPI web). Esta versión del SDK está disponible en el Centro [de descarga.](https://www.microsoft.com/downloads/details.aspx?FamilyID=f26b1aa4-741a-433a-9be5-fa919850bdbf) Los ejemplos no están disponibles en el SDK Windows Vista.

El ejemplo de oferta de acciones (ubicado en <Windows SDK Install Folder> \\ Samples Web \\ \\ WSDAPI \\ StockQuote) muestra un servicio con funcionalidad de mensajería básica. El ejemplo de servicio de archivos (ubicado en <Windows SDK Install Folder> \\ Samples Web \\ \\ WSDAPI FileService) muestra un servicio con funcionalidad avanzada, como mensajería asincrónica, datos \\ adjuntos y eventos.

Ambos ejemplos incluyen los siguientes tipos de archivos.

-   Archivos WSDL que contienen las descripciones del servicio.
-   [Archivos de configuración WsdCodeGen usados](wsdcodegen-configuration-file.md) para generar código WSDAPI.
-   Archivos de código fuente y encabezado de C++ generados.
-   Archivos de implementación de cliente y servicio.
-   Visual Studio archivos de proyecto y solución.

Ambos ejemplos implementan hosts de dispositivo [**(IWSDDeviceHost),**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost)servidores proxy de dispositivo [**(IWSDDeviceProxy)**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy)y servidores proxy de servicio [**(IWSDServiceProxy).**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdserviceproxy) Además, el ejemplo de servicio de archivos muestra el uso de mensajería asincrónica ([**IWSDAsyncCallback**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasynccallback), [**IWSDAsyncResult),**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdasyncresult)datos adjuntos ([**IWSDInboundAttachment**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdinboundattachment), [**IWSDOutboundAttachment**](/windows/desktop/api/WsdAttachment/nn-wsdattachment-iwsdoutboundattachment)) y eventos.

Los archivos FileServiceContract.vcproj y StockQuoteContract.vcproj incluidos con los ejemplos llaman a [WsdCodeGen](web-services-for-devices-code-generator.md) para generar archivos de encabezado y origen de C++ a partir del archivo WSDL especificado en el archivo de configuración WsdCodeGen. Esto significa que si se cambia el archivo de configuración WSDL o WsdCodeGen de ejemplo y se recompila el proyecto de ejemplo, WsdCodeGen genera automáticamente nuevos archivos de encabezado y origen que reflejan los cambios. Este es el método preferido para compilar aplicaciones WSDAPI. Normalmente, se llama a WsdCodeGen desde la línea de comandos. Abra el archivo .vcproj correspondiente para ver las llamadas de línea de comandos \* de WsdCodeGen de ejemplo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desarrollo de aplicaciones WSD en Windows](wsd-application-development-on-windows.md)
</dt> </dl>

 

 



