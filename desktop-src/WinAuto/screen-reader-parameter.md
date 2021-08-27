---
title: Parámetro lector de pantalla
description: El parámetro lector de pantalla indica si una aplicación debe proporcionar información textual en situaciones en las que, de lo contrario, presentaría la información gráficamente.
ms.assetid: ac79c389-511c-4403-a8d5-75b2eba2b39f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 818ad36cfe833c1c9a3f39047cd88e6b4e8be55972d521ce524bb1e0618a48ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098425"
---
# <a name="screen-reader-parameter"></a>Parámetro lector de pantalla

El parámetro lector de pantalla indica si una aplicación debe proporcionar información textual en situaciones en las que, de lo contrario, presentaría la información gráficamente.

Normalmente, este parámetro se establece mediante ayuda de accesibilidad, como lectores de pantalla. Las aplicaciones usan **las marcas SPI \_ GETSCREENREADER** y **SPI \_ SETSCREENREADER** con la función [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para obtener y establecer el parámetro del lector de pantalla.

> [!Note]  
> Narrador, el lector de pantalla que se incluye con Windows, no establece las marcas **SPI \_ SETSCREENREADER** **o SPI \_ GETSCREENREADER.**

 

 

 