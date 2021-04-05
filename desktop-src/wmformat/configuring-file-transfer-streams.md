---
title: Configuración de secuencias de transferencia de archivos
description: Configuración de secuencias de transferencia de archivos
ms.assetid: faed54ae-9e80-492a-9602-e726bdb3b54a
keywords:
- flujos, configurar secuencias de transferencia de archivos
- códecs, configurar secuencias de transferencia de archivos
- flujos de transferencia de archivos
- secuencias, extensiones de unidad de datos
- códecs, extensiones de unidad de datos
- extensiones de unidad de datos, secuencias de transferencia de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75fac7d2270da82f1f9e82ed9123611ae608dd3c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077353"
---
# <a name="configuring-file-transfer-streams"></a>Configuración de secuencias de transferencia de archivos

Las secuencias de transferencia de archivos no requieren ninguna configuración especial en la estructura de [**\_ \_ tipo de medio de WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) . Requieren una extensión de unidad de datos para asociar un nombre de archivo a cada ejemplo. Para enviar un nombre con ejemplos de transferencia de archivos, debe implementar un sistema de extensión de unidad de datos para la secuencia.

Para establecer una extensión de unidad de datos para la secuencia, realice los pasos siguientes:

1.  Obtenga un puntero a la interfaz [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) del objeto de configuración de la secuencia llamando a **IWMStreamConfig:: QueryInterface**.
2.  Agregue una extensión de unidad de datos para la secuencia mediante una llamada a [**IWMStreamConfig2:: AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) como se indica a continuación:
    ```C++
    hr = pStreamConfig2->AddDataUnitExtension(CLSID_WMTPropertyFileName,
                                              -1, NULL, 0);
    ```

    

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración común para todos los flujos**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configuración de tipos de flujo arbitrarios**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Secuencias de archivo**](file-streams.md)
</dt> </dl>

 

 




