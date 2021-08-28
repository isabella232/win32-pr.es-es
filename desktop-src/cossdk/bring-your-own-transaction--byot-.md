---
description: Bring Your Own Transaction (BYOT)
ms.assetid: 492875cb-52a7-484f-810e-bd838373b603
title: Bring Your Own Transaction (BYOT)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89b6177471d1c56956bba5fafd4f728a6295b29afcc6873495ddb690d2e59c12
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118308668"
---
# <a name="bring-your-own-transaction-byot"></a>Bring Your Own Transaction (BYOT)

BYOT permite crear un componente con o heredar una transacción externa. Es decir, un componente que aún no tiene una transacción asociada puede adquirir una transacción. Actualmente, las transacciones MTS son automáticas; si una instancia de componente reside en una transacción se determina en el momento de la creación. Los atributos transaccionales de un componente y su creador determinan qué transacción está asociada a una instancia determinada. En todos los casos, MTS controla la duración de las transacciones. COM+ lo amplía para permitir establecer una transacción DTC o TIP arbitraria preexistida como la propiedad de transacción del contexto de un nuevo componente. Esto permite asociar los componentes configurados a transacciones cuya duración se controla mediante un monitor TP, OTS o DBMS.

> [!Note]  
> Las transacciones BYOT se deben usar con precaución. En determinadas situaciones, pueden dar lugar a una transacción que abarca varios dominios de sincronización, es decir, permiten paralelismo con una transacción, lo que provoca una condición de interbloqueo. Las transacciones automáticas, en lugar de las transacciones BYOT, son el modelo de programación preferido para los escritores de componentes empresariales.

 

Las interfaces para las transacciones BYOT incluyen la interfaz [**ICreateWithTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) y la [**interfaz ICreateWithTipTransactionEx.**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex) La **interfaz ICreateWithTransactionEx** crea un objeto que se da de alta dentro de una transacción manual. La **interfaz ICreateWithTipTransactionEx** crea un objeto que se da de alta dentro de una transacción manual mediante el Protocolo de Internet de transacciones (TIP).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Heredar transacciones manuales](inheriting-manual-transactions.md)
</dt> </dl>

 

 



