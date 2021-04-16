---
title: Consideraciones de seguridad marco de trabajo de servicios de texto
description: Consideraciones de seguridad marco de trabajo de servicios de texto
ms.assetid: c1250ca0-3887-4519-888f-2ed436a39917
keywords:
- Marco de trabajo de servicios de texto (TSF), seguridad
- TSF (marco de trabajo de servicios de texto), seguridad
- servicios de texto, seguridad
- Aplicaciones habilitadas para TSF, seguridad
- seguridad para TSF
- Marco de trabajo de servicios de texto (TSF), procedimientos recomendados
- TSF (marco de trabajo de servicios de texto), procedimientos recomendados
- Aplicaciones habilitadas para TSF, procedimientos recomendados
- servicios de texto, procedimientos recomendados
- prácticas recomendadas para TSF
- Marco de trabajo de servicios de texto (TSF), comprobación de errores
- TSF (marco de trabajo de servicios de texto), comprobación de errores
- Aplicaciones habilitadas para TSF, comprobación de errores
- servicios de texto, comprobación de errores
- comprobación de errores
- Text Services Framework (TSF), firmas digitales
- TSF (marco de trabajo de servicios de texto), firmas digitales
- servicios de texto, firmas digitales
- Aplicaciones habilitadas para TSF, firmas digitales
- Firmas digitales
- Text Services Framework (TSF), llamadas LoadLibrary
- TSF (marco de trabajo de servicios de texto), llamadas LoadLibrary
- servicios de texto, llamadas LoadLibrary
- Aplicaciones habilitadas para TSF, llamadas LoadLibrary
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d71966106cde0f59d39442f7e2bf9b2a216cd94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105685722"
---
# <a name="security-considerations-text-services-framework"></a>Consideraciones de seguridad: marco de trabajo de servicios de texto

## <a name="best-practices-for-developing-with-tsf"></a>Prácticas recomendadas para el desarrollo con TSF

-   **Firmas digitales:** Los proveedores de servicios de texto deben proporcionar firmas digitales con sus ejecutables binarios. Un servicio de texto registrado tiene acceso a los subprocesos del sistema y podría exponer información que de otro modo no sería accesible. Para ayudar a garantizar una operación estable y segura, el usuario debe comprobar la firma digital de un servicio de texto antes de que el servicio de texto pueda cargarse. Consulte [Introduction to Code Signing (introducción a la firma de código](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85)) ) para obtener el procedimiento adecuado para crear una firma digital.
-   **Comprobación de errores:** Se debe comprobar si se ha realizado correctamente cada llamada de método o función. En caso de error, se deben omitir las llamadas a funciones o métodos restantes. La mayoría de los ejemplos de código de esta documentación tienen una comprobación de errores limitada, o ninguno, para evitar que se oculte el punto. No debe pegar los ejemplos de la documentación directamente en el código de producción. en su lugar, debe mejorar los ejemplos agregando su propia comprobación de errores.

-   **Llamadas LoadLibrary:** Para obtener un puntero a cualquiera de las [funciones de TSF](text-services-framework-functions.md), deberá utilizar [LoadLibrary](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [GetProcAddress](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress). Sin embargo, es importante seguir los procedimientos para dar formato al nombre de la ruta de acceso del archivo DLL, como se indica en la documentación de **LoadLibrary** .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Prácticas recomendadas de seguridad](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> <dt>

[Introducción a la firma de código](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
</dt> <dt>

[Funciones de TSF](text-services-framework-functions.md)
</dt> <dt>

[LoadLibrary](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[GetProcAddress](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> </dl>

 

 