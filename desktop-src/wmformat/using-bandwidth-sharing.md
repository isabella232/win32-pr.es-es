---
title: Uso compartido de ancho de banda
description: Uso compartido de ancho de banda
ms.assetid: 1df61a3a-d34a-447e-a7ee-d5d409e7c4fa
keywords:
- Windows SDK de formato multimedia, uso compartido de ancho de banda
- uso compartido de ancho de banda, acerca de
- perfiles, uso compartido de ancho de banda
- streams,bandwidth sharing
- uso compartido de ancho de banda, interfaz IWMProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 298c690b484a8b4b5990aacd5d525867da8923c0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572141"
---
# <a name="using-bandwidth-sharing"></a>Uso compartido de ancho de banda

Puede usar objetos de uso compartido de ancho de banda para especificar que determinadas secuencias, cuando se combinan, no usarán más ancho de banda del especificado. El escritor no genera ni comprueba la información de un objeto de uso compartido de ancho de banda ni la utiliza el lector para nada.

Cuando se escribe un archivo que tiene información de uso compartido de ancho de banda en su perfil, los datos se almacenan en su sección de encabezado. Puede usar la interfaz [**IWMProfile**](iwmprofile.md) en el lector para comprobar la información de uso compartido de ancho de banda cuando se reproduce el archivo.

Cada objeto de uso compartido de ancho de banda se define mediante dos configuraciones. En primer lugar, es el ancho de banda, definido por un ancho de banda y una ventana de búfer. La segunda configuración es un tipo de uso compartido de ancho de banda, que puede ser exclusivo o parcial. El uso compartido de ancho de banda exclusivo significa que las secuencias constituyentes se reproducen de una en una, mientras que parcialmente significa que las secuencias se entregan simultáneamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMProfile (interfaz)**](iwmprofile.md)
</dt> <dt>

[**IWMProfile3::AddBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-addbandwidthsharing)
</dt> <dt>

[**IWMProfile3::CreateNewBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-createnewbandwidthsharing)
</dt> <dt>

[**IWMProfile3::GetBandwidthSharing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharing)
</dt> <dt>

[**IWMProfile3::GetBandwidthSharingCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile3-getbandwidthsharingcount)
</dt> <dt>

[**Trabajar con perfiles**](working-with-profiles.md)
</dt> </dl>

 

 




