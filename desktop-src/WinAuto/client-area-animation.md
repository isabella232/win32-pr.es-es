---
title: Parámetro de animación del área de cliente
description: La marca de animación del área de cliente indica si el usuario desea deshabilitar las animaciones en elementos de la interfaz de usuario.
ms.assetid: 4a3ec9da-d5ae-4cd9-8222-f02143895ce4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c62e25fdb08022d53cbe9e818a0a1089988cd6a6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104271362"
---
# <a name="client-area-animation-parameter"></a>Parámetro de animación del área de cliente

El parámetro de animación del área de cliente indica si el usuario desea deshabilitar las animaciones en elementos de la interfaz de usuario. La visualización de características como el parpadeo, el parpadeo, el parpadeo y el traslado de contenido pueden provocar ataques a los usuarios con una epilepsia sensible a la fotografía. Este parámetro permite habilitar o deshabilitar todas las animaciones de este tipo.

Las aplicaciones usan las marcas **SPI \_ GETCLIENTAREAANIMATION** y **SPI \_ SETCLIENTAREAANIMATION** con la función [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) para activar o desactivar las animaciones del área de cliente.

 

 