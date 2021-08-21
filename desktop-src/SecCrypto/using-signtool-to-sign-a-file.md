---
description: Explica cómo usar SignTool para firmar un archivo.
ms.assetid: fa8ee4d3-8927-4f7d-a09e-dbcf75a164d3
title: Usar SignTool para firmar un archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a71d8e85e8e22f65ccbe8b5f15453b0a0cac34fc27697bad648b1c815f255b10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117971475"
---
# <a name="using-signtool-to-sign-a-file"></a>Usar SignTool para firmar un archivo

El comando siguiente firma el archivo denominado MyControl.exe [*mediante*](../secgloss/c-gly.md) un certificado almacenado en un archivo de Exchange personal (PFX):

<pre>SignTool sign /f <b>MyCert</b>.pfx MyControl.exe</pre>

El comando siguiente firma el archivo mediante un certificado almacenado en un archivo PFX protegido con contraseña:

<pre>SignTool sign /f <b>MyCert</b>.pfx /p <b>MyPassword</b> MyControl.exe</pre>

> [!Note]  
> Asegúrese de proteger correctamente la contraseña.

 

El siguiente comando firma y marca de tiempo el archivo:

<pre>SignTool sign /f <b>MyCert</b>.pfx /t http://timestamp.digicert.com MyControl.exe</pre>

> [!Note]  
> Para obtener información sobre la marca de tiempo de un archivo después de que ya se haya firmado, vea [Adding Time Stamps to Previously Signed Files](adding-time-stamps-to-previously-signed-files.md).

 

El comando siguiente firma el archivo mediante un certificado ubicado en Mi tienda con un nombre de sujeto de Mi empresa Publisher:

<pre>SignTool sign /n "<b>My Company Publisher</b>" MyControl.exe</pre>

El comando siguiente firma un control ActiveX y proporciona información que Internet Explorer cuando se le pide al usuario que instale el control:

<pre>SignTool sign /f <b>MyCert</b>.pfx /d "<b>My Product Name</b>" /du <b>"https://www.example.com/myproductinfo.html"</b> MyControl.exe</pre>

El comando siguiente firma el archivo mediante un certificado cuya [*información de clave*](../secgloss/p-gly.md) privada está protegida por un módulo criptografía de hardware. Por ejemplo, suponga que el certificado denominado "Mi certificado de High-Value" tiene una clave privada instalada en un módulo criptografía de hardware y que el certificado está instalado correctamente.

<pre>SignTool sign /n "<b>My High-Value Certificate</b>" MyControl.exe</pre>

El comando siguiente firma el archivo mediante un certificado cuya [*información de clave*](../secgloss/p-gly.md) privada está protegida por un módulo criptografía de hardware. Se especifica un almacén de equipos para el [*almacén de entidad de certificación*](../secgloss/c-gly.md) (CA).

<pre>SignTool sign /n "<b>My High Value Certificate</b>" /sm /s CA MyControl.exe</pre>

El comando siguiente firma el archivo mediante un certificado almacenado en un archivo. La información de clave privada está protegida por un módulo criptográfico [](../secgloss/k-gly.md) de hardware y el proveedor de servicios criptográficos [*(CSP)*](../secgloss/c-gly.md) y el contenedor de claves se especifican por nombre. Este comando es útil si el certificado no está instalado correctamente.

<pre>SignTool sign /f <b>HighValue</b>.cer /csp "<b>Hardware Cryptography Module</b>" /k <b>HighValueContainer</b> MyControl.exe</pre>

[SignTool](signtool.md) devuelve texto de línea de comandos que indica el resultado de la operación de firma. Además, SignTool devuelve un código de salida de cero para la ejecución correcta, uno para la ejecución con errores y dos para la ejecución que se completó con advertencias.

Para obtener información sobre cómo comprobar la firma de un archivo, vea [Usar SignTool para comprobar una firma de archivo.](using-signtool-to-verify-a-file-signature.md) Para obtener información sobre cómo agregar una marca de tiempo si el archivo ya se ha firmado, vea [Adding Time Stamps to Previously Signed Files](adding-time-stamps-to-previously-signed-files.md). Para obtener información adicional sobre [SignTool,](signtool.md)vea [SignTool](signtool.md).

 

 
