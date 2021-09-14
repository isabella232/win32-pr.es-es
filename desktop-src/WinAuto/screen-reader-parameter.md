---
title: Parámetro lector de pantalla
description: El parámetro lector de pantalla indica si una aplicación debe proporcionar información textual en situaciones en las que, de lo contrario, presentaría la información gráficamente.
ms.assetid: ac79c389-511c-4403-a8d5-75b2eba2b39f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0c237f3d945b9782884ffc655cf87a203159a16
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127070640"
---
# <a name="screen-reader-parameter"></a>Parámetro lector de pantalla

El parámetro lector de pantalla indica si una aplicación debe proporcionar información textual en situaciones en las que, de lo contrario, presentaría la información gráficamente.

Normalmente, este parámetro se establece mediante ayuda de accesibilidad, como lectores de pantalla. Las aplicaciones usan **las marcas SPI \_ GETSCREENREADER** y **SPI \_ SETSCREENREADER** con la función [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para obtener y establecer el parámetro del lector de pantalla.

> [!Note]  
> Narrador, el lector de pantalla que se incluye con Windows, no establece las marcas **SPI \_ SETSCREENREADER** **o SPI \_ GETSCREENREADER.**

 

 

 