---
description: Los autores de paquetes deben asegurarse de que los nombres de las tablas, propiedades o acciones personalizadas definidas en su paquete no entren en conflicto con los nombres de las tablas, propiedades o acciones estándar que son nativas para el Windows Installer.
ms.assetid: f86b51c5-161a-4218-987d-f17116e4f668
title: Asignar nombres a tablas, propiedades y acciones personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aabd35fb1456f6aefbd05d486b1d86420bf5013
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908707"
---
# <a name="naming-custom-tables-properties-and-actions"></a><span data-ttu-id="65bd3-103">Asignar nombres a tablas, propiedades y acciones personalizadas</span><span class="sxs-lookup"><span data-stu-id="65bd3-103">Naming Custom Tables, Properties, and Actions</span></span>

<span data-ttu-id="65bd3-104">Los autores de paquetes deben asegurarse de que los nombres de las tablas, propiedades o acciones personalizadas definidas en su paquete no entren en conflicto con los nombres de las tablas, propiedades o acciones estándar que son nativas para el Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="65bd3-104">Package authors should ensure that the names of any custom tables, properties, or actions defined in their package will not conflict with the names of standard tables, properties, or actions that are native to the Windows Installer.</span></span>

<span data-ttu-id="65bd3-105">Los autores de paquetes deben cumplir las siguientes directrices para los nombres de tabla, propiedad o acción personalizados.</span><span class="sxs-lookup"><span data-stu-id="65bd3-105">Package authors should adhere to the following guidelines for custom table, property, or action names.</span></span>

-   <span data-ttu-id="65bd3-106">Cree nombres para las tablas, las propiedades o las acciones personalizadas que tengan un prefijo que identifique la aplicación.</span><span class="sxs-lookup"><span data-stu-id="65bd3-106">Make names for custom tables, properties, or actions that have a prefix that identifies your application.</span></span>
-   <span data-ttu-id="65bd3-107">Nunca use un nombre con MSI como prefijo.</span><span class="sxs-lookup"><span data-stu-id="65bd3-107">Never use a name with Msi as the prefix.</span></span> <span data-ttu-id="65bd3-108">A partir de Windows Installer 2,0, todas las nuevas propiedades, acciones y tablas de Windows Installer nativas reciben nombres con el prefijo MSI.</span><span class="sxs-lookup"><span data-stu-id="65bd3-108">Starting with Windows Installer 2.0, all new native Windows Installer properties, actions, and tables are given names prefixed by Msi.</span></span> <span data-ttu-id="65bd3-109">Este prefijo no distingue entre mayúsculas y minúsculas, por ejemplo MsiNewInternalTable.</span><span class="sxs-lookup"><span data-stu-id="65bd3-109">This prefix is not case sensitive, for example MsiNewInternalTable.</span></span> <span data-ttu-id="65bd3-110">Dado que el prefijo no distingue entre mayúsculas y minúsculas, los autores deben evitar todos los casos del prefijo MSI.</span><span class="sxs-lookup"><span data-stu-id="65bd3-110">Because the prefix is not case sensitive, authors should avoid all cases of the Msi prefix.</span></span>

<span data-ttu-id="65bd3-111">Para obtener más información, vea [nombres de tabla](table-names.md).</span><span class="sxs-lookup"><span data-stu-id="65bd3-111">For more information, see [Table Names](table-names.md).</span></span>

 

 



