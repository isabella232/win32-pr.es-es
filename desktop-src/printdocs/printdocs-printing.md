---
description: Windows proporciona a las aplicaciones un conjunto completo de funciones que permiten la impresión en varios dispositivos, como impresoras láser, trazadores vectoriales, impresoras de tramas y equipos de fax.
ms.assetid: e5c115b0-9c1e-46e7-8fb5-eddbc2c75298
title: Impresión (documentos e impresión)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 607e845ffc525701489a53c2a6b4628eceb5840d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716339"
---
# <a name="printing-documents-and-printing"></a>Impresión (documentos e impresión)

Windows proporciona a las aplicaciones un conjunto completo de funciones que permiten la impresión en varios dispositivos, como impresoras láser, trazadores vectoriales, impresoras de tramas y equipos de fax.

## <a name="desktop-app-printing"></a>Impresión de aplicaciones de escritorio

Los programadores de Windows pueden seleccionar entre varias tecnologías diferentes para imprimir desde su aplicación.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Technology</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/printdocs/tailored-app-printing-api">Print Document Package API</a><br/></td>
<td>Proporciona una interfaz que permite a una aplicación tener acceso al paquete de documentos de impresión y administrarlo. Esta API está disponible con Windows 8 y versiones posteriores de Windows.<br/></td>
</tr>
<tr class="even">
<td><a href="print-spooler-api.md">API del administrador de trabajos de impresión</a><br/></td>
<td>Proporciona una interfaz al administrador de trabajos de impresión para que las aplicaciones puedan administrar impresoras y trabajos de impresión.<br/> Las aplicaciones usan la <a href="print-spooler-api.md">API del administrador de trabajos de impresión</a> para iniciar, detener, controlar y configurar los trabajos de impresión administrados por el administrador de trabajos de impresión, tanto si usan la API de impresión de paquetes de <a href="/windows/desktop/printdocs/tailored-app-printing-api">documentos</a> como la API de <a href="gdi-printing.md">impresión de GDI</a> para imprimir el contenido.<br/></td>
</tr>
<tr class="odd">
<td><a href="print-ticket-api.md">Print ticket API</a><br/></td>
<td>Proporciona a las aplicaciones funciones para administrar y convertir los vales de impresión.<br/></td>
</tr>
<tr class="even">
<td><a href="gdi-printing.md">API de impresión GDI</a><br/></td>
<td>Proporciona a las aplicaciones una interfaz de impresión independiente del dispositivo. <br/>
<blockquote>
[!Note]<br />
Los desarrolladores que escriben aplicaciones para Windows Vista y versiones posteriores de Windows deben considerar el uso de la <a href="/previous-versions/windows/desktop/dd316976(v=vs.85)">API de documentos XPS</a> en su aplicación.
</blockquote>
<br/> La <a href="gdi-printing.md">API de impresión de GDI</a> es adecuada para las aplicaciones que se deben ejecutar en Windows XP y versiones anteriores de Windows.<br/></td>
</tr>
</tbody>
</table>



 

En la ilustración siguiente se proporciona una vista de alto nivel de cómo se relacionan las diferentes API de impresión.

![un diagrama que muestra cómo una aplicación nativa de Windows puede usar las API de impresión](images/print-apis.png)

 

En la [API de impresión de paquetes de documentos](./tailored-app-printing-api.md)de esta sección se describen las interfaces de impresión de paquetes y de vista previa de impresión que se pueden usar con Windows 8 y versiones posteriores del escritorio de Windows.

Para obtener más información sobre la impresión desde aplicaciones de la tienda Windows escritas en JavaScript y HTML, consulta [impresión (aplicaciones de la tienda Windows con JavaScript y HTML)](/previous-versions/windows/apps/hh465225(v=win.10)). Para obtener más información sobre la impresión desde aplicaciones de la tienda Windows escritas en C#, Microsoft Visual Basic o C++ y XAML, consulta [impresión (aplicaciones de la tienda Windows con C)](/previous-versions/windows/apps/hh465196(v=win.10)).

> [!Note]  
> Vea [Win32 y com para aplicaciones de la tienda Windows (impresión y documentos)](/uwp/win32-and-com/win32-and-com-for-uwp-apps) para ver la lista de las API de impresión de aplicaciones de escritorio que también se pueden usar en aplicaciones de la tienda Windows.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[API de documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85))
</dt> <dt>

[Comunicaciones de impresora bidireccional (centro de desarrollo de hardware)](/windows-hardware/drivers/print/bidirectional-communication)
</dt> </dl>

