---
title: Interfaces de complemento de DSP
description: Interfaces de complemento de DSP
ms.assetid: 4660f928-2e92-468f-9e2b-b411931dfded
keywords:
- Complementos de Windows Media Player, interfaces DSP
- Complementos de Windows Media Player, interfaces
- complementos, interfaces DSP
- complementos, interfaces
- Complementos de procesamiento de señal digital, interfaces
- Complementos de procesamiento de señal digital, interfaz ISpecifyPropertyPage
- Complementos DSP, interfaces
- Complementos DSP, interfaz ISpecifyPropertyPage
- interfaces, Complementos DSP
- ISpecifyPropertyPage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5458ab945b24f8646d986ab7d5d44e12ef3249d
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/21/2020
ms.locfileid: "104420433"
---
# <a name="dsp-plug-in-interfaces"></a>Interfaces de complemento de DSP

Las interfaces de complemento de procesamiento de señal digital (DSP) se usan para administrar la transferencia de datos entre Windows Media Player y el complemento. Todos los complementos de DSP pueden implementar opcionalmente la interfaz **ISpecifyPropertyPage** para proporcionar una implementación de la página de propiedades.

Se requieren las siguientes interfaces para crear complementos de DSP.



| Interfaz                                                | Descripción                                                                                                                                            |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| **IMediaObject**                                         | Administra el intercambio de datos con Windows Media Player y realiza tareas de procesamiento de señal digital. La documentación detallada se incluye con el SDK de DirectX. |
| [IWMPMediaPluginRegistrar](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpmediapluginregistrar) | Administra el registro del complemento.                                                                                                                          |
| [IWMPPlugin](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpplugin)                             | Administra la conexión a Windows Media Player.                                                                                                        |
| [IWMPPluginEnable](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmppluginenable)                 | Almacena si el complemento está habilitado actualmente por Media Player de Windows.                                                                               |
| [IWMPServices](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpservices)                         | Recupera información del reproductor sobre el estado de flujo y la hora de la secuencia actual.                                                                  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Referencia de programación de complementos DSP**](dsp-plug-ins-programming-reference.md)
</dt> </dl>

 

 




