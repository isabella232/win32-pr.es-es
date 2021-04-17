---
description: Comience a crear el paquete de actualización copiando el paquete de instalación y el árbol de directorio de origen del producto original.
ms.assetid: 279f0ab6-a6fc-4594-af6c-5a69d6167300
title: Importar la base de datos de instalación original
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 390a51e1ef068124fcdf85142ab01406d92f9a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652854"
---
# <a name="importing-original-installation-database"></a><span data-ttu-id="f7694-103">Importar la base de datos de instalación original</span><span class="sxs-lookup"><span data-stu-id="f7694-103">Importing Original Installation Database</span></span>

<span data-ttu-id="f7694-104">Comience a crear el paquete de actualización copiando el paquete de instalación y el árbol de directorio de origen del producto original.</span><span class="sxs-lookup"><span data-stu-id="f7694-104">Begin authoring the upgrade package by copying the installation package and source directory tree of the of original product.</span></span> <span data-ttu-id="f7694-105">Las instrucciones para crear el paquete de instalación para MNP2000 se proporcionan en [un ejemplo de instalación](an-installation-example.md).</span><span class="sxs-lookup"><span data-stu-id="f7694-105">Instructions for authoring the installation package for MNP2000 are given in [An Installation Example](an-installation-example.md).</span></span> <span data-ttu-id="f7694-106">Debe copiar el contenido de las carpetas siguientes:</span><span class="sxs-lookup"><span data-stu-id="f7694-106">You should copy the contents of the following folders:</span></span>

<span data-ttu-id="f7694-107">C: \\MNP2000.msi de ejemplo \\</span><span class="sxs-lookup"><span data-stu-id="f7694-107">C:\\Sample\\MNP2000.msi</span></span>

<span data-ttu-id="f7694-108">C: \\ Bloc de notas de ejemplo </span><span class="sxs-lookup"><span data-stu-id="f7694-108">C:\\Sample\\Notepad</span></span>\\\\

<span data-ttu-id="f7694-109">C: \\ \\ binario de ejemplo</span><span class="sxs-lookup"><span data-stu-id="f7694-109">C:\\Sample\\Binary</span></span>\\

<span data-ttu-id="f7694-110">C: \\ icono de muestra </span><span class="sxs-lookup"><span data-stu-id="f7694-110">C:\\Sample\\Icon</span></span>\\\\

<span data-ttu-id="f7694-111">Actualice el contenido de la carpeta del Bloc de notas para que coincida con el origen descrito en [planeación de una actualización principal](planning-a-major-upgrade.md).</span><span class="sxs-lookup"><span data-stu-id="f7694-111">Update the contents of the Notepad folder so that they match the source described in [Planning a Major Upgrade](planning-a-major-upgrade.md).</span></span> <span data-ttu-id="f7694-112">Quite todos los archivos de código fuente obsoletos, como Baseball.txt, y reemplácelos por los archivos actualizados, como Baseba01.txt.</span><span class="sxs-lookup"><span data-stu-id="f7694-112">Remove all obsolete source files, such as Baseball.txt, and replace with the updated files, such as Baseba01.txt.</span></span> <span data-ttu-id="f7694-113">Agregue los nuevos archivos adicionales proporcionados por la actualización, como Opera01.txt.</span><span class="sxs-lookup"><span data-stu-id="f7694-113">Add the additional new files provided by the upgrade, such as Opera01.txt.</span></span>

<span data-ttu-id="f7694-114">Cambie el nombre de MNP2000.msi a MNP2001.msi.</span><span class="sxs-lookup"><span data-stu-id="f7694-114">Rename MNP2000.msi to MNP2001.msi.</span></span> <span data-ttu-id="f7694-115">En los pasos siguientes, usará un editor de tablas para modificar esta base de datos en el archivo. msi de la actualización.</span><span class="sxs-lookup"><span data-stu-id="f7694-115">In subsequent steps you will use a table editor to modify this database into the .msi file for the upgrade.</span></span> <span data-ttu-id="f7694-116">Las tablas de base de datos que no se modifican explícitamente en las secciones siguientes son idénticas a las tablas de la base de datos del producto original, MNP2000.msi.</span><span class="sxs-lookup"><span data-stu-id="f7694-116">Database tables that are not explicitly modified in the subsequent sections are identical to the tables in the original product's database, MNP2000.msi.</span></span>

[<span data-ttu-id="f7694-117">Continuar</span><span class="sxs-lookup"><span data-stu-id="f7694-117">Continue</span></span>](updating-directory-structure-for-an-upgrade.md)

 

 



