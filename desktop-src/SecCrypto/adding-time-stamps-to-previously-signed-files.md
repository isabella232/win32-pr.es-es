---
description: Las marcas de tiempo normalmente se incluyen cuando se firma un archivo mediante SignTool con la opción -t.
ms.assetid: ca22d055-dc34-447c-991b-27ff21ca3afc
title: Agregar marcas de tiempo a archivos firmados previamente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef2e750dcb178b2a089bfbde0b2aea882b097c86
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127173314"
---
# <a name="adding-time-stamps-to-previously-signed-files"></a>Agregar marcas de tiempo a archivos firmados previamente

Las marcas de tiempo normalmente se incluyen cuando se firma un archivo mediante SignTool con **la opción -t.** Además, se pueden agregar marcas de tiempo a los archivos que se firmaron sin marca de tiempo. El siguiente comando agrega una marca de tiempo a un archivo firmado previamente:

**signtool timestamp -t https: \/ /timestamp.digicert.com *MyControl.exe***

> [!Note]  
> El archivo que se va a marcar de tiempo debe haber sido firmado previamente.

 

Para obtener más información sobre SignTool, vea [SignTool](signtool.md).

 

 



