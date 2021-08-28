---
description: Windows proporciona a las aplicaciones un conjunto completo de funciones que permiten imprimir en varios dispositivos, como impresoras de rayos, trazadores vectoriales, impresoras de trama y máquinas de fax.
ms.assetid: e5c115b0-9c1e-46e7-8fb5-eddbc2c75298
title: Impresión (documentos e impresión)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6317275e60346428173bf47bdc8e9f84b7a3e523
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465662"
---
# <a name="printing-documents-and-printing"></a>Impresión (documentos e impresión)

Windows proporciona a las aplicaciones un conjunto completo de funciones que permiten imprimir en varios dispositivos, como impresoras de rayos, trazadores vectoriales, impresoras de trama y máquinas de fax.

## <a name="desktop-app-printing"></a>Impresión de aplicaciones de escritorio

Windows programadores pueden seleccionar entre varias tecnologías diferentes para imprimir desde su aplicación.




| Tecnología | Descripción | 
|------------|-------------|
| <a href="/windows/desktop/printdocs/tailored-app-printing-api">API de paquete de impresión de documentos</a><br /> | Proporciona una interfaz que permite a una aplicación acceder al paquete de impresión de documentos y administrarlo. Esta API está disponible con Windows 8 versiones posteriores de Windows.<br /> | 
| <a href="print-spooler-api.md">Print Spooler API</a><br /> | Proporciona una interfaz al colador de impresión para que las aplicaciones puedan administrar impresoras e imprimir trabajos.<br /> Las aplicaciones usan <a href="print-spooler-api.md">Print Spooler API</a> para iniciar, detener, controlar y configurar trabajos de impresión administrados por el administrador de trabajos de impresión, independientemente de si usan <a href="/windows/desktop/printdocs/tailored-app-printing-api">print document package API</a> o <a href="gdi-printing.md">GDI Print API</a> para imprimir el contenido.<br /> | 
| <a href="print-ticket-api.md">API de impresión de vales</a><br /> | Proporciona a las aplicaciones funciones para administrar y convertir vales de impresión.<br /> | 
| <a href="gdi-printing.md">API de impresión de GDI</a><br /> | Proporciona a las aplicaciones una interfaz de impresión independiente del dispositivo. <br /><blockquote>[!Note]<br />Los desarrolladores que escriben aplicaciones para Windows Vista y versiones posteriores de Windows deben considerar el uso de <a href="/previous-versions/windows/desktop/dd316976(v=vs.85)">document API XPS</a> en su aplicación.</blockquote><br /> La <a href="gdi-printing.md">API de impresión GDI</a> es adecuada para las aplicaciones que deben ejecutarse en Windows XP y versiones anteriores de Windows.<br /> | 




 

En la ilustración siguiente se proporciona una vista general de cómo se relacionan las distintas API de impresión.

![diagrama que muestra cómo una aplicación nativa de Windows puede usar las API de impresión](images/print-apis.png)

 

Las [API print document package](./tailored-app-printing-api.md)de esta sección describen el paquete de documentos de impresión y las interfaces de vista previa de impresión que puede usar con Windows 8 y versiones posteriores de Windows desktop.

Para obtener más información sobre la impresión desde aplicaciones de Windows Store escritas en JavaScript y HTML, vea Impresión (Windows Store con [JavaScript y HTML).](/previous-versions/windows/apps/hh465225(v=win.10)) Para obtener más información sobre cómo imprimir desde aplicaciones de Windows Store escritas en C#, Microsoft Visual Basic o C++ y XAML, vea [Impresión (Windows Store](/previous-versions/windows/apps/hh465196(v=win.10))con C).

> [!Note]  
> Consulte [Win32 y COM](/uwp/win32-and-com/win32-and-com-for-uwp-apps) para Windows Store (impresión y documentos) para obtener la lista de las API de impresión de aplicaciones de escritorio que también se pueden usar en Windows Store.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[XPS Document API](/previous-versions/windows/desktop/dd316976(v=vs.85))
</dt> <dt>

[Comunicaciones de impresora bidireccional (Centro de desarrollo de hardware)](/windows-hardware/drivers/print/bidirectional-communication)
</dt> </dl>

