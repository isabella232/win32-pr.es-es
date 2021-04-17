---
description: Determine la versión de Windows Update Agent (WUA) antes de utilizarlo.
ms.assetid: fc915535-f87d-43fb-8755-fa6c80fedea5
title: Determinar la versión actual de WUA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af79371839bb621bed9eea199817c0fd9fe7fd8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105706023"
---
# <a name="determining-the-current-version-of-wua"></a>Determinar la versión actual de WUA

Para obtener información general sobre la actualización del WUA, incluidas las instrucciones paso a paso para determinar mediante programación desde dentro de la aplicación si la versión de WUA que se está ejecutando en el equipo satisface sus necesidades, consulte [actualización del agente de Windows Update](updating-the-windows-update-agent.md).

En las versiones de Windows anteriores a Windows 7 y Windows Server 2008 R2, debe determinar la versión instalada de Windows Update Agent (WUA) antes de utilizarla. La versión actual de WUA viene determinada por la versión de la Wuaueng.dll que se ejecuta en el \\ subdirectorio system32 de la instalación actual de Windows. Si la versión de Wuaueng.dll es la versión 5.4.3790.1000 o una versión posterior, se instala WUA. Una versión anterior a 5.4.3790.1000 indica que el servicio de actualización de software (su) 1,0 está instalado.

Cuando se realiza una llamada a SUS 1,0 mediante la API de WUA, se devuelve un **valor HRESULT** de Wu \_ E \_ au \_ LEGACYSERVER.

También puede usar el método [**IWindowsUpdateAgentInfo:: GetInfo**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsupdateagentinfo-getinfo) para recuperar la versión actual del archivo Wuapi.dll que se ejecuta en un equipo. La interfaz [**IWindowsUpdateAgentInfo**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsupdateagentinfo) no se admite en WUA 1,0.
