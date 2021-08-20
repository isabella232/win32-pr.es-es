---
title: Funcionalidades del dispositivo MCI
description: Funcionalidades del dispositivo MCI
ms.assetid: ac79fbe6-23ea-44ce-ada1-abea1fd07394
keywords:
- Macro MCIWndCanConfig
- Macro MCIWndCanEject
- Macro MCIWndCanPlay
- Macro MCIWndCanRecord
- Macro MCIWndCanSave
- Macro MCIWndCanWindow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f6dbc6b9d1e7bbfc1c1e3651edd40c0f5953989dee6d2462e065d5c2109b5b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117986703"
---
# <a name="mci-device-capabilities"></a>Funcionalidades del dispositivo MCI

MCIWnd incluye las siguientes macros para que le permita consultar sus funcionalidades en los dispositivos MCI.



| Macro                                      | Descripción                                                                                                                                 |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**MCIWndCanConfig**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig) | Determina si un dispositivo tiene un cuadro de diálogo de configuración para admitir varias configuraciones, como el dispositivo MCIAVI.                   |
| [**MCIWndCanEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject)   | Determina si un dispositivo tiene una función de expulsión controlada por software.                                                                       |
| [**MCIWndCanPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay)     | Determina si un dispositivo puede reproducir el contenido existente.                                                                                  |
| [**MCIWndCanRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) | Determina si un dispositivo puede grabar.                                                                                                     |
| [**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave)     | Determina si un dispositivo puede almacenar datos.                                                                                                 |
| [**MCIWndCanWindow**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow) | Determina si un dispositivo admite comandos de ventana de MCI (como [**window**](window.md), [**put**](put.md) y [**where).**](where.md) |



 

Estas macros **devuelven TRUE** si el dispositivo admite la funcionalidad específica o **FALSE** en caso contrario.

 

 




