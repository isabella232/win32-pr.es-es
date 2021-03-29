---
description: Aplicación WpdApiSample
ms.assetid: 854a6304-5d62-4f00-9366-8c2244568250
title: Aplicación WpdApiSample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87c384d542c9b93ac733c91ee249938d744e40ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809536"
---
# <a name="wpdapisample-application"></a><span data-ttu-id="ab772-103">Aplicación WpdApiSample</span><span class="sxs-lookup"><span data-stu-id="ab772-103">WpdApiSample Application</span></span>

<span data-ttu-id="ab772-104">La aplicación de ejemplo WpdApiSample es una aplicación de escritorio de línea de comandos que permite enumerar dispositivos conectados, explorar dispositivos, consultar objetos para propiedades y atributos, enviar y recuperar objetos, etc.</span><span class="sxs-lookup"><span data-stu-id="ab772-104">The WpdApiSample sample application is a command-line desktop application that enables you to enumerate connected devices, explore devices, query objects for properties and attributes, send and retrieve objects, and so on.</span></span> <span data-ttu-id="ab772-105">Al iniciarse, la aplicación abre una ventana de comandos que enumera las tareas que puede realizar.</span><span class="sxs-lookup"><span data-stu-id="ab772-105">On startup, the application opens a command window that lists the tasks you can perform.</span></span>

<span data-ttu-id="ab772-106">La aplicación de ejemplo WpdApiSample incluye los siguientes archivos:</span><span class="sxs-lookup"><span data-stu-id="ab772-106">The WpdApiSample sample application includes the following files:</span></span>



| <span data-ttu-id="ab772-107">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="ab772-107">**File**</span></span>               | <span data-ttu-id="ab772-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ab772-108">**Description**</span></span>                                                                                                                                                                                           |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab772-109">ContentEnumeration. cpp</span><span class="sxs-lookup"><span data-stu-id="ab772-109">ContentEnumeration.cpp</span></span> | <span data-ttu-id="ab772-110">Contiene funciones que enumeran todos los objetos de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ab772-110">Contains functions that enumerate all the objects on a device.</span></span>                                                                                                                                            |
| <span data-ttu-id="ab772-111">ContentProperties. cpp</span><span class="sxs-lookup"><span data-stu-id="ab772-111">ContentProperties.cpp</span></span>  | <span data-ttu-id="ab772-112">Contiene funciones que leen y escriben propiedades de objeto y hacen solicitudes set/get de propiedad masivas.</span><span class="sxs-lookup"><span data-stu-id="ab772-112">Contains functions that read and write object properties and make bulk property set/get requests.</span></span>                                                                                                         |
| <span data-ttu-id="ab772-113">ContentTransfer. cpp</span><span class="sxs-lookup"><span data-stu-id="ab772-113">ContentTransfer.cpp</span></span>    | <span data-ttu-id="ab772-114">Contiene funciones que transfieren contenido hacia o desde el dispositivo, leen los requisitos de tipo de objeto y crean una carpeta en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ab772-114">Contains functions that transfer content to or from the device, read object type requirements, and create a folder on the device.</span></span>                                                                         |
| <span data-ttu-id="ab772-115">DeviceCapabilities. cpp</span><span class="sxs-lookup"><span data-stu-id="ab772-115">DeviceCapabilities.cpp</span></span> | <span data-ttu-id="ab772-116">Contiene funciones para enumerar los tipos de objeto funcional en el dispositivo, enumerar los tipos de contenido admitidos por cada tipo de objeto funcional y mostrar los perfiles de objeto de representación.</span><span class="sxs-lookup"><span data-stu-id="ab772-116">Contains functions to list the functional object types on the device, list the content types supported by each functional object type, and display rendering object profiles.</span></span>                             |
| <span data-ttu-id="ab772-117">DeviceEnumeration. cpp</span><span class="sxs-lookup"><span data-stu-id="ab772-117">DeviceEnumeration.cpp</span></span>  | <span data-ttu-id="ab772-118">Enumera los nombres descriptivos, los fabricantes y las descripciones de todos los dispositivos conectados.</span><span class="sxs-lookup"><span data-stu-id="ab772-118">Lists the friendly names, manufacturers, and descriptions of all connected devices.</span></span>                                                                                                                       |
| <span data-ttu-id="ab772-119">DeviceEvents. cpp</span><span class="sxs-lookup"><span data-stu-id="ab772-119">DeviceEvents.cpp</span></span>       | <span data-ttu-id="ab772-120">Contiene funciones que registran eventos de dispositivo y sus parámetros cada vez que se activan eventos.</span><span class="sxs-lookup"><span data-stu-id="ab772-120">Contains functions that log device events and their parameters whenever events are fired.</span></span>                                                                                                                 |
| <span data-ttu-id="ab772-121">stdafx.cpp</span><span class="sxs-lookup"><span data-stu-id="ab772-121">Stdafx.cpp</span></span>             | <span data-ttu-id="ab772-122">Incluye los archivos estándar.</span><span class="sxs-lookup"><span data-stu-id="ab772-122">Includes the standard files.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="ab772-123">WpdApiSample. cpp</span><span class="sxs-lookup"><span data-stu-id="ab772-123">WpdApiSample.cpp</span></span>       | <span data-ttu-id="ab772-124">Hospeda la función de inicio **\_ tmain** , que llama a la función local del **menú** , que muestra una lista de los dispositivos y las tareas disponibles y llama a la función adecuada para la selección del menú del usuario.</span><span class="sxs-lookup"><span data-stu-id="ab772-124">Hosts the **\_tmain** startup function, which calls the local **DoMenu** function, which displays a list of available devices and tasks and calls the function appropriate for the user's menu selection.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ab772-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ab772-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab772-126">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="ab772-126">Sample</span></span>](sample.md)
</dt> </dl>

 

 



