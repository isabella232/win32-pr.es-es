---
title: Aplicación de escritorio de ejemplo
description: Aplicación de escritorio de ejemplo
ms.assetid: 3736dd01-b02f-4056-b19b-0e7cc6c9aa67
keywords:
- Administrador de dispositivos de Windows Media, ejemplos
- Administrador de dispositivos, ejemplos
- aplicaciones de escritorio, ejemplos
- Windows Media Administrador de dispositivos, ejemplo de aplicación de escritorio
- Administrador de dispositivos, ejemplo de aplicación de escritorio
- aplicación de ejemplo wmdmapp
- ejemplos, aplicaciones de escritorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f4008a25ca4448d4d4be7c9f667c5a9e4f08023
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418754"
---
# <a name="sample-desktop-application"></a><span data-ttu-id="b5f56-110">Aplicación de escritorio de ejemplo</span><span class="sxs-lookup"><span data-stu-id="b5f56-110">Sample Desktop Application</span></span>

<span data-ttu-id="b5f56-111">Windows Media Administrador de dispositivos se suministra con una aplicación de escritorio de ejemplo denominada wmdmapp.</span><span class="sxs-lookup"><span data-stu-id="b5f56-111">The Windows Media Device Manager ships with a sample desktop application called wmdmapp.</span></span> <span data-ttu-id="b5f56-112">Esta aplicación tiene una interfaz gráfica de usuario que le permite examinar los dispositivos conectados, crear listas de reproducción en el dispositivo y arrastrar archivos multimedia al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b5f56-112">This application has a graphical user interface that allows you to browse connected devices, create playlists on the device, and drag media files to the device.</span></span>

<span data-ttu-id="b5f56-113">Esta aplicación de ejemplo consta de dos partes:</span><span class="sxs-lookup"><span data-stu-id="b5f56-113">This sample application consists of two pieces:</span></span>

-   <span data-ttu-id="b5f56-114">wmdapp.exe, un archivo ejecutable que muestra una ventana y realiza la mayor parte de la interfaz de usuario y la funcionalidad básica del programa.</span><span class="sxs-lookup"><span data-stu-id="b5f56-114">wmdapp.exe, an executable that displays a window and performs most of the user interface and basic functionality of the program, and</span></span>
-   <span data-ttu-id="b5f56-115">proghelp.dll, un archivo DLL auxiliar que realiza funciones de utilidad para la aplicación.</span><span class="sxs-lookup"><span data-stu-id="b5f56-115">proghelp.dll, a helper DLL that performs utility functions for the application.</span></span> <span data-ttu-id="b5f56-116">Debe registrar este archivo DLL después de compilar el proyecto.</span><span class="sxs-lookup"><span data-stu-id="b5f56-116">You must register this DLL after building the project.</span></span>

<span data-ttu-id="b5f56-117">Para compilar la aplicación de ejemplo, puede usar Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="b5f56-117">To compile the sample application, you can use Visual Studio.</span></span> <span data-ttu-id="b5f56-118">En la siguiente sección se describe cómo hacerlo:</span><span class="sxs-lookup"><span data-stu-id="b5f56-118">The following section describes how this is done:</span></span>

-   [<span data-ttu-id="b5f56-119">Compilar la aplicación de ejemplo con Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b5f56-119">Compiling the Sample Application Using Visual Studio</span></span>](compiling-the-sample-application-using-visual-studio.md)

<span data-ttu-id="b5f56-120">Después de compilar el proyecto, registre el archivo de proghelp.dll.</span><span class="sxs-lookup"><span data-stu-id="b5f56-120">After compiling the project, register the proghelp.dll file.</span></span> <span data-ttu-id="b5f56-121">Para registrar este archivo DLL, abra un símbolo del sistema y vaya al directorio que contiene este archivo DLL y escriba `regsvr32 proghelp.dll` .</span><span class="sxs-lookup"><span data-stu-id="b5f56-121">To register this DLL, open a command prompt and browse to the directory containing this DLL and type `regsvr32 proghelp.dll`.</span></span>

 

 




