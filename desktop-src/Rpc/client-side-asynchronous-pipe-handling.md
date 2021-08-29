---
title: Control de canalización asincrónica del lado cliente
description: Antes de realizar una llamada remota asincrónica, el cliente debe inicializar primero el identificador asincrónico.
ms.assetid: 3d54b233-d8b0-45d1-b759-0d2d24c1e247
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 041e33ec998da568aa6836d141e7208aa43025f28b60c2582a8fc30faee4f901
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931748"
---
# <a name="client-side-asynchronous-pipe-handling"></a>Control de canalización asincrónica del lado cliente

Antes de realizar una llamada remota asincrónica, el cliente debe inicializar primero el identificador asincrónico. Al igual que con los procedimientos que no son de canalización, el cliente llama a una función asincrónica con el identificador asincrónico como primer parámetro y usa el identificador asincrónico para enviar y recibir datos de canalización, consultar el estado de la llamada y recibir la respuesta.

El cliente realiza la llamada a procedimiento remoto asincrónico con el identificador asincrónico como primer parámetro. El cliente puede usar este identificador para consultar el estado de la llamada y recibir la respuesta. El modelo de canalización asincrónica es simétrico. Las aplicaciones cliente y servidor envían y reciben datos de canalización activamente (en lugar de RPC sincrónico, donde los datos de canalización se envían y reciben pasivamente).

El cliente envía datos de canalización asincrónicos llamando a la función **de** inserción en la canalización asincrónica adecuada, con la variable de estado de la canalización como primer parámetro. Cuando la **función de** inserción vuelve, el cliente puede modificar o liberar el búfer de envío.

Si la marca RPC ASYNC NOTIFY ON SEND COMPLETE está establecida en el identificador asincrónico y si se usan LAS API como mecanismo de notificación, se pone en cola un APC cuando el envío de canalización se completa \_ \_ \_ \_ \_ realmente. Puede aprovechar este mecanismo para implementar el control de flujo. Sin embargo, tenga en cuenta que si el cliente inserta otro búfer antes de que se complete la inserción anterior, el cliente puede,  en función de la velocidad de la operación de transferencia, recibir solo una notificación de envío completo, en lugar de una notificación para cada búfer o cada operación de inserción. Cuando el cliente ha enviado todos los datos de canalización, realiza una última llamada **push** con el número de elementos establecido en 0.

El programa cliente recibe datos de canalización asincrónicos llamando a la función **de** extracción en la canalización asincrónica adecuada, con la variable de estado de la canalización como primer parámetro. Si no hay datos de canalización disponibles, la función **de extracción** devuelve RPC \_ S \_ ASYNC CALL \_ \_ PENDING.

Si el mecanismo de notificación es APC y el servidor devolvió RPC S ASYNC CALL PENDING, el cliente debe esperar hasta que reciba el \_ \_ \_ \_ APC **RpcReceiveComplete**  del tiempo de ejecución antes de llamar a pull de nuevo.

 

 




