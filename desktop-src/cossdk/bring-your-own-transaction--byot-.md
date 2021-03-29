---
description: Traiga su propia transacción (transacciones)
ms.assetid: 492875cb-52a7-484f-810e-bd838373b603
title: Traiga su propia transacción (transacciones)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16ca6f7f12babbf3ad183c4695a68591d9e181a1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666192"
---
# <a name="bring-your-own-transaction-byot"></a>Traiga su propia transacción (transacciones)

La operación de transacciones permite crear un componente con o para heredar una transacción externa. Es decir, un componente que todavía no tiene una transacción asociada puede adquirir una transacción. Actualmente, las transacciones MTS son automáticas; Si una instancia de componente vive en una transacción se determina en el momento de la creación. Los atributos transaccionales de un componente y su creador determinan qué transacción está asociada a una instancia determinada. En todos los casos, MTS controla la duración de las transacciones. COM+ lo amplía para permitir la configuración de un DTC o una transacción TIP ya existentes como la propiedad de transacción del contexto de un componente nuevo. Esto permite asociar los componentes configurados con las transacciones cuya duración está controlada por un monitor de TP, un OTS o un DBMS.

> [!Note]  
> Las transacciones manuales deben usarse con precaución. En determinadas situaciones, pueden dar lugar a una transacción que abarque varios dominios de sincronización, es decir, que permiten el paralelismo con una transacción, lo que provoca una condición de interbloqueo. Las transacciones automáticas, en lugar de las transacciones manuales, son el modelo de programación preferido para escritores de componentes empresariales.

 

Las interfaces para las transacciones de transacciones manuales incluyen la interfaz [**ICreateWithTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) y la interfaz [**ICreateWithTipTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex) . La interfaz **ICreateWithTransactionEx** crea un objeto que se da de alta en una transacción manual. La interfaz **ICreateWithTipTransactionEx** crea un objeto que se da de alta en una transacción manual mediante el protocolo de Internet de transacciones (TIP).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Heredar transacciones manuales](inheriting-manual-transactions.md)
</dt> </dl>

 

 



