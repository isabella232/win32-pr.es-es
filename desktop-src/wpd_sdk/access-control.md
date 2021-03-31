---
description: Control de acceso
ms.assetid: d17137f9-b206-4ced-82e5-96a7d927c89b
title: Access Control (API de WPD)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7820f38a41cbf9ff0199e5fde8de8ed3609063
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912890"
---
# <a name="access-control-wpd-api"></a><span data-ttu-id="1440a-103">Access Control (API de WPD)</span><span class="sxs-lookup"><span data-stu-id="1440a-103">Access Control (WPD API)</span></span>

<span data-ttu-id="1440a-104">El Modelo de controlador de Windows (WDM) permite restringir el acceso a los dispositivos a través de listas de Access Control (ACL) en los nodos de dispositivo Plug and Play (PnP).</span><span class="sxs-lookup"><span data-stu-id="1440a-104">The Windows Driver Model (WDM) supports restricting device access via Access Control Lists (ACLs) on the Plug and Play (PnP) Device Nodes.</span></span> <span data-ttu-id="1440a-105">Esto significa que los proveedores y administradores de red pueden restringir el acceso a cualquier tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1440a-105">This means that vendors and network administrators can restrict access to any device type.</span></span> <span data-ttu-id="1440a-106">Cuando una aplicación abre un identificador a un controlador mediante una llamada a [**IPortableDevice:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open), el administrador de e/s del controlador comprueba si el usuario especificado tiene el acceso necesario y, de igual modo, realiza comprobaciones de acceso cuando se envía IOCTL al controlador desde ese controlador.</span><span class="sxs-lookup"><span data-stu-id="1440a-106">When an application opens a handle to a driver by calling [**IPortableDevice::Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open), the driver's I/O Manager verifies whether the given user has the required access, and similarly does access checks when IOCTLs are sent to the driver from that handle.</span></span>

<span data-ttu-id="1440a-107">Por ejemplo, un administrador de red puede restringir a los usuarios invitados a acceso de solo lectura para dispositivos portátiles, mientras que pueden conceder a usuarios autenticados acceso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="1440a-107">For example, a network administrator could restrict Guest users to read-only access for portable devices, while they could grant Authenticated users read/write access.</span></span> <span data-ttu-id="1440a-108">En este caso, implica que si un invitado ha emitido un comando de WPD que requiere acceso de lectura y escritura (por ejemplo, eliminar objeto); se produciría un error de acceso denegado, mientras que si un usuario autenticado hubiera emitido el mismo comando, se realizaría correctamente.</span><span class="sxs-lookup"><span data-stu-id="1440a-108">In this case, it implies that if a Guest issued a WPD command that required read/write access (such as Delete Object); it would fail with Access Denied, whereas if an Authenticated user issued the same command, it would succeed.</span></span>

<span data-ttu-id="1440a-109">Las entradas directiva de grupos para controlar el acceso al almacenamiento extraíble y a los dispositivos portátiles no es realmente nada más que una manera sencilla para que los administradores apliquen las ACL de nodo del dispositivo PnP a una clase completa de dispositivos a la vez (por ejemplo, al aplicar el directiva de grupo "denegar el acceso de escritura a dispositivos portátiles" ajustaría las ACL de todos los dispositivos WPD para denegar el acceso</span><span class="sxs-lookup"><span data-stu-id="1440a-109">The Group Policy entries for controlling access to removable storage and portable devices is actually nothing more than an easy way for Administrators to apply PnP device node ACLs to a whole class of devices at a time (for example, applying the "Deny Write Access to Portable Devices" Group Policy would adjust the ACLs of all WPD devices to deny write access).</span></span>

## <a name="io-control-codes-in-wpd"></a><span data-ttu-id="1440a-110">Códigos de control de e/s en WPD</span><span class="sxs-lookup"><span data-stu-id="1440a-110">I/O Control Codes in WPD</span></span>

<span data-ttu-id="1440a-111">Las aplicaciones de WPD se comunican con los controladores abriendo los controladores de dispositivos y enviando códigos de control de e/s (ioctl).</span><span class="sxs-lookup"><span data-stu-id="1440a-111">WPD applications communicate with drivers by opening device handles and sending I/O Control Codes (IOCTLs).</span></span> <span data-ttu-id="1440a-112">Estos ioctl se componen de cuatro secciones:</span><span class="sxs-lookup"><span data-stu-id="1440a-112">These IOCTLs consist of four sections:</span></span>

1.  <span data-ttu-id="1440a-113">Tipo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="1440a-113">Device Type</span></span>
2.  <span data-ttu-id="1440a-114">Código de función</span><span class="sxs-lookup"><span data-stu-id="1440a-114">Function Code</span></span>
3.  <span data-ttu-id="1440a-115">Buffer (método)</span><span class="sxs-lookup"><span data-stu-id="1440a-115">Buffer Method</span></span>
4.  <span data-ttu-id="1440a-116">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="1440a-116">Access Type</span></span>

<span data-ttu-id="1440a-117">La cuarta sección, el tipo de acceso, especifica el requisito de acceso específico para el comando especificado.</span><span class="sxs-lookup"><span data-stu-id="1440a-117">The fourth section, the Access Type, specifies the specific access requirement for the given command.</span></span> <span data-ttu-id="1440a-118">El administrador de e/s del controlador usa estos datos para realizar la comprobación de la lista de Access Control (ACL).</span><span class="sxs-lookup"><span data-stu-id="1440a-118">The driver's I/O manager uses this data to perform the Access Control List (ACL) check.</span></span>

<span data-ttu-id="1440a-119">Por tanto, si se definió un IOCTL como:</span><span class="sxs-lookup"><span data-stu-id="1440a-119">So if an IOCTL were defined as:</span></span>


```C++
    #define MY_READ_IOCTL CTL_CODE(FILE_DEVICE_X, CONTROL_FUNCTION_Y, METHOD_BUFFERED, FILE_READ_ACCESS)
```



<span data-ttu-id="1440a-120">El administrador de e/s del controlador comprobará que el propietario del controlador del dispositivo tiene acceso de lectura al dispositivo cuando se envía este mensaje.</span><span class="sxs-lookup"><span data-stu-id="1440a-120">The driver's I/O manager would check that the owner of the device handle has read access to the device when this message is sent.</span></span>

<span data-ttu-id="1440a-121">Y, si se definió un IOCTL como:</span><span class="sxs-lookup"><span data-stu-id="1440a-121">And, if an IOCTL were defined as:</span></span>


```C++
    #define MY_READWRITE_IOCTL CTL_CODE(FILE_DEVICE_X, CONTROL_FUNCTION_Z, METHOD_BUFFERED, (FILE_READ_ACCESS | FILE_WRITE_ACCESS))
```



<span data-ttu-id="1440a-122">El administrador de e/s del controlador comprobaría que el propietario del identificador del dispositivo tiene acceso de lectura y escritura al dispositivo cuando se envía este mensaje.</span><span class="sxs-lookup"><span data-stu-id="1440a-122">The driver's I/O manager would check that the owner of the device handle has read/write access to the device when this message is sent.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1440a-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1440a-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1440a-124">**Información general de la aplicación**</span><span class="sxs-lookup"><span data-stu-id="1440a-124">**Application Overview**</span></span>](application-overview.md)
</dt> <dt>

[<span data-ttu-id="1440a-125">**IPortableDevice:: Open**</span><span class="sxs-lookup"><span data-stu-id="1440a-125">**IPortableDevice::Open**</span></span>](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open)
</dt> <dt>

[<span data-ttu-id="1440a-126">**IPortableDevice::SendCommand**</span><span class="sxs-lookup"><span data-stu-id="1440a-126">**IPortableDevice::SendCommand**</span></span>](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)
</dt> </dl>

 

 



