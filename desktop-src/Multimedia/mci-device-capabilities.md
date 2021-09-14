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
ms.openlocfilehash: 59effd4e00106a2bb0175bf39b7eb07fa8b65d30
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246080"
---
# <a name="mci-device-capabilities"></a>Funcionalidades del dispositivo MCI

MCIWnd incluye las macros siguientes para que se le permita consultar sus funcionalidades en los dispositivos MCI.



| Macro                                      | Descripción                                                                                                                                 |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**MCIWndCanConfig**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig) | Determina si un dispositivo tiene un cuadro de diálogo de configuración para admitir varias configuraciones, como el dispositivo MCIAVI.                   |
| [**MCIWndCanEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject)   | Determina si un dispositivo tiene una función de expulsión controlada por software.                                                                       |
| [**MCIWndCanPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay)     | Determina si un dispositivo puede reproducir el contenido existente.                                                                                  |
| [**MCIWndCanRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) | Determina si un dispositivo puede grabar.                                                                                                     |
| [**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave)     | Determina si un dispositivo puede almacenar datos.                                                                                                 |
| [**MCIWndCanWindow**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow) | Determina si un dispositivo admite comandos de ventana de MCI (como [**window**](window.md), [**put**](put.md) y [**where).**](where.md) |



 

Estas macros **devuelven TRUE** si el dispositivo admite la funcionalidad específica o **FALSE** en caso contrario.

 

 




