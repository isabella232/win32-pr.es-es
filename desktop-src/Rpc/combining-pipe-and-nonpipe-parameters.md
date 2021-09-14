---
title: Combinación de parámetros de canalización y no de canalización
description: Combinación de parámetros de canalización y no de canalización en llamada a procedimiento remoto (RPC).
ms.assetid: 52109ba9-4e10-4426-8dfc-e3052d403e9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0776f995dacb4d477724b0ee1e5c2fa969723199
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071428"
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

 

 