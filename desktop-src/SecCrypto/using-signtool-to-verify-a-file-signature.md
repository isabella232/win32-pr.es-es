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
# <a name="using-signtool-to-verify-a-file-signature"></a><span data-ttu-id="e0ab3-103">Uso de SignTool para comprobar una firma de archivo</span><span class="sxs-lookup"><span data-stu-id="e0ab3-103">Using SignTool to Verify a File Signature</span></span>

<span data-ttu-id="e0ab3-104">El comando siguiente comprueba la firma de un archivo denominado *MyControl.exe*:</span><span class="sxs-lookup"><span data-stu-id="e0ab3-104">The following command verifies the signature of a file named *MyControl.exe*:</span></span>

<span data-ttu-id="e0ab3-105">**Comprobación de signTool** *MyControl.exe*</span><span class="sxs-lookup"><span data-stu-id="e0ab3-105">**SignTool verify** *MyControl.exe*</span></span>

<span data-ttu-id="e0ab3-106">Si se produce un error en el ejemplo anterior, podría ser que la firma usó un certificado de firma de código.</span><span class="sxs-lookup"><span data-stu-id="e0ab3-106">If the preceding example fails, it could be that the signature used a code-signing certificate.</span></span> <span data-ttu-id="e0ab3-107">[SignTool tiene](signtool.md) como valor predeterminado la directiva de controladores de Windows para la comprobación.</span><span class="sxs-lookup"><span data-stu-id="e0ab3-107">[SignTool](signtool.md) defaults to the Windows driver policy for verification.</span></span>

<span data-ttu-id="e0ab3-108">El siguiente comando comprueba la firma mediante la directiva de comprobación de autenticación predeterminada:</span><span class="sxs-lookup"><span data-stu-id="e0ab3-108">The following command verifies the signature, using the Default Authentication Verification Policy:</span></span>

<span data-ttu-id="e0ab3-109">**SignTool verify /pa** *MyControl.exe*</span><span class="sxs-lookup"><span data-stu-id="e0ab3-109">**SignTool verify /pa** *MyControl.exe*</span></span>

<span data-ttu-id="e0ab3-110">El siguiente comando comprueba un archivo del sistema que se puede firmar en un catálogo:</span><span class="sxs-lookup"><span data-stu-id="e0ab3-110">The following command verifies a system file that may be signed in a catalog:</span></span>

<span data-ttu-id="e0ab3-111">**SignTool verify /a** *SysFile.dll*</span><span class="sxs-lookup"><span data-stu-id="e0ab3-111">**SignTool verify /a** *SysFile.dll*</span></span>

<span data-ttu-id="e0ab3-112">El siguiente comando comprueba un archivo del sistema que está firmado en un catálogo denominado *MyCat.cat*:</span><span class="sxs-lookup"><span data-stu-id="e0ab3-112">The following command verifies a system file that is signed in a catalog named *MyCat.cat*:</span></span>

<span data-ttu-id="e0ab3-113">**SignTool verify /c** *MyCat.cat* *MyFile.ini*</span><span class="sxs-lookup"><span data-stu-id="e0ab3-113">**SignTool verify /c** *MyCat.cat* *MyFile.ini*</span></span>

<span data-ttu-id="e0ab3-114">Para cualquier [comprobación de SignTool,](signtool.md) puede recuperar el firmante del certificado.</span><span class="sxs-lookup"><span data-stu-id="e0ab3-114">For any [SignTool](signtool.md) verification, you can retrieve the signer of the certificate.</span></span> <span data-ttu-id="e0ab3-115">El comando siguiente comprueba un archivo del sistema y muestra el certificado de firmante:</span><span class="sxs-lookup"><span data-stu-id="e0ab3-115">The following command verifies a system file and displays the signer certificate:</span></span>

<span data-ttu-id="e0ab3-116">**Comprobación de SignTool /v** *MyControl.exe*</span><span class="sxs-lookup"><span data-stu-id="e0ab3-116">**SignTool verify /v** *MyControl.exe*</span></span>

<span data-ttu-id="e0ab3-117">[SignTool](signtool.md) devuelve texto de línea de comandos que indica el resultado de la comprobación de firma.</span><span class="sxs-lookup"><span data-stu-id="e0ab3-117">[SignTool](signtool.md) returns command-line text that states the result of the signature check.</span></span> <span data-ttu-id="e0ab3-118">Además, SignTool devuelve un código de salida de cero para la ejecución correcta, uno para la ejecución con error y dos para la ejecución que se completó con advertencias.</span><span class="sxs-lookup"><span data-stu-id="e0ab3-118">Additionally, SignTool returns an exit code of zero for successful execution, one for failed execution, and two for execution that completed with warnings.</span></span>

<span data-ttu-id="e0ab3-119">Para obtener más información sobre [SignTool,](signtool.md)vea [SignTool](signtool.md).</span><span class="sxs-lookup"><span data-stu-id="e0ab3-119">For more information about [SignTool](signtool.md), see [SignTool](signtool.md).</span></span>

 

 



