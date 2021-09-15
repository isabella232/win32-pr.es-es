---
description: En estos temas se describen los documentos y las características de impresión Windows que permiten a las aplicaciones guardar, ver e imprimir.
ms.assetid: 20e56af6-9598-4d6a-a2bf-454cef8a3368
title: 'Documentos e impresión '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87d7af92af0615dcb11d2623be8f2e21ae813aa1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127248450"
---
# <a name="documents-and-printing"></a>Documentos e impresión 

En estos temas se describen los documentos y las características de impresión Windows que permiten a las aplicaciones guardar, ver e imprimir.

## <a name="in-this-section"></a>En esta sección




| Tema | Descripción | 
|-------|-------------|
| <a href="/windows/desktop/printdocs/what-s-new-for-printing-in-windows-vnext">Novedades de la impresión</a><br /> | Windows 8 admite la impresión para aplicaciones de Windows Store mediante <a href="/previous-versions/windows/apps/hh465225(v=win.10)">JavaScript</a> y HTML e impresión para aplicaciones de Windows Store mediante <a href="/previous-versions/windows/apps/hh465196(v=win.10)">C#/VB/C++</a>y XAML.<br /> Windows 8 incluye una nueva API basada en COM que proporciona compatibilidad completa con Open XPS y acceso a partes de los nuevos controladores de impresora que Windows 8 admite. Para obtener más información sobre la nueva API, consulte <a href="/windows/desktop/printdocs/tailored-app-printing-api">Print Document Package API</a>.<br /> El Windows de bandeja de entrada del controlador de impresión Windows 8 compatibilidad con un alto porcentaje de las impresoras populares.<br /> | 
| <a href="/windows/desktop/printdocs/jobbindalldocuments">Documentos XPS</a><br /> | Información sobre las firmas digitales xps de Document API de XPS.<br /><ul><li><a href="/previous-versions/windows/desktop/dd316976(v=vs.85)">XPS Document API</a><br /> XpS Document API es una API Windows que admite XPS OM. La API de documentos XPS se introdujo en Windows 7 y se puede usar en programas en modo de usuario y controladores de impresora XPSDrv.<br /></li><li><a href="/previous-versions/windows/desktop/ff819108(v=vs.85)">XPS Digital Signature API</a><br /> XpS Digital Signatures habilita la firma de documentos, la comprobación de la identidad del firmante y la indicación de si un documento XPS ha cambiado desde que se firmó.<br /></li></ul> | 
| <a href="printdocs-printing.md">Impresión</a><br /> | Información sobre las características de impresión admitidas por Windows. Estas características son:<br /><ul><li><a href="/windows/desktop/printdocs/tailored-app-printing-api">API para imprimir paquetes de documentos</a><br /> Proporciona a las aplicaciones una interfaz que permite la administración del <strong>paquete PrintDocument.</strong><br /></li><li><a href="print-spooler-api.md">Print Spooler API</a><br /> Proporciona una interfaz al colador de impresión para que las aplicaciones puedan administrar impresoras y trabajos de impresión.<br /></li><li><a href="print-ticket-api.md">API de impresión de vales</a><br /> Proporciona a las aplicaciones funciones para administrar y convertir vales de impresión.<br /></li><li><a href="gdi-printing.md">API de impresión de GDI</a><br /> Proporciona a las aplicaciones una interfaz de impresión independiente del dispositivo. <br /></li><li><p><a href="xps-printing.md">XPS Print API</a><br /> Proporciona una interfaz al colador de impresión que las aplicaciones pueden usar para enviar documentos XPS a una impresora.</p><blockquote>[!Note]<br />XpS Print API no se admite y puede modificarse o no estar disponible en el futuro. Las aplicaciones cliente deben usar <a href="/windows/desktop/printdocs/tailored-app-printing-api">la API Print Document Package en</a> su lugar.</blockquote><p><br /><br /></p></li></ul> | 
| <a href="/windows/desktop/printdocs/printschema">Esquema de impresión</a><br /> | El esquema de impresión y las tecnologías relacionadas describen las características de una impresora y especifican las preferencias de impresión de un documento para impresoras y aplicaciones de visualización. La <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">especificación de esquema de</a> impresión es un documento descargable que contiene información sobre el esquema de impresión y cómo usarlo en documentos e impresión. La información en línea que se encuentra en esta sección solo se proporciona para su información y es posible que no refleje con precisión la versión actual de la especificación <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">de esquema de impresión</a>.<br /> Consulte especificación <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">de esquema de impresión</a> para obtener la información de diseño más reciente.<br /> | 




 

## <a name="additional-resources"></a>Recursos adicionales

La [aplicación De ejemplo de impresión](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208)) muestra cómo imprimir desde una aplicación Windows Store a partir de Windows 8.

Las características descritas en esta sección son para la programación Windows nativa. Para usar características similares en la programación de .NET (administrado), [vea Windows Presentation Foundation Documentos](/previous-versions/dotnet/netframework-3.0/ms749165(v=vs.85)).

Los documentos XPS se integran en [Packaging](/previous-versions/windows/desktop/opc/packaging) API. Consulte Packaging API para obtener acceso de nivel inferior al contenido de un documento XPS.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Comunicaciones bidireccionales de impresora (Centro de desarrollo de hardware)](/windows-hardware/drivers/print/bidirectional-communication)
</dt> </dl>
