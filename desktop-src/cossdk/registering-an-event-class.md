---
description: Para que los suscriptores puedan encontrar una clase de eventos y suscribirse a ella, las clases de eventos deben estar registradas en el catálogo de COM+.
ms.assetid: b9d59b9d-52ba-4c71-9226-9cb5b93ec3d4
title: Registro de una clase de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07cceddaf01cff9677bb36ecc5315c15c1fa59e2c21046c3b7cd2bb4f3749f69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047303"
---
# <a name="registering-an-event-class"></a>Registro de una clase de eventos

Para que los suscriptores puedan encontrar una clase de eventos y suscribirse a ella, las clases de eventos deben estar registradas en el catálogo de COM+. COM+ requiere una biblioteca de tipos que describa las interfaces de eventos y los métodos para que puedan coincidir y conectar correctamente a suscriptores y publicadores. La biblioteca de tipos debe residir en o ir acompañada de un archivo DLL de registro propio.

Puede usar la herramienta administrativa Servicios de componentes o las funciones administrativas de COM+ para registrar una clase de eventos en el catálogo de COM+.

**Para registrar una clase de eventos con la herramienta administrativa Servicios de componentes**

1.  Crear una nueva aplicación COM+.

2.  Abra la carpeta de la aplicación y seleccione **Componentes**.

3.  En el menú **Acción**, haga clic en **Nuevo**. (También puede seleccionar la carpeta **Componentes,** hacer clic con el botón derecho, seleccionar **Nuevo** y, a continuación, hacer clic **en Componente**).

4.  Haga **clic en Install new event class(es) (Instalar nuevas clases de eventos).**

5.  Escriba la ruta de acceso al archivo DLL del componente de la clase de eventos.

6.  Haga clic en **Aceptar**.

La clase de eventos está registrada en el catálogo de COM+ y los suscriptores interesados en obtener la información proporcionada por la clase de eventos pueden encontrarla. Para obtener información sobre cómo registrar la clase de eventos mediante las interfaces administrativas de COM+, vea [**ICOMAdminCatalog::InstallEventClass**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installeventclass).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro de una suscripción](registering-a-subscription.md)
</dt> </dl>

 

 



