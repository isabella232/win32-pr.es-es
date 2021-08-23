---
description: La exclusión mutua \_ \_ msiPromptForCD existe cuando el instalador solicita al usuario que inserte un CD-ROM.
ms.assetid: f6319cda-48ac-4351-8eb5-f326490e3aff
title: __MsiPromptForCD exclusión mutua
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba2c829cb0102192b4c2bc2670892f8849000a6ed9cad2a88e7f3e3e557b259
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764295"
---
# <a name="__msipromptforcd-mutex"></a>\_\_Exclusión mutua de MsiPromptForCD

La exclusión mutua \_ \_ msiPromptForCD existe cuando el instalador solicita al usuario que inserte un CD-ROM. Los programas de reproducción automática deben comprobar que la exclusión mutua \_ \_ msiPromptForCD no está establecida actualmente antes de iniciarse. Tenga en cuenta que es posible que se produzca un mensaje de CD-ROM antes de que exista la clave InProgress o \_ msiExecute Mutex.

 

 



