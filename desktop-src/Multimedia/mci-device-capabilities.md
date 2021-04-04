---
title: Funcionalidades del dispositivo MCI
description: Funcionalidades del dispositivo MCI
ms.assetid: ac79fbe6-23ea-44ce-ada1-abea1fd07394
keywords:
- MCIWndCanConfig (macro)
- MCIWndCanEject (macro)
- MCIWndCanPlay (macro)
- MCIWndCanRecord (macro)
- MCIWndCanSave (macro)
- MCIWndCanWindow (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59effd4e00106a2bb0175bf39b7eb07fa8b65d30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076273"
---
# <a name="mci-device-capabilities"></a>Funcionalidades del dispositivo MCI

MCIWnd incluye las siguientes macros que permiten consultar los dispositivos MCI en busca de sus capacidades.



| Macro                                      | Descripción                                                                                                                                 |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**MCIWndCanConfig**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig) | Determina si un dispositivo tiene un cuadro de diálogo de configuración para admitir varias configuraciones, como el dispositivo MCIAVI.                   |
| [**MCIWndCanEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject)   | Determina si un dispositivo tiene una función EJECT controlada por software.                                                                       |
| [**MCIWndCanPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay)     | Determina si un dispositivo puede reproducir el contenido existente.                                                                                  |
| [**MCIWndCanRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) | Determina si un dispositivo puede grabar.                                                                                                     |
| [**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave)     | Determina si un dispositivo puede almacenar datos.                                                                                                 |
| [**MCIWndCanWindow**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow) | Determina si un dispositivo admite comandos de ventana MCI (como [**Window**](window.md), [**Put**](put.md) y [**Where**](where.md)). |



 

Estas macros devuelven **true** si el dispositivo admite la funcionalidad específica o **false** en caso contrario.

 

 




