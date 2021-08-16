---
description: Una aplicación que se ejecuta como un usuario estándar realiza operaciones que requieren privilegios de administrador mediante la creación de un objeto De modelo de objetos componentes con privilegios elevados.
ms.assetid: 246fdf74-cc5b-47b1-b3a8-20441544e7be
title: Modelo de objetos COM de administrador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b331d71f83428ad821bc1c2f9de24984025aaf7f95874c2203ee9fb1f9158a88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784792"
---
# <a name="administrator-com-object-model"></a>Modelo de objetos COM de administrador

En el modelo de objetos COM de administrador, una aplicación que se ejecuta como un usuario estándar realiza operaciones que requieren privilegios de administrador mediante la creación de un objeto De modelo de [objetos componentes con](/windows/desktop/com/component-object-model--com--portal) privilegios elevados. Para obtener información sobre cómo crear un objeto COM con privilegios elevados, vea [The COM Elevation Moniker](../com/the-com-elevation-moniker.md).

Un inconveniente del uso del modelo de objetos COM de administrador es que se solicita al usuario cada vez que se realiza una operación con privilegios.

El propio objeto COM debe presentar cualquier interfaz de usuario que pueda controlar el objeto COM. De lo contrario, un proceso sin privilegios podría hacer que el objeto COM con privilegios elevados realice operaciones con privilegios sin que se solicite al usuario.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Desarrollo de aplicaciones que requieren privilegios de administrador](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[Modelo de Agente de administrador](administrator-broker-model.md)
</dt> <dt>

[Modelo de tareas con privilegios elevados](elevated-task-model.md)
</dt> <dt>

[Modelo de servicio de sistema operativo](operating-system-service-model.md)
</dt> </dl>

 

 
