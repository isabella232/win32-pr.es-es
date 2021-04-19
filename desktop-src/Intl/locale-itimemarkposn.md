---
description: configuración regional \_ ITIMEMARKPOSN
ms.assetid: 4aef2631-c05b-41e8-8f4d-f40da4143ab4
title: LOCALE_ITIMEMARKPOSN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0182235754d8f5b6b95bad6c58b4fee87d394d4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105689564"
---
# <a name="locale_itimemarkposn"></a>configuración regional \_ ITIMEMARKPOSN

Especificador que indica si la cadena de marcador de hora (AM o PM) precede o sigue a la cadena de hora. El valor del registro es iTimePrefix para la compatibilidad con versiones asiáticas anteriores de Windows. El especificador debe tener uno de los valores siguientes. No se permiten valores especificados por el usuario. Es preferible que la aplicación use la constante [ \_ STIMEFORMAT de configuración regional](locale-stime-constants.md) en lugar de la configuración regional \_ ITIMEMARKPOSN.



| Value | Significado        |
|-------|----------------|
| 0     | Use como sufijo. |
| 1     | Use como prefijo. |



 

 

 



