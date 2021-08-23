---
description: Mediante el subsistema de tarjetas inteligentes, puede comunicarse con tarjetas que no se ajusten a las especificaciones iso 7816.
ms.assetid: ea6cfa5a-2abf-4b7f-b3f4-99655266f030
title: Funciones de acceso directo a tarjetas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d72b606cd766ea9a8930599bd2a44e117dea0bffdef6474c038b39294c08acf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008463"
---
# <a name="direct-card-access-functions"></a>Funciones de acceso directo a tarjetas

Mediante el subsistema [*de tarjetas inteligentes,*](/windows/desktop/SecGloss/s-gly) puede comunicarse con tarjetas que no se ajusten a las especificaciones iso 7816. Para ello, las siguientes funciones permiten controlar los atributos de las comunicaciones entre la aplicación y la tarjeta, ya que le permiten manipular el lector de forma directa y de bajo [*nivel.*](/windows/desktop/SecGloss/r-gly)

Para usar estas funciones, debe proporcionar un identificador para el atributo en cuestión. Para obtener valores y identificadores de atributo válidos, consulte la tabla 3-1 en *Requisitos para PC-Connected dispositivos de interfaz .*



| Tema                                    | Descripción                           |
|------------------------------------------|---------------------------------------|
| [**SCardControl**](/windows/desktop/api/Winscard/nf-winscard-scardcontrol)     | Proporcione el control directo del lector. |
| [**SCardGetAttrib**](/windows/desktop/api/Winscard/nf-winscard-scardgetattrib) | Obtiene los atributos del lector.                |
| [**SCardSetAttrib**](/windows/desktop/api/Winscard/nf-winscard-scardsetattrib) | Establezca el atributo reader.                 |



 

 

 
