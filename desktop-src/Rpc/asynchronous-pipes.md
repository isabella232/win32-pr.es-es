---
title: Canalizaciones asincrónicas
description: El uso de parámetros de canalización con RPC asincrónica permite transmitir datos de forma incremental, a medida que están disponibles, sin asociar el cliente y el servidor.
ms.assetid: e5c466b8-c0b0-4fa8-8867-d0715fd614b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be9d6dd5a3e8de7d5c4ad233a577187a49d04ed8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173558"
---
# <a name="asynchronous-pipes"></a>Canalizaciones asincrónicas

El [uso de](/windows/desktop/Midl/pipe) parámetros de canalización con RPC asincrónica permite transmitir datos de forma incremental, a medida que están disponibles, sin asociar el cliente y el servidor. Esto es especialmente útil cuando tiene una gran cantidad de datos para transferir, combinados con un cliente lento, un servidor lento o una red lenta. Si usa una canalización en una llamada de función asincrónica, es, por definición, una canalización asincrónica. Las canalizaciones sincrónicas no se admiten junto con las funciones asincrónicas.

A diferencia de las canalizaciones convencionales (sincrónicas) en las que el servidor controla todos los detalles de envío y recepción de datos de canalización, las canalizaciones asincrónicas son simétricas. Es decir, tanto el cliente como el servidor pueden insertar y extraer datos a través de la canalización.

> [!Note]  
> Los parámetros de canalización solo se pueden pasar por referencia. Incluso si el archivo IDL muestra [los](/windows/desktop/Midl/pipe) parámetros de canalización que se pasan por valor, los códigos auxiliares generados solo aceptarán parámetros de canalización por referencia.

 

En la siguiente explicación de las canalizaciones asincrónicas, se supone que está familiarizado con el constructor de tipo de canalización. Para obtener más información sobre los procedimientos de canalización descritos en estos temas, vea [Canalizaciones](pipes.md).

 

 