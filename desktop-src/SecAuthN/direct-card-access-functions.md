---
description: Al usar el subsistema de tarjeta inteligente, puede comunicarse con tarjetas que podrían no cumplir con las especificaciones ISO 7816.
ms.assetid: ea6cfa5a-2abf-4b7f-b3f4-99655266f030
title: Funciones de acceso directo a tarjetas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad360974210114a1069db3226ee814d08008cc98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907658"
---
# <a name="direct-card-access-functions"></a>Funciones de acceso directo a tarjetas

Al usar el subsistema de [*tarjeta inteligente*](/windows/desktop/SecGloss/s-gly) , puede comunicarse con tarjetas que podrían no cumplir con las especificaciones ISO 7816. Para ello, las siguientes funciones le permiten controlar los atributos de las comunicaciones entre la aplicación y la tarjeta, ya que le proporcionan una manipulación directa de bajo nivel del [*lector*](/windows/desktop/SecGloss/r-gly).

Para usar estas funciones, debe proporcionar un identificador para el atributo en cuestión. En el caso de los identificadores y valores de atributo válidos, consulte la tabla 3-1 en *requisitos para los dispositivos de interfaz de PC-Connected*.



| Tema                                    | Descripción                           |
|------------------------------------------|---------------------------------------|
| [**SCardControl**](/windows/desktop/api/Winscard/nf-winscard-scardcontrol)     | Proporcione el control directo del lector. |
| [**SCardGetAttrib**](/windows/desktop/api/Winscard/nf-winscard-scardgetattrib) | Obtiene los atributos del lector.                |
| [**SCardSetAttrib**](/windows/desktop/api/Winscard/nf-winscard-scardsetattrib) | Establezca el atributo de lector.                 |



 

 

 
