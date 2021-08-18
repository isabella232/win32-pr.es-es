---
description: Después de determinar las funcionalidades de un dispositivo de teléfono, una aplicación debe abrir el dispositivo para poder acceder a las funciones de ese teléfono.
ms.assetid: 0215db43-b4d7-4a1e-8d4f-d17013c14e61
title: Apertura y cierre de Teléfono dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6dacda3e98e96ed4a11334443a7b99b949e6d1b3823e42e1790c5a346b52dac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012525"
---
# <a name="opening-and-closing-phone-devices"></a>Apertura y cierre de Teléfono dispositivos

Después de determinar las funcionalidades de un dispositivo de teléfono, una aplicación debe abrir el dispositivo para poder acceder a las funciones de ese teléfono. Una vez que se ha abierto correctamente un dispositivo de teléfono, se devuelve a la aplicación un identificador que representa el teléfono abierto. Un dispositivo de teléfono se puede abrir en diferentes modos, lo que proporciona una manera estructurada de compartir un dispositivo de teléfono.

La [**función phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) abre el dispositivo telefónico especificado para proporcionar a la aplicación acceso a funciones en el teléfono. Un dispositivo de teléfono se identifica como **phoneOpen por** medio de su identificador de dispositivo, que se pasa como el *parámetro dwDeviceID.*

 

 



