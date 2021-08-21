---
title: Visual Basic Interfaces privadas
description: Visual Basic Interfaces privadas
ms.assetid: 782e5d87-680e-4d0c-b1e6-cf97d1a37ce5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd69e70d351245ebafa62d521a133726be568a0437f4e04ece4ef761535f4625
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047713"
---
# <a name="visual-basic-private-interfaces"></a>Visual Basic Interfaces privadas

Dos interfaces implementadas por Visual Basic se identifican aquí para las categorías de componentes. No se espera que los controles requieran estas categorías, ya que es posible que los controles oferten una funcionalidad alternativa cuando no están disponibles.

La [**interfaz IVBFormat permite**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbformat) que los controles se integren mejor en el Visual Basic al dar formato a los datos.

CATID - {02496840-3AC4-11cf-87B9-00AA006C8166} CATID \_ VBFormat

La [**interfaz IVBGetControl**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbgetcontrol) permite que un control enumere otros controles en VB formulario.

CATID - {02496841-3AC4-11cf-87B9-00AA006C8166} CATID \_ VBGetControl

Aquí se describen dos interfaces privadas adicionales, [**IGetVBAObject**](/windows/desktop/api/VbInterf/nn-vbinterf-igetvbaobject) e [**IGetOleObject,**](/windows/desktop/api/VbInterf/nn-vbinterf-igetoleobject)aunque no definan categorías de componentes. No se recomienda el uso de estas cuatro interfaces porque no son compatibles con contenedores distintos de Visual Basic.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Categorías del componente](component-categories.md)
</dt> </dl>

 

 




