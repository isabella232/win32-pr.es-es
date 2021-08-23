---
description: Las acciones personalizadas no deben llamar a la función SRSetRestorePoint porque esto puede dar lugar a que se escriba un punto de entrada de restauración en medio de una instalación de Windows Installer.
ms.assetid: 5c3df769-e24d-47b4-af6a-b58e3cbcf00c
title: Establecer un punto de restauración a partir de una acción personalizada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2b30dad9f8f250c0ae82286425d092538ad8324715e632e2c5074e428454f76
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628585"
---
# <a name="setting-a-restore-point-from-a-custom-action"></a>Establecer un punto de restauración a partir de una acción personalizada

Las acciones personalizadas no deben llamar a la función [**SRSetRestorePoint**](/windows/win32/api/srrestoreptapi/nf-srrestoreptapi-srsetrestorepointa) porque esto puede dar lugar a que se escriba un punto de entrada de restauración en medio de una instalación de Windows Installer.

Para obtener más información, [vea Restaurar sistema Points y Windows Installer](system-restore-points-and-the-windows-installer.md).

 

 
