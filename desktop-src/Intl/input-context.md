---
description: Un &\# 0034; contexto de entrada&\# 0034; es una estructura interna que mantiene el IMM.
ms.assetid: 2b639e30-5368-45bb-943d-db1ab6b62582
title: Contexto de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16f1f83a397373e17a7d637b61a3232a3d72acde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909498"
---
# <a name="input-context"></a>Contexto de entrada

Un "contexto de entrada" es una estructura interna mantenida por el IMM. Contiene información sobre el estado del IME y lo usan las ventanas de IME. De forma predeterminada, el sistema operativo crea y asigna un contexto de entrada a cada subproceso. En el subproceso, este contexto de entrada predeterminado es un recurso compartido y está asociado a cada ventana recién creada.

Para recuperar o establecer información en el IME, una aplicación que tenga en cuenta el IME debe recuperar primero un identificador para el contexto de entrada asociado a una ventana especificada. La aplicación recupera el identificador mediante la función [**ImmGetContext**](/windows/desktop/api/Imm/nf-imm-immgetcontext) . Puede usar el controlador recuperado en las llamadas posteriores a las funciones de IMM para recuperar y establecer valores de IME, como el estilo de la ventana de composición, el estilo de composición y la posición de la ventana de estado. Una vez que la aplicación ha terminado de usar el contexto, debe liberar el contexto mediante la función [**ImmReleaseContext**](/windows/desktop/api/Imm/nf-imm-immreleasecontext) .

Dado que el contexto de entrada predeterminado es un recurso compartido, todos los cambios que realiza la aplicación se aplican a todas las ventanas del subproceso. Sin embargo, la aplicación puede invalidar este comportamiento predeterminado mediante la creación de su propio contexto de entrada y su asociación con una o más ventanas del subproceso. Los cambios realizados en un contexto de entrada específico de la aplicación se aplican solo a las ventanas asociadas al contexto.

La aplicación puede crear un contexto de entrada mediante la función [**ImmCreateContext**](/windows/desktop/api/Imm/nf-imm-immcreatecontext) . Para asignar el contexto a una ventana, la aplicación llama a la función [**ImmAssociateContext**](/windows/desktop/api/Imm/nf-imm-immassociatecontext) . Esta función devuelve un identificador al contexto de entrada asociado previamente. Si la aplicación aún no ha asociado un contexto de entrada con la ventana, el identificador devuelto es para el contexto de entrada predeterminado. Normalmente, la aplicación guarda este identificador y después lo vuelve a asociar a la ventana cuando el contexto de entrada personalizado ya no se necesita.

Una vez que un contexto de entrada se asocia a una ventana, el sistema operativo selecciona automáticamente ese contexto cuando la ventana se activa y recibe el foco de entrada. El estilo y otra información del contexto de entrada afecta a la entrada de teclado subsiguiente para esa ventana, lo que determina la forma en que funciona el IME.

La aplicación debe destruir cualquier contexto de entrada personalizado antes de finalizar. En primer lugar, la aplicación quita el contexto de entrada de cualquier asociación que haya realizado con Windows en el subproceso mediante la función [**ImmAssociateContext**](/windows/desktop/api/Imm/nf-imm-immassociatecontext) . A continuación, llama a la función [**ImmDestroyContext**](/windows/desktop/api/Imm/nf-imm-immdestroycontext) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca del administrador de métodos de entrada](about-input-method-manager.md)
</dt> </dl>

 

 



