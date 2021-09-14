---
title: Límite de tiempo
description: Límite de tiempo
ms.assetid: 7c07755b-ba4d-4ec0-82ee-f76a533c6c5b
keywords:
- Estructura CAPTUREPARMS
- WM_CAP_GET_SEQUENCE_SETUP mensaje
- CapCaptureGetSetup macro
- Estructura CAPTUREPARMS
- WM_CAP_SET_SEQUENCE_SETUP mensaje
- CapCaptureSetSetup macro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 878c76ab1e380fe878cd8c9493163bcb71e574cf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260604"
---
# <a name="time-limit"></a>Límite de tiempo

Puede limitar la duración de una operación de captura mediante los miembros **fLimitEnabled** y **wTimeLimit** de la [**estructura CAPTUREPARMS.**](/windows/win32/api/vfw/ns-vfw-captureparms) El **miembro fLimitEnabled** indica si se va a realizar el tiempo de la operación de captura, mientras **que wTimeLimit especifica** la duración máxima de la operación de captura.

Puede recuperar los valores de **fLimitEnabled** y **wTimeLimit** mediante el mensaje [**GET SEQUENCE \_ \_ \_ \_ SETUP**](wm-cap-get-sequence-setup.md) de WM CAP (o la macro [**capCaptureGetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) Puede habilitar un temporizador para la operación de captura especificando **TRUE** como el valor de **fLimitEnabled** o puede establecer la duración de la operación de captura especificando un valor, en segundos, para **wTimeLimit**. Después de establecer estos miembros, envíe la estructura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) actualizada a la ventana de captura mediante el mensaje [**SET SEQUENCE SETUP \_ \_ \_ \_ de WM CAP**](wm-cap-set-sequence-setup.md) (o la macro [**capCaptureSetSetup).**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) El valor predeterminado de **fLimitEnabled** es **FALSE.**

 

 




