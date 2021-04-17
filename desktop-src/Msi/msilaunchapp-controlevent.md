---
description: Este evento de control ejecuta un archivo especificado. Si el archivo no existe, o si se produce un error en el evento, Windows Installer registra el error en el registro detallado sin mostrar un cuadro de diálogo que contiene un mensaje de error.
ms.assetid: a185c5a1-6584-4916-967a-313e6b7cf97c
title: MsiLaunchApp ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 298867868a80eb2cb831a2304325d14355adc669
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652527"
---
# <a name="msilaunchapp-controlevent"></a><span data-ttu-id="1ce99-104">MsiLaunchApp ControlEvent,</span><span class="sxs-lookup"><span data-stu-id="1ce99-104">MsiLaunchApp ControlEvent</span></span>

<span data-ttu-id="1ce99-105">Este evento de control ejecuta un archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="1ce99-105">This control event runs a specified file.</span></span> <span data-ttu-id="1ce99-106">Si el archivo no existe, o si se produce un error en el evento, Windows Installer registra el error en el registro detallado sin mostrar un cuadro de diálogo que contiene un mensaje de error.</span><span class="sxs-lookup"><span data-stu-id="1ce99-106">If the file does not exist, or if the event fails, Windows Installer logs the error in the verbose log without displaying a dialog box containing an error message.</span></span>

<span data-ttu-id="1ce99-107">**[Windows Installer 4,5 o una versión anterior](not-supported-in-windows-installer-4-5.md):** No compatible.</span><span class="sxs-lookup"><span data-stu-id="1ce99-107">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="1ce99-108">Este ControlEvent, está disponible a partir de Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="1ce99-108">This ControlEvent is available beginning with Windows Installer 5.0.</span></span>

## <a name="published-by"></a><span data-ttu-id="1ce99-109">Publicado por</span><span class="sxs-lookup"><span data-stu-id="1ce99-109">Published By</span></span>

<span data-ttu-id="1ce99-110">Este ControlEvent, lo publica el instalador.</span><span class="sxs-lookup"><span data-stu-id="1ce99-110">This ControlEvent is published by the installer.</span></span>

## <a name="argument"></a><span data-ttu-id="1ce99-111">Argumento</span><span class="sxs-lookup"><span data-stu-id="1ce99-111">Argument</span></span>

<span data-ttu-id="1ce99-112">Los campos del valor del argumento están delimitados por espacios.</span><span class="sxs-lookup"><span data-stu-id="1ce99-112">The fields of the argument value are delimited by spaces.</span></span> <span data-ttu-id="1ce99-113">El primer campo contiene un valor de cadena que especifica el archivo que se va a ejecutar.</span><span class="sxs-lookup"><span data-stu-id="1ce99-113">The first field contains a string value that specifies the file that is to be run.</span></span> <span data-ttu-id="1ce99-114">Use un valor de cadena de \[ \# *filekey* \] para identificar el archivo y reemplace *filekey* por el identificador del archivo que aparece en la columna archivo de la tabla [archivo](file-table.md) .</span><span class="sxs-lookup"><span data-stu-id="1ce99-114">Use a string value of \[\#*filekey*\] to identify the file and replace *filekey* with the file's identifier appearing in the File column of the [File](file-table.md) table.</span></span> <span data-ttu-id="1ce99-115">Los campos restantes del argumento pueden contener parámetros utilizados por el archivo que se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="1ce99-115">Any remaining fields of the argument can contain parameters being used by the file being run.</span></span>

## <a name="action-on-subscribers"></a><span data-ttu-id="1ce99-116">Acción en los suscriptores</span><span class="sxs-lookup"><span data-stu-id="1ce99-116">Action on Subscribers</span></span>

<span data-ttu-id="1ce99-117">Este ControlEvent, no realiza ninguna acción en los suscriptores.</span><span class="sxs-lookup"><span data-stu-id="1ce99-117">This ControlEvent performs no actions on subscribers.</span></span>

## <a name="typical-use"></a><span data-ttu-id="1ce99-118">Uso típico</span><span class="sxs-lookup"><span data-stu-id="1ce99-118">Typical Use</span></span>

<span data-ttu-id="1ce99-119">Para permitir que un usuario elija ejecutar un archivo al final de una instalación.</span><span class="sxs-lookup"><span data-stu-id="1ce99-119">To enable a user to choose to run a file at the end of an installation.</span></span> <span data-ttu-id="1ce99-120">Este evento puede estar condicionado en una propiedad establecida por un control [CheckBox](checkbox-control.md) mostrado en el cuadro de diálogo final de la instalación.</span><span class="sxs-lookup"><span data-stu-id="1ce99-120">This event can be conditioned on a property set by a [CheckBox](checkbox-control.md) control displayed on the final dialog box of the installation.</span></span> <span data-ttu-id="1ce99-121">El control CheckBox no debe mostrarse durante la eliminación del paquete.</span><span class="sxs-lookup"><span data-stu-id="1ce99-121">The CheckBox control should not be displayed during the removal of the package.</span></span>

 

 



