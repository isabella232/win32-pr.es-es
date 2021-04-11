---
description: Después de terminar con una clase o una instancia, puede que desee eliminar esa clase o instancia de WMI.
ms.assetid: 8d4bf548-a332-4058-92d0-d613bbeaa408
ms.tgt_platform: multiple
title: Eliminar una clase o una instancia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42a46a52400623e31df3e051a0b587f49326733b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276262"
---
# <a name="deleting-a-class-or-instance"></a><span data-ttu-id="05ede-103">Eliminar una clase o una instancia</span><span class="sxs-lookup"><span data-stu-id="05ede-103">Deleting a Class or Instance</span></span>

<span data-ttu-id="05ede-104">Después de terminar con una clase o una instancia, puede que desee eliminar esa clase o instancia de WMI.</span><span class="sxs-lookup"><span data-stu-id="05ede-104">After you finish with a class or an instance, you may wish to delete that class or instance from WMI.</span></span> <span data-ttu-id="05ede-105">Al igual que otras tecnologías orientadas a objetos, puede eliminar objetos de clase o instancia para limpiar el espacio de nombres WMI y devolver recursos del sistema.</span><span class="sxs-lookup"><span data-stu-id="05ede-105">Like other object-oriented technologies, you can delete class or instance objects to clean up the WMI namespace and to return system resources.</span></span> <span data-ttu-id="05ede-106">Sin embargo, muchas clases e instancias en WMI son persistentes y se usan en una gran variedad de aplicaciones en un momento dado. por lo tanto, debe tener cuidado al eliminar una clase o instancia de WMI: la aplicación u otra aplicación probablemente necesitará la clase o instancia en una fecha posterior.</span><span class="sxs-lookup"><span data-stu-id="05ede-106">However, many classes and instances in WMI are persistent and are used by a variety of applications at any given time Therefore, you should be careful when deleting a WMI class or instance: your application or another application will probably need the class or instance at a later date.</span></span>

<span data-ttu-id="05ede-107">Eliminar una clase o una instancia es un procedimiento sencillo.</span><span class="sxs-lookup"><span data-stu-id="05ede-107">Deleting a class or an instance is a simple procedure.</span></span> <span data-ttu-id="05ede-108">Sin embargo, debido a la naturaleza permanente de una clase, probablemente no necesitará eliminar una clase a menudo.</span><span class="sxs-lookup"><span data-stu-id="05ede-108">However, due to the permanent nature of a class, you will probably not need to delete a class often.</span></span> <span data-ttu-id="05ede-109">Por ejemplo, es poco probable que elimine la clase [**\_ DiskDrive de Win32**](/windows/desktop/CIMWin32Prov/win32-diskdrive) , porque es improbable que no tenga una unidad de disco en alguna parte de la empresa.</span><span class="sxs-lookup"><span data-stu-id="05ede-109">For example, you are unlikely to delete the [**Win32\_DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive) class, because it is unlikely that you do not have a disk drive somewhere in your enterprise.</span></span> <span data-ttu-id="05ede-110">En su lugar, es más probable que se elimine una instancia de una clase.</span><span class="sxs-lookup"><span data-stu-id="05ede-110">Instead, you will be more likely to delete an instance of a class.</span></span> <span data-ttu-id="05ede-111">Para obtener más información, consulte [eliminar una instancia](deleting-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="05ede-111">For more information, see [Deleting an Instance](deleting-an-instance.md).</span></span>

<span data-ttu-id="05ede-112">Aunque es poco frecuente, puede que le interese una vez que desee actualizar una clase que haya creado.</span><span class="sxs-lookup"><span data-stu-id="05ede-112">Although uncommon, you may come across a time where you wish to update a class that you created.</span></span> <span data-ttu-id="05ede-113">Por ejemplo, podría crear una clase para representar una aplicación de otro fabricante.</span><span class="sxs-lookup"><span data-stu-id="05ede-113">For example, you could create a class to represent a third-party application.</span></span> <span data-ttu-id="05ede-114">Si el software de terceros actualizara su software hasta el punto de que la clase ya no represente correctamente el software, es posible que tenga que eliminar la clase original.</span><span class="sxs-lookup"><span data-stu-id="05ede-114">If the third-party updated their software to the extent that your class no longer properly represented the software, you may need to delete your original class.</span></span> <span data-ttu-id="05ede-115">Para obtener más información, vea [eliminar una clase](deleting-a-class.md).</span><span class="sxs-lookup"><span data-stu-id="05ede-115">For more information, see [Deleting a Class](deleting-a-class.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="05ede-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="05ede-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05ede-117">Diseñar clases de Managed Object Format (MOF)</span><span class="sxs-lookup"><span data-stu-id="05ede-117">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 
