---
description: Interfaz de programación de aplicaciones de WPD
ms.assetid: 3e2be15f-7af7-4e76-89b1-f9bc591c4f1b
title: Interfaz de programación de aplicaciones de WPD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c44dbcf731aa46941599b99766e52fa67a5c5a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716657"
---
# <a name="wpd-application-programming-interface"></a><span data-ttu-id="e2560-103">Interfaz de programación de aplicaciones de WPD</span><span class="sxs-lookup"><span data-stu-id="e2560-103">WPD Application Programming Interface</span></span>

<span data-ttu-id="e2560-104">Las aplicaciones compiladas en dispositivos portátiles de Windows pueden explorar un dispositivo, enviar y recibir contenido, e incluso controlar el dispositivo, por ejemplo, tomar una imagen o enviar un mensaje de texto.</span><span class="sxs-lookup"><span data-stu-id="e2560-104">Applications built on Windows Portable Devices can explore a device, send and receive content, and even control the device, for example, take a picture or send a text message.</span></span> <span data-ttu-id="e2560-105">El sistema está diseñado para ser flexible, de modo que se puedan explorar muchos tipos de dispositivos, y extensibles para que los desarrolladores de controladores puedan definir propiedades y comandos personalizados para dispositivos personalizados.</span><span class="sxs-lookup"><span data-stu-id="e2560-105">The system is designed to be flexible so that many types of devices can be explored, and extensible so that driver developers can define custom properties and commands for custom devices.</span></span>

<span data-ttu-id="e2560-106">En la tabla siguiente se describen los temas principales de esta documentación.</span><span class="sxs-lookup"><span data-stu-id="e2560-106">The following table describes the main topics of this documentation.</span></span>



| <span data-ttu-id="e2560-107">Tema</span><span class="sxs-lookup"><span data-stu-id="e2560-107">Topic</span></span>                                                                                                                  | <span data-ttu-id="e2560-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="e2560-108">Description</span></span>                                                                                                |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e2560-109">Requisitos generales para el desarrollo de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="e2560-109">General Requirements for Application Development</span></span>](general-requirements-for-application-development.md)               | <span data-ttu-id="e2560-110">Requisitos de hardware y software para desarrollar controladores y aplicaciones con dispositivos portátiles de Windows.</span><span class="sxs-lookup"><span data-stu-id="e2560-110">Hardware and software requirements to develop drivers and applications using Windows Portable Devices.</span></span>     |
| [<span data-ttu-id="e2560-111">Requisitos para las aplicaciones de Windows Media DRM-Enabled</span><span class="sxs-lookup"><span data-stu-id="e2560-111">Requirements for Windows Media DRM-Enabled Applications</span></span>](requirements-for-windows-media-drm-enabled-applications.md) | <span data-ttu-id="e2560-112">Propiedades necesarias para habilitar las transferencias de contenido protegidas con DRM de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e2560-112">Properties that are required to enable Windows Media DRM-protected content transfers.</span></span>                      |
| [<span data-ttu-id="e2560-113">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="e2560-113">Samples</span></span>](sample.md)                                                                                                  | <span data-ttu-id="e2560-114">Descripción de dos aplicaciones de escritorio de línea de comandos que se proporcionan con este kit de desarrollo de software.</span><span class="sxs-lookup"><span data-stu-id="e2560-114">Description of two command-line desktop applications that are supplied with this software development kit.</span></span> |
| [<span data-ttu-id="e2560-115">Información general de la aplicación</span><span class="sxs-lookup"><span data-stu-id="e2560-115">Application Overview</span></span>](application-overview.md)                                                                       | <span data-ttu-id="e2560-116">Conceptos clave usados en dispositivos portátiles de Windows.</span><span class="sxs-lookup"><span data-stu-id="e2560-116">Key concepts used in Windows Portable Devices.</span></span>                                                             |
| [<span data-ttu-id="e2560-117">Guía de programación</span><span class="sxs-lookup"><span data-stu-id="e2560-117">Programming Guide</span></span>](programming-guide.md)                                                                             | <span data-ttu-id="e2560-118">Tareas clave que realizará una aplicación, con instrucciones paso a paso y fragmentos de código.</span><span class="sxs-lookup"><span data-stu-id="e2560-118">Key tasks that an application will perform, with step-by-step instructions and code snippets.</span></span>              |
| [<span data-ttu-id="e2560-119">Referencia de programación</span><span class="sxs-lookup"><span data-stu-id="e2560-119">Programming Reference</span></span>](programming-reference.md)                                                                     | <span data-ttu-id="e2560-120">Guía de referencia de las interfaces y los tipos de datos definidos por dispositivos portátiles de Windows.</span><span class="sxs-lookup"><span data-stu-id="e2560-120">Reference guide to the interfaces and data types defined by Windows Portable Devices.</span></span>                      |



 

<span data-ttu-id="e2560-121">Las aplicaciones basadas en Windows Media Administrador de dispositivos o la adquisición de imágenes de Windows pueden tener acceso a dispositivos portátiles de Windows a través de un nivel de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="e2560-121">Applications built on Windows Media Device Manager or Windows Image Acquisition can access Windows Portable Devices through a compatibility layer.</span></span>

<span data-ttu-id="e2560-122">Microsoft proporciona varios controladores para los protocolos y dispositivos estándar, incluidos los dispositivos de protocolo de transporte de multimedia (MTP) y los dispositivos de clase de almacenamiento masivo (MSC).</span><span class="sxs-lookup"><span data-stu-id="e2560-122">Microsoft provides several drivers for standard protocols and devices, including Media Transport Protocol (MTP) devices and Mass Storage Class (MSC) devices.</span></span> <span data-ttu-id="e2560-123">Si está familiarizado con el marco de User-Mode driver, puede desarrollar sus propios controladores para dispositivos personalizados.</span><span class="sxs-lookup"><span data-stu-id="e2560-123">If you are familiar with the User-Mode Driver Framework, you can develop your own drivers for custom devices.</span></span>

 

 



