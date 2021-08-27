---
description: Una aplicación puede convertir una ruta de acceso en una región mediante una llamada a la función PathToRegion.
ms.assetid: c4261516-7872-4118-99e2-138f0ac3c38a
title: Conversión de rutas de acceso a regiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d404aa50669fe2349b3e39f172dd652ef765c9de8c615cde446e8540e6051bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062465"
---
# <a name="conversion-of-paths-to-regions"></a>Conversión de rutas de acceso a regiones

Una aplicación puede convertir una ruta de acceso en una región mediante una llamada a [**la función PathToRegion.**](/windows/desktop/api/Wingdi/nf-wingdi-pathtoregion) Al [**igual que SelectClipPath,**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath) **PathToRegion** es útil en la creación de efectos gráficos especiales. Por ejemplo, no hay ninguna función que permita a una aplicación desplazar una ruta de acceso; sin embargo, hay una función que permite a una aplicación desplazar una región [**(OffsetRgn**](/windows/desktop/api/Wingdi/nf-wingdi-offsetrgn)). Con **PathToRegion** , una aplicación puede crear el efecto de animar una forma compleja mediante la creación de una ruta de acceso que define la forma, la conversión de la ruta de acceso en una región (mediante una llamada a **PathToRegion**) y, a continuación, pintar, mover y borrar repetidamente la región (llamando a funciones de una secuencia, como [**FillRgn,**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn) **OffsetRgn** y **FillRgn).**

 

 



