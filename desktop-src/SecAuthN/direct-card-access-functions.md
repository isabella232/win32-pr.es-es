---
description: Mediante el subsistema de tarjetas inteligentes, puede comunicarse con tarjetas que no se ajusten a las especificaciones iso 7816.
ms.assetid: ea6cfa5a-2abf-4b7f-b3f4-99655266f030
title: Funciones de acceso directo a tarjetas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad360974210114a1069db3226ee814d08008cc98
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171258"
---
# <a name="direct-card-access-functions"></a>Funciones de acceso directo a tarjetas

Mediante el subsistema [*de tarjetas inteligentes,*](/windows/desktop/SecGloss/s-gly) puede comunicarse con tarjetas que no se ajusten a las especificaciones iso 7816. Para ello, las siguientes funciones permiten controlar los atributos de las comunicaciones entre la aplicación y la tarjeta, ya que le permiten manipular el lector de forma directa y de bajo [*nivel.*](/windows/desktop/SecGloss/r-gly)

Para usar estas funciones, debe proporcionar un identificador para el atributo en cuestión. Para obtener valores y identificadores de atributo válidos, consulte la tabla 3-1 en *Requisitos para PC-Connected dispositivos de interfaz .*



| Tema                                    | Descripción                           |
|------------------------------------------|---------------------------------------|
| [**SCardControl**](/windows/desktop/api/Winscard/nf-winscard-scardcontrol)     | Proporcione el control directo del lector. |
| [**SCardGetAttrib**](/windows/desktop/api/Winscard/nf-winscard-scardgetattrib) | Obtiene los atributos del lector.                |
| [**SCardSetAttrib**](/windows/desktop/api/Winscard/nf-winscard-scardsetattrib) | Establezca el atributo reader.                 |



 

 

 
