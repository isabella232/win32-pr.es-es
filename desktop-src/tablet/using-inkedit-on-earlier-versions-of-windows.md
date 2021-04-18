---
description: Debido a la falta de reconocedores en las ediciones que no son de Tablet PC de Microsoft Windows XP, no puede usar InkEdit para representar la entrada manuscrita en Windows 2000, Windows Server 2003 y las ediciones que no son de Tablet PC de Windows XP, y no puede usar el control para introducir entradas manuscritas en estos sistemas operativos.
ms.assetid: eb80ff91-5c09-43d1-afd4-6391097000c1
title: Usar InkEdit en versiones anteriores de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08343b3d379a3f45985b1f586254e7a370998f15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715078"
---
# <a name="using-inkedit-on-earlier-versions-of-windows"></a>Usar InkEdit en versiones anteriores de Windows

Debido a la falta de reconocedores en las ediciones que no son de Tablet PC de Microsoft Windows XP, no puede usar [InkEdit](inkedit-control.md) para representar la entrada manuscrita en Windows 2000, windows Server 2003 y las ediciones que no son de Tablet PC de Windows XP, y no puede usar el control para introducir entradas manuscritas en estos sistemas operativos.

La propiedad [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) del control se establece en **Disabled** (**IEM \_ deshabilitada** para C++) y el intento de cambiar la propiedad no tiene ningún efecto. Puede asignar valores a otras propiedades y copiar y pegar entradas manuscritas en otras aplicaciones, pero no puede usar el control para aceptar gestos o recopilar entradas manuscritas.

 

 



