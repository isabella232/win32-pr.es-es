---
description: Explica cómo usar SignTool para comprobar una firma de archivo.
ms.assetid: 9c40a397-19ea-4600-97ee-987dd10f4ef8
title: Uso de SignTool para comprobar una firma de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 137a4117b64ca5d62ee2ffe5fb80a7e0751d91f840ce1270482d9e114f4dd61b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118896698"
---
# <a name="using-signtool-to-verify-a-file-signature"></a>Uso de SignTool para comprobar una firma de archivo

El comando siguiente comprueba la firma de un archivo denominado *MyControl.exe*:

**SignTool verify** *MyControl.exe*

Si se produce un error en el ejemplo anterior, podría ser que la firma usó un certificado de firma de código. [SignTool](signtool.md) tiene como valor predeterminado la directiva Windows controlador para la comprobación.

El comando siguiente comprueba la firma mediante la directiva de comprobación de autenticación predeterminada:

**SignTool verify /pa** *MyControl.exe*

El comando siguiente comprueba un archivo del sistema que puede estar firmado en un catálogo:

**SignTool verify /a** *SysFile.dll*

El comando siguiente comprueba un archivo del sistema que está firmado en un catálogo denominado *MyCat.cat*:

**SignTool verify /c** *MyCat.cat* *MyFile.ini*

Para cualquier [comprobación de SignTool,](signtool.md) puede recuperar el firmante del certificado. El comando siguiente comprueba un archivo del sistema y muestra el certificado de firmante:

**SignTool verify /v** *MyControl.exe*

[SignTool](signtool.md) devuelve texto de línea de comandos que indica el resultado de la comprobación de firma. Además, SignTool devuelve un código de salida de cero para la ejecución correcta, uno para la ejecución con errores y dos para la ejecución que se completó con advertencias.

Para obtener más información sobre [SignTool](signtool.md), vea [SignTool](signtool.md).

 

 



