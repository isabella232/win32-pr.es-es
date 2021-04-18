---
description: Utilice las siguientes directrices para crear una Windows Installer instalación que muestre un cuadro de mensaje que le pida al usuario que inserte un disco.
ms.assetid: 8b53a490-921f-4d89-83b7-dbc62231ef92
title: Creación de mensajes de solicitud de disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f536a27c2adb5896992eb19a86bff64b9498d83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652613"
---
# <a name="authoring-disk-prompt-messages"></a><span data-ttu-id="2dafc-103">Creación de mensajes de solicitud de disco</span><span class="sxs-lookup"><span data-stu-id="2dafc-103">Authoring Disk Prompt Messages</span></span>

<span data-ttu-id="2dafc-104">Utilice las siguientes directrices para crear una Windows Installer instalación que muestre un cuadro de mensaje que le pida al usuario que inserte un disco.</span><span class="sxs-lookup"><span data-stu-id="2dafc-104">Use the following guidelines to author a Windows Installer installation that displays a message box prompting the user to insert a disk.</span></span>

<span data-ttu-id="2dafc-105">**Para mostrar un cuadro de mensaje que pide al usuario que inserte un disco**</span><span class="sxs-lookup"><span data-stu-id="2dafc-105">**To display a message box prompting the user to insert a disk**</span></span>

1.  <span data-ttu-id="2dafc-106">Use las capacidades de creación del instalador para establecer la cadena de la propiedad [**DiskPrompt**](diskprompt.md) en la tabla de [propiedades](property-table.md) .</span><span class="sxs-lookup"><span data-stu-id="2dafc-106">Use the authoring capabilities of the installer to set the [**DiskPrompt**](diskprompt.md) property string in the [Property](property-table.md) table.</span></span> <span data-ttu-id="2dafc-107">Esto debe incluir el nombre del producto que se va a instalar y un parámetro de marcador de posición dentro de la cadena para el título impreso en el disco.</span><span class="sxs-lookup"><span data-stu-id="2dafc-107">This should include the name of the product being installed and a placeholder parameter within the string for the title printed on the disk.</span></span> <span data-ttu-id="2dafc-108">Por ejemplo, para Microsoft Publisher, la propiedad **DiskPrompt** podría ser "Microsoft Publisher: Disk \[ 1 \] ", donde \[ 1 \] es el marcador de posición del título del disco.</span><span class="sxs-lookup"><span data-stu-id="2dafc-108">For example, for Microsoft Publisher the **DiskPrompt** property could be "Microsoft Publisher: Disk \[1\]", where \[1\] is the placeholder for the disk title.</span></span>
2.  <span data-ttu-id="2dafc-109">Escriba los títulos de cada uno de los discos que se solicitan en filas independientes de la columna DiskPrompt de la tabla de [medios](media-table.md) .</span><span class="sxs-lookup"><span data-stu-id="2dafc-109">Enter the titles of each of the disks being prompted for into separate rows of the DiskPrompt column of the [Media](media-table.md) table.</span></span> <span data-ttu-id="2dafc-110">Por ejemplo, la primera y única entrada en la tabla de medios podría ser "1 – install".</span><span class="sxs-lookup"><span data-stu-id="2dafc-110">For example, the first and only entry into the Media table could be "1–Install."</span></span>
3.  <span data-ttu-id="2dafc-111">Durante la acción [InstallFiles](installfiles-action.md) , el valor de la columna DiskPrompt de la tabla de [medios](media-table.md) se sustituye por el marcador de posición en la cadena de la propiedad [**DiskPrompt**](diskprompt.md) .</span><span class="sxs-lookup"><span data-stu-id="2dafc-111">During the [InstallFiles](installfiles-action.md) action the value from the DiskPrompt column of the [Media](media-table.md) table is substituted for the placeholder in the string of the [**DiskPrompt**](diskprompt.md) property.</span></span>
4.  <span data-ttu-id="2dafc-112">El mensaje que muestra el cuadro de mensaje se crea a partir de una cadena de plantilla integrada en la [tabla de errores](error-table.md).</span><span class="sxs-lookup"><span data-stu-id="2dafc-112">The message displayed by the message box is created from a built-in template string in the [Error table](error-table.md).</span></span> <span data-ttu-id="2dafc-113">Se trata del error 1302 y la cadena de la plantilla es: "Inserte el disco: \[ 2 \] " y \[ 2 \] representa un marcador de posición para la propiedad [**DiskPrompt**](diskprompt.md) .</span><span class="sxs-lookup"><span data-stu-id="2dafc-113">This is Error 1302 and the template string is: "Please insert the disk: \[2\]", and the \[2\] represents a placeholder for the [**DiskPrompt**](diskprompt.md) property.</span></span>

<span data-ttu-id="2dafc-114">En el ejemplo se muestra el siguiente mensaje al usuario: "Inserte el disco: Microsoft Publisher: disco 1 – instalar".</span><span class="sxs-lookup"><span data-stu-id="2dafc-114">The example displays the following message to the user: "Please insert the disk: Microsoft Publisher: Disk 1 – Install."</span></span>

<span data-ttu-id="2dafc-115">Tenga en cuenta que los mensajes de petición de disco aparecen en todos los niveles de la [interfaz de usuario](user-interface-levels.md) , excepto ninguno.</span><span class="sxs-lookup"><span data-stu-id="2dafc-115">Note that disk prompt messages get displayed by all [User Interface Levels](user-interface-levels.md) except None.</span></span>

 

 



