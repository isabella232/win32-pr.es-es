---
title: Interfaces privadas de Visual Basic
description: Interfaces privadas de Visual Basic
ms.assetid: 782e5d87-680e-4d0c-b1e6-cf97d1a37ce5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5af32f46c02b9b76cdf3dd83e9a22a028aaa88d7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076368"
---
# <a name="visual-basic-private-interfaces"></a>Interfaces privadas de Visual Basic

Dos interfaces que se implementan mediante Visual Basic se identifican aquí para las categorías de componentes. No se espera que los controles requieran estas categorías porque es posible que los controles ofrezcan funcionalidad alternativa cuando no estén disponibles.

La interfaz [**IVBFormat**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbformat) permite que los controles se integren mejor en el entorno de Visual Basic al dar formato a los datos.

CATId-{02496840-3AC4-11cf-87B9-00AA006C8166} CATId \_ VBFormat

La interfaz [**IVBGetControl**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbgetcontrol) permite a un control enumerar otros controles en el formulario de VB.

CATId-{02496841-3AC4-11cf-87B9-00AA006C8166} CATId \_ VBGetControl

Aquí se describen dos interfaces privadas adicionales, [**IGetVBAObject**](/windows/desktop/api/VbInterf/nn-vbinterf-igetvbaobject) y [**IGetOleObject**](/windows/desktop/api/VbInterf/nn-vbinterf-igetoleobject), aunque no definen categorías de componentes. No se recomienda el uso de estas cuatro interfaces porque no son compatibles con los contenedores que no son Visual Basic.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Categorías del componente](component-categories.md)
</dt> </dl>

 

 




