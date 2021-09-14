---
description: ICE44 valida que NewDialog, SpawnDialog y SpawnWaitDialog ControlEvents hacen referencia a cuadros de diálogo válidos en la tabla Dialog.
ms.assetid: 401bae25-a361-45f6-af3f-0f31be463c84
title: ICE44
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16354ac435979d830ff14c33a846e97757b64962
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074604"
---
# <a name="ice44"></a>ICE44

ICE44 valida que [los objetos NewDialog](newdialog-controlevent.md), [SpawnDialog](spawndialog-controlevent.md)y [SpawnWaitDialog](spawnwaitdialog-controlevent.md) ControlEvents hacen referencia a cuadros de diálogo válidos en la [tabla Dialog](dialog-table.md).

## <a name="result"></a>Resultado

ICE44 envía un mensaje de error si hay un evento de control de diálogo que no hace referencia a un cuadro de diálogo que aparece en la tabla Diálogo.

## <a name="example"></a>Ejemplo

ICE44 notificaría los errores siguientes para el ejemplo mostrado.



| Error ICE44                                                                                                                               | Descripción                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Evento de control para el control 'Dialog1'.' Control1' es de tipo SpawnDialog, pero su argumento Dialog2 no es una entrada válida en la tabla dialog. | Hay acciones SpawnDialog, SpawnWaitDialog o NewDialog que tienen un argumento que no hace referencia a un cuadro de diálogo en la tabla Dialog. Para corregir este error, agregue un argumento que sea una clave en la tabla dialog.<br/> |



 

[Tabla de diálogos](dialog-table.md) (parcial)



| Diálogo  | Título |
|---------|-------|
| Dialog1 |       |



 

[Tabla ControlEvent](controlevent-table.md) (parcial)



| Diálogo\_ | control\_ | Tipo        | Argumento |
|----------|-----------|-------------|----------|
| Dialog1  | Control1  | SpawnDialog | Dialog2  |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 




