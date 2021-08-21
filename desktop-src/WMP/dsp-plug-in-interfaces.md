---
title: Interfaces de complemento DE DSP
description: Interfaces de complemento DE DSP
ms.assetid: 4660f928-2e92-468f-9e2b-b411931dfded
keywords:
- Reproductor de Windows Media complementos, interfaces DSP
- Reproductor de Windows Media complementos,interfaces
- complementos, interfaces DSP
- complementos, interfaces
- complementos de procesamiento de señales digitales, interfaces
- complementos de procesamiento de señales digitales, interfaz ISpecifyPropertyPage
- Complementos de DSP, interfaces
- Complementos DE DSP, interfaz ISpecifyPropertyPage
- interfaces, complementos DSP
- ISpecifyPropertyPage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3bd030b09377adfe965698d6c411f1a39a745979f2db2eae9f0c613cad843d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863375"
---
# <a name="dsp-plug-in-interfaces"></a>Interfaces de complemento DE DSP

Las interfaces de complemento de procesamiento de señal digital (DSP) se usan para administrar la transferencia de datos entre Reproductor de Windows Media y el complemento. Todos los complementos de DSP pueden implementar opcionalmente la **interfaz ISpecifyPropertyPage** para proporcionar una implementación de página de propiedades.

Las interfaces siguientes son necesarias para crear complementos DSP.



| Interfaz                                                | Descripción                                                                                                                                            |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **IMediaObject**                                         | Administra el intercambio de datos con Reproductor de Windows Media realiza tareas de procesamiento de señales digitales. La documentación detallada se incluye con el SDK de DirectX. |
| [IWMPMediaPluginRegistrar](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpmediapluginregistrar) | Administra el registro del complemento.                                                                                                                          |
| [IWMPPlugin](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpplugin)                             | Administra la conexión a Reproductor de Windows Media.                                                                                                        |
| [IWMPPluginEnable](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmppluginenable)                 | Almacena si el complemento está habilitado actualmente por Reproductor de Windows Media.                                                                               |
| [IWMPServices](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpservices)                         | Recupera información del reproductor sobre el tiempo de transmisión actual y el estado de la secuencia.                                                                  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación de complementos DE DSP**](dsp-plug-ins-programming-reference.md)
</dt> </dl>

 

 




