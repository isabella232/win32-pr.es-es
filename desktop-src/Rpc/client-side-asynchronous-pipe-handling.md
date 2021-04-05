---
title: Control de canalizaciones asincrónicas en el cliente
description: Antes de realizar una llamada remota asincrónica, el cliente debe inicializar primero el identificador asincrónico.
ms.assetid: 3d54b233-d8b0-45d1-b759-0d2d24c1e247
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ff503f80c77b2403d683c2b644d89836365956
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903745"
---
# <a name="client-side-asynchronous-pipe-handling"></a>Control de canalizaciones asincrónicas en el cliente

Antes de realizar una llamada remota asincrónica, el cliente debe inicializar primero el identificador asincrónico. Al igual que con los procedimientos no canalizados, el cliente llama a una función asincrónica con el identificador asincrónico como primer parámetro y usa el identificador asincrónico para enviar y recibir datos de canalización, consultar el estado de la llamada y recibir la respuesta.

El cliente realiza la llamada asincrónica al procedimiento remoto con el identificador asincrónico como primer parámetro. El cliente puede utilizar este identificador para consultar el estado de la llamada y recibir la respuesta. El modelo de canalización asincrónica es simétrico. Tanto las aplicaciones de cliente como de servidor envían y reciben activamente datos de canalización (en lugar de RPC sincrónicos, donde los datos de la canalización se envían y se reciben de manera pasiva).

El cliente envía datos de canalización asincrónicos mediante una llamada a **la función de la** canalización asincrónica adecuada, con la variable de estado de la canalización como primer parámetro. Cuando se devuelve **la función de envío,** el cliente puede modificar o liberar el búfer de envío.

Si la \_ marca RPC Async \_ Notify \_ on \_ send \_ Complete está establecida en el identificador asincrónico y si se usan APC como mecanismo de notificación, se pone en cola una APC cuando el envío de la canalización se ha completado. Puede aprovechar este mecanismo para implementar el control de flujo. Tenga en cuenta, sin embargo, que si el cliente envía otro búfer antes de que se complete la anterior, el cliente puede, en función de la velocidad de la operación de transferencia, recibir solo una notificación de envío y completo, en lugar de una notificación para cada búfer o cada operación de **extracción** . Cuando el cliente ha enviado todos los datos de la canalización, realiza una llamada de **envío** final con el número de elementos establecido en 0.

El programa cliente recibe datos de canalización asincrónicos mediante una llamada a la función **pull** en la canalización asincrónica adecuada, con la variable de estado de la canalización como primer parámetro. Si no hay datos de canalización disponibles, la función de **extracción** devuelve una \_ llamada asincrónica de RPC S \_ \_ \_ pendiente.

Si el mecanismo de notificación es APC y el servidor devolvió \_ \_ \_ una llamada asincrónica \_ de RPC S, el cliente debe esperar hasta que reciba el APC **RpcReceiveComplete** desde el tiempo de ejecución antes de volver a llamar a **pull** .

 

 




