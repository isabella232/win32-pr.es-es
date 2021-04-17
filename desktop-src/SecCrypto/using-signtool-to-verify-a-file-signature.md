---
description: Explica cómo usar SignTool para comprobar una firma de archivo.
ms.assetid: 9c40a397-19ea-4600-97ee-987dd10f4ef8
title: Usar SignTool para comprobar una firma de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8161d4c890400f3aa33b415e7ac16a5306aa094
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666719"
---
# <a name="using-signtool-to-verify-a-file-signature"></a>Usar SignTool para comprobar una firma de archivo

El comando siguiente comprueba la firma de un archivo denominado *MyControl.exe*:

**Comprobación** de la *MyControl.exe* de SignTool

Si se produce un error en el ejemplo anterior, es posible que la firma use un certificado de firma de código. De forma predeterminada, [SignTool](signtool.md) es la Directiva de controladores de Windows para la comprobación.

El siguiente comando comprueba la firma mediante la Directiva de comprobación de autenticación predeterminada:

**Comprobación de SignTool** *MyControl.exe* /PA

El comando siguiente comprueba un archivo del sistema que puede estar firmado en un catálogo:

**Comprobación de SignTool** *SysFile.dll*

El comando siguiente comprueba un archivo del sistema firmado en un catálogo denominado *MyCat.cat*:

Comprobar si se ha **comprobado/c** *MyCat.catMyFile.ini*

Para cualquier comprobación de [SignTool](signtool.md) , puede recuperar el firmante del certificado. El comando siguiente comprueba un archivo del sistema y muestra el certificado del firmante:

**Comprobación de SignTool/v** *MyControl.exe*

[SignTool](signtool.md) devuelve el texto de la línea de comandos que indica el resultado de la comprobación de la firma. Además, SignTool devuelve un código de salida de cero para que la ejecución sea correcta, una para la ejecución errónea y dos para la ejecución completada con advertencias.

Para obtener más información sobre [SignTool](signtool.md), consulte [SignTool](signtool.md).

 

 



