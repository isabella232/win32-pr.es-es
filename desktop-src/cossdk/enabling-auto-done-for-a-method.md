---
description: Puede habilitar la característica auto-done para cualquier método expuesto por un componente para el que esté habilitada la activación JIT de COM+. Si la activación JIT está deshabilitada, la función auto-done no está disponible.
ms.assetid: d699b85c-441f-4ea6-8d03-d1fa9a8a357f
title: Habilitar Auto-Done para un método
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58eec7a7b87284145ea880338bfe61db2aa1afca06f1f83ee811e4375a1e473c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637695"
---
# <a name="enabling-auto-done-for-a-method"></a>Habilitar Auto-Done para un método

Puede habilitar la característica auto-done para cualquier método expuesto por un componente para el que esté habilitada la activación JIT de COM+. Si la activación JIT está deshabilitada, la función auto-done no está disponible.

Debe habilitar auto-done solo para un método que se haya escrito intencionadamente para aprovecharlo, ya que esta característica puede cambiar potencialmente el comportamiento esperado del método.

Cuando se habilita la función auto-done, se cambia el comportamiento predeterminado de la activación JIT y las transacciones automáticas para ese método. Es posible que quiera usar esta característica porque puede quitar la necesidad de declarar explícitamente la coherencia y la realización. Esto se puede hacer simplemente devolviendo un HRESULT cuando se habilita la función auto-done. Básicamente, cuando se habilita la función auto-done, se indica a COM+ que haga lo siguiente:

-   Establezca el bit listo en True de forma predeterminada en el contexto en el que se ejecuta el objeto cada vez que se llama a este método.
-   Inspeccione el HRESULT devuelto por el método ; si indica SUCCESS o FAILURE, establezca el bit de coherencia en consecuencia. Esto puede dar lugar a una llamada automática a [**IObjectContext::SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete) o [**IObjectContext::SetAbort,**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setabort)dependiendo también de lo que haga internamente el método.

**Para habilitar la función auto-done para un método**

1.  En el panel de detalles de la herramienta administrativa Servicios de componentes, haga clic con el botón derecho en el método que desea configurar y, a continuación, haga clic en **Propiedades.**

2.  En el cuadro de diálogo propiedades del método , haga clic en **la pestaña General** .

3.  Para habilitar el proceso automático, active la **casilla Desactivar automáticamente este objeto cuando este método devuelva** . Si la casilla no está disponible, primero debe habilitar la activación JIT para el componente. (Consulte[Habilitación de la activación JIT para un componente para](enabling-jit-activation-for-a-component.md) obtener instrucciones detalladas).

4.  Haga clic en **Aceptar**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de activación Just-In-Time de COM+](com--just-in-time-activation-concepts.md)
</dt> <dt>

[Habilitación de la activación JIT para un componente](enabling-jit-activation-for-a-component.md)
</dt> <dt>

[Establecer el bit listo](setting-the-done-bit.md)
</dt> </dl>

 

 



