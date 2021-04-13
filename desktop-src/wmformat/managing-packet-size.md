---
title: Administración del tamaño del paquete
description: Administración del tamaño del paquete
ms.assetid: 75ccda39-255a-4213-824e-1ca778a741dc
keywords:
- SDK de Windows Media Format, administrar tamaños de paquetes
- SDK de Windows Media Format, tamaños de paquete
- perfiles, tamaños de paquete
- perfiles, administración de tamaños de paquetes
- paquetes, tamaños
- paquetes, interfaz IWMPacketSize
- IWMPacketSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22e5bb0720d54338a754838e3d44c4479e55af9d
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104420450"
---
# <a name="managing-packet-size"></a>Administración del tamaño del paquete

El escritor está diseñado para administrar el tamaño de los paquetes internamente. Sin embargo, puede que tenga requisitos específicos para su aplicación que llamen a un control manual sobre el tamaño de los paquetes en los archivos ASF que escriba. El SDK de Windows Media Format proporciona dos interfaces, [**IWMPacketSize**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize) y [**IWMPacketSize2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2) , que le permiten controlar el tamaño máximo y mínimo de los paquetes.

Ambas interfaces de tamaño de paquete se exponen en el objeto de perfil. También están disponibles para el objeto lector. Al igual que con otras interfaces relacionadas con perfiles, el lector solo puede tener acceso a los métodos de lectura.

El tamaño de los paquetes tiene algún efecto en el rendimiento. En general, cuanto menor es el tamaño del paquete, más se fragmentan los datos en un archivo. Cuanto más se fragmenta un archivo, menos eficaz será reconstruirlo. En un escenario de streaming, esto puede no ser una consideración importante, ya que el proceso de lectura de un archivo de un origen de Internet suele ser ineficaz. No obstante, cuando se trabaja con un archivo de forma local, esto podría ser una consideración.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Interfaz IWMPacketSize**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize)
</dt> <dt>

[**Interfaz IWMPacketSize2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpacketsize2)
</dt> <dt>

[**Trabajar con perfiles**](working-with-profiles.md)
</dt> </dl>

 

 




