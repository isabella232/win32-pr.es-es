---
description: Una aplicación puede convertir un trazado en una región llamando a la función PathToRegion.
ms.assetid: c4261516-7872-4118-99e2-138f0ac3c38a
title: Conversión de rutas de acceso a regiones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc3a576f04035f6e29bb37a23de956322639daf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103812007"
---
# <a name="conversion-of-paths-to-regions"></a>Conversión de rutas de acceso a regiones

Una aplicación puede convertir un trazado en una región llamando a la función [**PathToRegion**](/windows/desktop/api/Wingdi/nf-wingdi-pathtoregion) . Al igual que [**SelectClipPath**](/windows/desktop/api/Wingdi/nf-wingdi-selectclippath), **PathToRegion** es útil en la creación de efectos gráficos especiales. Por ejemplo, no hay ninguna función que permita a una aplicación desplazar una ruta de acceso; sin embargo, hay una función que permite a una aplicación desplazar una región ([**OffsetRgn**](/windows/desktop/api/Wingdi/nf-wingdi-offsetrgn)). Con **PathToRegion** , una aplicación puede crear el efecto de animar una forma compleja creando una ruta de acceso que defina la forma, convirtiendo la ruta de acceso en una región (llamando a **PathToRegion**) y, a continuación, dibujando, moviendo y borrando la región repetidamente (llamando a funciones en una secuencia, como [**FillRgn**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn), **OffsetRgn** y **FillRgn**).

 

 



