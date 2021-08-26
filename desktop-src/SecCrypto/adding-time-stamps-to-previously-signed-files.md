---
description: Las marcas de tiempo normalmente se incluyen cuando se firma un archivo mediante SignTool con la opción -t.
ms.assetid: ca22d055-dc34-447c-991b-27ff21ca3afc
title: Agregar marcas de tiempo a archivos firmados previamente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d988f63e7b5c58f5d8346d074d3ec98d31dc87443670480f7ded2e72f2272275
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119880235"
---
# <a name="adding-time-stamps-to-previously-signed-files"></a>Agregar marcas de tiempo a archivos firmados previamente

Las marcas de tiempo normalmente se incluyen cuando se firma un archivo mediante SignTool con **la opción -t.** Además, se pueden agregar marcas de tiempo a los archivos que se firmaron sin marca de tiempo. El comando siguiente agrega una marca de tiempo a un archivo firmado previamente:

**signtool timestamp -t https: \/ /timestamp.digicert.com *MyControl.exe***

> [!Note]  
> El archivo que se va a marcar de tiempo debe haber sido firmado previamente.

 

Para obtener más información sobre SignTool, [vea SignTool](signtool.md).

 

 



