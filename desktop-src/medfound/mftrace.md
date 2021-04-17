---
description: MFTrace es una herramienta para generar registros de seguimiento para aplicaciones Media Foundation.
ms.assetid: 55b421c8-e87c-4dd2-8649-93832c93f999
title: MFTrace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4a216f225141ceccf3f1357025dd069afa494d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653383"
---
# <a name="mftrace"></a>MFTrace

MFTrace es una herramienta para generar registros de seguimiento para aplicaciones Media Foundation.

## <a name="in-this-section"></a>En esta sección

-   [Usar MFTrace](using-mftrace.md)
-   [Palabras clave de MFTrace](mftrace-keywords.md)
-   [Archivo de configuración MFTrace](mftrace-configuration-file.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------------|---------------------------------------------------------------------------------------|
| Versión mínima del SDK      | Kit de desarrollo de software (SDK) de Microsoft Windows para Windows 7 y .NET Framework 4,0 |
| Sistema operativo mínimo | Windows Vista                                                                         |



 

MFTrace requiere los siguientes archivos dll, que también se proporcionan en el SDK.

-   detoured.dll
-   mfdetours.dll

El SDK proporciona versiones de 32 bits y de 64 bits de MFTrace. MFTrace no admite WOW64; para realizar el seguimiento de un proceso de 32 bits que se ejecuta en Windows de 64 bits, use la versión de 32 bits de MFTrace.

SDK-root en sistemas de 32 bits: \Archivos de Programa\windows Kits\10 SDK-root on 64 bits System: \Archivos de programa (x86) \Windows Kits\10 encontrará mftrace en <SDK-root> \Bin \<sdk-version> \<architecture>\mftrace.exe

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Herramientas de Media Foundation](media-foundation-tools.md)
</dt> </dl>

 

 



