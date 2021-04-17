---
description: Para generar un cuadro de diálogo que solicite al usuario que inserte el siguiente disco o especifique una nueva ruta de acceso de origen, llame a SetupPromptForDisk.
ms.assetid: a780e7ab-bd96-43e4-9425-e15a758391f4
title: Solicitar un disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 404e88611ec21b7a29d69ab306dc0e7c4e1b98e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667603"
---
# <a name="prompting-for-a-disk"></a>Solicitar un disco

Para generar un cuadro de diálogo que solicite al usuario que inserte el siguiente disco o especifique una nueva ruta de acceso de origen, llame a [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska). Esta función se usa en las rutinas de devolución de llamada para generar una interfaz de usuario cuando se envía la notificación [**SPFILENOTIFY \_ NEEDMEDIA**](spfilenotify-needmedia.md)a la rutina de devolución de llamada.

El cuadro de diálogo generado por [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska) proporciona al usuario la opción de insertar un disco, especificar una nueva ruta de acceso de origen o cancelar la instalación.

Puede usar las marcas especificadas durante la llamada a [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska) para modificar el diseño y el comportamiento del cuadro de diálogo. Con estas marcas, puede controlar si el cuadro de diálogo incluye botones que permiten al usuario buscar una nueva ruta de acceso de origen u omitir el archivo actual. Las marcas también permiten controlar el comportamiento del cuadro de diálogo como el pitido cuando se muestra por primera vez y la capacidad se muestra como una ventana de primer plano.

 

 



