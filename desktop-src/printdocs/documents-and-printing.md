---
description: En estos temas se describen los documentos y las características de impresión de Windows que permiten a las aplicaciones guardar, ver e imprimir.
ms.assetid: 20e56af6-9598-4d6a-a2bf-454cef8a3368
title: 'Documentos e impresión '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 19b23ae7040586d550c47f3fedc59104d83fe818
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105678663"
---
# <a name="documents-and-printing"></a>Documentos e impresión 

En estos temas se describen los documentos y las características de impresión de Windows que permiten a las aplicaciones guardar, ver e imprimir.

## <a name="in-this-section"></a>En esta sección



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tema</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/printdocs/what-s-new-for-printing-in-windows-vnext">Novedades de la impresión</a><br/></td>
<td>Windows 8 admite la <a href="/previous-versions/windows/apps/hh465225(v=win.10)">impresión en aplicaciones de la tienda Windows con JavaScript y HTML</a> , e <a href="/previous-versions/windows/apps/hh465196(v=win.10)">impresión para aplicaciones de la tienda Windows con C#/VB/C + + y XAML</a>.<br/> Windows 8 también incluye una nueva API basada en COM que proporciona compatibilidad total con Open XPS y acceso a partes de los nuevos controladores de impresora que admite Windows 8. Para obtener más información sobre la nueva API, consulte <a href="/windows/desktop/printdocs/tailored-app-printing-api">Print Document Package API</a>.<br/> El programa de bandeja de entrada del controlador de impresión de Windows se asegura de que Windows 8 incluye compatibilidad con un porcentaje alto de las impresoras conocidas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/printdocs/jobbindalldocuments">Documentos XPS</a><br/></td>
<td>Información sobre las firmas digitales XPS en la API de documentos XPS.<br/>
<ul>
<li><a href="/previous-versions/windows/desktop/dd316976(v=vs.85)">API de documento XPS</a><br/> La API de documento XPS es una API nativa de Windows que admite el OM XPS. La API de documento XPS se presentó en Windows 7 y se puede usar en programas de modo de usuario y controladores de impresora XPSDrv.<br/></li>
<li><a href="/previous-versions/windows/desktop/ff819108(v=vs.85)">API de firma digital XPS</a><br/> Las firmas digitales XPS permiten firmar documentos, comprobar la identidad del firmante e indicar si un documento XPS ha cambiado desde que se firmó.<br/></li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="printdocs-printing.md">Impresión</a><br/></td>
<td>Información acerca de las características de impresión compatibles con Windows. Estas características son:<br/>
<ul>
<li><a href="/windows/desktop/printdocs/tailored-app-printing-api">Print Document Package API</a><br/> Proporciona aplicaciones con una interfaz que permite la administración del paquete <strong>PrintDocument</strong> .<br/></li>
<li><a href="print-spooler-api.md">API del administrador de trabajos de impresión</a><br/> Proporciona una interfaz al administrador de trabajos de impresión para que las aplicaciones puedan administrar impresoras y trabajos de impresión.<br/></li>
<li><a href="print-ticket-api.md">Print ticket API</a><br/> Proporciona a las aplicaciones funciones para administrar y convertir los vales de impresión.<br/></li>
<li><a href="gdi-printing.md">API de impresión GDI</a><br/> Proporciona a las aplicaciones una interfaz de impresión independiente del dispositivo. <br/></li>
<li><p><a href="xps-printing.md">API de impresión XPS</a><br/> Proporciona una interfaz para el administrador de trabajos de impresión que las aplicaciones pueden utilizar para enviar documentos XPS a una impresora.</p>
<blockquote>
[!Note]<br />
La API de impresión XPS no es compatible y puede modificarse o no estar disponible en el futuro. En su lugar, las aplicaciones cliente deben usar la <a href="/windows/desktop/printdocs/tailored-app-printing-api">API Print Document Package</a> .
</blockquote>
<p><br/> <br/></p></li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/printdocs/printschema">Imprimir esquema</a><br/></td>
<td>El esquema de impresión y las tecnologías relacionadas describen las características de una impresora y especifican las preferencias de impresión de un documento para las impresoras y para ver las aplicaciones. La <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">especificación del esquema de impresión</a> es un documento descargable que contiene información sobre el esquema de impresión y cómo se usa en los documentos y la impresión. La información en línea que se encuentra en esta sección se proporciona solo para su información y es posible que no refleje con precisión la versión actual de la <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">especificación del esquema de impresión</a>.<br/> Consulte la <a href="https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip">especificación del esquema de impresión</a> para obtener la información de diseño más actual.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="additional-resources"></a>Recursos adicionales

En la [aplicación de ejemplo de impresión](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Print%20sample%20(Windows%208)) de ejemplo se muestra cómo imprimir desde una aplicación de la tienda Windows a partir de Windows 8.

Las características descritas en esta sección son para la programación nativa de Windows. Para usar características similares en la programación de .NET (administrada), consulte [documentos de Windows Presentation Foundation](/previous-versions/dotnet/netframework-3.0/ms749165(v=vs.85)).

Los documentos XPS se basan en la API de [empaquetado](/previous-versions/windows/desktop/opc/packaging) . Vea la API de empaquetado para obtener un acceso de nivel inferior al contenido de un documento XPS.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Comunicaciones de impresora bidireccional (centro de desarrollo de hardware)](/windows-hardware/drivers/print/bidirectional-communication)
</dt> </dl>
