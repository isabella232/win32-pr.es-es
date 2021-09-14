---
description: Bring Your Own Transaction (BYOT)
ms.assetid: 492875cb-52a7-484f-810e-bd838373b603
title: Bring Your Own Transaction (BYOT)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16ca6f7f12babbf3ad183c4695a68591d9e181a1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126973573"
---
# <a name="bring-your-own-transaction-byot"></a>Bring Your Own Transaction (BYOT)

BYOT permite crear un componente con o heredar una transacción externa. Es decir, un componente que aún no tiene una transacción asociada puede adquirir una transacción. Actualmente, las transacciones MTS son automáticas; Si una instancia de componente reside en una transacción se determina en el momento de la creación. Los atributos transaccionales de un componente y su creador determinan qué transacción está asociada a una instancia determinada. En todos los casos, MTS controla la duración de las transacciones. COM+ amplía esto para permitir establecer una transacción DTC o TIP arbitraria preexistida como la propiedad de transacción del contexto de un nuevo componente. Esto permite que los componentes configurados se asocien a transacciones cuya duración se controla mediante un monitor tp, OTS o DBMS.

> [!Note]  
> Las transacciones BYOT se deben usar con precaución. En determinadas situaciones, pueden dar lugar a una transacción que abarca varios dominios de sincronización, es decir, permiten el paralelismo con una transacción, lo que provoca una condición de interbloqueo. Las transacciones automáticas, en lugar de las transacciones BYOT, son el modelo de programación preferido para los escritores de componentes empresariales.

 

Las interfaces para transacciones BYOT incluyen [**la interfaz ICreateWithTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) y la [**interfaz ICreateWithTipTransactionEx.**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex) La **interfaz ICreateWithTransactionEx** crea un objeto que se da de alta en una transacción manual. La **interfaz ICreateWithTipTransactionEx** crea un objeto que se da de alta dentro de una transacción manual mediante el Protocolo de Internet de transacciones (TIP).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Heredar transacciones manuales](inheriting-manual-transactions.md)
</dt> </dl>

 

 



