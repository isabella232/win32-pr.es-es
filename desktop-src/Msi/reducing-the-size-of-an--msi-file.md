---
description: Es posible que los desarrolladores de paquetes de Windows Installer observen que sus archivos. msi son más grandes de lo esperado después de las modificaciones y guardaciones repetidas.
ms.assetid: d5229ef5-0cb5-4daf-8468-0cb653029c1c
title: Reducir el tamaño de un archivo. msi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b5a19c92f0567fc6081d772279ec2cc0b6cafef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001873"
---
# <a name="reducing-the-size-of-an-msi-file"></a><span data-ttu-id="d064e-103">Reducir el tamaño de un archivo. msi</span><span class="sxs-lookup"><span data-stu-id="d064e-103">Reducing the Size of an .msi File</span></span>

<span data-ttu-id="d064e-104">Es posible que los desarrolladores de paquetes de Windows Installer observen que sus archivos. msi son más grandes de lo esperado después de las modificaciones y guardaciones repetidas.</span><span class="sxs-lookup"><span data-stu-id="d064e-104">Developers of Windows Installer packages may notice their .msi files getting larger than expected after repeated edits and saves.</span></span> <span data-ttu-id="d064e-105">Windows Installer archivos. msi son archivos compuestos que contienen almacenamientos y secuencias, y tienen algunas de las mismas limitaciones de almacenamiento que los archivos de documento OLE.</span><span class="sxs-lookup"><span data-stu-id="d064e-105">Windows Installer .msi files are compound files that contain storages and streams, and have some of the same storage limitations as OLE document files.</span></span> <span data-ttu-id="d064e-106">Si edita y guarda el mismo archivo. msi una y otra vez, crea espacio de almacenamiento desperdiciado en el archivo.</span><span class="sxs-lookup"><span data-stu-id="d064e-106">If you edit and save the same .msi file over and over, it creates wasted storage space in the file.</span></span> <span data-ttu-id="d064e-107">Esto solo afecta a los autores de archivos. msi y no tiene ningún efecto en Windows Installer usuarios.</span><span class="sxs-lookup"><span data-stu-id="d064e-107">This only affects authors of .msi files and has no effect on Windows Installer users.</span></span> <span data-ttu-id="d064e-108">Los desarrolladores pueden querer quitar este espacio de almacenamiento desperdiciado antes de enviar su archivo. msi final.</span><span class="sxs-lookup"><span data-stu-id="d064e-108">Developers may want to remove this wasted storage space before shipping their final .msi file.</span></span>

<span data-ttu-id="d064e-109">Para quitar el espacio de almacenamiento desperdiciado y reducir el tamaño final de los archivos. msi, tiene las siguientes opciones.</span><span class="sxs-lookup"><span data-stu-id="d064e-109">To remove wasted storage space and reduce the final size of .msi files, you have the following options.</span></span>

-   <span data-ttu-id="d064e-110">Exporte todas las tablas de la base de datos a archivos. IDT y, a continuación, impórtelos en una nueva base de datos.</span><span class="sxs-lookup"><span data-stu-id="d064e-110">Export all of the tables in the database to .idt files, and then import those into a new database.</span></span> <span data-ttu-id="d064e-111">Esto produce el almacenamiento más compacto posible.</span><span class="sxs-lookup"><span data-stu-id="d064e-111">This produces the most compact storage possible.</span></span>
-   <span data-ttu-id="d064e-112">Use una utilidad de software para compactar el espacio de almacenamiento de los archivos de documento OLE.</span><span class="sxs-lookup"><span data-stu-id="d064e-112">Use a software utility for compacting the storage space of OLE document files.</span></span>

 

 



