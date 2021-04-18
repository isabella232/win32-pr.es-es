---
description: Trabajar con búferes de medios DMO
ms.assetid: 6d0c51b8-0d79-4f04-8e90-0cea4f3b1427
title: Trabajar con búferes de medios DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c870b3a4a035c71a4dcadf9a38b4c2a150097e7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105707539"
---
# <a name="working-with-dmo-media-buffers"></a>Trabajar con búferes de medios DMO

Los datos de entrada se pasan al códec DMOs con búferes de medios. Un búfer multimedia es un objeto que implementa la interfaz [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) . Puede implementar una clase para este propósito o, si usa el SDK de Windows Media Format en la aplicación, puede usar los objetos de búfer definidos en ese SDK.

Si implementa su propia clase de búfer, tenga cuidado sobre cómo se controla la memoria del búfer. Cuando se pasa una muestra de entrada, DMO mantiene una referencia al búfer hasta que termina con el ejemplo. Puede liberar inmediatamente la referencia a la interfaz [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) , pero no tiene ninguna manera de saber cuándo el códec ya no necesita su referencia. Para asegurarse de que la memoria se libera cuando el objeto se elimina, debe implementar la clase para que asigne y libere internamente la memoria para el búfer.

Dado que DMOs mantiene referencias a los búferes durante un período de tiempo desconocido, no es una cuestión trivial usar un grupo limitado de búferes. La solución más sencilla consiste en asignar un nuevo búfer para cada ejemplo, aunque esto es ineficaz.

Una solución mejor consiste en implementar un objeto para administrar un grupo de búferes. Para ello, escriba el código en el método de **versión** de la implementación de [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) que llama a un método del administrador de búfer (en lugar de eliminarlo) cuando el recuento de referencias desciende a cero. Después, el administrador de búfer puede mantener una lista de punteros a los objetos de búfer asignados. Cree un método en el administrador de búfer para comprobar la lista de búferes disponibles y devolver un puntero para que la aplicación pueda tener acceso a los búferes cuando sea necesario. Este método debe crear nuevos búferes según sea necesario y agregarlos a la lista.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con códec DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 
