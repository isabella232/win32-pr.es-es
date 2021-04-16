---
description: Habilitar la activación JIT para un componente
ms.assetid: ccf7c98b-8b1a-431d-b417-83f79734f691
title: Habilitar la activación JIT para un componente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f61cc5c79270a926bb50e3408766df63f4484c8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686446"
---
# <a name="enabling-jit-activation-for-a-component"></a>Habilitar la activación JIT para un componente

Debe configurar un componente para que se active JIT solo cuando se escribe correctamente para admitir el servicio de activación Just-in-Time (JIT) de COM+. Si un componente se desactiva entre las llamadas de método, perderá cualquier estado asociado. Dado el comportamiento predeterminado de la activación JIT, no es probable que se produzca cuando no se espera, pero debe tener en cuenta los requisitos de un componente antes de cambiar su configuración y de las expectativas de los clientes que llamarán al componente.

> [!Note]  
> Si un componente está configurado para requerir transacciones, el servicio de activación JIT de COM+ se habilita automáticamente. En este caso, no se puede deshabilitar. Para obtener más información, consulte [configuración de transacciones](configuring-transactions.md).

 

Cuando se habilita la activación JIT para un componente, su atributo de sincronización se establece en requerido para ese componente. En este caso, no se puede cambiar la configuración de sincronización. Para obtener más información, consulte [dependencias de sincronización](synchronization-dependencies.md).

**Para habilitar la activación JIT**

1.  En el panel de detalles de la herramienta administrativa Servicios de componentes, haga clic con el botón secundario en el componente que desee configurar y, a continuación, haga clic en **propiedades**.

2.  En el cuadro de diálogo Propiedades de componente, haga clic en la pestaña **activación** .

3.  Para habilitar la activación JIT para el componente, active la casilla **Habilitar activación Just-in-Time** .

4.  Haga clic en **OK**.

Cuando haya habilitado la activación JIT para un componente, tiene la opción de habilitar la característica de Autocompletar para cualquier método expuesto por ese componente. Consulte [habilitación de la función automática para un método](enabling-auto-done-for-a-method.md) para obtener más información.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Habilitar auto-Done para un método](enabling-auto-done-for-a-method.md)
</dt> <dt>

[Establecer el bit Done](setting-the-done-bit.md)
</dt> </dl>

 

 



