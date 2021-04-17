---
description: La lista espacio en disco permite calcular el espacio en disco necesario para completar las operaciones de instalación.
ms.assetid: 6514cbdd-2f23-4ab8-9e34-86d3837503dc
title: Acerca de la lista de Disk-Space
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b092d73c00f426fe5c0ab298e4b6a53c19131c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666433"
---
# <a name="about-the-disk-space-list"></a><span data-ttu-id="18f07-103">Acerca de la lista de Disk-Space</span><span class="sxs-lookup"><span data-stu-id="18f07-103">About the Disk-Space List</span></span>

<span data-ttu-id="18f07-104">La lista espacio en disco permite calcular el espacio en disco necesario para completar las operaciones de instalación.</span><span class="sxs-lookup"><span data-stu-id="18f07-104">The disk-space list enables you to calculate the disk space required to complete the installation operations.</span></span> <span data-ttu-id="18f07-105">Después de crear una lista de espacio en disco y de agregarle operaciones de archivo, puede consultar la lista para determinar las unidades de destino especificadas por las operaciones de archivo y el espacio en disco necesario en cada unidad.</span><span class="sxs-lookup"><span data-stu-id="18f07-105">After you create a disk-space list and add file operations to it, you can query the list to determine the target drives specified by the file operations, and the disk space required on each drive.</span></span>

<span data-ttu-id="18f07-106">Al comparar el espacio necesario para el espacio disponible en los discos de destino, puede determinar mediante programación si hay suficiente espacio disponible para la instalación actual.</span><span class="sxs-lookup"><span data-stu-id="18f07-106">By comparing the space required to the space available on the target disks, you can programmatically determine whether sufficient space is available for the current installation.</span></span>

<span data-ttu-id="18f07-107">Puede Agregar o quitar operaciones de archivo en la lista de espacio en disco y recalcular el espacio en disco necesario.</span><span class="sxs-lookup"><span data-stu-id="18f07-107">You can add or remove file operations to the disk-space list and recalculate the disk space required.</span></span> <span data-ttu-id="18f07-108">Esta funcionalidad permite, por ejemplo, escribir un programa que interactúe con el usuario, permitiéndole elegir qué componentes desean instalar en función del espacio en disco necesario.</span><span class="sxs-lookup"><span data-stu-id="18f07-108">This functionality enables you to, for example, write a program that interacts with the user, allowing him or her to choose what components they want to install based on the disk space required.</span></span>

<span data-ttu-id="18f07-109">Las funciones de lista de espacio en disco comprueban automáticamente si hay copias preexistentes de archivos en el disco de destino.</span><span class="sxs-lookup"><span data-stu-id="18f07-109">The disk-space list functions automatically check for preexisting copies of files on the target disk.</span></span> <span data-ttu-id="18f07-110">Si se encuentra una versión anterior del archivo, las funciones de lista de espacio en disco calculan el espacio adicional necesario para completar las operaciones de archivo.</span><span class="sxs-lookup"><span data-stu-id="18f07-110">If a previous version of the file is found, the disk-space list functions calculate the additional space required to complete the file operations.</span></span>

<span data-ttu-id="18f07-111">Por ejemplo, si una operación de copia especifica que se copie un archivo de 6000 bytes en la unidad C y ya existe una versión de 2000 bytes de ese archivo en la unidad C, las funciones de espacio en disco devolverán un espacio necesario de 4000 bytes.</span><span class="sxs-lookup"><span data-stu-id="18f07-111">For example, if a copy operation specifies that a 6000-byte file be copied to drive C, and a 2000-byte version of that file already exists on the drive C, the disk space functions would return a required space of 4000 bytes.</span></span> <span data-ttu-id="18f07-112">El espacio adicional se usa para reemplazar la versión anterior del archivo por la versión más reciente.</span><span class="sxs-lookup"><span data-stu-id="18f07-112">The additional space is used to replace the older version of the file with the newer version.</span></span>

<span data-ttu-id="18f07-113">Las funciones de lista de espacio en disco redondean los tamaños de archivo a los límites del clúster de disco.</span><span class="sxs-lookup"><span data-stu-id="18f07-113">The disk-space list functions round file sizes to the disk cluster boundaries.</span></span>

 

 



