---
description: ICE44 valida que NewDialog, SpawnDialog y SpawnWaitDialog ControlEvents hacen referencia a cuadros de diálogo válidos en la tabla del cuadro de diálogo.
ms.assetid: 401bae25-a361-45f6-af3f-0f31be463c84
title: ICE44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16354ac435979d830ff14c33a846e97757b64962
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667752"
---
# <a name="ice44"></a>ICE44

ICE44 valida que [NewDialog](newdialog-controlevent.md), [SpawnDialog](spawndialog-controlevent.md)y [SpawnWaitDialog](spawnwaitdialog-controlevent.md) ControlEvents hacen referencia a cuadros de diálogo válidos en la tabla del [cuadro de diálogo](dialog-table.md).

## <a name="result"></a>Resultado

ICE44 envía un mensaje de error si hay un evento de control de diálogo que no hace referencia a un cuadro de diálogo que aparece en la tabla del cuadro de diálogo.

## <a name="example"></a>Ejemplo

ICE44 notificaría los siguientes errores para el ejemplo que se muestra.



| Error ICE44                                                                                                                               | Descripción                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Evento de control para el control ' Dialog1 '. ' Control1 ' es de tipo SpawnDialog, pero su argumento Dialog2 no es una entrada válida en la tabla del cuadro de diálogo. | Hay una acción SpawnDialog, SpawnWaitDialog o NewDialog que tiene un argumento que no hace referencia a un cuadro de diálogo en la tabla del cuadro de diálogo. Para corregir este error, agregue un argumento que sea una clave en la tabla del cuadro de diálogo.<br/> |



 

[Tabla de cuadro de diálogo](dialog-table.md) (parcial)



| Diálogo  | Title |
|---------|-------|
| Dialog1 |       |



 

[Tabla ControlEvent,](controlevent-table.md) (parcial)



| Diálogo\_ | control\_ | Tipo        | Argumento |
|----------|-----------|-------------|----------|
| Dialog1  | Control1  | SpawnDialog | Dialog2  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 




