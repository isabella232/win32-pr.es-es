---
description: ATM es aplicable a entornos LAN y WAN.
ms.assetid: 532a876c-9b31-410e-9331-5e8aa98ccaee
title: Anexo del cajero automático de Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63ec056cc2b84c9449ed466a60a15683df29744b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967268"
---
# <a name="winsock-atm-annex"></a>Anexo del cajero automático de Winsock

ATM es aplicable a entornos LAN y WAN. Una red de cajeros automáticos transporta simultáneamente una amplia variedad de tráfico de red: voz, datos, imagen y vídeo. Proporciona a los usuarios una calidad de servicio garantizada en cada canal virtual (VC).



| Elemento          | Descripción                                                                                                                                                 |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nombres de protocolo | ATMPROTO \_ AAL5, ATMPROTO \_ AALUSER                                                                                                                           |
| Descripción      | AAL5 de ATM proporciona un servicio de transporte orientado a la conexión, se conserva el límite de mensajes y se garantiza qos. ATMPROTO \_ AALUSER es un AAL definido por el usuario. |
| Familia de direcciones   | CAJERO \_ AUTOMÁTICO DE AF                                                                                                                                                     |
| Archivo de encabezado      | Ws2atm.h                                                                                                                                                    |



 

En esta sección se describen las extensiones específicas del modo de transferencia asincrónica (ATM) necesarias para admitir los servicios de ATM nativos tal como se expone y se especifica en la especificación de la interfaz de red de usuario (UNI) del foro de ATM versión 3.x (3.0 y 3.1). Este documento admite AAL de tipo 5 (modo de mensaje) y AAL definido por el usuario. Las versiones futuras de este documento admitirán otros tipos de AAL, así como UNI 4.0.

 

 



