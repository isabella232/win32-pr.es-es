---
description: Un paquete de instalación contiene toda la información que el Windows Installer requiere para instalar o desinstalar una aplicación o un producto y para ejecutar la interfaz de usuario del programa de instalación.
ms.assetid: 532b3492-919f-4999-b86c-e3c210876141
title: Paquete de instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe5e5ff79d0c868036dd12ed533b1cd18f9f70d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652745"
---
# <a name="installation-package"></a><span data-ttu-id="5b954-103">Paquete de instalación</span><span class="sxs-lookup"><span data-stu-id="5b954-103">Installation Package</span></span>

<span data-ttu-id="5b954-104">Un paquete de instalación contiene toda la información que el Windows Installer requiere para instalar o desinstalar una aplicación o un producto y para ejecutar la interfaz de usuario del programa de instalación.</span><span class="sxs-lookup"><span data-stu-id="5b954-104">An installation package contains all of the information that the Windows Installer requires to install or uninstall an application or product and to run the setup user interface.</span></span> <span data-ttu-id="5b954-105">Cada paquete de instalación incluye un archivo. msi que contiene una base de datos de instalación, un flujo de información de Resumen y secuencias de datos para varias partes de la instalación.</span><span class="sxs-lookup"><span data-stu-id="5b954-105">Each installation package includes an .msi file, containing an installation database, a summary information stream, and data streams for various parts of the installation.</span></span> <span data-ttu-id="5b954-106">El archivo. msi también puede contener una o más transformaciones, archivos de código fuente internos y archivos de código fuente externos o archivos. cab necesarios para la instalación.</span><span class="sxs-lookup"><span data-stu-id="5b954-106">The .msi file can also contain one or more transforms, internal source files, and external source files or cabinet files required by the installation.</span></span>

<span data-ttu-id="5b954-107">Los desarrolladores de aplicaciones deben crear una instalación para usar el instalador.</span><span class="sxs-lookup"><span data-stu-id="5b954-107">Application developers must author an installation to use the installer.</span></span> <span data-ttu-id="5b954-108">Dado que el instalador organiza las instalaciones en torno al concepto de [componentes y características](components-and-features.md), y almacena toda la información sobre la instalación en una base de datos relacional, el proceso de creación de un paquete de instalación conlleva en general los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="5b954-108">Because the installer organizes installations around the concept of [components and features](components-and-features.md), and stores all information about the installation in a relational database, the process of authoring an installation package broadly entails the following steps:</span></span>

-   <span data-ttu-id="5b954-109">Identifique las características que se van a presentar a los usuarios.</span><span class="sxs-lookup"><span data-stu-id="5b954-109">Identify the features to be presented to users.</span></span>
-   <span data-ttu-id="5b954-110">Organice la aplicación en componentes.</span><span class="sxs-lookup"><span data-stu-id="5b954-110">Organize the application into components.</span></span>
-   <span data-ttu-id="5b954-111">Rellene la base de datos de instalación con información.</span><span class="sxs-lookup"><span data-stu-id="5b954-111">Populate the installation database with information.</span></span>
-   <span data-ttu-id="5b954-112">Valide el paquete de instalación.</span><span class="sxs-lookup"><span data-stu-id="5b954-112">Validate the installation package.</span></span>

<span data-ttu-id="5b954-113">En la siguiente sección se describen los componentes y las características del instalador.</span><span class="sxs-lookup"><span data-stu-id="5b954-113">The next section discusses installer components and features.</span></span> <span data-ttu-id="5b954-114">Para obtener más información, vea [componentes y características](components-and-features.md).</span><span class="sxs-lookup"><span data-stu-id="5b954-114">For more information, see [Components and Features](components-and-features.md).</span></span> <span data-ttu-id="5b954-115">La elección de las características viene determinada normalmente por la funcionalidad de la aplicación desde la perspectiva del usuario.</span><span class="sxs-lookup"><span data-stu-id="5b954-115">The choice of features is commonly determined by the application's functionality from the user's perspective.</span></span>

<span data-ttu-id="5b954-116">Se recomienda que los desarrolladores utilicen un procedimiento estándar para elegir componentes.</span><span class="sxs-lookup"><span data-stu-id="5b954-116">It is recommended that developers use a standard procedure for choosing components.</span></span> <span data-ttu-id="5b954-117">Para obtener más información, vea [organizar aplicaciones en componentes](organizing-applications-into-components.md).</span><span class="sxs-lookup"><span data-stu-id="5b954-117">For more information, see [Organizing Applications into Components](organizing-applications-into-components.md).</span></span>

<span data-ttu-id="5b954-118">Los autores de paquetes pueden usar herramientas de creación de paquetes de terceros, o un editor de tablas y el SDK de Windows Installer, para rellenar la base de datos de instalación.</span><span class="sxs-lookup"><span data-stu-id="5b954-118">Package authors can use third-party package creation tools, or a table editor and the Windows Installer SDK, to populate the installation database.</span></span> <span data-ttu-id="5b954-119">Todos los paquetes de instalación deben validarse para la coherencia interna.</span><span class="sxs-lookup"><span data-stu-id="5b954-119">All installation packages need to be validated for internal consistency.</span></span> <span data-ttu-id="5b954-120">Para obtener más información, vea [validación de paquetes](package-validation.md).</span><span class="sxs-lookup"><span data-stu-id="5b954-120">For more information, see [Package Validation](package-validation.md).</span></span>

 

 



