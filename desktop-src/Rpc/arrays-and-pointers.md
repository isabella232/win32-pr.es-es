---
title: Matrices y punteros
description: La llamada a procedimiento remoto (RPC) está diseñada para ser principalmente transparente para los desarrolladores.
ms.assetid: 5ad5a51d-a821-44a5-bbc3-14409cb42cb4
keywords:
- Llamada a procedimiento remoto RPC, descrita, matrices y punteros
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26cc588d4db7cb222ec0fb2689bf645a2a7ed0e12b632392264d480c26777531
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073505"
---
# <a name="arrays-and-pointers"></a>Matrices y punteros

La llamada a procedimiento remoto (RPC) está diseñada para ser principalmente transparente para los desarrolladores. Para lograr esta transparencia, el código auxiliar de cliente transmite al servidor tanto el puntero como el objeto de datos al que apunta. Si el procedimiento remoto cambia los datos, el servidor debe transmitir los nuevos datos al cliente para que el cliente pueda copiar los nuevos datos a través de los datos originales.

En general, una llamada a procedimiento remoto se comporta igual que una llamada a procedimiento local. Es decir, cuando un puntero es un parámetro, el procedimiento remoto puede acceder al objeto de datos al que hace referencia el puntero de la misma manera que un procedimiento local.

Puesto que los programas de cliente y servidor se ejecutan en espacios de direcciones diferentes, los desarrolladores deben usar atributos Lenguaje de definición de interfaz de Microsoft (MIDL) para describir cómo se transmiten los datos de matriz y puntero entre el cliente y el servidor. En esta sección se presenta información general sobre cómo usar matrices y punteros en aplicaciones distribuidas, en los temas siguientes:

-   [Matrices y RPC](arrays-and-rpc.md)
-   [Punteros y RPC](pointers-and-rpc.md)
-   [Usar matrices, cadenas y punteros](using-arrays-strings-and-pointers.md)

 

 




