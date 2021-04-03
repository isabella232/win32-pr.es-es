---
description: Usar menús dibujados por el propietario para admitir la funcionalidad de voz para Tablet PC.
ms.assetid: fbe2d420-f667-416b-bff3-0fee9ae22203
title: Uso de menús de Owner-Drawn
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42f16f9328fadfedccee2c730678fc4cd2d8ab3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809602"
---
# <a name="using-owner-drawn-menus"></a>Uso de menús de Owner-Drawn

Al usar menús dibujados por el propietario, debe hacer que los nombres de menú estén disponibles para admitir la funcionalidad de voz. Existen dos formas de hacerlo:

-   Exponga el nombre del elemento de menú mediante la estructura MSAAMENUINFO.
-   Proporcione una opción para reemplazar los menús gráficos por los menús de texto estándar cuando una ayuda de accesibilidad esté activa. Si la función [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) devuelve **true** con su parámetro *uiAction* establecido en SPI \_ GETSCREENREADER, use los menús estándar. La aplicación debe inspeccionar el mensaje de SETTINGSCHANGE de WM \_ y responder consultando el estado de esta opción y ajustando su presentación adecuadamente. Por ejemplo, Microsoft Visual Studio proporciona una opción para usar los menús estándar en lugar de los menús personalizados que se muestran de forma predeterminada.

 

 
