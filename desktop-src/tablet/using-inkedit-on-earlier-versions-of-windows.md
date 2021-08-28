---
description: Debido a la falta de reconocedores en las ediciones de equipos que no son tabletas de Microsoft Windows XP, no puede usar InkEdit para representar la entrada de lápiz en las ediciones Windows 2000, Windows Server 2003 y non-Tablet PC de Windows XP, y no puede usar el control para introducir entrada de lápiz en estos sistemas operativos.
ms.assetid: eb80ff91-5c09-43d1-afd4-6391097000c1
title: Uso de InkEdit en versiones anteriores de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefa98089a2ede778be09719767f96a1129a1be0d4004828172651e637cd81d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118966614"
---
# <a name="using-inkedit-on-earlier-versions-of-windows"></a>Uso de InkEdit en versiones anteriores de Windows

Debido a la falta de reconocedores en las ediciones de equipos que no son tabletas de Microsoft Windows XP, no puede usar [InkEdit](inkedit-control.md) para representar la entrada de lápiz en las ediciones Windows 2000, Windows Server 2003 y no tablet PC de Windows XP, y no puede usar el control para introducir entrada de lápiz en estos sistemas operativos.

La propiedad [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) del control se establece en **Deshabilitado** **(IEM \_ deshabilitado** para C++) y el intento de cambiar la propiedad no tiene ningún efecto. Puede asignar valores a otras propiedades y copiar y pegar la entrada de lápiz en otras aplicaciones, pero no puede usar el control para aceptar gestos ni recopilar lápiz.

 

 



