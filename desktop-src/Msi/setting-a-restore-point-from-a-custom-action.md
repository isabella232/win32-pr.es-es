---
description: Las acciones personalizadas no deben llamar a la función SRSetRestorePoint porque esto puede dar lugar a que se escriba un punto de entrada de restauración en medio de una instalación de Windows Installer.
ms.assetid: 5c3df769-e24d-47b4-af6a-b58e3cbcf00c
title: Establecer un punto de restauración a partir de una acción personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8539c436dbdb960c813b6125557639161dd4a329
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127272372"
---
# <a name="setting-a-restore-point-from-a-custom-action"></a>Establecer un punto de restauración a partir de una acción personalizada

Las acciones personalizadas no deben llamar a la función [**SRSetRestorePoint**](/windows/win32/api/srrestoreptapi/nf-srrestoreptapi-srsetrestorepointa) porque esto puede dar lugar a que se escriba un punto de entrada de restauración en medio de una instalación de Windows Installer.

Para obtener más información, [vea Restaurar sistema y el instalador Windows .](system-restore-points-and-the-windows-installer.md)

 

 
