---
description: Además de la habilitación de la supervisión de dígitos y la notificación de dígitos de uno en uno, una aplicación también puede solicitar que se recopilen varios dígitos en un búfer.
ms.assetid: db83c48a-5178-40ed-90a9-e7c8e1886fe0
title: Recopilación de dígitos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5eab4185882b86a5a8e5dcb1444f39c9db2b3ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677614"
---
# <a name="digit-gathering"></a>Recopilación de dígitos

Además de la habilitación de la supervisión de dígitos y la notificación de dígitos de uno en uno, una aplicación también puede solicitar que se recopilen varios dígitos en un búfer. Solo cuando el búfer está lleno o cuando se cumple alguna otra condición de finalización, se notifica a la aplicación. La recopilación de dígitos es útil para funciones como la colección de números de tarjetas de crédito. Se realiza cuando una aplicación llama a [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits), especificando un búfer que se va a rellenar con dígitos. La recopilación de dígitos finaliza cuando se cumple una de las siguientes condiciones:

-   Se ha recopilado el número solicitado de dígitos.
-   Se detecta uno de varios dígitos de finalización. Los dígitos de terminación se especifican en [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)y el dígito de terminación también se coloca en el búfer.
-   Uno de los dos tiempos de espera expira. Los tiempos de espera son un tiempo de espera de primer dígito, que especifica la duración máxima antes de que se recopile el primer dígito y un tiempo de espera entre dígitos que especifica la duración máxima entre los dígitos sucesivos.
-   [**LineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits) vuelve a cancelar explícitamente la recopilación de dígitos con otro conjunto de parámetros para iniciar una nueva solicitud de recopilación o mediante un parámetro de búfer de dígito **nulo** para cancelar.

Cuando la recopilación de dígitos finaliza por cualquier motivo, se envía un mensaje de [**línea \_ GATHERDIGITS**](line-gatherdigits.md) a la aplicación que solicitó la recopilación del dígito. Solo una solicitud de recopilación de un solo dígito puede estar pendiente en una llamada en un momento dado en todas las aplicaciones que son propietarios de la llamada.

La recopilación de dígitos y la supervisión de dígitos se pueden habilitar en la misma llamada al mismo tiempo. En ese caso, la aplicación recibirá un mensaje de [**línea \_ MONITORDIGITS**](line-monitordigits.md) para cada dígito detectado y un mensaje de línea \_ GATHERDIGITS independiente cuando se devuelva el búfer.

 

 



