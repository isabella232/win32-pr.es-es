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
# <a name="using-signtool-to-verify-a-file-signature"></a><span data-ttu-id="dcfa5-103">Usar SignTool para comprobar una firma de archivo</span><span class="sxs-lookup"><span data-stu-id="dcfa5-103">Using SignTool to Verify a File Signature</span></span>

<span data-ttu-id="dcfa5-104">El comando siguiente comprueba la firma de un archivo denominado *MyControl.exe*:</span><span class="sxs-lookup"><span data-stu-id="dcfa5-104">The following command verifies the signature of a file named *MyControl.exe*:</span></span>

<span data-ttu-id="dcfa5-105">**Comprobación** de la *MyControl.exe* de SignTool</span><span class="sxs-lookup"><span data-stu-id="dcfa5-105">**SignTool verify** *MyControl.exe*</span></span>

<span data-ttu-id="dcfa5-106">Si se produce un error en el ejemplo anterior, es posible que la firma use un certificado de firma de código.</span><span class="sxs-lookup"><span data-stu-id="dcfa5-106">If the preceding example fails, it could be that the signature used a code-signing certificate.</span></span> <span data-ttu-id="dcfa5-107">De forma predeterminada, [SignTool](signtool.md) es la Directiva de controladores de Windows para la comprobación.</span><span class="sxs-lookup"><span data-stu-id="dcfa5-107">[SignTool](signtool.md) defaults to the Windows driver policy for verification.</span></span>

<span data-ttu-id="dcfa5-108">El siguiente comando comprueba la firma mediante la Directiva de comprobación de autenticación predeterminada:</span><span class="sxs-lookup"><span data-stu-id="dcfa5-108">The following command verifies the signature, using the Default Authentication Verification Policy:</span></span>

<span data-ttu-id="dcfa5-109">**Comprobación de SignTool** *MyControl.exe* /PA</span><span class="sxs-lookup"><span data-stu-id="dcfa5-109">**SignTool verify /pa** *MyControl.exe*</span></span>

<span data-ttu-id="dcfa5-110">El comando siguiente comprueba un archivo del sistema que puede estar firmado en un catálogo:</span><span class="sxs-lookup"><span data-stu-id="dcfa5-110">The following command verifies a system file that may be signed in a catalog:</span></span>

<span data-ttu-id="dcfa5-111">**Comprobación de SignTool** *SysFile.dll*</span><span class="sxs-lookup"><span data-stu-id="dcfa5-111">**SignTool verify /a** *SysFile.dll*</span></span>

<span data-ttu-id="dcfa5-112">El comando siguiente comprueba un archivo del sistema firmado en un catálogo denominado *MyCat.cat*:</span><span class="sxs-lookup"><span data-stu-id="dcfa5-112">The following command verifies a system file that is signed in a catalog named *MyCat.cat*:</span></span>

<span data-ttu-id="dcfa5-113">Comprobar si se ha **comprobado/c** *MyCat.catMyFile.ini*</span><span class="sxs-lookup"><span data-stu-id="dcfa5-113">**SignTool verify /c** *MyCat.catMyFile.ini*</span></span>

<span data-ttu-id="dcfa5-114">Para cualquier comprobación de [SignTool](signtool.md) , puede recuperar el firmante del certificado.</span><span class="sxs-lookup"><span data-stu-id="dcfa5-114">For any [SignTool](signtool.md) verification, you can retrieve the signer of the certificate.</span></span> <span data-ttu-id="dcfa5-115">El comando siguiente comprueba un archivo del sistema y muestra el certificado del firmante:</span><span class="sxs-lookup"><span data-stu-id="dcfa5-115">The following command verifies a system file and displays the signer certificate:</span></span>

<span data-ttu-id="dcfa5-116">**Comprobación de SignTool/v** *MyControl.exe*</span><span class="sxs-lookup"><span data-stu-id="dcfa5-116">**SignTool verify /v** *MyControl.exe*</span></span>

<span data-ttu-id="dcfa5-117">[SignTool](signtool.md) devuelve el texto de la línea de comandos que indica el resultado de la comprobación de la firma.</span><span class="sxs-lookup"><span data-stu-id="dcfa5-117">[SignTool](signtool.md) returns command-line text that states the result of the signature check.</span></span> <span data-ttu-id="dcfa5-118">Además, SignTool devuelve un código de salida de cero para que la ejecución sea correcta, una para la ejecución errónea y dos para la ejecución completada con advertencias.</span><span class="sxs-lookup"><span data-stu-id="dcfa5-118">Additionally, SignTool returns an exit code of zero for successful execution, one for failed execution, and two for execution that completed with warnings.</span></span>

<span data-ttu-id="dcfa5-119">Para obtener más información sobre [SignTool](signtool.md), consulte [SignTool](signtool.md).</span><span class="sxs-lookup"><span data-stu-id="dcfa5-119">For more information about [SignTool](signtool.md), see [SignTool](signtool.md).</span></span>

 

 



