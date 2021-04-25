---
description: Explica cómo usar SignTool para comprobar una firma de archivo.
ms.assetid: 9c40a397-19ea-4600-97ee-987dd10f4ef8
title: Uso de SignTool para comprobar una firma de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e91df7a64a8db48d04ceba9df5fbc3fd358058
ms.sourcegitcommit: 7024106e3420607420bb04c3f88d9bb4827038c8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/25/2021
ms.locfileid: "107954928"
---
# <a name="using-signtool-to-verify-a-file-signature"></a>Uso de SignTool para comprobar una firma de archivo

El comando siguiente comprueba la firma de un archivo denominado *MyControl.exe*:

**Comprobación de signTool** *MyControl.exe*

Si se produce un error en el ejemplo anterior, podría ser que la firma usó un certificado de firma de código. [SignTool tiene](signtool.md) como valor predeterminado la directiva de controladores de Windows para la comprobación.

El siguiente comando comprueba la firma mediante la directiva de comprobación de autenticación predeterminada:

**SignTool verify /pa** *MyControl.exe*

El siguiente comando comprueba un archivo del sistema que se puede firmar en un catálogo:

**SignTool verify /a** *SysFile.dll*

El siguiente comando comprueba un archivo del sistema que está firmado en un catálogo denominado *MyCat.cat*:

**SignTool verify /c** *MyCat.cat* *MyFile.ini*

Para cualquier [comprobación de SignTool,](signtool.md) puede recuperar el firmante del certificado. El comando siguiente comprueba un archivo del sistema y muestra el certificado de firmante:

**Comprobación de SignTool /v** *MyControl.exe*

[SignTool](signtool.md) devuelve texto de línea de comandos que indica el resultado de la comprobación de firma. Además, SignTool devuelve un código de salida de cero para la ejecución correcta, uno para la ejecución con error y dos para la ejecución que se completó con advertencias.

Para obtener más información sobre [SignTool,](signtool.md)vea [SignTool](signtool.md).

 

 



