---
description: Eliminación de WPDUSB.SYS driver for Windows Portable Devices
ms.assetid: 3ad0c892-8b19-465d-af2f-9207f98e27b7
title: Eliminación de WPDUSB.SYS driver for Windows Portable Devices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5931b63c5abb4534b2c8dd6619b4a3ead8b339be
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116253"
---
# <a name="removal-of-wpdusbsys-driver-for-windows-portable-devices"></a><span data-ttu-id="4f037-103">Eliminación de WPDUSB.SYS driver for Windows Portable Devices</span><span class="sxs-lookup"><span data-stu-id="4f037-103">Removal of WPDUSB.SYS Driver for Windows Portable Devices</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="4f037-104">Plataformas afectadas</span><span class="sxs-lookup"><span data-stu-id="4f037-104">Affected Platforms</span></span>

<span data-ttu-id="4f037-105">**Clientes:** Windows 7</span><span class="sxs-lookup"><span data-stu-id="4f037-105">**Clients** - Windows 7</span></span>  
<span data-ttu-id="4f037-106">**Servidores:** Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4f037-106">**Servers** - Windows Server 2008 R2</span></span>  









## <a name="feature-impact"></a><span data-ttu-id="4f037-107">Impacto en las características</span><span class="sxs-lookup"><span data-stu-id="4f037-107">Feature Impact</span></span>

 <span data-ttu-id="4f037-108">**Gravedad:** baja</span><span class="sxs-lookup"><span data-stu-id="4f037-108">**Severity** - Low</span></span>  
<span data-ttu-id="4f037-109">**Frecuencia:** baja</span><span class="sxs-lookup"><span data-stu-id="4f037-109">**Frequency** - Low</span></span>  





## <a name="description"></a><span data-ttu-id="4f037-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="4f037-110">Description</span></span>

<span data-ttu-id="4f037-111">Microsoft ha reemplazado el componente de modo kernel de la pila de controladores USB de Windows Vista (WPDUSB.SYS) para dispositivos portátiles de Windows (WPD) por el controlador WINUSB.SYS genérico.</span><span class="sxs-lookup"><span data-stu-id="4f037-111">Microsoft has replaced the kernel mode component of the Windows Vista USB driver stack (WPDUSB.SYS) for Windows Portable Devices (WPD) with the generic WINUSB.SYS driver.</span></span> <span data-ttu-id="4f037-112">La comunicación con el controlador WPDUSB.SYS era a través de códigos privados de control de E/S (IOCTL); También se ha quitado la compatibilidad de estos.</span><span class="sxs-lookup"><span data-stu-id="4f037-112">Communication with the original WPDUSB.SYS driver was via private I/O Control (IOCTL) codes; support of these has also been removed.</span></span>

<span data-ttu-id="4f037-113">Cualquier consumidor de estos códigos IOCTL habría sido responsable de la correcta interpretación e implementación del Protocolo de transferencia de medios (MTP).</span><span class="sxs-lookup"><span data-stu-id="4f037-113">Any consumer of these IOCTL codes would have been responsible for proper interpretation and implementation of the Media Transfer Protocol (MTP).</span></span> <span data-ttu-id="4f037-114">Windows Vista no admite el uso de estos códigos IOCTL por parte de aplicaciones de terceros.</span><span class="sxs-lookup"><span data-stu-id="4f037-114">Windows Vista did not support use of these IOCTL codes by third-party applications.</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="4f037-115">Demostración del impacto</span><span class="sxs-lookup"><span data-stu-id="4f037-115">Manifestation of Impact</span></span>

<span data-ttu-id="4f037-116">Cualquier aplicación que dependiera de la disponibilidad de estos códigos IOCTL privados ya no tendría acceso a los dispositivos MTP conectados a USB.</span><span class="sxs-lookup"><span data-stu-id="4f037-116">Any application that depended on the availability of these private IOCTL codes would no longer have access to USB-connected MTP devices.</span></span>

## <a name="mitigation"></a><span data-ttu-id="4f037-117">Mitigación</span><span class="sxs-lookup"><span data-stu-id="4f037-117">Mitigation</span></span>

<span data-ttu-id="4f037-118">Los usuarios de una aplicación que dependa de los códigos IOCTL privados deben usar una aplicación diferente (o una versión actualizada de la aplicación) para acceder al dispositivo MTP conectado a USB.</span><span class="sxs-lookup"><span data-stu-id="4f037-118">Users of an application that depends on the private IOCTL codes must use a different application (or an updated version of the application) to access the USB-connected MTP device.</span></span>

## <a name="solution"></a><span data-ttu-id="4f037-119">Solución</span><span class="sxs-lookup"><span data-stu-id="4f037-119">Solution</span></span>

<span data-ttu-id="4f037-120">Las aplicaciones deben usar la API de dispositivos portátiles de Windows (WPD) para buscar e interactuar con cualquier dispositivo WPD.</span><span class="sxs-lookup"><span data-stu-id="4f037-120">Applications should use the Windows Portable Devices (WPD) API to find and interact with any WPD Device.</span></span> <span data-ttu-id="4f037-121">Aunque un porcentaje significativo de dispositivos WPD implementan MTP para la comunicación con el equipo, WPD no se limita solo a los dispositivos MTP.</span><span class="sxs-lookup"><span data-stu-id="4f037-121">Although a significant percentage of WPD devices implement MTP for communication with the PC, WPD is not limited to just MTP devices.</span></span> <span data-ttu-id="4f037-122">Además, cuando el acceso directo al dispositivo a través de las ICTL privadas habría limitado la aplicación a la comunicación solo con dispositivos conectados mediante USB, el uso de la API de WPD amplía la lista de opciones de conectividad a otros protocolos de comunicación (por ejemplo, Wi-Fi).</span><span class="sxs-lookup"><span data-stu-id="4f037-122">In addition, where direct access to the device via the private IOCTLs would have limited the application to communication with only USB-connected devices, use of the WPD API expands the list of connectivity options to other communication protocols (for example, Wi-Fi).</span></span> <span data-ttu-id="4f037-123">En los casos poco frecuentes en los que la aplicación debe tener en cuenta MTP, la API de WPD proporciona un mecanismo de paso a través para los comandos MTP sin procesar.</span><span class="sxs-lookup"><span data-stu-id="4f037-123">In the rare cases when the application must be MTP-aware, the WPD API provides a pass-through mechanism for raw MTP commands.</span></span>

## <a name="leveraging-feature-capabilities"></a><span data-ttu-id="4f037-124">Aprovechamiento de las funcionalidades de características</span><span class="sxs-lookup"><span data-stu-id="4f037-124">Leveraging Feature Capabilities</span></span>

<span data-ttu-id="4f037-125">La API de WPD se admite en Windows XP (a través del SDK de Windows Format), Windows Vista y Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4f037-125">The WPD API is supported in Windows XP (via the Windows Format SDK), Windows Vista and Windows 7.</span></span> <span data-ttu-id="4f037-126">La implementación de Windows 7 de WPD agrega compatibilidad con MTP a través de Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="4f037-126">The Windows 7 implementation of WPD adds support for MTP over Bluetooth.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="4f037-127">Vínculos a otros recursos</span><span class="sxs-lookup"><span data-stu-id="4f037-127">Links to Other Resources</span></span>

[<span data-ttu-id="4f037-128">Dispositivos portátiles Windows</span><span class="sxs-lookup"><span data-stu-id="4f037-128">Windows Portable Devices</span></span>](../windows-portable-devices.md)

 

 
