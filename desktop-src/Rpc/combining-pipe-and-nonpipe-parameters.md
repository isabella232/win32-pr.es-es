---
title: Combinación de parámetros de canalización y no de canalización
description: Combinación de parámetros de canalización y no de canalización en llamada a procedimiento remoto (RPC).
ms.assetid: 52109ba9-4e10-4426-8dfc-e3052d403e9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac76bc2f334325c87cbf8c4a09898cf0fe54153cd84f6f2809995e66cc08e843
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022675"
---
# <a name="combining-pipe-and-nonpipe-parameters"></a>Combinación de parámetros de canalización y no de canalización

Al combinar tipos de canalización y otros tipos en una llamada a procedimiento remoto, los datos se transmiten según la dirección del parámetro :

-   En la **\[ dirección , \]** los datos de todos los argumentos que no son de canalización se transmiten primero, seguidos de los datos de canalización.
-   En la **\[ dirección de \]** salida, el servidor envía primero los datos de canalización. Una vez que se devuelve la rutina de administrador, el servidor transmite los datos que no son de escape.
-   Cuando hay **\[ argumentos \]** de canalización **\[ \]** de entrada y salida combinados con argumentos de entrada y salida que no son de canalización, primero los datos de entrada se transmiten en su totalidad, como se describió anteriormente. A continuación, los datos de salida se transmiten como se describió anteriormente.

La restricción siguiente se aplica a esta implementación de canalizaciones (MIDL 3.0): al combinar tipos de canalización y otros tipos en una sola llamada a procedimiento remoto, los parámetros que no son de canalización deben tener un tamaño bien definido para permitir que el compilador MIDL calcule el tamaño de búfer necesario. Por ejemplo, no se pueden combinar parámetros de canalización con un puntero único o una estructura compatible, ya que sus tamaños no se \[ [](/windows/desktop/Midl/unique) \] pueden determinar en tiempo de compilación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Pipa](/windows/desktop/Midl/pipe)
</dt> <dt>

[/Oi](/windows/desktop/Midl/-oi)
</dt> </dl>

 

 