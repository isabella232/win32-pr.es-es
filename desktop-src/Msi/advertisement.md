---
description: El Windows Installer puede anunciar la disponibilidad de una aplicación a los usuarios u otras aplicaciones sin instalar realmente la aplicación.
ms.assetid: 67170daa-448a-4a20-b38a-2dd36c95440f
title: Anuncio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0bb31f14fb4cd6f589e94939afdd5575df52c43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652621"
---
# <a name="advertisement"></a><span data-ttu-id="dc8cb-103">Anuncio</span><span class="sxs-lookup"><span data-stu-id="dc8cb-103">Advertisement</span></span>

<span data-ttu-id="dc8cb-104">El Windows Installer puede anunciar la disponibilidad de una aplicación a los usuarios u otras aplicaciones sin instalar realmente la aplicación.</span><span class="sxs-lookup"><span data-stu-id="dc8cb-104">The Windows Installer can advertise the availability of an application to users or other applications without actually installing the application.</span></span> <span data-ttu-id="dc8cb-105">Si se anuncia una aplicación, solo se presentan al usuario u otras aplicaciones las interfaces requeridas para cargar e iniciar la aplicación.</span><span class="sxs-lookup"><span data-stu-id="dc8cb-105">If an application is advertised, only the interfaces required for loading and launching the application are presented to the user or other applications.</span></span> <span data-ttu-id="dc8cb-106">Si un usuario o una aplicación activa una interfaz anunciada, el instalador continúa con la instalación de los componentes necesarios, como se describe en [instalación a petición](installation-on-demand.md).</span><span class="sxs-lookup"><span data-stu-id="dc8cb-106">If a user or application activates an advertised interface the installer then proceeds to install the necessary components as described in [Installation-On-Demand](installation-on-demand.md).</span></span>

<span data-ttu-id="dc8cb-107">Los dos tipos de publicidad son la asignación y publicación.</span><span class="sxs-lookup"><span data-stu-id="dc8cb-107">The two types of advertising are assigning and publishing.</span></span> <span data-ttu-id="dc8cb-108">Una aplicación aparece instalada para un usuario cuando esa aplicación se asigna al usuario.</span><span class="sxs-lookup"><span data-stu-id="dc8cb-108">An application appears installed to a user when that application is assigned to the user.</span></span> <span data-ttu-id="dc8cb-109">El menú **Inicio** contiene los métodos abreviados adecuados, se muestran iconos, los archivos se asocian a la aplicación y las entradas del registro reflejan la instalación de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="dc8cb-109">The **Start** menu contains the appropriate shortcuts, icons are displayed, files are associated with the application, and registry entries reflect the application's installation.</span></span> <span data-ttu-id="dc8cb-110">Cuando el usuario intenta abrir una aplicación asignada, se instala a petición.</span><span class="sxs-lookup"><span data-stu-id="dc8cb-110">When the user tries to open an assigned application it is installed upon demand.</span></span>

<span data-ttu-id="dc8cb-111">El instalador admite el anuncio de las aplicaciones y características según el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="dc8cb-111">The installer supports the advertisement of applications and features according to the operating system.</span></span> <span data-ttu-id="dc8cb-112">El instalador registra la información de la clase COM para las aplicaciones asignadas a partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="dc8cb-112">The installer registers COM class information for assigned applications beginning with Windows XP.</span></span> <span data-ttu-id="dc8cb-113">Esto permite al instalador instalar la aplicación al crear una instancia de una clase anunciada.</span><span class="sxs-lookup"><span data-stu-id="dc8cb-113">This enables the installer to install the application upon the creation of an instance of an advertised class.</span></span> <span data-ttu-id="dc8cb-114">Para obtener más información, vea [compatibilidad de la plataforma con el anuncio](platform-support-of-advertisement.md).</span><span class="sxs-lookup"><span data-stu-id="dc8cb-114">For more information, see [Platform Support of Advertisement](platform-support-of-advertisement.md).</span></span>

<span data-ttu-id="dc8cb-115">Puede publicar una aplicación desde el servidor a partir de Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="dc8cb-115">You can publish an application from the server beginning with Windows Server 2003.</span></span> <span data-ttu-id="dc8cb-116">La aplicación publicada se instala a través de la Asociación de archivos o el tipo de extensión multipropósito de correo Internet (MIME).</span><span class="sxs-lookup"><span data-stu-id="dc8cb-116">The published application is then installed through its file association or Multipurpose Internet Mail Extension (MIME) type.</span></span> <span data-ttu-id="dc8cb-117">La publicación no rellena la interfaz de usuario con ninguno de los iconos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="dc8cb-117">Publishing does not populate the user interface with any of the application's icons.</span></span> <span data-ttu-id="dc8cb-118">El sistema operativo cliente puede instalar una aplicación publicada a partir de Windows XP.</span><span class="sxs-lookup"><span data-stu-id="dc8cb-118">The client operating system can install a published application beginning with Windows XP.</span></span>

 

 



