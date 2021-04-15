---
description: ATM es aplicable a entornos de LAN y WAN.
ms.assetid: 532a876c-9b31-410e-9331-5e8aa98ccaee
title: Anexo de Winsock ATM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63ec056cc2b84c9449ed466a60a15683df29744b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715470"
---
# <a name="winsock-atm-annex"></a>Anexo de Winsock ATM

ATM es aplicable a entornos de LAN y WAN. Una red ATM transporta simultáneamente una amplia variedad de tráfico de red (voz, datos, imagen y vídeo). Proporciona a los usuarios una calidad de servicio garantizada por canal virtual (VC).



| Elemento          | Descripción                                                                                                                                                 |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nombre (s) de protocolo | ATMPROTO \_ AAL5, ATMPROTO \_ AALUSER                                                                                                                           |
| Descripción      | ATM AAL5 proporciona un servicio de transporte que está orientado a la conexión, se conserva el límite del mensaje y se garantiza el QOS. ATMPROTO \_ AALUSER es un Aal definido por el usuario. |
| Familia de direcciones   | \_ATM AF                                                                                                                                                     |
| Archivo de encabezado      | Ws2atm. h                                                                                                                                                    |



 

En esta sección se describen las extensiones específicas del modo de transferencia asincrónico (ATM) necesarias para admitir los servicios ATM nativos tal y como se exponen y se especifican en la especificación de la interfaz de red de usuario (UNI) del Foro ATM versión 3. x (3,0 y 3,1). Este documento admite el tipo de AAL 5 (modo de mensaje) y el AAL definido por el usuario. Las versiones futuras de este documento serán compatibles con otros tipos de AAL, así como de UNI 4,0.

 

 



