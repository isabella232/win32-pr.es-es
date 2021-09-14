---
description: Un cuadro de diálogo Cancelar confirma que el usuario desea finalizar la instalación. Se trata de un cuadro de diálogo modal.
ms.assetid: 5dab4315-721e-417d-91e0-b38653a65c23
title: Cuadro de diálogo Cancelar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1022a7613f3f5341d8c833b7cbe2645ce871aeb7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158947"
---
# <a name="cancel-dialog"></a>Cuadro de diálogo Cancelar

Un **cuadro de** diálogo Cancelar confirma que el usuario desea finalizar la instalación. Se trata de un cuadro de diálogo modal.

Este tipo de cuadro de diálogo normalmente contiene un [control Text y](text-control.md) dos [PushButtons](pushbutton-control.md). Los dos botones dan al usuario la opción de volver al último cuadro de diálogo o confirmar la finalización de la instalación.

EndDialog ControlEvent está vinculado a estos dos botones de la [tabla ControlEvent](controlevent-table.md). [](enddialog-controlevent.md) El *parámetro Return* del control EndDialogEvent está vinculado a  uno de los botones y hace que el cuadro de diálogo Cancelar finalice y el foco vuelva al cuadro de diálogo anterior. El *parámetro Exit* está vinculado al otro botón y hace que la interfaz de usuario devuelva el control al instalador con el código adecuado que indica que el usuario quiere salir. A continuación, el instalador se cierra y muestra el [cuadro de diálogo UserExit](userexit-dialog.md).

 

 



