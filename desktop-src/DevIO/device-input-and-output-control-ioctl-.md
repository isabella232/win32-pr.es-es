---
description: La función DeviceIoControl proporciona una interfaz de control de entrada y salida (IOCTL) de dispositivo a través de la cual una aplicación puede comunicarse directamente con un controlador de dispositivo.
ms.assetid: 2dffd86a-162c-4e09-bfa1-73b87522741a
title: Control de entrada y salida de dispositivo (IOCTL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce2bb2ee26c63c2aad02d8e8d167ff12383fc6b8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907409"
---
# <a name="device-input-and-output-control-ioctl"></a><span data-ttu-id="91e29-103">Control de entrada y salida de dispositivo (IOCTL)</span><span class="sxs-lookup"><span data-stu-id="91e29-103">Device Input and Output Control (IOCTL)</span></span>

<span data-ttu-id="91e29-104">La función [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) proporciona una interfaz de control de entrada y salida (ioctl) de dispositivo a través de la cual una aplicación puede comunicarse directamente con un controlador de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="91e29-104">The [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function provides a device input and output control (IOCTL) interface through which an application can communicate directly with a device driver.</span></span> <span data-ttu-id="91e29-105">La función **DeviceIoControl** es una interfaz de uso general que puede enviar códigos de control a una variedad de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="91e29-105">The **DeviceIoControl** function is a general-purpose interface that can send control codes to a variety of devices.</span></span> <span data-ttu-id="91e29-106">Cada código de control representa una operación que el controlador debe realizar.</span><span class="sxs-lookup"><span data-stu-id="91e29-106">Each control code represents an operation for the driver to perform.</span></span> <span data-ttu-id="91e29-107">Por ejemplo, un código de control puede pedir a un controlador de dispositivo que devuelva información sobre el dispositivo correspondiente, o bien dirigir el controlador para llevar a cabo una acción en el dispositivo, como el formato de un disco.</span><span class="sxs-lookup"><span data-stu-id="91e29-107">For example, a control code can ask a device driver to return information about the corresponding device, or direct the driver to carry out an action on the device, such as formatting a disk.</span></span>

<span data-ttu-id="91e29-108">En los archivos de encabezado del SDK se definen varios códigos de control estándar.</span><span class="sxs-lookup"><span data-stu-id="91e29-108">A number of standard control codes are defined in the SDK header files.</span></span> <span data-ttu-id="91e29-109">Además, los controladores de dispositivo pueden definir sus propios códigos de control específicos del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="91e29-109">In addition, device drivers can define their own device-specific control codes.</span></span> <span data-ttu-id="91e29-110">Para obtener una lista de los códigos de control estándar que se incluyen en la documentación del SDK, consulte la sección Comentarios de [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol).</span><span class="sxs-lookup"><span data-stu-id="91e29-110">For a list of standard control codes included in the SDK documentation, see the Remarks section of [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol).</span></span>

<span data-ttu-id="91e29-111">Los tipos de códigos de control que puede especificar dependen del dispositivo al que se está accediendo y de la plataforma en la que se ejecuta la aplicación.</span><span class="sxs-lookup"><span data-stu-id="91e29-111">The types of control codes you can specify depend on the device being accessed and the platform on which your application is running.</span></span> <span data-ttu-id="91e29-112">Las aplicaciones pueden usar códigos de control estándar o códigos de control específicos del dispositivo para realizar operaciones de entrada y salida directas en una unidad de disquete, en una unidad de disco duro, en una unidad de cinta o en una unidad de CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="91e29-112">Applications can use the standard control codes or device-specific control codes to perform direct input and output operations on a floppy disk drive, hard disk drive, tape drive, or CD-ROM drive.</span></span>

## <a name="related-topics"></a><span data-ttu-id="91e29-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="91e29-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91e29-114">Llamar a DeviceIoControl</span><span class="sxs-lookup"><span data-stu-id="91e29-114">Calling DeviceIoControl</span></span>](calling-deviceiocontrol.md)
</dt> </dl>

 

 
