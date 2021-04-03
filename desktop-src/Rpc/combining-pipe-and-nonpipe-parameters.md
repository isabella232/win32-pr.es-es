---
title: Combinación de parámetros de canalización y no de canalización
description: Combinación de parámetros de canalización y no de canalización en llamada a procedimiento remoto (RPC).
ms.assetid: 52109ba9-4e10-4426-8dfc-e3052d403e9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0776f995dacb4d477724b0ee1e5c2fa969723199
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103904751"
---
# <a name="combining-pipe-and-nonpipe-parameters"></a>Combinación de parámetros de canalización y no de canalización

Cuando se combinan tipos de canalización y otros tipos en una llamada a procedimiento remoto, los datos se transmiten según la dirección del parámetro:

-   En la **\[ \] dirección,** los datos de todos los argumentos que no son de canalización se transmiten primero, seguidos de los datos de canalización.
-   En la dirección de **\[ salida \]** , el servidor envía los datos de la canalización en primer lugar. Una vez que la rutina de administrador devuelve, el servidor transmite los datos no canalizados.
-   Cuando hay **\[ en, \]** los argumentos out Pipe combinados con argumentos **\[ in, \] out** sin canalización, primero se transmiten los datos de entrada en su totalidad, como se ha descrito anteriormente. A continuación, los datos de salida se transmiten como se ha descrito anteriormente.

La siguiente restricción se aplica a esta implementación de canalizaciones (MIDL 3,0): cuando se combinan tipos de canalización y otros tipos en una única llamada a procedimiento remoto, los parámetros no de canalización deben tener un tamaño bien definido para permitir que el compilador de MIDL calcule el tamaño de búfer necesario. Por ejemplo, no puede combinar parámetros de canalización con un \[ puntero [único](/windows/desktop/Midl/unique) \] o una estructura conforme, ya que sus tamaños no se pueden determinar en tiempo de compilación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[codo](/windows/desktop/Midl/pipe)
</dt> <dt>

[/Oi](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 