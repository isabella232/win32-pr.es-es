---
description: Normalmente, las marcas de tiempo se incluyen cuando se firma un archivo mediante SignTool con la opción-t.
ms.assetid: ca22d055-dc34-447c-991b-27ff21ca3afc
title: Agregar marcas de tiempo a archivos firmados anteriormente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef2e750dcb178b2a089bfbde0b2aea882b097c86
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "105670213"
---
# <a name="adding-time-stamps-to-previously-signed-files"></a>Agregar marcas de tiempo a archivos firmados anteriormente

Normalmente, las marcas de tiempo se incluyen cuando se firma un archivo mediante SignTool con la opción **-t** . Además, se pueden agregar marcas de tiempo a archivos firmados sin una marca de tiempo. El comando siguiente agrega una marca de tiempo a un archivo firmado anteriormente:

**SignTool timestamp-t https: \/ /timestamp.digicert.com *MyControl.exe***

> [!Note]  
> El archivo que se va a marcar para la marca de tiempo debe haberse firmado previamente.

 

Para obtener más información sobre SignTool, consulte [SignTool](signtool.md).

 

 



