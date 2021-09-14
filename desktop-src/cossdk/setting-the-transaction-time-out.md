---
description: Puede establecer manualmente el tiempo de espera para las transacciones mediante la herramienta administrativa Servicios de componentes, o bien puede configurar el tiempo de espera mediante programación mediante las interfaces de administración de COM+.
ms.assetid: f7a35bdf-ea6d-40ea-b3c0-c2a3ae2276c4
title: Establecer el valor de Transaction Time-Out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b002448ca21e97e2e4996679d87a4b6a7680161f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361663"
---
# <a name="setting-the-transaction-time-out"></a>Establecer el valor de Transaction Time-Out

Puede establecer manualmente el tiempo de espera para las transacciones mediante la herramienta administrativa Servicios de componentes, o bien puede configurar mediante programación el tiempo de espera mediante las interfaces de administración [de COM+.](com--administration-interfaces.md) El tiempo de espera se puede configurar en el nivel de equipo local y también para componentes individuales.

**Para establecer el tiempo de espera de transacción para el equipo local mediante la herramienta administrativa Servicios de componentes**

1.  En el árbol de consola, haga clic con el botón derecho en el equipo local que desea configurar y, a continuación, haga clic en **Propiedades.**

2.  En el cuadro de diálogo Propiedades del equipo, haga clic en **la pestaña** Opciones.

3.  En **Tiempo de espera de** transacción , escriba el tiempo de espera de la transacción en segundos. El tiempo de espera predeterminado es de 60 segundos.

4.  Haga clic en **OK**.

**Para establecer el tiempo de espera de transacción para un componente mediante la herramienta administrativa Servicios de componentes**

1.  En el árbol de consola, haga clic con el botón derecho en el componente que desea configurar y, a continuación, haga clic en **Propiedades.**

2.  En el cuadro de diálogo Propiedades del componente, haga clic **en la pestaña** Transacciones .

3.  Active la casilla Override **global transaction timeout value (Invalidar valor de tiempo de espera de transacción global).**

    > [!Note]  
    > No puede marcar la casilla para invalidar el  valor de tiempo de espera de transacción global si la compatibilidad con transacciones está establecida en **Deshabilitado,** No admitido o **Admitido.**

     

4.  En **Tiempo de espera de** transacción , escriba el tiempo de espera de la transacción en segundos. El tiempo de espera predeterminado es de 0 segundos, lo que significa que el componente nunca hará que la transacción se resalte.

5.  Haga clic en **OK**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administración de transacciones automáticas en COM+](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



