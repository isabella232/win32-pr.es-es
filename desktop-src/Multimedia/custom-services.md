---
title: Servicios personalizados
description: Servicios personalizados
ms.assetid: 98b68205-3a34-4406-84de-bf2c8a5ed5b0
keywords:
- e/s de archivos multimedia, servicios personalizados
- e/s de archivos, servicios personalizados
- entrada y salida (e/s), servicios personalizados
- E/s (entrada y salida), servicios personalizados
- e/s personalizada
- mmioInstallIOProc función)
- mmioOpen función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e41e3c5974fee9903c0864b1cfefccc8354b26a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077705"
---
# <a name="custom-services"></a><span data-ttu-id="b8c7b-110">Servicios personalizados</span><span class="sxs-lookup"><span data-stu-id="b8c7b-110">Custom Services</span></span>

<span data-ttu-id="b8c7b-111">Los servicios de e/s de archivos multimedia usan procedimientos de e/s para controlar la entrada y la salida física asociadas a la lectura y la escritura en diferentes tipos de sistemas de almacenamiento, como sistemas de archivo de archivos y sistemas de almacenamiento de base de datos.</span><span class="sxs-lookup"><span data-stu-id="b8c7b-111">Multimedia file I/O services use I/O procedures to handle the physical input and output associated with reading and writing to different types of storage systems, such as file-archival systems and database-storage systems.</span></span> <span data-ttu-id="b8c7b-112">Existen procedimientos de e/s predefinidos para los sistemas de archivos estándar y para los archivos de memoria, pero puede proporcionar un procedimiento de e/s personalizado para tener acceso a un sistema de almacenamiento único mediante la función [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) .</span><span class="sxs-lookup"><span data-stu-id="b8c7b-112">Predefined I/O procedures exist for the standard file systems and for memory files, but you can supply a custom I/O procedure for accessing a unique storage system by using the [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) function.</span></span>

<span data-ttu-id="b8c7b-113">Para abrir un archivo mediante un procedimiento de e/s personalizado, use la función [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) .</span><span class="sxs-lookup"><span data-stu-id="b8c7b-113">To open a file by using a custom I/O procedure, use the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function.</span></span> <span data-ttu-id="b8c7b-114">Incluya un signo más (+) o la constante CFSEPCHAR en el nombre de archivo para separar el nombre del archivo físico del nombre del elemento del archivo que desea abrir.</span><span class="sxs-lookup"><span data-stu-id="b8c7b-114">Include a plus sign (+) or the CFSEPCHAR constant in the filename to separate the name of the physical file from the name of the element of the file you want to open.</span></span> <span data-ttu-id="b8c7b-115">En el ejemplo siguiente se abre un elemento de archivo denominado "Element" desde un archivo denominado FILENAME. VERÍA</span><span class="sxs-lookup"><span data-stu-id="b8c7b-115">The following example opens a file element named "element" from a file named FILENAME.ARC:</span></span>


```C++
mmioOpen("filename.arc+element", NULL, MMIO_READ); 
```



<span data-ttu-id="b8c7b-116">Cuando el administrador de e/s de archivos encuentra un signo más en un nombre de archivo, examina la extensión del nombre de archivo para determinar el procedimiento de e/s que se va a asociar al archivo.</span><span class="sxs-lookup"><span data-stu-id="b8c7b-116">When the file I/O manager encounters a plus sign in a filename, it examines the filename extension to determine which I/O procedure to associate with the file.</span></span> <span data-ttu-id="b8c7b-117">En el ejemplo anterior, el administrador de e/s de archivos intentaría usar el procedimiento de e/s asociado a. Extensión de nombre de archivo ARC; Este procedimiento de e/s se habría instalado con [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc).</span><span class="sxs-lookup"><span data-stu-id="b8c7b-117">In the previous example, the file I/O manager would attempt to use the I/O procedure associated with the .ARC filename extension; this I/O procedure would have been installed by using [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc).</span></span> <span data-ttu-id="b8c7b-118">Si no hay ningún procedimiento de e/s instalado, [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="b8c7b-118">If no I/O procedure is installed, [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) returns an error.</span></span>

<span data-ttu-id="b8c7b-119">Los procedimientos de e/s deben responder a los siguientes mensajes:</span><span class="sxs-lookup"><span data-stu-id="b8c7b-119">I/O procedures must respond to the following messages:</span></span>

-   [<span data-ttu-id="b8c7b-120">**MMIOM \_ cerrar**</span><span class="sxs-lookup"><span data-stu-id="b8c7b-120">**MMIOM\_CLOSE**</span></span>](mmiom-close.md)
-   [<span data-ttu-id="b8c7b-121">**MMIOM \_ abrir**</span><span class="sxs-lookup"><span data-stu-id="b8c7b-121">**MMIOM\_OPEN**</span></span>](mmiom-open.md)
-   [<span data-ttu-id="b8c7b-122">**MMIOM \_ lectura**</span><span class="sxs-lookup"><span data-stu-id="b8c7b-122">**MMIOM\_READ**</span></span>](mmiom-read.md)
-   [<span data-ttu-id="b8c7b-123">**escritura de MMIOM \_**</span><span class="sxs-lookup"><span data-stu-id="b8c7b-123">**MMIOM\_WRITE**</span></span>](mmiom-write.md)
-   [<span data-ttu-id="b8c7b-124">**búsqueda de MMIOM \_**</span><span class="sxs-lookup"><span data-stu-id="b8c7b-124">**MMIOM\_SEEK**</span></span>](mmiom-seek.md)
-   [<span data-ttu-id="b8c7b-125">**MMIOM \_ cambiar nombre**</span><span class="sxs-lookup"><span data-stu-id="b8c7b-125">**MMIOM\_RENAME**</span></span>](mmiom-rename.md)
-   [<span data-ttu-id="b8c7b-126">**MMIOM \_ WRITEFLUSH**</span><span class="sxs-lookup"><span data-stu-id="b8c7b-126">**MMIOM\_WRITEFLUSH**</span></span>](mmiom-writeflush.md)

<span data-ttu-id="b8c7b-127">También puede crear mensajes personalizados y enviarlos al procedimiento de e/s mediante la función [**mmioSendMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosendmessage) .</span><span class="sxs-lookup"><span data-stu-id="b8c7b-127">You can also create custom messages and send them to your I/O procedure by using the [**mmioSendMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosendmessage) function.</span></span> <span data-ttu-id="b8c7b-128">Si define sus propios mensajes, asegúrese de que están definidos en o por encima del valor definido por la \_ constante de usuario MMIOM.</span><span class="sxs-lookup"><span data-stu-id="b8c7b-128">If you define your own messages, make sure they are defined at or above the value defined by the MMIOM\_USER constant.</span></span>

<span data-ttu-id="b8c7b-129">Además de procesar mensajes, un procedimiento de e/s debe mantener el miembro **lDiskOffset** de la estructura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) (al que apunta el parámetro *lpmmioinfo* de la función **mmioOpen** ).</span><span class="sxs-lookup"><span data-stu-id="b8c7b-129">In addition to processing messages, an I/O procedure must maintain the **lDiskOffset** member of the [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure (pointed to by the *lpmmioinfo* parameter of the **mmioOpen** function).</span></span> <span data-ttu-id="b8c7b-130">El miembro **lDiskOffset** debe contener siempre el desplazamiento de archivo en la ubicación a la que tendrá acceso el siguiente MMIOM de \_ lectura o MMIOM escritura de \_ .</span><span class="sxs-lookup"><span data-stu-id="b8c7b-130">The **lDiskOffset** member must always contain the file offset to the location that the next MMIOM\_READ or MMIOM\_WRITE message will access.</span></span> <span data-ttu-id="b8c7b-131">El desplazamiento se especifica en bytes y es relativo al principio del archivo.</span><span class="sxs-lookup"><span data-stu-id="b8c7b-131">The offset is specified in bytes and is relative to the beginning of the file.</span></span> <span data-ttu-id="b8c7b-132">El procedimiento de e/s puede usar el miembro **adwInfo** para mantener la información de estado necesaria.</span><span class="sxs-lookup"><span data-stu-id="b8c7b-132">The I/O procedure can use the **adwInfo** member to maintain any required state information.</span></span> <span data-ttu-id="b8c7b-133">El procedimiento de e/s no debe modificar ningún otro miembro de la estructura **MMIOINFO** .</span><span class="sxs-lookup"><span data-stu-id="b8c7b-133">The I/O procedure should not modify any other members in the **MMIOINFO** structure.</span></span>

 

 