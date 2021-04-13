---
title: Compartir un procedimiento de e/s con otras aplicaciones
description: Compartir un procedimiento de e/s con otras aplicaciones
ms.assetid: 56e4804b-fe88-4b3b-93f6-f8e41048780d
keywords:
- e/s de archivos multimedia, procedimientos compartidos
- e/s de archivos, procedimientos compartidos
- entrada y salida (e/s), procedimientos compartidos
- E/s (entrada y salida), procedimientos compartidos
- compartir procedimientos de e/s con otras aplicaciones
- mmioInstallIOProc función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd7931bde28338cc625c828128e05047d8ec3370
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420594"
---
# <a name="sharing-an-io-procedure-with-other-applications"></a><span data-ttu-id="2e549-109">Compartir un procedimiento de e/s con otras aplicaciones</span><span class="sxs-lookup"><span data-stu-id="2e549-109">Sharing an I/O Procedure with Other Applications</span></span>

<span data-ttu-id="2e549-110">Si desea compartir un procedimiento de e/s con otras aplicaciones, debe escribir una biblioteca de vínculos dinámicos (DLL) para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="2e549-110">If you want to share an I/O procedure with other applications, you need to write a dynamic-link library (DLL) for your application.</span></span> <span data-ttu-id="2e549-111">Puede compartir el procedimiento de e/s mediante una de las siguientes acciones:</span><span class="sxs-lookup"><span data-stu-id="2e549-111">You can share the I/O procedure by doing one of the following:</span></span>

-   <span data-ttu-id="2e549-112">Incluya el código para el procedimiento de e/s en el archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="2e549-112">Include the code for the I/O procedure in the DLL.</span></span>
-   <span data-ttu-id="2e549-113">Cree una función en el archivo DLL que llame a la función [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) para instalar el procedimiento de e/s.</span><span class="sxs-lookup"><span data-stu-id="2e549-113">Create a function in the DLL that calls the [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) function to install the I/O procedure.</span></span>
-   <span data-ttu-id="2e549-114">Exporte esta función en el archivo de definiciones de módulo de la DLL.</span><span class="sxs-lookup"><span data-stu-id="2e549-114">Export this function in the module-definitions file of the DLL.</span></span>

<span data-ttu-id="2e549-115">Para usar el procedimiento de e/s compartido, una aplicación debe llamar primero a la función en el archivo DLL para instalar el procedimiento de e/s.</span><span class="sxs-lookup"><span data-stu-id="2e549-115">To use the shared I/O procedure, an application must first call the function in the DLL to install the I/O procedure.</span></span>

 

 