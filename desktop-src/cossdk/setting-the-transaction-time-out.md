---
description: Puede establecer manualmente el tiempo de espera para las transacciones mediante la herramienta administrativa Servicios de componentes, o bien puede configurar el tiempo de espera mediante programación con las interfaces de administración de COM+.
ms.assetid: f7a35bdf-ea6d-40ea-b3c0-c2a3ae2276c4
title: Establecer la Time-Out de transacciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b002448ca21e97e2e4996679d87a4b6a7680161f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496589"
---
# <a name="setting-the-transaction-time-out"></a>Establecer la Time-Out de transacciones

Puede establecer manualmente el tiempo de espera para las transacciones mediante la herramienta administrativa Servicios de componentes, o bien puede configurar el tiempo de espera mediante programación con las [interfaces de administración de com+](com--administration-interfaces.md). El tiempo de espera se puede configurar en el nivel de equipo local y también para componentes individuales.

**Para establecer el tiempo de espera de la transacción para el equipo local mediante la herramienta administrativa Servicios de componentes**

1.  En el árbol de consola, haga clic con el botón secundario en el equipo local que desee configurar y, a continuación, haga clic en **propiedades**.

2.  En el cuadro de diálogo Propiedades del equipo, haga clic en la pestaña **Opciones** .

3.  En tiempo de **espera de transacción**, escriba el tiempo de espera de la transacción en segundos. El tiempo de espera predeterminado es de 60 segundos.

4.  Haga clic en **OK**.

**Para establecer el tiempo de espera de la transacción para un componente mediante la herramienta administrativa Servicios de componentes**

1.  En el árbol de consola, haga clic con el botón secundario en el componente que desee configurar y, a continuación, haga clic en **propiedades**.

2.  En el cuadro de diálogo Propiedades de componente, haga clic en la pestaña **transacciones** .

3.  Active la casilla de verificación **invalidar el valor de tiempo de espera de la transacción global**.

    > [!Note]  
    > No se puede activar la casilla para invalidar el valor de tiempo de espera de la transacción global si la **compatibilidad con transacciones** está establecida en **deshabilitado**, **no compatible o no** **compatible**.

     

4.  En tiempo de **espera de transacción**, escriba el tiempo de espera de la transacción en segundos. El tiempo de espera predeterminado es de 0 segundos, lo que significa que el componente nunca hará que se agote el tiempo de espera de la transacción.

5.  Haga clic en **OK**.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Administrar transacciones automáticas en COM+](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



