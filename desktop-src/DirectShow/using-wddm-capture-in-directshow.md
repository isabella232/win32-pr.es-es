---
description: Uso de la captura de WDDM en DirectShow
ms.assetid: 57ee86b0-50bc-4992-94d4-f290f83d2afc
title: Uso de la captura de WDDM en DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7926af70a3b7f1c4ba67c791d98c9928c3809b89
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126891553"
---
# <a name="using-wddm-capture-in-directshow"></a>Uso de la captura de WDDM en DirectShow

Este tema se aplica a Windows Vista y versiones posteriores.

Algunas tarjetas de vídeo tienen funcionalidad de captura de vídeo integrada. En estas tarjetas, los fotogramas de vídeo capturados se colocan en la memoria de vídeo (VRAM). Antes de Windows Vista, no había ningún mecanismo estándar para procesar los fotogramas mientras permanecía en VRAM. En su lugar, los datos tenían que copiarse en la memoria del sistema, procesarse y, a continuación, copiarse de nuevo en VRAM para mostrarse. En Windows Vista, DirectShow ahora admite un mecanismo para mantener los fotogramas de vídeo en VRAM a lo largo de la canalización de procesamiento, desde la captura hasta la presentación.

El filtro KsProxy determina si el controlador admite la captura de superficie de VRAM consultando el controlador para la propiedad KSPROPERTY \_ PREFERRED \_ CAPTURE \_ SURFACE. (Esta propiedad se documenta en la documentación Windows Driver Kit). Si el controlador admite la captura de superficie de VRAM, KsProxy asigna un tipo especial de ejemplo multimedia que contiene un puntero a una superficie de Direct3D.

A continuación, KsProxy determina si el filtro de bajada admite DirectX Video Acceleration (DXVA) 2.0, como se indica a continuación:

1.  KsProxy consulta la patilla de entrada de bajada para la **interfaz DENGETService.**
2.  Si el pin expone **ELSERVICIOGETGET,** KsProxy llama **a ALGETGetService::GetService** para la **interfaz IDirect3DDeviceManager.** El servicio identier es MR \_ VIDEO \_ ACCELERATION \_ SERVICE.

Ambas interfaces se documentan en la documentación Media Foundation SDK.

Si el filtro de nivel inferior no admite DXVA 2.0, KsProxy asigna un búfer de memoria del sistema adicional. Usa este búfer para copiar los fotogramas de vídeo de VRAM a la memoria del sistema. El método [**IMediaSample::GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) del ejemplo multimedia devuelve un puntero a este búfer de memoria del sistema.

Sin embargo, si el filtro de nivel inferior admite DXVA 2.0, KsProxy no asigna un búfer de memoria del sistema. En ese caso, el **método GetPointer** devuelve E \_ NOTIMPL. En su lugar, se espera que el filtro de nivel inferior acceda directamente a la superficie de Direct3D del ejemplo. Hay dos maneras de que el filtro de nivel inferior obtenga un puntero a la superficie, ambas equivalentes:

-   Consulte el ejemplo de la **interfaz IMFGetService** y llame **a GetService** para la **interfaz IDirect3DSurface9.** El identificador de servicio es MR \_ BUFFER \_ SERVICE.
-   Consulte el ejemplo de la [**interfaz IMediaSample2Config**](/windows/desktop/api/Strmif/nn-strmif-imediasample2config) y llame a [**IMediaSample2Config::GetSurface**](/windows/desktop/api/Strmif/nf-strmif-imediasample2config-getsurface).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Temas de captura avanzada](advanced-capture-topics.md)
</dt> </dl>

 

 



