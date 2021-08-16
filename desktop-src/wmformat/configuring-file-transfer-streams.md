---
title: Configuración de la transferencia de archivos Secuencias
description: Configuración de la transferencia de archivos Secuencias
ms.assetid: faed54ae-9e80-492a-9602-e726bdb3b54a
keywords:
- streams,configuring file transfer streams
- códecs, configuración de flujos de transferencia de archivos
- flujos de transferencia de archivos
- streams,data unit extensions
- códecs, extensiones de unidad de datos
- extensiones de unidad de datos, flujos de transferencia de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c0be95c9760a02275e223f56785149f6867d4aaf2462d07d158991b3cd21c01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117849068"
---
# <a name="configuring-file-transfer-streams"></a>Configuración de la transferencia de archivos Secuencias

Los flujos de transferencia de archivos no requieren ninguna configuración especial en la [**estructura \_ WM MEDIA \_ TYPE.**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) Requieren una extensión de unidad de datos para asociar un nombre de archivo a cada ejemplo. Para enviar un nombre con ejemplos de transferencia de archivos, debe implementar un sistema de extensión de unidad de datos para la secuencia.

Para establecer una extensión de unidad de datos para la secuencia, realice los pasos siguientes:

1.  Obtenga un puntero a la [**interfaz IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) del objeto de configuración de flujo llamando a **IWMStreamConfig::QueryInterface**.
2.  Agregue una extensión de unidad de datos para la secuencia mediante una llamada a [**IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) como se muestra a continuación:
    ```C++
    hr = pStreamConfig2->AddDataUnitExtension(CLSID_WMTPropertyFileName,
                                              -1, NULL, 0);
    ```

    

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Configuración común a todas las Secuencias**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configuración de tipos de secuencia arbitrarios**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Archivos Secuencias**](file-streams.md)
</dt> </dl>

 

 




