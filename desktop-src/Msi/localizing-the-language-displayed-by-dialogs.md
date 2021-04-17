---
description: El servicio Windows Installer usa el idioma del usuario actual en todos los cuadros de diálogo hasta que se abre un paquete de Windows Installer.
ms.assetid: c9902990-7a26-48fd-96ac-4d5a749e34be
title: Localizar el idioma que se muestra en los cuadros de diálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 042b2b7f9ac256ebad265b75a8756fc422403e37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687823"
---
# <a name="localizing-the-language-displayed-by-dialogs"></a>Localizar el idioma que se muestra en los cuadros de diálogo

El servicio Windows Installer usa el idioma del usuario actual en todos los cuadros de diálogo hasta que se abre un paquete de Windows Installer. El Windows Installer determina esto mediante **GetUserDefaultUILanguage**. Cuando se abre un paquete de Windows Installer, el instalador muestra los cuadros de diálogo con el idioma del paquete tal y como se especifica en la propiedad de Resumen de la [**plantilla**](template-summary.md) .

Para obtener más información sobre cómo localizar el idioma de un paquete de Windows Installer, vea también [un ejemplo de localización](a-localization-example.md).

 

 



