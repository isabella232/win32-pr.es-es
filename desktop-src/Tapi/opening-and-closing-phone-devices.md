---
description: Después de determinar las capacidades de un dispositivo de teléfono, una aplicación debe abrir el dispositivo antes de poder acceder a las funciones de ese teléfono.
ms.assetid: 0215db43-b4d7-4a1e-8d4f-d17013c14e61
title: Apertura y cierre de dispositivos telefónicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4692901d09c680276bda1a5dba77bc57ce599e77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677473"
---
# <a name="opening-and-closing-phone-devices"></a>Apertura y cierre de dispositivos telefónicos

Después de determinar las capacidades de un dispositivo de teléfono, una aplicación debe abrir el dispositivo antes de poder acceder a las funciones de ese teléfono. Una vez que un dispositivo telefónico se ha abierto correctamente, se devuelve un identificador que representa el teléfono abierto a la aplicación. Un dispositivo telefónico se puede abrir en modos diferentes, lo que proporciona una manera estructurada de compartir un dispositivo telefónico.

La función [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) abre el dispositivo de teléfono especificado para conceder a la aplicación acceso a las funciones del teléfono. Un dispositivo telefónico se identifica como **phoneOpen** por medio de su identificador de dispositivo, que se pasa como el parámetro *dwDeviceID* .

 

 



