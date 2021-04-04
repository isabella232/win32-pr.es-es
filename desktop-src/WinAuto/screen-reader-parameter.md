---
title: Parámetro de lector de pantalla
description: El parámetro lector de pantalla indica si una aplicación debe proporcionar información de texto en situaciones en las que, de lo contrario, presentaría la información de forma gráfica.
ms.assetid: ac79c389-511c-4403-a8d5-75b2eba2b39f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0c237f3d945b9782884ffc655cf87a203159a16
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078024"
---
# <a name="screen-reader-parameter"></a>Parámetro de lector de pantalla

El parámetro lector de pantalla indica si una aplicación debe proporcionar información de texto en situaciones en las que, de lo contrario, presentaría la información de forma gráfica.

Este parámetro se establece normalmente por ayudas de accesibilidad, como lectores de pantalla. Las aplicaciones usan las marcas **SPI \_ GETSCREENREADER** y **SPI \_ SETSCREENREADER** con la función [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para obtener y establecer el parámetro de lector de pantalla.

> [!Note]  
> Narrador, el lector de pantalla incluido en Windows, no establece las marcas **SPI \_ SETSCREENREADER** o **SPI \_ GETSCREENREADER** .

 

 

 