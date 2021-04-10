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
# <a name="using-signtool-to-sign-a-file"></a><span data-ttu-id="7c17b-103">Usar SignTool para firmar un archivo</span><span class="sxs-lookup"><span data-stu-id="7c17b-103">Using SignTool to Sign a File</span></span>

<span data-ttu-id="7c17b-104">El comando siguiente firma el archivo denominado MyControl.exe mediante un [*certificado*](../secgloss/c-gly.md) almacenado en un archivo de intercambio de información personal (pfx):</span><span class="sxs-lookup"><span data-stu-id="7c17b-104">The following command signs the file named MyControl.exe using a [*certificate*](../secgloss/c-gly.md) stored in a Personal Information Exchange (PFX) file:</span></span>

<pre>SignTool sign /f <b>MyCert</b>.pfx MyControl.exe</pre>

<span data-ttu-id="7c17b-105">El siguiente comando firma el archivo con un certificado almacenado en un archivo PFX protegido por contraseña:</span><span class="sxs-lookup"><span data-stu-id="7c17b-105">The following command signs the file using a certificate stored in a password-protected PFX file:</span></span>

<pre>SignTool sign /f <b>MyCert</b>.pfx /p <b>MyPassword</b> MyControl.exe</pre>

> [!Note]  
> <span data-ttu-id="7c17b-106">Asegúrese de que protege correctamente la contraseña.</span><span class="sxs-lookup"><span data-stu-id="7c17b-106">Ensure that you properly protect the password.</span></span>

 

<span data-ttu-id="7c17b-107">El siguiente comando firma y marca de tiempo el archivo:</span><span class="sxs-lookup"><span data-stu-id="7c17b-107">The following command signs and time stamps the file:</span></span>

<pre>SignTool sign /f <b>MyCert</b>.pfx /t http://timestamp.digicert.com MyControl.exe</pre>

> [!Note]  
> <span data-ttu-id="7c17b-108">Para obtener información acerca de la marca de tiempo de un archivo una vez que ya se ha firmado, vea [Agregar marcas de tiempo a archivos firmados anteriormente](adding-time-stamps-to-previously-signed-files.md).</span><span class="sxs-lookup"><span data-stu-id="7c17b-108">For information about time stamping a file after it has already been signed, see [Adding Time Stamps to Previously Signed Files](adding-time-stamps-to-previously-signed-files.md).</span></span>

 

<span data-ttu-id="7c17b-109">El comando siguiente firma el archivo con un certificado ubicado en el almacén My con un nombre de sujeto del publicador de la compañía:</span><span class="sxs-lookup"><span data-stu-id="7c17b-109">The following command signs the file using a certificate located in the My store with a subject name of My Company Publisher:</span></span>

<pre>SignTool sign /n "<b>My Company Publisher</b>" MyControl.exe</pre>

<span data-ttu-id="7c17b-110">El comando siguiente firma un control ActiveX y proporciona información que Internet Explorer muestra cuando se solicita al usuario que instale el control:</span><span class="sxs-lookup"><span data-stu-id="7c17b-110">The following command signs an ActiveX control and provides information that is displayed by Internet Explorer when the user is prompted to install the control:</span></span>

<pre>SignTool sign /f <b>MyCert</b>.pfx /d "<b>My Product Name</b>" /du <b>"https://www.example.com/myproductinfo.html"</b> MyControl.exe</pre>

<span data-ttu-id="7c17b-111">El siguiente comando firma el archivo con un certificado cuya información de [*clave privada*](../secgloss/p-gly.md) está protegida por un módulo de criptografía de hardware.</span><span class="sxs-lookup"><span data-stu-id="7c17b-111">The following command signs the file using a certificate whose [*private key*](../secgloss/p-gly.md) information is protected by a hardware cryptography module.</span></span> <span data-ttu-id="7c17b-112">Por ejemplo, supongamos que el certificado denominado "mi High-Value certificado" tiene una clave privada instalada en un módulo de criptografía de hardware y el certificado está instalado correctamente.</span><span class="sxs-lookup"><span data-stu-id="7c17b-112">For example purposes, assume that the certificate called "My High-Value Certificate," has a private key installed in a hardware cryptography module, and the certificate is properly installed.</span></span>

<pre>SignTool sign /n "<b>My High-Value Certificate</b>" MyControl.exe</pre>

<span data-ttu-id="7c17b-113">El siguiente comando firma el archivo con un certificado cuya información de [*clave privada*](../secgloss/p-gly.md) está protegida por un módulo de criptografía de hardware.</span><span class="sxs-lookup"><span data-stu-id="7c17b-113">The following command signs the file using a certificate whose [*private key*](../secgloss/p-gly.md) information is protected by a hardware cryptography module.</span></span> <span data-ttu-id="7c17b-114">Se especifica un almacén del equipo para el almacén de la [*entidad de certificación*](../secgloss/c-gly.md) (CA).</span><span class="sxs-lookup"><span data-stu-id="7c17b-114">A computer store is specified for the [*certification authority*](../secgloss/c-gly.md) (CA) store.</span></span>

<pre>SignTool sign /n "<b>My High Value Certificate</b>" /sm /s CA MyControl.exe</pre>

<span data-ttu-id="7c17b-115">El comando siguiente firma el archivo con un certificado almacenado en un archivo.</span><span class="sxs-lookup"><span data-stu-id="7c17b-115">The following command signs the file using a certificate stored in a file.</span></span> <span data-ttu-id="7c17b-116">La información de la clave privada está protegida por un módulo de criptografía de hardware, y el [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) y el [*contenedor de claves*](../secgloss/k-gly.md) se especifican mediante el nombre.</span><span class="sxs-lookup"><span data-stu-id="7c17b-116">The private key information is protected by a hardware cryptography module, and the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP)and [*key container*](../secgloss/k-gly.md) are specified by name.</span></span> <span data-ttu-id="7c17b-117">Este comando es útil si el certificado no está instalado correctamente.</span><span class="sxs-lookup"><span data-stu-id="7c17b-117">This command is useful if the certificate is not properly installed.</span></span>

<pre>SignTool sign /f <b>HighValue</b>.cer /csp "<b>Hardware Cryptography Module</b>" /k <b>HighValueContainer</b> MyControl.exe</pre>

<span data-ttu-id="7c17b-118">[SignTool](signtool.md) devuelve el texto de la línea de comandos que indica el resultado de la operación de firma.</span><span class="sxs-lookup"><span data-stu-id="7c17b-118">[SignTool](signtool.md) returns command line text that states the result of the signing operation.</span></span> <span data-ttu-id="7c17b-119">Además, SignTool devuelve un código de salida de cero para que la ejecución sea correcta, una para la ejecución errónea y dos para la ejecución completada con advertencias.</span><span class="sxs-lookup"><span data-stu-id="7c17b-119">Additionally, SignTool returns an exit code of zero for successful execution, one for failed execution, and two for execution that completed with warnings.</span></span>

<span data-ttu-id="7c17b-120">Para obtener información acerca de cómo comprobar la firma de un archivo, consulte [usar SignTool para comprobar una firma de archivo](using-signtool-to-verify-a-file-signature.md).</span><span class="sxs-lookup"><span data-stu-id="7c17b-120">For information about verifying a file's signature, see [Using SignTool to Verify a File Signature](using-signtool-to-verify-a-file-signature.md).</span></span> <span data-ttu-id="7c17b-121">Para obtener información sobre cómo agregar una marca de tiempo si el archivo ya se ha firmado, vea [Agregar marcas de tiempo a archivos firmados anteriormente](adding-time-stamps-to-previously-signed-files.md).</span><span class="sxs-lookup"><span data-stu-id="7c17b-121">For information about adding a time stamp if the file has already been signed, see [Adding Time Stamps to Previously Signed Files](adding-time-stamps-to-previously-signed-files.md).</span></span> <span data-ttu-id="7c17b-122">Para obtener información adicional sobre [SignTool](signtool.md), consulte [SignTool](signtool.md).</span><span class="sxs-lookup"><span data-stu-id="7c17b-122">For additional information about [SignTool](signtool.md), see [SignTool](signtool.md).</span></span>

 

 
