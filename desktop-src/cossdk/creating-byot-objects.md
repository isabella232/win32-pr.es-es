---
description: Crear objetos de transacciones
ms.assetid: 16b68ce2-46b2-4e35-bf92-f132dcb354e3
title: Crear objetos de transacciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6544c5085061be5d1100706930a3e1617ec24890
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105705306"
---
# <a name="creating-byot-objects"></a>Crear objetos de transacciones

Un nuevo objeto de transacciones crea objetos con transacciones manuales. Las dos interfaces, [**ICreateWithTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) y [**ICreateWithTipTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex), tienen un único método, **CreateInstance**, que toma un puntero de interfaz de **ITransaction** y una dirección URL de sugerencia, respectivamente. [**CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-icreatewithtransactionex-createinstance) devuelve un puntero de interfaz al objeto recién creado, que se da de alta en la transacción especificada.

Cuando se libera un objeto con una transacción manual, COM+ no intenta confirmar la transacción. La transacción se controla explícitamente por el administrador de transacciones externo que disponía la transacción en la que se creó este objeto.

> [!Note]  
> El objeto de transacciones. ByotServerEx se debe importar en una aplicación COM+.

 

 

 



