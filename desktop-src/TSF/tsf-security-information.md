---
title: Consideraciones de seguridad Text Services Framework
description: Consideraciones de seguridad Text Services Framework
ms.assetid: c1250ca0-3887-4519-888f-2ed436a39917
keywords:
- Text Services Framework (TSF), seguridad
- TSF (Text Services Framework), seguridad
- servicios de texto, seguridad
- Aplicaciones habilitadas para TSF, seguridad
- seguridad para TSF
- Text Services Framework (TSF), procedimientos recomendados
- TSF (Text Services Framework), procedimientos recomendados
- Aplicaciones habilitadas para TSF, procedimientos recomendados
- servicios de texto, procedimientos recomendados
- procedimientos recomendados para TSF
- Text Services Framework (TSF), comprobación de errores
- TSF (Text Services Framework), comprobación de errores
- Aplicaciones habilitadas para TSF, comprobación de errores
- servicios de texto, comprobación de errores
- comprobación de errores
- Text Services Framework (TSF), firmas digitales
- TSF (Text Services Framework), firmas digitales
- servicios de texto, firmas digitales
- Aplicaciones habilitadas para TSF, firmas digitales
- Firmas digitales
- Text Services Framework (TSF), llamadas LoadLibrary
- TSF (Text Services Framework),llamadas LoadLibrary
- text services,LoadLibrary calls
- Aplicaciones habilitadas para TSF, llamadas LoadLibrary
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 432418fbcb6221082083d6595aa374939bc2f4d5cf5aad145cac87444e75bdc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118873580"
---
# <a name="security-considerations-text-services-framework"></a>Consideraciones de seguridad: Text Services Framework

## <a name="best-practices-for-developing-with-tsf"></a>Procedimientos recomendados para desarrollar con TSF

-   **Firmas digitales:** Los proveedores de servicios de texto deben proporcionar firmas digitales con sus archivos ejecutables binarios. Un servicio de texto registrado tiene acceso a los subprocesos del sistema y podría exponer información que, de lo contrario, no sería accesible. Para ayudar a garantizar un funcionamiento estable y seguro, el usuario debe comprobar la firma digital de un servicio de texto antes de que el servicio de texto pueda cargarse. Consulte [Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)) (Introducción a la firma de código) para obtener el procedimiento adecuado para crear una firma digital.
-   **Comprobación de errores:** Se debe comprobar si cada llamada a método o función se ha correcto. En caso de error, se deben omitir las llamadas de función o método restantes. La mayoría de los ejemplos de código de esta documentación tienen una comprobación de errores limitada, o ninguna, para evitar ocultar el punto que se va a ilustrar. No debe pegar ejemplos de la documentación directamente en el código de producción; en su lugar, debe mejorar los ejemplos agregando su propia comprobación de errores.

-   **Llamadas LoadLibrary:** Para obtener un puntero a cualquiera de las [funciones de TSF](text-services-framework-functions.md), deberá usar [LoadLibrary](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [GetProcAddress](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress). Sin embargo, es importante seguir los procedimientos para dar formato al nombre de la ruta de acceso del archivo DLL, como se proporciona en **la documentación de LoadLibrary.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Procedimientos recomendados de seguridad](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> <dt>

[Introducción a la firma de código](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
</dt> <dt>

[Funciones de TSF](text-services-framework-functions.md)
</dt> <dt>

[LoadLibrary](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[GetProcAddress](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> </dl>

 

 