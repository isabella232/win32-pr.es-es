---
description: Trabajar con búferes DMO multimedia
ms.assetid: 6d0c51b8-0d79-4f04-8e90-0cea4f3b1427
title: Trabajar con búferes DMO multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c870b3a4a035c71a4dcadf9a38b4c2a150097e7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363562"
---
# <a name="working-with-dmo-media-buffers"></a>Trabajar con búferes DMO multimedia

Los datos de entrada se pasan a las DDO de códec mediante búferes multimedia. Un búfer multimedia es un objeto que implementa la [**interfaz IMediaBuffer.**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) Puede implementar una clase para este propósito o, si usa el SDK de formato multimedia de Windows en la aplicación, puede usar los objetos de búfer definidos en ese SDK.

Si implementa su propia clase de búfer, tenga cuidado sobre cómo se controla la memoria del búfer. Cuando se pasa un ejemplo de entrada, el DMO mantiene una referencia al búfer hasta que finaliza con el ejemplo. Puede liberar inmediatamente la referencia a la interfaz [**IMediaBuffer,**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) pero no tiene forma de saber cuándo el códec ya no necesita su referencia. Para estar seguro de que la memoria se libera cuando el objeto se elimina a sí mismo, debe implementar la clase para que asigne y libera la memoria para el búfer internamente.

Dado que las DDO mantienen referencias a búferes durante un período de tiempo desconocido, no es una cuestión trivial usar un grupo limitado de búferes. La solución más sencilla es asignar un nuevo búfer para cada ejemplo, aunque hacerlo es ineficaz.

Una mejor solución es implementar un objeto para administrar un grupo de búferes. Para ello, escriba código en el método **Release** de la implementación de [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) que llama a un método del administrador de búferes (en lugar de eliminarse a sí mismo) cuando el recuento de referencias cae a cero. A continuación, el administrador del búfer puede mantener una lista de punteros a objetos de búfer asignados. Cree un método en el administrador de búferes para comprobar la lista de búferes libres y devolver un puntero para que la aplicación pueda acceder a los búferes cuando sea necesario. Este método debe crear nuevos búferes según sea necesario y agregarlos a la lista.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Trabajar con DDO de códec](workingwithcodecdmos.md)
</dt> </dl>

 

 
