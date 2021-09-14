---
title: Extensiones de unidad de datos
description: Extensiones de unidad de datos
ms.assetid: f95de189-0449-4b88-aba3-7b19f385c8fe
keywords:
- Windows SDK de formato multimedia, extensiones de unidad de datos
- Formato de sistemas avanzados (ASF), extensiones de unidad de datos
- ASF (formato de sistemas avanzados), extensiones de unidad de datos
- Windows SDK de formato multimedia, sistemas de extensión de carga
- Advanced Systems Format (ASF), sistemas de extensión de carga
- ASF (formato de sistemas avanzados), sistemas de extensión de carga
- extensiones de unidad de datos, acerca de
- extensiones de unidad de carga
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c8ed5c9db82d0002648148ca14bd7f94baa9029
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256341"
---
# <a name="data-unit-extensions"></a>Extensiones de unidad de datos

El SDK Windows Media Format le permite complementar los datos en ejemplos con extensiones de unidad de datos, también *denominadas* sistemas de extensión de carga. En esta documentación se usa el término "extensiones de unidad de datos" para mantener la coherencia con nombres de método como [**AddDataUnitExtension.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) Una extensión de unidad de datos es un par nombre-valor que está asociado al ejemplo en la sección de datos del archivo. Puede acceder a los datos extendidos mediante métodos del objeto de búfer cuando el lector recupera el ejemplo.

Puede crear extensiones de unidad de datos según sus propias especificaciones, pero varios tipos están predefinidos y admitidos por los objetos de este SDK. Estas extensiones estándar se usan para proporcionar datos adicionales para nombres de archivo (en secuencias web y de script), datos de código de tiempo SMPTE, relación de aspecto de píxeles no cuadrados, duración y tipo de entrelazado.

Para usar extensiones de unidad de datos, debe configurar la secuencia para que las acepte y, a continuación, agregar extensiones a cada ejemplo para esa secuencia.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características del archivo ASF**](asf-file-features.md)
</dt> <dt>

[**Configuración de extensiones de unidades de datos**](configuring-data-unit-extensions.md)
</dt> <dt>

[**Establecer extensiones de unidad de datos**](setting-data-unit-extensions.md)
</dt> </dl>

 

 




