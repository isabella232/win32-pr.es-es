---
description: Crear objetos BYOT
ms.assetid: 16b68ce2-46b2-4e35-bf92-f132dcb354e3
title: Crear objetos BYOT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9c2f0f999cb758a46dc779d29dac9fdfc71d2dbc245a84d1ca86060108e5663
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128776"
---
# <a name="creating-byot-objects"></a>Crear objetos BYOT

Un nuevo objeto BYOT crea objetos con transacciones manuales. Las dos interfaces, [**ICreateWithTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) e [**ICreateWithTipTransactionEx,**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex)tienen un único método, **CreateInstance**, que toma un puntero de interfaz **ITransaction** y una dirección URL de TIP, respectivamente. [**CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-icreatewithtransactionex-createinstance) devuelve un puntero de interfaz al objeto recién creado, que se inselecciona dentro de la transacción especificada.

Cuando se libera un objeto con una transacción manual, COM+ no intenta confirmar la transacción. El administrador de transacciones externo controla explícitamente la transacción en la que se ha creado este objeto.

> [!Note]  
> El objeto Byot.ByotServerEx debe importarse en una aplicación COM+.

 

 

 



