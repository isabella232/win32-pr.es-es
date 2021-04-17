---
description: Los monitores pueden examinar fotogramas en modo solo local o en modo promiscuo.
ms.assetid: 4646f5bb-e3e3-4929-91b7-f68c5b70ccb3
title: Modos Local-Only e promiscuo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd1188760d8de31836de3fbd437854a5df138402
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666546"
---
# <a name="local-only-and-promiscuous-modes"></a>Modos Local-Only e promiscuo

Los monitores pueden examinar fotogramas en modo solo local o en modo promiscuo.

En el modo de solo local, el proveedor de paquetes de red (NPP) devuelve los fotogramas que se envían al equipo en el que se ejecuta el monitor, incluidas las difusiones y multidifusión dirigidas a la máquina local. Aunque se limita a los marcos dirigidos localmente, el modo local también es mucho menos procesador.

En el modo promiscuo, el monitor también puede ver el tráfico que no se dirige a o desde el equipo local. A menos que el monitor haya especificado la marca, MCS \_ Create \_ PMODE \_ no \_ es necesario, en la función [OnLoadingDLL](onloadingdll.md) , el servicio de control de supervisión (MCSVC) supone que el monitor requiere el modo promiscuo cuando carga el archivo DLL del monitor.

 

 



