---
title: Uso de Bluetooth
description: En esta sección se describen las tareas relacionadas con la escritura de aplicaciones basadas en Windows para Bluetooth.
ms.assetid: a5eddf48-b548-44a8-ac09-ce16f8aa3943
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4b9b396de2635f9d1e76005c6638abb1d49c0ff
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/09/2020
ms.locfileid: "103797049"
---
# <a name="using-bluetooth"></a><span data-ttu-id="9811f-103">Uso de Bluetooth</span><span class="sxs-lookup"><span data-stu-id="9811f-103">Using Bluetooth</span></span>

<span data-ttu-id="9811f-104">En esta sección se describen las tareas relacionadas con la escritura de aplicaciones basadas en Windows para Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="9811f-104">This section describes tasks that are related to writing Windows-based applications for Bluetooth.</span></span>

<span data-ttu-id="9811f-105">Bluetooth proporciona definiciones de programación en los archivos Ws2bth. h y BluetoothAPIs. h.</span><span class="sxs-lookup"><span data-stu-id="9811f-105">Bluetooth provides programming definitions in the Ws2bth.h and BluetoothAPIs.h files.</span></span> <span data-ttu-id="9811f-106">El archivo Bthsdpdef. h se debe incluir antes de BluetoothAPIs. h.</span><span class="sxs-lookup"><span data-stu-id="9811f-106">The Bthsdpdef.h file must be included before BluetoothAPIs.h.</span></span> <span data-ttu-id="9811f-107">El archivo Ws2bth. h debe estar incluido después de WinSock2. h para usar sockets Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="9811f-107">The Ws2bth.h file must be included after Winsock2.h to use Bluetooth sockets.</span></span> <span data-ttu-id="9811f-108">Vincule solo a Bthprops. lib y evite la vinculación a Irprops. lib.</span><span class="sxs-lookup"><span data-stu-id="9811f-108">Link only to Bthprops.lib, and avoid linking to Irprops.lib.</span></span> <span data-ttu-id="9811f-109">Irprops. lib solo se proporciona por motivos de compatibilidad con versiones anteriores.</span><span class="sxs-lookup"><span data-stu-id="9811f-109">Irprops.lib is provided for backward compatibility only.</span></span> <span data-ttu-id="9811f-110">Bthprops. lib está disponible en el SDK de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9811f-110">Bthprops.lib is available in the Windows Vista SDK.</span></span> <span data-ttu-id="9811f-111">Puede usar el SDK de Windows Vista para desarrollar aplicaciones para Windows XP con Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="9811f-111">You can use the Windows Vista SDK to develop applications for Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="9811f-112">El SDK de Windows Vista está disponible en el [centro de descarga](https://download.microsoft.com/download/a/7/7/a7767f09-0136-4a96-a1f8-276bf0ee31fa/Setup.exe).</span><span class="sxs-lookup"><span data-stu-id="9811f-112">The Windows Vista SDK is available from the [Download Center](https://download.microsoft.com/download/a/7/7/a7767f09-0136-4a96-a1f8-276bf0ee31fa/Setup.exe).</span></span>

<span data-ttu-id="9811f-113">Todos los mecanismos sincrónicos y superpuestos estándar para leer y escribir datos que se admiten actualmente con otras familias de direcciones funcionan correctamente con la \_ familia de direcciones AF BTH también.</span><span class="sxs-lookup"><span data-stu-id="9811f-113">All standard synchronous and overlapped mechanisms to read and write data that are currently supported with other address families operate properly with the AF\_BTH address family as well.</span></span>

<span data-ttu-id="9811f-114">Hay algún código de ejemplo incluido en el SDK que muestra una aplicación Bluetooth sencilla que usa el protocolo de Winsock 2,2 y RFCOMM.</span><span class="sxs-lookup"><span data-stu-id="9811f-114">There is some example code included with the SDK that shows a simple Bluetooth application using Winsock 2.2 and RFCOMM protocol.</span></span> <span data-ttu-id="9811f-115">El código fuente del ejemplo se puede encontrar en la ubicación de instalación del SDK en C: \\ archivos de programa \\ Microsoft SDK \\ Windows \\ <version number> \\ Samples \\ NetDs \\ Winsock \\ Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="9811f-115">The source code for the sample can be found in the SDK installation location under C:\\Program Files\\Microsoft SDKs\\Windows\\<version number>\\Samples\\NetDs\\winsock\\Bluetooth.</span></span>

<span data-ttu-id="9811f-116">En esta sección se describen los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="9811f-116">This section describes the following topics.</span></span>



| <span data-ttu-id="9811f-117">Sección</span><span class="sxs-lookup"><span data-stu-id="9811f-117">Section</span></span>                                                                                      | <span data-ttu-id="9811f-118">Contenido</span><span class="sxs-lookup"><span data-stu-id="9811f-118">Content</span></span>                                                                          |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [<span data-ttu-id="9811f-119">Programación de Bluetooth con Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="9811f-119">Bluetooth Programming with Windows Sockets</span></span>](bluetooth-programming-with-windows-sockets.md) | <span data-ttu-id="9811f-120">Explica cómo usar las interfaces de Windows Sockets para implementar una red Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="9811f-120">Explains how to use Windows Sockets interfaces to implement a Bluetooth network.</span></span> |



 

 

 




