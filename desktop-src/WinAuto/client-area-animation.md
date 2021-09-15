---
title: Parámetro de animación de área de cliente
description: La marca de animación de área de cliente indica si el usuario desea deshabilitar animaciones en elementos de la interfaz de usuario.
ms.assetid: 4a3ec9da-d5ae-4cd9-8222-f02143895ce4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c62e25fdb08022d53cbe9e818a0a1089988cd6a6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570068"
---
# <a name="client-area-animation-parameter"></a>Parámetro de animación de área de cliente

El parámetro de animación de área de cliente indica si el usuario desea deshabilitar animaciones en elementos de la interfaz de usuario. Mostrar características como parpadear, parpadear, parpadear y mover contenido puede provocar incobraciones en los usuarios con sensibilidad a fotos. Este parámetro le permite habilitar o deshabilitar todas estas animaciones.

Las aplicaciones usan las marcas **\_ SPI GETCLIENTAREAANIMATION** y **SPI \_ SETCLIENTAREAANIMATION** con la función [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para activar o desactivar las animaciones de área de cliente.

 

 