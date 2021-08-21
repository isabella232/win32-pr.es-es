---
description: Determine la versión de Windows Update Agent (WUA) antes de usarla.
ms.assetid: fc915535-f87d-43fb-8755-fa6c80fedea5
title: Determinar la versión actual de WUA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa8d8e013f4e8189c71b9e4510fdaebcdf1e2f749e3d8dfffd6256128e214ce4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049503"
---
# <a name="determining-the-current-version-of-wua"></a>Determinar la versión actual de WUA

Para obtener información general sobre cómo actualizar el WUA, incluidas las instrucciones paso a paso para determinar mediante programación desde dentro de la aplicación si la versión de WUA que se ejecuta en el equipo satisface sus necesidades, consulte Actualización del agente de actualización de [Windows](updating-the-windows-update-agent.md).

En las versiones de Windows anteriores a Windows 7 y Windows Server 2008 R2, debe determinar la versión instalada de Windows Update Agent (WUA) antes de usarla. La versión actual de WUA viene determinada por la versión del Wuaueng.dll que se ejecuta en el subdirectorio System32 de la instalación Windows \\ actual. Si la versión de Wuaueng.dll es la versión 5.4.3790.1000 o una versión posterior, wua se instala. Una versión anterior a 5.4.3790.1000 indica que software Update Services (SUS) 1.0 está instalado.

Cuando se realiza una llamada a SUS 1.0 mediante la API de WUA, se devuelve **un HRESULT** de WU \_ E AU \_ \_ LEGACYSERVER.

También puede usar el [**método IWindowsUpdateAgentInfo::GetInfo**](/windows/desktop/api/Wuapi/nf-wuapi-iwindowsupdateagentinfo-getinfo) para recuperar la versión de archivo actual de Wuapi.dll que se ejecuta en un equipo. La [**interfaz IWindowsUpdateAgentInfo**](/windows/desktop/api/Wuapi/nn-wuapi-iwindowsupdateagentinfo) no se admite en WUA 1.0.
