---
title: Extensiones de unidad de datos
description: Extensiones de unidad de datos
ms.assetid: f95de189-0449-4b88-aba3-7b19f385c8fe
keywords:
- Windows Media Format SDK, extensiones de unidad de datos
- Advanced Systems Format (ASF), extensiones de unidad de datos
- ASF (formato de sistemas avanzados), extensiones de unidad de datos
- SDK de Windows Media Format, sistemas de extensión de carga
- Advanced Systems Format (ASF), sistemas de extensión de carga útil
- ASF (formato de sistemas avanzados), sistemas de extensión de carga útil
- extensiones de unidad de datos, acerca de
- extensiones de unidad de carga
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c8ed5c9db82d0002648148ca14bd7f94baa9029
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788763"
---
# <a name="data-unit-extensions"></a>Extensiones de unidad de datos

El SDK de Windows Media Format permite complementar los datos de ejemplos con *extensiones de unidad de datos*, también denominados sistemas de extensión de carga. En esta documentación se usa el término "extensiones de unidad de datos" para mantener la coherencia con los nombres de método como [**AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension). Una extensión de unidad de datos es un par nombre-valor que se adjunta al ejemplo en la sección de datos del archivo. Puede tener acceso a los datos extendidos mediante los métodos del objeto de búfer cuando el lector recupera el ejemplo.

Puede crear extensiones de unidad de datos para sus propias especificaciones, pero hay varios tipos predefinidos y compatibles con los objetos de este SDK. Estas extensiones estándar se utilizan para proporcionar datos adicionales para los nombres de archivo (en scripts y secuencias Web), datos de código de tiempo SMPTE, relación de aspecto de píxeles no cuadrado, duración y tipo de entrelazado.

Para usar las extensiones de unidad de datos, debe configurar la secuencia para aceptarlas y, a continuación, agregar extensiones a cada ejemplo de la secuencia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de archivos ASF**](asf-file-features.md)
</dt> <dt>

[**Configuración de extensiones de unidades de datos**](configuring-data-unit-extensions.md)
</dt> <dt>

[**Configuración de las extensiones de unidad de datos**](setting-data-unit-extensions.md)
</dt> </dl>

 

 




