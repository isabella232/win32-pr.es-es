---
title: Referencia del mezclador de audio
description: Referencia del mezclador de audio
ms.assetid: 9d8751b1-9c0b-4238-a961-27c09a869bb3
keywords:
- audio multimedia, mezcladores de audio
- audio, mezclador de audio
- audio multimedia, referencia de mezclador
- audio, referencia de mezclador
- mezclador de audio, referencia
- mezclador, referencia
- referencia de los mezcladores de audio, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be1d86f305714d72631b56495753417699b1a146
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104271202"
---
# <a name="audio-mixer-reference"></a>Referencia del mezclador de audio

En esta sección se describen las funciones, las estructuras y los mensajes asociados a los mezcladores de audio. Estos elementos se agrupan de la siguiente manera.

## <a name="querying-devices"></a>Consultar dispositivos

-   [**MIXERCAPS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercaps)
-   [**mixerGetDevCaps**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetdevcaps)
-   [**mixerGetNumDevs**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetnumdevs)

## <a name="opening-and-closing"></a>Abrir y cerrar

-   [**mixerClose**](/windows/win32/api/mmeapi/nf-mmeapi-mixerclose)
-   [**mixerOpen**](/windows/win32/api/mmeapi/nf-mmeapi-mixeropen)

## <a name="retrieving-mixer-identifiers"></a>Recuperando identificadores de mezclador

-   [**mixerGetID**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetid)

## <a name="retrieving-line-controls"></a>Recuperar controles de línea

-   [**MIXERCONTROL**](/windows/win32/api/mmeapi/ns-mmeapi-mixercontrol)
-   [**mixerGetLineControls**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlinecontrols)
-   [**MIXERLINECONTROLS**](/windows/win32/api/mmeapi/ns-mmeapi-mixerlinecontrols)

## <a name="changing-control-attributes"></a>Cambiar atributos de control

-   [**MIXERCONTROLDETAILS**](/windows/win32/api/mmeapi/ns-mmeapi-mixercontroldetails_listtexta)
-   [**MIXERCONTROLDETAILS \_ booleano**](/previous-versions//dd757295(v=vs.85))
-   [**MIXERCONTROLDETAILS \_ LISTTEXT**](/previous-versions//dd757296(v=vs.85))
-   [**MIXERCONTROLDETAILS \_ firmado**](/previous-versions//dd757297(v=vs.85))
-   [**MIXERCONTROLDETAILS \_ sin signo**](/previous-versions//dd757298(v=vs.85))
-   [**mixerGetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetcontroldetails)
-   [**mixerSetControlDetails**](/windows/win32/api/mmeapi/nf-mmeapi-mixersetcontroldetails)

## <a name="retrieving-line-information"></a>Recuperar información de línea

-   [**mixerGetLineInfo**](/windows/win32/api/mmeapi/nf-mmeapi-mixergetlineinfo)
-   [**MIXERLINE**](/windows/win32/api/mmeapi/ns-mmeapi-mixerline)
-   [**cambio de control de MM \_ MIXM \_ \_**](mm-mixm-control-change.md)
-   [**\_cambio de \_ línea mm MIXM \_**](mm-mixm-line-change.md)

## <a name="sending-user-defined-messages"></a>Envío de mensajes de User-Defined

-   [**mixerMessage**](/windows/win32/api/mmeapi/nf-mmeapi-mixermessage)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia del mezclador de audio](audio-mixer-reference.md)
</dt> </dl>

 

 