---
description: Un &\# 0034;input context&0034; es una estructura interna mantenida \# por IMM.
ms.assetid: 2b639e30-5368-45bb-943d-db1ab6b62582
title: Contexto de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2927d3f573704aadb1ef72bdb26a35d37d90c1f90ab58d3a947ee84f8f38f7c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145904"
---
# <a name="input-context"></a>Contexto de entrada

Un "contexto de entrada" es una estructura interna mantenida por IMM. Contiene información sobre el estado del IME y lo usan las ventanas de IME. De forma predeterminada, el sistema operativo crea y asigna un contexto de entrada a cada subproceso. Dentro del subproceso, este contexto de entrada predeterminado es un recurso compartido y está asociado a cada ventana recién creada.

Para recuperar o establecer información en el IME, una aplicación que tenga en cuenta IME debe recuperar primero un identificador en el contexto de entrada asociado a una ventana especificada. La aplicación recupera el identificador mediante la [**función ImmGetContext.**](/windows/desktop/api/Imm/nf-imm-immgetcontext) Puede usar el identificador recuperado en llamadas posteriores a las funciones de IMM para recuperar y establecer valores IME, como el estilo de ventana de composición, el estilo de composición y la posición de la ventana de estado. Una vez que la aplicación ha terminado de usar el contexto, debe liberar el contexto mediante la [**función ImmReleaseContext.**](/windows/desktop/api/Imm/nf-imm-immreleasecontext)

Dado que el contexto de entrada predeterminado es un recurso compartido, los cambios que la aplicación realice en él se aplicarán a todas las ventanas del subproceso. Sin embargo, la aplicación puede invalidar este comportamiento predeterminado creando su propio contexto de entrada y asociándolo a una o varias ventanas del subproceso. Los cambios realizados en un contexto de entrada específico de la aplicación solo se aplican a las ventanas asociadas al contexto.

La aplicación puede crear un contexto de entrada mediante la [**función ImmCreateContext.**](/windows/desktop/api/Imm/nf-imm-immcreatecontext) Para asignar el contexto a una ventana, la aplicación llama a la [**función ImmAssociateContext.**](/windows/desktop/api/Imm/nf-imm-immassociatecontext) Esta función devuelve un identificador al contexto de entrada previamente asociado. Si la aplicación aún no ha asociado un contexto de entrada a la ventana, el identificador devuelto es para el contexto de entrada predeterminado. Normalmente, la aplicación guarda este identificador y, posteriormente, lo vuelve a asociar con la ventana cuando ya no se necesita el contexto de entrada personalizado.

Una vez que un contexto de entrada está asociado a una ventana, el sistema operativo selecciona automáticamente ese contexto cuando la ventana se activa y recibe el foco de entrada. El estilo y otra información en el contexto de entrada afectan a la entrada de teclado posterior para esa ventana, determinando cómo funciona el IME.

La aplicación debe destruir cualquier contexto de entrada personalizado antes de que finalice. En primer lugar, la aplicación quita el contexto de entrada de cualquier asociación que haya realizado con las ventanas del subproceso mediante la función [**ImmAssociateContext.**](/windows/desktop/api/Imm/nf-imm-immassociatecontext) A continuación, llama a [**la función ImmDestroyContext.**](/windows/desktop/api/Imm/nf-imm-immdestroycontext)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca del Administrador de métodos de entrada](about-input-method-manager.md)
</dt> </dl>

 

 



