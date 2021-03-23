---
title: Usar una firma raíz
description: La firma raíz es la definición de una colección de tablas de descriptores organizadas de forma arbitraria (incluido su diseño), constantes raíz y descriptores raíz.
ms.assetid: 0131CDE4-02DB-440A-92B8-B0933C6414B0
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3babe26dc06d4f85ce3d6fb771e18c78b54a3701
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104672"
---
# <a name="using-a-root-signature"></a>Usar una firma raíz

La firma raíz es la definición de una colección de tablas de descriptores organizadas de forma arbitraria (incluido su diseño), constantes raíz y descriptores raíz. Cada entrada tiene un costo hacia un límite máximo, por lo que la aplicación puede desplazarse por el equilibrio entre el número de cada tipo de entrada que contendrá la firma raíz.

-   [Semántica de la lista de comandos](#command-list-semantic)
-   [Semántica de agrupación](#bundle-semantics)
-   [Temas relacionados](#related-topics)

La firma raíz es un objeto que se puede crear mediante la especificación manual en la API. Todos los sombreadores de un PSO deben ser compatibles con el diseño raíz especificado con el PSO o, de lo contrario, los sombreadores individuales deben incluir diseños raíz incrustados que coincidan entre sí. de lo contrario, se producirá un error en la creación de PSO. Una propiedad de la firma raíz es que los sombreadores no tienen que conocerlo cuando se crean, aunque las firmas de raíz también se pueden crear directamente en los sombreadores si se desea. Los recursos del sombreador existentes no requieren ningún cambio para ser compatibles con las firmas de raíz. El modelo de sombreador 5,1 se incluye para proporcionar una flexibilidad adicional (indexación dinámica de los descriptores de los sombreadores) y se puede adoptar incrementalmente a partir de los recursos del sombreador existentes, según sea necesario.

## <a name="command-list-semantic"></a>Semántica de la lista de comandos

Al principio de una lista de comandos, la firma raíz no está definida. Los sombreadores de gráficos tienen una firma raíz independiente del sombreador de cálculo, cada una de las cuales se asigna de forma independiente en una lista de comandos. La firma raíz establecida en una lista de comandos o un lote también debe coincidir con el valor actual de PSO en Draw/Dispatch. de lo contrario, el comportamiento es indefinido. Las discrepancias de la firma raíz transitorias antes de Draw/Dispatch son correctas, como establecer un valor de PSO incompatible antes de cambiar a una firma raíz compatible (siempre que sean compatibles en el momento en que se llama a Draw/Dispatch). La configuración de un PSO no cambia la firma raíz. La aplicación debe llamar a una API dedicada para establecer la firma raíz.

Una vez que se ha establecido una firma raíz en una lista de comandos, el diseño define el conjunto de enlaces que se espera que proporcione la aplicación y qué PSO se puede usar (los compilados con el mismo diseño) para las siguientes llamadas a Draw/Dispatch. Por ejemplo, la aplicación podría definir una firma raíz para tener las siguientes entradas. Cada entrada se denomina "espacio".

-   \[0 \] un descriptor de CBV insertado (descriptores raíz)
-   \[1 \] una tabla de descriptores que contiene 2 SRVs, 1 CBVs y 1 UAV
-   \[2 \] una tabla de descriptores que contiene 1 muestra
-   \[3 \] una colección de 4x32 bits de constantes raíz
-   \[4 \] una tabla de descriptores que contiene un número no especificado de SRVs

En este caso, antes de poder emitir un draw/Dispatch, se espera que la aplicación establezca el enlace adecuado en cada una de las ranuras \[ 0.. 4 \] que la aplicación ha definido con su firma raíz actual. Por ejemplo, en la ranura \[ 1 \] , una tabla de descriptores debe estar enlazada, que es una región contigua de un montón descriptor que contiene (o contendrá en ejecución) 2 SRVs, 1 CBVs y 1 UAV. Del mismo modo, las tablas de descriptor deben establecerse en las ranuras \[ 2 \] y \[ 4 \] .

La aplicación puede cambiar parte de los enlaces de la firma raíz a la vez (el resto permanece sin cambios). Por ejemplo, si lo único que debe cambiar entre dibujar es una de las constantes en la ranura \[ 2 \] , es necesario volver a enlazar todas las aplicaciones. Como se explicó anteriormente, las versiones del controlador o el hardware de todos los Estados enlazan la firma raíz a medida que se modifican automáticamente. Si se cambia una firma raíz en una lista de comandos, todos los enlaces de firma raíz anteriores se vuelven obsoletos y todos los enlaces que se esperan recientemente se deben establecer antes de Draw/Dispatch. de lo contrario, el comportamiento es indefinido. Si la firma raíz está establecida de forma redundante en la misma que está establecida actualmente, los enlaces de firma raíz existentes no se vuelven obsoletos.

## <a name="bundle-semantics"></a>Semántica de agrupación

Las agrupaciones heredan los enlaces de firma raíz de la lista de comandos (los enlaces a las distintas ranuras en el ejemplo anterior de la lista de comandos). Si un paquete necesita cambiar algunos de los enlaces de la firma raíz heredada, primero debe establecer la firma raíz para que sea igual que la lista de comandos que realiza la llamada (los enlaces heredados no se vuelven obsoletos). Si la agrupación establece la firma raíz para que sea diferente de la lista de comandos que realiza la llamada, que tiene el mismo efecto que cambiar la firma raíz en la lista de comandos descrita anteriormente: todos los enlaces de firma raíz anteriores están obsoletos y los enlaces recién esperados se deben establecer antes de Draw/Dispatch; de lo contrario, el comportamiento es indefinido. Si una agrupación no necesita cambiar ningún enlace de firma raíz, no es necesario establecer la firma raíz.

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

Al salir de un paquete, los cambios de diseño raíz y/o los cambios de enlace que realiza una agrupación se heredan de nuevo en la lista de comandos de llamada cuando finaliza la ejecución de una agrupación.

Para obtener más información sobre la herencia, consulte la sección **herencia de estado de canalización de gráficos** de administración del [Estado de canalización de gráficos en Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Firmas raíz](root-signatures.md)
</dt> </dl>

 

 




