---
description: En esta sección se describen las tecnologías de documentos compatibles con Microsoft Windows.
ms.assetid: 14ae2c97-8596-46db-a55c-ef706d2cd00b
title: Documentos XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa96324014d00a2a9fc106347fbeafe9842dedd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707234"
---
# <a name="xps-documents"></a>Documentos XPS

En esta sección se describen las tecnologías de documentos compatibles con Microsoft Windows.

-   [Elección de una tecnología de documentos](#choosing-a-document-technology)
-   [En esta sección](#in-this-section)
-   [Herramientas de documento XPS](#xps-document-tools)
-   [Temas relacionados](#related-topics)


## <a name="choosing-a-document-technology"></a>Elección de una tecnología de documentos

Microsoft proporciona varias tecnologías de documentos diferentes para admitir una gran variedad de aplicaciones de documentos:

-   **XPS y OpenXPS**

    XPS y OpenXPS se admiten en Windows 8 y versiones posteriores de Windows. Vea el diagrama anterior para determinar el escenario de uso correcto para XPS y OpenXPS. Para obtener más información acerca de estas tecnologías de documentos, consulte [Open XML Paper Specification (OpenXPS)](https://www.ecma-international.org/publications/standards/Ecma-388.htm).

    En el caso de usar OpenXPS con Windows 8 y Windows Server 2012, la compatibilidad solo se proporciona a través de la [API de documento XPS](documents-xps.md)

    Si necesita realizar la conversión entre Microsoft XPS (MSXPS) y OpenXPS, Microsoft ha proporcionado una herramienta (XPSConverter.exe) que le permite convertir documentos con formato MSXPS al formato OpenXPS y viceversa. La herramienta forma parte de Windows Driver Kit (WDK). Para descargar el WDK, consulte [Cómo obtener el WDK](/windows-hardware/drivers/download-the-wdk).

    Y para obtener más información sobre OpenXPS y Windows 8, consulte [compatibilidad con OpenXPS en Windows](/windows-hardware/drivers/print/driver-support-for-openxps).

-   **API de documento XPS**

    La API de documento XPS es una API nativa de Windows que admite el OM XPS. La API de documento XPS se presentó en Windows 7 y se puede usar en programas de modo de usuario y controladores de impresora XPSDrv.

    Para obtener más información, consulte la API de documento XPS y la [API de firma digital XPS](xps-digital-signatures.md).

    \*También se admite la API de documento XPS en Windows Vista con Service Pack 2 (SP2) con la actualización de la plataforma para Windows Vista y Windows Server 2008 con SP2 mediante la actualización de la plataforma para Windows Server 2008. Para obtener más información acerca de la actualización de la plataforma para Windows Vista o la actualización de la plataforma para Windows Server 2008, consulte [actualización de la plataforma para Windows Vista](/windows/desktop/win7ip/platform-update-for-windows-vista-portal) .

-   **.NET Framework**

    .NET Framework proporciona compatibilidad con documentos XPS para programas de código administrado en modo de usuario.

    .NET Framework 3,0 es compatible con Windows XP con Service Pack 2 (SP2) y versiones posteriores de los sistemas operativos de cliente de Windows, y en Windows Server 2003 con Service Pack 2 (SP2) y versiones posteriores de los sistemas operativos Windows Server.

    .NET Framework 3,5 es compatible con las versiones de Windows XP de los sistemas operativos de cliente de Windows y en Windows Server 2003 y versiones posteriores de los sistemas operativos Windows Server.

    > [!Note]  
    > Se recomienda el uso de .NET Framework para crear documentos XPS solo en aplicaciones cliente, no en aplicaciones de servidor a menos que la aplicación se cierre periódicamente, como si fuera una aplicación cliente.

     

    Para obtener más información sobre la compatibilidad de documentos en .NET Framework, vea [Windows Presentation Foundation Documents](/previous-versions/dotnet/netframework-3.0/ms749165(v=vs.85)).

> [!Note]  
> Para trabajar con documentos XPS en un programa, use la API de documento XPS nativo o la .NET Framework; no se admite el uso simultáneo de ambos en el mismo programa.

 

## <a name="in-this-section"></a>En esta sección

En esta sección se describen las tecnologías nativas de documentos de Windows compatibles con Microsoft Windows.



|                                                                    |                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [API de documento XPS](documents-xps.md)<br/>                   | Proporciona un formato de confianza para las notas electrónicas.<br/> La API de documentos XPS que se describe en esta sección proporciona a los programas y controladores de impresión XPSDrv acceso al contenido y los metadatos de un documento XPS.<br/> |
| [API de firma digital XPS](xps-digital-signatures.md)<br/> | Habilita la firma de documentos, la comprobación de la identidad del firmante y la indicación de si un documento XPS ha cambiado desde que se firmó.<br/>                                                                          |
| [Glosario de documentos XPS](xpsapi-glossary.md)<br/>           | Definiciones de términos usados por la [API de documento XPS](documents-xps.md) y la [API de firma digital XPS](xps-digital-signatures.md).<br/>                                                                              |



 

## <a name="xps-document-tools"></a>Herramientas de documento XPS

Las siguientes herramientas están disponibles para ayudarle con las pruebas y la solución de problemas de archivos de documentos XPS.

-   [IsXPS](/previous-versions/aa348104(v=vs.110))

    Prueba la conformidad de un archivo con XML Paper Specification (XPS) y la especificación de convenciones de empaquetado abierto (OPC).

-   [XpsAnalyzer](/windows-hardware/drivers/devtest/xpsanalyzer)

    Herramienta de símbolo del sistema que analiza los archivos de documento XPS para la compatibilidad con la especificación XPS 1,0.

-   [PTConform](/previous-versions/dd327476(v=msdn.10))

    Herramienta que comprueba la validez de los documentos PrintTicket y PrintCapabilities.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[API de impresión XPS](./printing-with-the-xpsprint-api.md)
</dt> <dt>

[Packaging](/previous-versions/windows/desktop/opc/packaging)
</dt> <dt>

[Impresión](./printdocs-printing.md)
</dt> <dt>
  
[Imprimir programa de ejemplo](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208))
</dt> </dl>

 

