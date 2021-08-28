---
description: MFTrace es una herramienta para generar registros de seguimiento para Media Foundation aplicaciones.
ms.assetid: 55b421c8-e87c-4dd2-8649-93832c93f999
title: MFTrace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 542ac9325b33fc8f1a76394d203dbf1d27919bd6
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885226"
---
# <a name="mftrace"></a>MFTrace

MFTrace es una herramienta para generar registros de seguimiento para Media Foundation aplicaciones.

## <a name="in-this-section"></a>En esta sección

-   [Uso de MFTrace](using-mftrace.md)
-   [Palabras clave de MFTrace](mftrace-keywords.md)
-   [Archivo de configuración de MFTrace](mftrace-configuration-file.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------------|---------------------------------------------------------------------------------------|
| Versión mínima del SDK      | Kit Windows de desarrollo de software (SDK) de Microsoft Windows 7 y .NET Framework 4.0 |
| Sistema operativo mínimo | Windows Vista                                                                         |



 

MFTrace requiere los siguientes archivos DLL, que también se proporcionan en el SDK.

-   detoured.dll
-   mfdetours.dll

El SDK proporciona versiones de 32 y 64 bits de MFTrace. MFTrace no admite WOW64; para hacer un seguimiento de un proceso de 32 bits que se ejecuta Windows 64 bits, use la versión de 32 bits de MFTrace.

sdk-root en sistemas de 32 bits: \Archivos de programa\Windows Kits\10 sdk-root en un sistema de 64 bits: \Archivos de programa (x86)\Windows Kits\10 Encontrará mftrace en &lt; sdk-root &gt; \bin \<sdk-version> \<architecture>\mftrace.exe

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Media Foundation Tools](media-foundation-tools.md)
</dt> </dl>

 

 



