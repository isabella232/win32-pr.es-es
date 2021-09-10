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
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124372349"
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

 

 




