---
description: Un cuadro de diálogo cancelar confirma que el usuario desea finalizar la instalación. Este es un cuadro de diálogo modal.
ms.assetid: 5dab4315-721e-417d-91e0-b38653a65c23
title: Cuadro de diálogo cancelar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1022a7613f3f5341d8c833b7cbe2645ce871aeb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652597"
---
# <a name="cancel-dialog"></a>Cuadro de diálogo cancelar

Un cuadro de diálogo **Cancelar** confirma que el usuario desea finalizar la instalación. Este es un cuadro de diálogo modal.

Este tipo de cuadro de diálogo normalmente contiene un [control de texto](text-control.md) y dos [botones](pushbutton-control.md)de control. Los dos botones proporcionan al usuario la opción de volver al último cuadro de diálogo o confirmar la finalización de la instalación.

[EndDialog](enddialog-controlevent.md) ControlEvent, está vinculado a estos dos botones en la [tabla ControlEvent,](controlevent-table.md). El parámetro *devuelto* de EndDialog ControlEvent, está vinculado a uno de los botones y hace que se termine el cuadro de diálogo **Cancelar** y que el foco vuelva al cuadro de diálogo anterior. El parámetro *Exit* está vinculado al otro botón y hace que la interfaz de usuario devuelva el control al instalador con el código adecuado que indica que el usuario desea salir. A continuación, el instalador se apaga y muestra el [cuadro de diálogo UserExit](userexit-dialog.md).

 

 



