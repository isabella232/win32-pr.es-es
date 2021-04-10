---
description: Explica cómo usar SignTool para firmar un archivo.
ms.assetid: fa8ee4d3-8927-4f7d-a09e-dbcf75a164d3
title: Usar SignTool para firmar un archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 089026cde629278e5c6ac033164c2a9d26528917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155081"
---
# <a name="using-signtool-to-sign-a-file"></a>Usar SignTool para firmar un archivo

El comando siguiente firma el archivo denominado MyControl.exe mediante un [*certificado*](../secgloss/c-gly.md) almacenado en un archivo de intercambio de información personal (pfx):

<pre>SignTool sign /f <b>MyCert</b>.pfx MyControl.exe</pre>

El siguiente comando firma el archivo con un certificado almacenado en un archivo PFX protegido por contraseña:

<pre>SignTool sign /f <b>MyCert</b>.pfx /p <b>MyPassword</b> MyControl.exe</pre>

> [!Note]  
> Asegúrese de que protege correctamente la contraseña.

 

El siguiente comando firma y marca de tiempo el archivo:

<pre>SignTool sign /f <b>MyCert</b>.pfx /t http://timestamp.digicert.com MyControl.exe</pre>

> [!Note]  
> Para obtener información acerca de la marca de tiempo de un archivo una vez que ya se ha firmado, vea [Agregar marcas de tiempo a archivos firmados anteriormente](adding-time-stamps-to-previously-signed-files.md).

 

El comando siguiente firma el archivo con un certificado ubicado en el almacén My con un nombre de sujeto del publicador de la compañía:

<pre>SignTool sign /n "<b>My Company Publisher</b>" MyControl.exe</pre>

El comando siguiente firma un control ActiveX y proporciona información que Internet Explorer muestra cuando se solicita al usuario que instale el control:

<pre>SignTool sign /f <b>MyCert</b>.pfx /d "<b>My Product Name</b>" /du <b>"https://www.example.com/myproductinfo.html"</b> MyControl.exe</pre>

El siguiente comando firma el archivo con un certificado cuya información de [*clave privada*](../secgloss/p-gly.md) está protegida por un módulo de criptografía de hardware. Por ejemplo, supongamos que el certificado denominado "mi High-Value certificado" tiene una clave privada instalada en un módulo de criptografía de hardware y el certificado está instalado correctamente.

<pre>SignTool sign /n "<b>My High-Value Certificate</b>" MyControl.exe</pre>

El siguiente comando firma el archivo con un certificado cuya información de [*clave privada*](../secgloss/p-gly.md) está protegida por un módulo de criptografía de hardware. Se especifica un almacén del equipo para el almacén de la [*entidad de certificación*](../secgloss/c-gly.md) (CA).

<pre>SignTool sign /n "<b>My High Value Certificate</b>" /sm /s CA MyControl.exe</pre>

El comando siguiente firma el archivo con un certificado almacenado en un archivo. La información de la clave privada está protegida por un módulo de criptografía de hardware, y el [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) y el [*contenedor de claves*](../secgloss/k-gly.md) se especifican mediante el nombre. Este comando es útil si el certificado no está instalado correctamente.

<pre>SignTool sign /f <b>HighValue</b>.cer /csp "<b>Hardware Cryptography Module</b>" /k <b>HighValueContainer</b> MyControl.exe</pre>

[SignTool](signtool.md) devuelve el texto de la línea de comandos que indica el resultado de la operación de firma. Además, SignTool devuelve un código de salida de cero para que la ejecución sea correcta, una para la ejecución errónea y dos para la ejecución completada con advertencias.

Para obtener información acerca de cómo comprobar la firma de un archivo, consulte [usar SignTool para comprobar una firma de archivo](using-signtool-to-verify-a-file-signature.md). Para obtener información sobre cómo agregar una marca de tiempo si el archivo ya se ha firmado, vea [Agregar marcas de tiempo a archivos firmados anteriormente](adding-time-stamps-to-previously-signed-files.md). Para obtener información adicional sobre [SignTool](signtool.md), consulte [SignTool](signtool.md).

 

 
