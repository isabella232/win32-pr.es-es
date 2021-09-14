---
title: Visual Basic Interfaces privadas
description: Visual Basic Interfaces privadas
ms.assetid: 782e5d87-680e-4d0c-b1e6-cf97d1a37ce5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5af32f46c02b9b76cdf3dd83e9a22a028aaa88d7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127358920"
---
# <a name="visual-basic-private-interfaces"></a>Visual Basic Interfaces privadas

Aquí se identifican dos interfaces implementadas por Visual Basic para las categorías de componentes. No se espera que los controles requieran estas categorías, ya que es posible que estos ofrecimientos de funcionalidad alternativa cuando estos no estén disponibles.

La [**interfaz IVBFormat**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbformat) permite que los controles se integren mejor en el Visual Basic al dar formato a los datos.

CATID - {02496840-3AC4-11cf-87B9-00AA006C8166} CATID \_ VBFormat

La [**interfaz IVBGetControl**](/windows/desktop/api/VbInterf/nn-vbinterf-ivbgetcontrol) permite que un control enumere otros controles en el VB formulario.

CATID - {02496841-3AC4-11cf-87B9-00AA006C8166} CATID \_ VBGetControl

Aquí se describen dos interfaces privadas adicionales, [**IGetVBAObject**](/windows/desktop/api/VbInterf/nn-vbinterf-igetvbaobject) e [**IGetOleObject,**](/windows/desktop/api/VbInterf/nn-vbinterf-igetoleobject)aunque no definan categorías de componentes. No se recomienda el uso de estas cuatro interfaces porque no son compatibles con contenedores que no sean Visual Basic.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Categorías del componente](component-categories.md)
</dt> </dl>

 

 




