---
description: Representación de dispositivos
ms.assetid: bf8b9c67-b023-40ed-97c6-9ca030de610a
title: Representación de dispositivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c95352c191d3e2d34392f4236b926b81cf65fd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497308"
---
# <a name="device-representation"></a><span data-ttu-id="d1510-103">Representación de dispositivos</span><span class="sxs-lookup"><span data-stu-id="d1510-103">Device Representation</span></span>

<span data-ttu-id="d1510-104">Los dispositivos tienen dos comportamientos principales que se resuelven mediante la arquitectura de dispositivos portátiles de Windows (WPD):</span><span class="sxs-lookup"><span data-stu-id="d1510-104">Devices have two main behaviors that are addressed by the Windows Portable Devices (WPD) architecture:</span></span>

-   <span data-ttu-id="d1510-105">Acceder al contenido y almacenarlo.</span><span class="sxs-lookup"><span data-stu-id="d1510-105">Accessing and storing content.</span></span> <span data-ttu-id="d1510-106">Por ejemplo, las aplicaciones deben poder agregar archivos de música a un reproductor de música portátil.</span><span class="sxs-lookup"><span data-stu-id="d1510-106">For example, applications must be able to add music files to a portable music player.</span></span>
-   <span data-ttu-id="d1510-107">Programar el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d1510-107">Programming the device.</span></span> <span data-ttu-id="d1510-108">Esto incluye operaciones sencillas, como cambiar la configuración y preparar el dispositivo para la captura de datos o operaciones más complejas, como la carga de firmware.</span><span class="sxs-lookup"><span data-stu-id="d1510-108">This includes simple operations such as changing settings and preparing the device for data capture, or more complex operations such as uploading firmware.</span></span> <span data-ttu-id="d1510-109">Entre los ejemplos se incluye la emisión de un comando "tomar imagen" a una cámara digital.</span><span class="sxs-lookup"><span data-stu-id="d1510-109">Examples include issuing a "Take Picture" command to a digital still camera.</span></span>

<span data-ttu-id="d1510-110">En WPD, estos comportamientos se describen mediante la representación del dispositivo como una jerarquía de objetos.</span><span class="sxs-lookup"><span data-stu-id="d1510-110">In WPD, these behaviors are described by representing the device as a hierarchy of objects.</span></span> <span data-ttu-id="d1510-111">En la ilustración siguiente se muestra una representación de objeto de WPD para un dispositivo de varias funciones, que en este caso es un teléfono móvil.</span><span class="sxs-lookup"><span data-stu-id="d1510-111">The following illustration shows a WPD object representation for a multi-function device, which in this case is a mobile phone.</span></span>

![Ilustración en la que se muestra la jerarquía de objetos de un teléfono móvil](images/wpd-overview-figure3.gif)

<span data-ttu-id="d1510-113">Esta jerarquía muestra la funcionalidad y el contenido siguientes.</span><span class="sxs-lookup"><span data-stu-id="d1510-113">This hierarchy illustrates the following functionality and contents.</span></span>

<span data-ttu-id="d1510-114">Functional</span><span class="sxs-lookup"><span data-stu-id="d1510-114">Functionality:</span></span>

-   <span data-ttu-id="d1510-115">Objeto de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="d1510-115">Storage object.</span></span> <span data-ttu-id="d1510-116">Este dispositivo tiene almacenamiento de datos.</span><span class="sxs-lookup"><span data-stu-id="d1510-116">This device has data storage.</span></span>
-   <span data-ttu-id="d1510-117">Servicio de contactos.</span><span class="sxs-lookup"><span data-stu-id="d1510-117">Contacts Service.</span></span> <span data-ttu-id="d1510-118">Este servicio es un objeto funcional que se puede usar para sincronizar y almacenar contactos en el teléfono.</span><span class="sxs-lookup"><span data-stu-id="d1510-118">This service is a functional object that can be used to synchronize and store contacts on the phone.</span></span>
-   <span data-ttu-id="d1510-119">Servicio de SMS.</span><span class="sxs-lookup"><span data-stu-id="d1510-119">SMS Service.</span></span> <span data-ttu-id="d1510-120">Este servicio es un objeto funcional que se puede usar para enviar, recibir y almacenar mensajes SMS.</span><span class="sxs-lookup"><span data-stu-id="d1510-120">This service is a functional object that can be used to send, receive, and store SMS messages.</span></span>

<span data-ttu-id="d1510-121">Contenido:</span><span class="sxs-lookup"><span data-stu-id="d1510-121">Contents:</span></span>

-   <span data-ttu-id="d1510-122">Objetos multimedia.</span><span class="sxs-lookup"><span data-stu-id="d1510-122">Media objects.</span></span> <span data-ttu-id="d1510-123">Este dispositivo almacena imágenes, música y archivos de vídeo en carpetas en el objeto de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="d1510-123">This device stores images, music, and video files in folders on the Storage object.</span></span> <span data-ttu-id="d1510-124">Aunque los archivos que se muestran en la ilustración se almacenan en una carpeta, un dispositivo puede subdividir el contenido en carpetas organizadas por el tipo de medios almacenados; por ejemplo, carpetas de imagen, carpetas de música y carpetas de vídeo.</span><span class="sxs-lookup"><span data-stu-id="d1510-124">While the files shown in the illustration are stored under one folder, a device can subdivide content into folders organized by the type of media stored; for example, image folders, music folders, and video folders.</span></span>
-   <span data-ttu-id="d1510-125">Objetos de contacto.</span><span class="sxs-lookup"><span data-stu-id="d1510-125">Contact objects.</span></span> <span data-ttu-id="d1510-126">Este dispositivo almacena información de contacto (como el nombre, el número de teléfono y la dirección) como elemento secundario del servicio de contactos.</span><span class="sxs-lookup"><span data-stu-id="d1510-126">This device stores contact information (such as name, phone number, and address) as children of the Contacts Service</span></span>
-   <span data-ttu-id="d1510-127">Objetos de mensaje.</span><span class="sxs-lookup"><span data-stu-id="d1510-127">Message objects.</span></span> <span data-ttu-id="d1510-128">Este dispositivo almacena mensajes SMS como elementos secundarios del servicio SMS.</span><span class="sxs-lookup"><span data-stu-id="d1510-128">This device stores SMS messages as children of the SMS Service.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1510-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d1510-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1510-130">**Información general de la aplicación**</span><span class="sxs-lookup"><span data-stu-id="d1510-130">**Application Overview**</span></span>](application-overview.md)
</dt> </dl>

 

 



