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
ms.openlocfilehash: 75fac7d2270da82f1f9e82ed9123611ae608dd3c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251565"
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

[**Archivo Secuencias**](file-streams.md)
</dt> </dl>

 

 




