---
description: Un proceso utiliza la función CreateFile para abrir un identificador de un recurso de comunicaciones.
ms.assetid: eaef6067-97a6-40c4-84ec-c0d86af6bb4a
title: Identificadores de recursos de comunicaciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f709fc041f6125d93a1c52f3e17b77c96f35825c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423355"
---
# <a name="communications-resource-handles"></a><span data-ttu-id="cd097-103">Identificadores de recursos de comunicaciones</span><span class="sxs-lookup"><span data-stu-id="cd097-103">Communications Resource Handles</span></span>

<span data-ttu-id="cd097-104">Un proceso utiliza la función [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir un identificador de un recurso de comunicaciones.</span><span class="sxs-lookup"><span data-stu-id="cd097-104">A process uses the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function to open a handle to a communications resource.</span></span> <span data-ttu-id="cd097-105">Por ejemplo, si se especifica COM1, se abre un identificador de un puerto serie y LPT1 se abre un identificador a un puerto paralelo.</span><span class="sxs-lookup"><span data-stu-id="cd097-105">For example, specifying COM1 opens a handle to a serial port, and LPT1 opens a handle to a parallel port.</span></span> <span data-ttu-id="cd097-106">Si otro proceso está usando actualmente el recurso especificado, se produce un error en **CreateFile** .</span><span class="sxs-lookup"><span data-stu-id="cd097-106">If the specified resource is currently being used by another process, **CreateFile** fails.</span></span> <span data-ttu-id="cd097-107">Cualquier subproceso del proceso puede utilizar el identificador devuelto por **CreateFile** para identificar el recurso en cualquiera de las funciones que tienen acceso al recurso.</span><span class="sxs-lookup"><span data-stu-id="cd097-107">Any thread of the process can use the handle returned by **CreateFile** to identify the resource in any of the functions that access the resource.</span></span>

<span data-ttu-id="cd097-108">Cuando el proceso llama a [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir un recurso de comunicaciones, especifica los siguientes atributos:</span><span class="sxs-lookup"><span data-stu-id="cd097-108">When the process calls [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) to open a communications resource, it specifies the following attributes:</span></span>

-   <span data-ttu-id="cd097-109">El tipo de acceso de lectura y escritura para el recurso especificado.</span><span class="sxs-lookup"><span data-stu-id="cd097-109">What type of read/write access exists for the specified resource.</span></span>
-   <span data-ttu-id="cd097-110">Si los procesos secundarios pueden heredar el identificador.</span><span class="sxs-lookup"><span data-stu-id="cd097-110">Whether the handle can be inherited by child processes.</span></span>
-   <span data-ttu-id="cd097-111">Si el identificador se puede usar en operaciones de e/s superpuestas (asincrónicas).</span><span class="sxs-lookup"><span data-stu-id="cd097-111">Whether the handle can be used in overlapped (asynchronous) I/O operations.</span></span> <span data-ttu-id="cd097-112">(Para obtener una descripción de las operaciones superpuestas, vea [Synchronization](/windows/desktop/Sync/synchronization)).</span><span class="sxs-lookup"><span data-stu-id="cd097-112">(For a description of overlapped operations, see [Synchronization](/windows/desktop/Sync/synchronization).)</span></span>

<span data-ttu-id="cd097-113">Cuando el proceso utiliza [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir un recurso de comunicaciones, debe especificar ciertos valores para los parámetros siguientes:</span><span class="sxs-lookup"><span data-stu-id="cd097-113">When the process uses [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) to open a communications resource, it must specify certain values for the following parameters:</span></span>

-   <span data-ttu-id="cd097-114">El parámetro *fdwShareMode* debe ser cero y abrir el recurso para el acceso exclusivo.</span><span class="sxs-lookup"><span data-stu-id="cd097-114">The *fdwShareMode* parameter must be zero, opening the resource for exclusive access.</span></span>
-   <span data-ttu-id="cd097-115">El parámetro *fdwCreate* debe especificar la \_ marca existente abrir.</span><span class="sxs-lookup"><span data-stu-id="cd097-115">The *fdwCreate* parameter must specify the OPEN\_EXISTING flag.</span></span>
-   <span data-ttu-id="cd097-116">El parámetro *hTemplateFile* debe ser **null**.</span><span class="sxs-lookup"><span data-stu-id="cd097-116">The *hTemplateFile* parameter must be **NULL**.</span></span>

<span data-ttu-id="cd097-117">Al usar [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir un controlador directamente en un dispositivo, una aplicación debe usar los caracteres especiales " \\ \\ . \\ " para identificar el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cd097-117">When using [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) to open a handle directly to a device, an application must use the special characters " \\\\ .\\" to identify the device.</span></span> <span data-ttu-id="cd097-118">Por ejemplo, para abrir un identificador de la unidad a, especifique \\ \\ . \\ r: para el parámetro *lpszName* de **CreateFile**.</span><span class="sxs-lookup"><span data-stu-id="cd097-118">For example, to open a handle to drive A, specify \\\\ .\\a: for the *lpszName* parameter of **CreateFile**.</span></span> <span data-ttu-id="cd097-119">El proceso de llamada puede usar el identificador de la función [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) para enviar códigos de control al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cd097-119">The calling process can use the handle in the [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function to send control codes to the device.</span></span>

 

 
