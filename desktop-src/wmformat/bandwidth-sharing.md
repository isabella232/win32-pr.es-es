---
title: Uso compartido de ancho de banda
description: Uso compartido de ancho de banda
ms.assetid: d33f3454-d20a-4b4d-9902-dabc5b806ad6
keywords:
- Windows SDK de formato multimedia, uso compartido de ancho de banda
- Formato de sistemas avanzados (ASF), uso compartido de ancho de banda
- ASF (formato de sistemas avanzados), uso compartido de ancho de banda
- Windows SDK de formato multimedia, secuencias
- Formato de sistemas avanzados (ASF),streams
- ASF (formato de sistemas avanzados), secuencias
- uso compartido de ancho de banda, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b01ff94e82f2ce3609a93278fef30c68e1a59445eea22f68f4b0a5d92371a19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709415"
---
# <a name="bandwidth-sharing"></a>Uso compartido de ancho de banda

Puede especificar secuencias en un archivo que, cuando se toman juntas, usan menos ancho de banda que la suma de sus velocidades de bits indicadas combinadas. Al especificar el uso compartido de ancho de banda en el perfil, se aclara a la lectura de las aplicaciones que el ancho de banda disponible necesario para transmitir el archivo no es lo que podría parecer.

Ninguno de los objetos del SDK de formato multimedia de Windows cambia su comportamiento en respuesta a la información de uso compartido de ancho de banda, que se proporciona únicamente para que las aplicaciones de lectura puedan tenerla en cuenta al determinar si un archivo se puede reproducir con la entrega de ancho de banda restringido.

El uso compartido de ancho de banda se configura con un objeto de uso compartido de ancho de banda y se agrega a un perfil antes de empezar a escribir un archivo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Características del archivo ASF**](asf-file-features.md)
</dt> <dt>

[**Objeto de uso compartido de ancho de banda**](bandwidth-sharing-object.md)
</dt> <dt>

[**Interfaz IWMBandwidthSharing**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmbandwidthsharing)
</dt> <dt>

[**IWMProfile3 (interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)
</dt> <dt>

[**Uso compartido de ancho de banda**](using-bandwidth-sharing.md)
</dt> </dl>

 

 




