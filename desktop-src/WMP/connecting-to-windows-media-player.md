---
title: Conexión a Reproductor de Windows Media
description: Conexión a Reproductor de Windows Media
ms.assetid: c6afbd95-bcf8-438a-b854-776c543a5d51
keywords:
- Reproductor de Windows Media complementos,entradas del Registro
- complementos, entradas del Registro
- Reproductor de Windows Media complementos, conectarse
- complementos, conectarse
- complementos de procesamiento de señales digitales, conexión
- Complementos DE DSP, conexión
- complementos de procesamiento de señales digitales, entradas del Registro
- Complementos de DSP, entradas del Registro
- registry,DSP plug-ins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8fa0851e271631e2c37bf716c427b5af34ade14
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967747"
---
# <a name="connecting-to-windows-media-player"></a>Conexión a Reproductor de Windows Media

Reproductor de Windows Media se conecta automáticamente a los complementos de DSP que se han instalado y registrado correctamente. Los complementos de DSP deben llamar a [IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin) para crear las entradas del Registro necesarias para  permitir que Reproductor de Windows Media reconozca el complemento y lo enumere en la pestaña Complementos del cuadro de diálogo Opciones. Para quitar las entradas del Registro creadas por **IWMPMediaPluginRegistrar::WMPRegisterPlayerPlugin**, el complemento llama a [IWMPMediaPluginRegistrar::WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Introducción al desarrollador del complemento DSP**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




