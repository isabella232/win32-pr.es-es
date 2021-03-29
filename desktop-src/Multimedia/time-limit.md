---
title: Límite de tiempo
description: Límite de tiempo
ms.assetid: 7c07755b-ba4d-4ec0-82ee-f76a533c6c5b
keywords:
- Estructura CAPTUREPARMS
- Mensaje WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup (macro)
- Estructura CAPTUREPARMS
- Mensaje WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 878c76ab1e380fe878cd8c9493163bcb71e574cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779975"
---
# <a name="time-limit"></a>Límite de tiempo

Puede limitar la duración de una operación de captura mediante los miembros **fLimitEnabled** y **wTimeLimit** de la estructura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) . El miembro **fLimitEnabled** indica si se va a establecer el tiempo de la operación de captura, mientras que **wTimeLimit** especifica la duración máxima de la operación de captura.

Puede recuperar los valores de **fLimitEnabled** y **wTimeLimit** mediante el mensaje de [**configuración de la secuencia de \_ \_ \_ salida \_ Cap de WM**](wm-cap-get-sequence-setup.md) (o la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ). Puede habilitar un temporizador para la operación de captura especificando **true** como el valor de **fLimitEnabled**, o bien puede establecer la duración de la operación de captura especificando un valor, en segundos, para **wTimeLimit**. Después de establecer estos miembros, envíe la estructura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) actualizada a la ventana de captura mediante el mensaje de configuración de la secuencia de definición de [](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) Cap de [**WM \_ \_ \_ \_**](wm-cap-set-sequence-setup.md) (o la macro capCaptureSetSetup). El valor predeterminado de **fLimitEnabled** es **false**.

 

 




