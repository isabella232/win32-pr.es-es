---
description: Uso de menús dibujados por el propietario para admitir la funcionalidad de voz para tablet PC.
ms.assetid: fbe2d420-f667-416b-bff3-0fee9ae22203
title: Usar Owner-Drawn menús
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a14e63e3602e31edc506a6c9c070fa0bfcce670ec2248c73d68944a2f83a12f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119842805"
---
# <a name="using-owner-drawn-menus"></a>Usar Owner-Drawn menús

Al usar menús dibujados por el propietario, debe hacer que los nombres de menú estén disponibles para admitir la funcionalidad de voz. Existen dos modos para hacer esto:

-   Exponga el nombre del elemento de menú mediante la estructura MSAAMENUINFO.
-   Proporcione una opción para reemplazar los menús gráficos por menús de texto estándar cuando hay una ayuda de accesibilidad activa. Si la [**función SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) devuelve **TRUE con** su parámetro *uiAction* establecido en SPI \_ GETSCREENREADER, use menús estándar. La aplicación debe observar el mensaje WM SETTINGSCHANGE y responder consultando el estado de esta opción y ajustando \_ su visualización adecuadamente. Por ejemplo, Microsoft Visual Studio proporciona una opción para usar menús estándar en lugar de los menús personalizados que se muestran de forma predeterminada.

 

 
