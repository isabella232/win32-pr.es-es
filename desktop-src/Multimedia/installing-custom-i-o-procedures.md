---
title: Instalación de procedimientos de e/s personalizados
description: Instalación de procedimientos de e/s personalizados
ms.assetid: 7b26a062-fa52-4de3-b8c8-b9f9167068fc
keywords:
- e/s de archivos multimedia, procedimientos personalizados
- e/s de archivos, procedimientos personalizados
- entrada y salida (e/s), procedimientos personalizados
- E/s (entrada y salida), procedimientos personalizados
- instalación de procedimientos de e/s personalizados
- e/s personalizada
- mmioInstallIOProc función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1574b7076e7344fa8e800ef1f18ad13fcfd3f3af
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420704"
---
# <a name="installing-custom-io-procedures"></a><span data-ttu-id="442d3-110">Instalación de procedimientos de e/s personalizados</span><span class="sxs-lookup"><span data-stu-id="442d3-110">Installing Custom I/O Procedures</span></span>

<span data-ttu-id="442d3-111">Para instalar un procedimiento de e/s asociado a. Extensión de nombre de archivo ARC, use la función [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="442d3-111">To install an I/O procedure associated with the .ARC filename extension, use the [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) function as follows:</span></span>


```C++
mmioInstallIOProc (mmioFOURCC('A', 'R', 'C', ' '), 
    (LPMMIOPROC)lpmmioproc, MMIO_INSTALLPROC); 
```



<span data-ttu-id="442d3-112">Al instalar un procedimiento de e/s mediante [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc), el procedimiento permanece instalado hasta que lo quite.</span><span class="sxs-lookup"><span data-stu-id="442d3-112">When you install an I/O procedure using [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc), the procedure remains installed until you remove it.</span></span> <span data-ttu-id="442d3-113">El procedimiento de e/s se usa para cualquier archivo que se abra siempre que el archivo tenga la extensión de nombre de archivo adecuada.</span><span class="sxs-lookup"><span data-stu-id="442d3-113">The I/O procedure is used for any file you open as long as the file has the appropriate filename extension.</span></span>

<span data-ttu-id="442d3-114">También puede instalar temporalmente un procedimiento de e/s mediante la función [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) .</span><span class="sxs-lookup"><span data-stu-id="442d3-114">You can also temporarily install an I/O procedure by using the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function.</span></span> <span data-ttu-id="442d3-115">En este caso, el procedimiento de e/s se usa solo con un archivo abierto mediante **mmioOpen** y se quita cuando se cierra el archivo mediante la función [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) .</span><span class="sxs-lookup"><span data-stu-id="442d3-115">In this case, the I/O procedure is used only with a file opened by using **mmioOpen** and is removed when the file is closed by using the [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) function.</span></span> <span data-ttu-id="442d3-116">Para especificar un procedimiento de e/s al abrir un archivo con **mmioOpen**, use el parámetro *lpmmioinfo* para hacer referencia a una estructura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="442d3-116">To specify an I/O procedure when you open a file by using **mmioOpen**, use the *lpmmioinfo* parameter to reference an [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure as follows:</span></span>

1.  <span data-ttu-id="442d3-117">Establezca el miembro **fccIOProc** en **null**.</span><span class="sxs-lookup"><span data-stu-id="442d3-117">Set the **fccIOProc** member to **NULL**.</span></span>
2.  <span data-ttu-id="442d3-118">Establezca el miembro **pIOProc** en la dirección de instancia de procedimiento del procedimiento de e/s.</span><span class="sxs-lookup"><span data-stu-id="442d3-118">Set the **pIOProc** member to the procedure-instance address of the I/O procedure.</span></span>
3.  <span data-ttu-id="442d3-119">Establezca el resto de miembros en cero (a menos que esté abriendo un archivo de memoria o leyendo o escribiendo directamente en el búfer de e/s de archivo).</span><span class="sxs-lookup"><span data-stu-id="442d3-119">Set all other members to zero (unless you are opening a memory file, or directly reading or writing to the file I/O buffer).</span></span>

<span data-ttu-id="442d3-120">Asegúrese de quitar los procedimientos de e/s que haya instalado antes de salir de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="442d3-120">Be sure to remove any I/O procedures you have installed before you exit your application.</span></span>

 

 