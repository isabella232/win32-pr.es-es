---
description: Microsoft telefonía modela los botones y las lámparas de un teléfono como pares de luces de botón.
ms.assetid: 6ac912bb-8d2b-4aa3-a6e8-af86fbaabd58
title: Botones (API de telefonía)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd1fc18e02331f98f4dbb98cfea7d9df2ca7f33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677621"
---
# <a name="buttons-telephony-api"></a>Botones (API de telefonía)

Microsoft telefonía modela los botones y las lámparas de un teléfono como pares de luces de botón. Un botón sin luz junto a él o una lámpara sin botón se especifica mediante un indicador ficticio para el botón o lámpara que falta. Un botón con varias lámparas se modela con varios pares de luz de botón.

La información asociada a un botón de teléfono se puede establecer y recuperar. Cuando se presiona un botón, el proveedor de servicios envía un mensaje de [**\_ botón de teléfono**](/previous-versions/windows/desktop/legacy/ms725254(v=vs.85)) a la función de devolución de llamada TAPI. Los parámetros de este mensaje son un identificador del dispositivo telefónico y el identificador de botón o lámpara del botón que se presionó. Al botón del teclado ' 0 ' a ' 9 ', ' \* ' y ' \# ' se les asignan los identificadores de botón/lámpara fijos del 0 al 11.

La función [**TSPI \_ phoneSetButtonInfo**](/windows/win32/api/tspi/nf-tspi-tspi_phonesetbuttoninfo) establece la información asociada a un botón en un dispositivo telefónico. [**TSPI \_ phoneGetButtonInfo**](/windows/win32/api/tspi/nf-tspi-tspi_phonegetbuttoninfo) devuelve información asociada a un botón en un dispositivo telefónico. El proveedor de servicios envía un \_ mensaje de botón de teléfono a la función de devolución de llamada TAPI cuando se presiona un botón del teléfono.

La información asociada a un botón no lleva ningún significado semántico en lo que se refiere a TSPI. Resulta útil para aplicaciones específicas del dispositivo que interpretan esta información para un dispositivo telefónico determinado, o para que se muestre al usuario, como en el sistema de ayuda de una aplicación.

 

 
