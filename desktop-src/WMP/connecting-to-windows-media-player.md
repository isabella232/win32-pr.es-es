---
title: Conectarse a Media Player de Windows
description: Conectarse a Media Player de Windows
ms.assetid: c6afbd95-bcf8-438a-b854-776c543a5d51
keywords:
- Complementos de Windows Media Player, entradas del registro
- complementos, entradas del registro
- Complementos de Windows Media Player, conectar
- complementos, conectar
- Complementos de procesamiento de señal digital, conectar
- Complementos DSP, conectar
- Complementos de procesamiento de señal digital, entradas del registro
- Complementos DSP, entradas del registro
- registro, Complementos DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8fa0851e271631e2c37bf716c427b5af34ade14
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104420232"
---
# <a name="connecting-to-windows-media-player"></a>Conectarse a Media Player de Windows

Windows Media Player se conecta automáticamente a los complementos DSP que se han instalado y registrado correctamente. Los complementos DSP deben llamar a [IWMPMediaPluginRegistrar:: WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) para crear las entradas del registro necesarias para permitir que Windows Media Player reconozca el complemento y lo muestre en la **pestaña** complementos del cuadro de diálogo Opciones. Para quitar las entradas del registro creadas por **IWMPMediaPluginRegistrar:: WMPRegisterPlayerPlugin**, el complemento llama a [IWMPMediaPluginRegistrar:: WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Introducción al desarrollador de complementos de DSP**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




