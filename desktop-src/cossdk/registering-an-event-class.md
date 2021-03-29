---
description: Para que los suscriptores puedan encontrar una clase de eventos y suscribirse a ella, las clases de eventos deben estar registradas en el catálogo de COM+.
ms.assetid: b9d59b9d-52ba-4c71-9226-9cb5b93ec3d4
title: Registrar una clase de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89a5968b8cb5981db3eb39c446104e1801a18e2e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807369"
---
# <a name="registering-an-event-class"></a>Registrar una clase de eventos

Para que los suscriptores puedan encontrar una clase de eventos y suscribirse a ella, las clases de eventos deben estar registradas en el catálogo de COM+. COM+ requiere una biblioteca de tipos que describa los métodos y las interfaces de eventos para que pueda coincidir y conectar correctamente los suscriptores y los publicadores. La biblioteca de tipos debe residir o ir acompañada de un archivo DLL de registro automático.

Puede usar la herramienta administrativa Servicios de componentes o las funciones administrativas de COM+ para registrar una clase de eventos en el catálogo de COM+.

**Para registrar una clase de eventos con la herramienta administrativa Servicios de componentes**

1.  Crear una nueva aplicación COM+.

2.  Abra la carpeta de la aplicación y seleccione **componentes**.

3.  En el menú **Acción**, haga clic en **Nuevo**. (También puede seleccionar la carpeta **componentes** , hacer clic con el botón secundario, elegir **nuevo** y hacer clic en **componente**).

4.  Haga clic en **instalar nuevas clases de eventos**.

5.  Escriba la ruta de acceso al archivo DLL del componente de la clase de evento.

6.  Haga clic en **OK**.

La clase de eventos se registra en el catálogo de COM+ y la pueden encontrar los suscriptores interesados en obtener la información proporcionada por la clase de eventos. Para obtener información sobre cómo registrar la clase de eventos mediante las interfaces administrativas de COM+, vea [**ICOMAdminCatalog:: InstallEventClass**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installeventclass).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro de una suscripción](registering-a-subscription.md)
</dt> </dl>

 

 



