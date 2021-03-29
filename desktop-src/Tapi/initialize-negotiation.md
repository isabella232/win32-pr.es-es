---
description: El \_ tipo de DataType Initialize de negociación es un valor especial de tipo DWORD.
ms.assetid: ce978913-47a1-4387-bd1b-1795aaf82dd7
title: INITIALIZE_NEGOTIATION
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51a55879a0952d3f8b5e268ec6a01a666bdbf5ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811215"
---
# <a name="initialize_negotiation"></a>INICIALIZAr \_ negociación

El tipo de DataType **Initialize de \_ negociación** es un valor especial de tipo **DWORD**. Se puede pasar como el parámetro *dwDeviceID* en las funciones [**TSPI \_ lineNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion) y [**TSPI \_ phoneNegotiateTSPIVersion**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiatetspiversion) . Esto indica que TAPI puede negociar un número de versión de la interfaz TSPI independientemente de cualquier dispositivo específico.

 

 
