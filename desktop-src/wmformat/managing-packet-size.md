---
title: Administración del tamaño del paquete
description: Administración del tamaño del paquete
ms.assetid: 75ccda39-255a-4213-824e-1ca778a741dc
keywords:
- Windows SDK de formato multimedia, administración de tamaños de paquetes
- Windows SDK de formato multimedia, tamaños de paquete
- perfiles, tamaños de paquete
- perfiles, administración de tamaños de paquete
- packets,sizes
- packets,IWMPacketSize (interfaz)
- IWMPacketSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22e5bb0720d54338a754838e3d44c4479e55af9d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127267039"
---
# <a name="managing-packet-size"></a>Administración del tamaño del paquete

El escritor está diseñado para administrar internamente el tamaño de los paquetes. Sin embargo, es posible que tenga requisitos específicos para la aplicación que llamen a un control manual sobre el tamaño de los paquetes en los archivos ASF que escriba. El SDK Windows Media Format proporciona dos interfaces, [**IWMPacketSize**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize) e [**IWMPacketSize2,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2) que permiten controlar el tamaño máximo y mínimo de los paquetes.

Ambas interfaces de tamaño de paquete se exponen en el objeto de perfil. También están disponibles para el objeto de lector. Al igual que con otras interfaces relacionadas con el perfil, el lector solo puede acceder a los métodos de lectura.

El tamaño de los paquetes tiene algún efecto en el rendimiento. En general, cuanto menor sea el tamaño del paquete, más fragmentados están los datos dentro de un archivo. Cuando más fragmentado sea un archivo, menos eficaz será reconstruirlo. En un escenario de streaming, esto puede no ser una consideración importante, ya que el proceso de lectura de un archivo desde un origen de Internet suele ser ineficaz. Sin embargo, al tratar con un archivo localmente, esto podría ser una consideración.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMPacketSize (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize)
</dt> <dt>

[**IWMPacketSize2 (Interfaz)**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2)
</dt> <dt>

[**Trabajar con perfiles**](working-with-profiles.md)
</dt> </dl>

 

 




