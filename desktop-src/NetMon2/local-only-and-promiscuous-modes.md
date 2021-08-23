---
description: Los monitores pueden examinar fotogramas en modo solo local o en modo promiscuo.
ms.assetid: 4646f5bb-e3e3-4929-91b7-f68c5b70ccb3
title: Local-Only y promiscuos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8155c968f82154712ec8926f114e63380cdb1099bf7908d5a4dde86d7646dc20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555895"
---
# <a name="local-only-and-promiscuous-modes"></a>Local-Only y promiscuos

Los monitores pueden examinar fotogramas en modo solo local o en modo promiscuo.

En modo de solo local, el proveedor de paquetes de red (NPP) devuelve fotogramas que se envían a o desde el equipo en el que se ejecuta el monitor, incluidas las difusiones y multidifusión dirigidas al equipo local. Aunque se limita a fotogramas dirigidos localmente, el modo local también consume mucho menos procesador.

En modo promiscuo, el monitor también puede observar el tráfico que no se dirige al equipo local ni desde este. A menos que el monitor haya especificado la marca MCS CREATE PMODE NOT REQUIRED, en la función \_ \_ \_ \_ [OnLoadingDLL,](onloadingdll.md) monitor Control Service (MCSVC) supone que el monitor requiere el modo promiscuo cuando carga el archivo DLL del monitor.

 

 



