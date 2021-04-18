---
description: Puede habilitar la característica auto-Done para cualquier método expuesto por un componente para el que esté habilitada la activación JIT de COM+. Si la activación JIT está deshabilitada, la operación automática no está disponible.
ms.assetid: d699b85c-441f-4ea6-8d03-d1fa9a8a357f
title: Habilitar auto-Done para un método
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0130e5f8b2fde6c6755ef4174892aa35be8a24cd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714871"
---
# <a name="enabling-auto-done-for-a-method"></a>Habilitar auto-Done para un método

Puede habilitar la característica auto-Done para cualquier método expuesto por un componente para el que esté habilitada la activación JIT de COM+. Si la activación JIT está deshabilitada, la operación automática no está disponible.

Debe habilitar la función auto-Done solo para un método que se ha escrito intencionadamente para aprovecharlo porque esta característica puede cambiar el comportamiento esperado del método.

Cuando habilita auto-Done, cambia el comportamiento predeterminado de la activación JIT y las transacciones automáticas para ese método. Puede que desee usar esta característica porque puede quitar la necesidad de declarar explícitamente la coherencia y la realización. En su lugar, esto se puede hacer simplemente devolviendo un valor HRESULT cuando está habilitada la operación automática. En esencia, cuando se habilita auto-Done, se indica a COM+ que haga lo siguiente:

-   Establezca el bit done en true de forma predeterminada en el contexto en el que se ejecuta el objeto cada vez que se llama a este método.
-   Inspeccione el HRESULT devuelto por el método; Si indica éxito o error, establezca el bit de coherencia en consecuencia. Esto puede dar lugar a una llamada automática a [**IObjectContext:: SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) o [**IObjectContext:: SetAbort**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort), dependiendo también de lo que el método hace internamente.

**Para habilitar la función automática para un método**

1.  En el panel de detalles de la herramienta administrativa Servicios de componentes, haga clic con el botón secundario en el método que desee configurar y, a continuación, haga clic en **propiedades**.

2.  En el cuadro de diálogo Propiedades del método, haga clic en la pestaña **General** .

3.  Para habilitar la función automática, active la casilla **desactivar automáticamente este objeto cuando se devuelva este método** . Si la casilla no está disponible, primero debe habilitar la activación JIT para el componente. (Consulte[habilitación de la activación JIT para un componente](enabling-jit-activation-for-a-component.md) para obtener instrucciones detalladas).

4.  Haga clic en **OK**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de activación Just-in-Time de COM+](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Habilitar la activación JIT para un componente](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[Establecer el bit Done](setting-the-done-bit.md)
</dt> </dl>

 

 



