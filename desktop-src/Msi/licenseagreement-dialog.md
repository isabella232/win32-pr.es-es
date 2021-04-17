---
description: Este cuadro de diálogo modal muestra el contrato de licencia para el usuario.
ms.assetid: 367fe264-6e08-4b40-b61b-617bb92986b7
title: Cuadro de diálogo LicenseAgreement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8876f315787671ee36de42e5b86167659611a77a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686798"
---
# <a name="licenseagreement-dialog"></a>Cuadro de diálogo LicenseAgreement

Este cuadro de diálogo modal muestra el contrato de licencia para el usuario. Normalmente, el cuadro de diálogo muestra el texto del acuerdo mediante un [control ScrollableText](scrollabletext-control.md) y un par de botones de opción que permiten al usuario aceptar o rechazar el contrato. Por motivos legales, es aconsejable que no se presente ningún botón al usuario como ya seleccionado de forma predeterminada. Esto obliga al usuario a establecer una opción activa. Normalmente, los autores usan un [control RadioButtonGroup](radiobuttongroup-control.md) para este propósito. Sin embargo, tenga en cuenta que el foco en un cuadro de diálogo no se mueve a un control RadioButtonGroup hasta que se ha seleccionado uno de los botones del grupo.

 

 



