---
description: Habilitación de la activación JIT para un componente
ms.assetid: ccf7c98b-8b1a-431d-b417-83f79734f691
title: Habilitación de la activación JIT para un componente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f61cc5c79270a926bb50e3408766df63f4484c8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160503"
---
# <a name="enabling-jit-activation-for-a-component"></a>Habilitación de la activación JIT para un componente

Debe configurar un componente para que se active JIT solo cuando se escriba correctamente para admitir el servicio de activación Just-In-Time (JIT) de COM+. Si un componente se desactiva entre llamadas de método, perderá cualquier estado asociado. Dado el comportamiento predeterminado de la activación JIT, es poco probable que esto ocurra cuando no lo espera, pero debe tener en cuenta los requisitos de un componente antes de cambiar su configuración y de las expectativas de los clientes que llamarán al componente.

> [!Note]  
> Si un componente está configurado para requerir transacciones, el servicio de activación JIT de COM+ se habilita automáticamente. En este caso, no se puede deshabilitar. Para obtener más información, [vea Configuring Transactions](configuring-transactions.md).

 

Al habilitar la activación JIT para un componente, su atributo de sincronización se establece en requerido para ese componente. En este caso, no se puede cambiar la configuración de sincronización. Para obtener más información, vea [Dependencias de sincronización.](synchronization-dependencies.md)

**Para habilitar la activación JIT**

1.  En el panel de detalles de la herramienta administrativa Servicios de componentes, haga clic con el botón derecho en el componente que desea configurar y, a continuación, haga clic en **Propiedades.**

2.  En el cuadro de diálogo Propiedades del componente, haga clic en **la pestaña** Activación.

3.  Para habilitar la activación JIT para el componente, active la casilla Habilitar activación **Just-In-Time.**

4.  Haga clic en **OK**.

Cuando haya habilitado la activación JIT para un componente, tiene la opción de habilitar la característica auto-done para cualquier método expuesto por ese componente. Consulte [Habilitación de Auto-Done para un método para](enabling-auto-done-for-a-method.md) obtener más información.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Habilitar Auto-Done para un método](enabling-auto-done-for-a-method.md)
</dt> <dt>

[Establecer el bit listo](setting-the-done-bit.md)
</dt> </dl>

 

 



