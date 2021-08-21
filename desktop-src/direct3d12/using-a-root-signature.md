---
title: Uso de una firma raíz
description: La firma raíz es la definición de una colección organizada arbitrariamente de tablas de descriptores (incluido su diseño), constantes raíz y descriptores raíz.
ms.assetid: 0131CDE4-02DB-440A-92B8-B0933C6414B0
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d17fdefe5e0f6633cb81755a0344caba7823e24986334bdddba7f20eb309dfbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118806675"
---
# <a name="using-a-root-signature"></a>Uso de una firma raíz

La firma raíz es la definición de una colección organizada arbitrariamente de tablas de descriptores (incluido su diseño), constantes raíz y descriptores raíz. Cada entrada tiene un costo hacia un límite máximo, por lo que la aplicación puede equilibrar el equilibrio entre el número de entradas que contendrá la firma raíz.

-   [Semántica de la lista de comandos](#command-list-semantic)
-   [Semántica de agrupación](#bundle-semantics)
-   [Temas relacionados](#related-topics)

La firma raíz es un objeto que se puede crear mediante especificación manual en la API. Todos los sombreadores de un PSO deben ser compatibles con el diseño raíz especificado con el PSO o, de lo contrario, los sombreadores individuales deben incluir diseños raíz incrustados que coincidan entre sí. De lo contrario, se producirá un error en la creación del PSO. Una propiedad de la firma raíz es que los sombreadores no tienen que conocerla cuando se han creado, aunque las firmas raíz también se pueden crear directamente en sombreadores si se desea. Los recursos de sombreador existentes no requieren que los cambios sean compatibles con las firmas raíz. El modelo de sombreador 5.1 se introdujo para proporcionar cierta flexibilidad adicional (indexación dinámica de descriptores desde dentro de los sombreadores) y se puede adoptar incrementalmente a partir de los recursos de sombreador existentes según sea necesario.

## <a name="command-list-semantic"></a>Semántica de la lista de comandos

Al principio de una lista de comandos, la firma raíz no está definida. Los sombreadores de gráficos tienen una firma raíz independiente del sombreador de proceso, cada uno asignado de forma independiente en una lista de comandos. La firma raíz establecida en una lista de comandos o agrupación también debe coincidir con el PSO establecido actualmente en Draw/Dispatch; de lo contrario, el comportamiento es indefinido. Las discrepancias de firma raíz transitorias antes de Draw/Dispatch son buenas, como establecer un PSO incompatible antes de cambiar a una firma raíz compatible (siempre que sean compatibles en el momento en que se llama a Draw/Dispatch). Establecer un PSO no cambia la firma raíz. La aplicación debe llamar a una API dedicada para establecer la firma raíz.

Una vez que se ha establecido una firma raíz en una lista de comandos, el diseño define el conjunto de enlaces que se espera que proporcione la aplicación y qué PSO se pueden usar (los compilados con el mismo diseño) para las siguientes llamadas de draw/dispatch. Por ejemplo, la aplicación podría definir una firma raíz para que tenga las siguientes entradas. Cada entrada se conoce como "ranura".

-   \[0 \] Un descriptor CBV en línea (descriptores raíz)
-   \[1 \] Tabla de descriptores que contiene 2 SRV, 1 CBV y 1 UAV
-   \[2 \] Tabla de descriptores que contiene 1 sampler
-   \[3 Colección de constantes raíz \] de 4x32 bits
-   \[4 \] Tabla de descriptores que contiene un número no especificado de SRV

En este caso, antes de poder emitir un Draw/Dispatch, se espera que la aplicación establezca el enlace adecuado en cada una de las ranuras 0..4 que la aplicación definió con su firma \[ \] raíz actual. Por ejemplo, en la ranura 1, se debe enlazar una tabla de descriptores, que es una región contigua en un montón de descriptores que contiene (o contendrá en \[ \] ejecución) 2 SRV, 1 CBV y 1 UAV. Del mismo modo, las tablas de descriptores deben establecerse en las ranuras \[ 2 \] y \[ 4 \] .

La aplicación puede cambiar parte de los enlaces de firma raíz a la vez (el resto permanece sin cambios). Por ejemplo, si lo único que necesita cambiar entre los draws es una de las constantes de la ranura 2, es decir, todo lo que la aplicación necesita volver a \[ \] enlatar. Como se ha comentado anteriormente, el controlador o el hardware versiones de todo el estado de enlace de firma raíz a medida que se modifica automáticamente. Si se cambia una firma raíz en una lista de comandos, todos los enlaces de firma raíz anteriores se vuelven obsoletos y todos los enlaces recién esperados deben establecerse antes de Draw/Dispatch; de lo contrario, el comportamiento es indefinido. Si la firma raíz se establece de forma redundante en la misma establecida actualmente, los enlaces de firma raíz existentes no se vuelven obsoletos.

## <a name="bundle-semantics"></a>Semántica de agrupación

Los paquetes heredan los enlaces de firma raíz de la lista de comandos (los enlaces a las distintas ranuras del ejemplo de lista de comandos anterior). Si una agrupación necesita cambiar algunos de los enlaces de firma raíz heredados, primero debe establecer la firma raíz para que sea la misma que la lista de comandos de llamada (los enlaces heredados no se vuelven obsoletos). Si la agrupación establece que la firma raíz sea diferente de la lista de comandos que realiza la llamada, esto tiene el mismo efecto que cambiar la firma raíz en la lista de comandos descrita anteriormente: todos los enlaces de firma raíz anteriores son obsoletos y los enlaces recién esperados deben establecerse antes de Draw/Dispatch; De lo contrario, el comportamiento es indefinido. Si una agrupación no necesita cambiar ningún enlace de firma raíz, no es necesario establecer la firma raíz.

En el código siguiente se muestra un flujo de llamadas de ejemplo en una agrupación.

``` syntax
// Command List
...
pCmdList->SetGraphicsRootSignature(pRootSig); // new parameter space
MyEngine_SetTextures(); // bundle inherits descriptor table setting
MyEngine_SetAnimationFactor(fTime); // bundle inherits root constant
pCmdList->ExecuteBundle(...);
...
// Bundle
pBundle->SetGraphicsRootSignature(pRootSig); // same as caller, in order to inherits bindings
pBundle->SetPipelineState(pPS); 
pBundle->SetGraphicsRoot32BitConstant(drawConstantsSlot,0,drawIDOffset);
pBundle->Draw(...); // using inherited textures / animation factor
pBundle->SetGraphicsRoot32BitConstant(drawConstantsSlot,1,drawIDOffset);
pBundle->Draw(...);
...
```

Al salir de una agrupación, los cambios de diseño raíz o los cambios de enlace que realiza una agrupación se heredan de nuevo a la lista de comandos de llamada cuando finaliza la ejecución de un paquete.

Para obtener más información sobre la herencia, consulte la sección **Herencia** de estado de canalización de gráficos de Administración del estado de canalización de [gráficos en Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Firmas raíz](root-signatures.md)
</dt> </dl>

 

 




