---
title: Referencia de Mixer audio
description: Referencia de Mixer audio
ms.assetid: 9d8751b1-9c0b-4238-a961-27c09a869bb3
keywords:
- audio multimedia, mezcladores de audio
- audio, mezcladores de audio
- audio multimedia, referencia de mezclador
- audio, referencia de mezclador
- mezcladores de audio, referencia
- mixers,reference
- referencia de mezcladores de audio, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be1d86f305714d72631b56495753417699b1a146
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062971"
---
# <a name="audio-mixer-reference"></a>Referencia de Mixer audio

En esta sección se describen las funciones, las estructuras y los mensajes asociados a los mezcladores de audio. Estos elementos se agrupan como se muestra a continuación.

## <a name="querying-devices"></a>Consultar dispositivos

-   [**MIXERCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercaps)
-   [**mixerGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetdevcaps)
-   [**mixerGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs)

## <a name="opening-and-closing"></a>Apertura y cierre

-   [**mixerClose**](/windows/win32/api/mmeapi/nf-mmeapi-mixerclose)
-   [**mixerOpen**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen)

## <a name="retrieving-mixer-identifiers"></a>Recuperación de Mixer identificadores

-   [**mixerGetID**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetid)

## <a name="retrieving-line-controls"></a>Recuperar controles de línea

-   [**MIXERCONTROL**](/windows/win32/api/mmeapi/ns-mmeapi-mixercontrol)
-   [**mixerGetLineControls**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlinecontrols)
-   [**MIXERLINECONTROLS**](/windows/win32/api/mmeapi/ns-mmeapi-mixerlinecontrols)

## <a name="changing-control-attributes"></a>Cambiar atributos de control

-   [**MIXERCONTROLDETAILS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercontroldetails_listtexta)
-   [**MIXERCONTROLDETAILS \_ BOOLEAN**](/previous-versions//dd757295(v=vs.85))
-   [**MIXERCONTROLDETAILS \_ LISTTEXT**](/previous-versions//dd757296(v=vs.85))
-   [**MIXERCONTROLDETAILS \_ FIRMADO**](/previous-versions//dd757297(v=vs.85))
-   [**MIXERCONTROLDETAILS \_ SIN SIGNO**](/previous-versions//dd757298(v=vs.85))
-   [**mixerGetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetcontroldetails)
-   [**mixerSetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixersetcontroldetails)

## <a name="retrieving-line-information"></a>Recuperar información de línea

-   [**mixerGetLineInfo**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlineinfo)
-   [**MIXERLINE**](/windows/win32/api/mmeapi/ns-mmeapi-mixerline)
-   [**CAMBIO \_ DE CONTROL DE MIXM \_ \_ MM**](mm-mixm-control-change.md)
-   [**CAMBIO \_ DE LÍNEA DE MM MIXM \_ \_**](mm-mixm-line-change.md)

## <a name="sending-user-defined-messages"></a>Envío de User-Defined mensajes

-   [**mixerMessage**](/windows/win32/api/mmeapi/nf-mmeapi-mixermessage)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de Mixer audio](audio-mixer-reference.md)
</dt> </dl>

 

 