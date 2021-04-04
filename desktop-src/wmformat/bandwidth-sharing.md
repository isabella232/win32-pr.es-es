---
title: Uso compartido de ancho de banda
description: Uso compartido de ancho de banda
ms.assetid: d33f3454-d20a-4b4d-9902-dabc5b806ad6
keywords:
- SDK de Windows Media Format, uso compartido de ancho de banda
- Advanced Systems Format (ASF), uso compartido de ancho de banda
- ASF (formato de sistemas avanzados), uso compartido de ancho de banda
- Windows Media Format SDK, secuencias
- Advanced Systems Format (ASF), streams
- ASF (formato de sistemas avanzados), secuencias
- uso compartido de ancho de banda, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2221d2fbc44654af7f12acf6e45fb85ca32b7d2b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077336"
---
# <a name="bandwidth-sharing"></a>Uso compartido de ancho de banda

Puede especificar flujos en un archivo que, cuando se tomen juntos, utilicen menos ancho de banda que la suma de las velocidades de bits indicadas. Al especificar el uso compartido del ancho de banda en el perfil, se aclara a la lectura de las aplicaciones que el ancho de banda disponible necesario para transmitir por secuencias el archivo no es lo que podría parecer.

Ninguno de los objetos del SDK de Windows Media Format cambia su comportamiento en respuesta a la información de uso compartido del ancho de banda, que se proporciona únicamente para que la lectura de las aplicaciones pueda tener en cuenta a la hora de determinar si un archivo se puede reproducir con la entrega de ancho de banda restringida.

El uso compartido de ancho de banda se configura con un objeto de uso compartido de ancho de banda y se agrega a un perfil antes de empezar a escribir un archivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características de archivos ASF**](asf-file-features.md)
</dt> <dt>

[**Objeto de uso compartido de ancho de banda**](bandwidth-sharing-object.md)
</dt> <dt>

[**Interfaz IWMBandwidthSharing**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing)
</dt> <dt>

[**Interfaz IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)
</dt> <dt>

[**Uso del uso compartido de ancho de banda**](using-bandwidth-sharing.md)
</dt> </dl>

 

 




