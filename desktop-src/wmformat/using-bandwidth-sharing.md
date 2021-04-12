---
title: Uso del uso compartido de ancho de banda
description: Uso del uso compartido de ancho de banda
ms.assetid: 1df61a3a-d34a-447e-a7ee-d5d409e7c4fa
keywords:
- SDK de Windows Media Format, uso compartido de ancho de banda
- uso compartido de ancho de banda, acerca de
- perfiles, uso compartido de ancho de banda
- flujos, uso compartido de ancho de banda
- uso compartido de ancho de banda, interfaz IWMProfile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 298c690b484a8b4b5990aacd5d525867da8923c0
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104420457"
---
# <a name="using-bandwidth-sharing"></a>Uso del uso compartido de ancho de banda

Puede usar objetos de uso compartido de ancho de banda para especificar que determinados flujos, cuando se combinan, no utilicen más ancho de banda de lo especificado. El escritor no genera ni comprueba la información de un objeto de uso compartido de ancho de banda ni lo usa el lector para nada.

Cuando se escribe un archivo que tiene información de uso compartido de ancho de banda en su perfil, los datos se almacenan en la sección de encabezado. Puede usar la interfaz [**IWMProfile**](iwmprofile.md) en el lector para comprobar la información de uso compartido del ancho de banda cuando se reproduzca el archivo.

Cada objeto de uso compartido de ancho de banda se define con dos valores. El primero es el ancho de banda, tal y como se define en un ancho de banda y una ventana de búfer. La segunda opción es un tipo de uso compartido de ancho de banda, que puede ser exclusivo o parcial. El uso compartido de ancho de banda exclusivo significa que las secuencias constituyentes se reproducen de una en una, mientras que parcial significa que las secuencias se entregan al mismo tiempo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz IWMProfile**](iwmprofile.md)
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

 

 




