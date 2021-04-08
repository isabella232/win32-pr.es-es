---
description: Puede establecer manualmente el nivel de aislamiento de transacción de los componentes mediante la herramienta administrativa Servicios de componentes, o bien puede configurar mediante programación el nivel de aislamiento de transacción para un componente mediante las interfaces de administración de COM+.
ms.assetid: 3ef5b805-334d-4803-be67-00c9e35cdcc6
title: Establecer el nivel de aislamiento de la transacción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b0447af2591c4f4b3e8e76c017157c02908367
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807783"
---
# <a name="setting-the-transaction-isolation-level"></a>Establecer el nivel de aislamiento de la transacción

Puede establecer manualmente el nivel de aislamiento de transacción de los componentes mediante la herramienta administrativa Servicios de componentes, o bien puede configurar mediante programación el nivel de aislamiento de transacción para un componente mediante las [interfaces de administración de com+](com--administration-interfaces.md).

Para más información sobre los niveles de aislamiento de transacción, consulte [configuración de los niveles de aislamiento de transacción](configuring-transaction-isolation-levels.md).

**Para establecer el nivel de aislamiento de transacción mediante la herramienta administrativa Servicios de componentes**

1.  En el árbol de consola, haga clic con el botón secundario en el componente que desee configurar y, a continuación, haga clic en **propiedades**.

2.  En el cuadro de diálogo Propiedades de componente, haga clic en la pestaña **transacciones** .

3.  En **nivel de aislamiento de transacción**, seleccione el valor que desee en el cuadro desplegable. Se **serializa** el valor predeterminado de todos los componentes.

    > [!Note]  
    > Si está seleccionada la opción **deshabilitada** o **no admitida** en **compatibilidad con transacciones**, no se puede establecer el nivel de aislamiento de transacción.

     

4.  Haga clic en **OK**.

Debe repetir este procedimiento para cada componente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de los niveles de aislamiento de transacción](configuring-transaction-isolation-levels.md)
</dt> </dl>

 

 



