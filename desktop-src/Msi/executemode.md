---
description: La propiedad EXECUTEMODE especifica cómo el instalador ejecuta las actualizaciones del sistema.
ms.assetid: 7b90d2e6-d661-412b-b054-2c218c95c02a
title: Propiedad EXECUTEMODE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ebf1de2fb7538ece838e674b62847f0c526842e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691094"
---
# <a name="executemode-property"></a><span data-ttu-id="d03c7-103">Propiedad EXECUTEMODE</span><span class="sxs-lookup"><span data-stu-id="d03c7-103">EXECUTEMODE property</span></span>

<span data-ttu-id="d03c7-104">La propiedad **EXECUTEMODE** especifica cómo el instalador ejecuta las actualizaciones del sistema.</span><span class="sxs-lookup"><span data-stu-id="d03c7-104">The **EXECUTEMODE** property specifies how the installer executes system updates.</span></span> <span data-ttu-id="d03c7-105">Esta propiedad puede ser útil cuando es necesario ejecutar una instalación sin cambiar realmente el sistema.</span><span class="sxs-lookup"><span data-stu-id="d03c7-105">This property may be useful when it is necessary to run an installation without actually changing the system.</span></span> <span data-ttu-id="d03c7-106">La propiedad se puede establecer en None para deshabilitar las operaciones de actualización, como la instalación de archivos y valores del registro.</span><span class="sxs-lookup"><span data-stu-id="d03c7-106">The property can be set to None to disable updating operations such as the installation of files and registry values.</span></span>

<span data-ttu-id="d03c7-107">Esta propiedad puede tener uno de los dos valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="d03c7-107">This property can have one of the following two values.</span></span> <span data-ttu-id="d03c7-108">El instalador solo examina la primera letra del valor y no distingue entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="d03c7-108">The installer only examines the first letter of the value and is case insensitive.</span></span>

<dl> <dt>

<span data-ttu-id="d03c7-109"><span id="None"></span><span id="none"></span><span id="NONE"></span>Ninguna</span><span class="sxs-lookup"><span data-stu-id="d03c7-109"><span id="None"></span><span id="none"></span><span id="NONE"></span>None</span></span>
</dt> <dd>

<span data-ttu-id="d03c7-110">No se realiza ningún cambio en el sistema.</span><span class="sxs-lookup"><span data-stu-id="d03c7-110">No changes are made to the system.</span></span> <span data-ttu-id="d03c7-111">El instalador ejecuta la interfaz de usuario y, a continuación, consulta la base de datos.</span><span class="sxs-lookup"><span data-stu-id="d03c7-111">The installer runs the user interface and then queries the database.</span></span>

</dd> <dt>

<span data-ttu-id="d03c7-112"><span id="Script"></span><span id="script"></span><span id="SCRIPT"></span>Manuscrit</span><span class="sxs-lookup"><span data-stu-id="d03c7-112"><span id="Script"></span><span id="script"></span><span id="SCRIPT"></span>Script</span></span>
</dt> <dd>

<span data-ttu-id="d03c7-113">Todos los cambios en el sistema se realizan a través de la ejecución del script.</span><span class="sxs-lookup"><span data-stu-id="d03c7-113">All changes to the system are made through script execution.</span></span> <span data-ttu-id="d03c7-114">Este es el modo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d03c7-114">This is the default mode.</span></span>

</dd> </dl>

## <a name="default-value"></a><span data-ttu-id="d03c7-115">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="d03c7-115">Default Value</span></span>

<span data-ttu-id="d03c7-116">Si no se define esta propiedad, el valor predeterminado del modo de ejecución es script.</span><span class="sxs-lookup"><span data-stu-id="d03c7-116">If this property is not defined, the execution mode defaults to Script.</span></span>

## <a name="requirements"></a><span data-ttu-id="d03c7-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d03c7-117">Requirements</span></span>



| <span data-ttu-id="d03c7-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="d03c7-118">Requirement</span></span> | <span data-ttu-id="d03c7-119">Value</span><span class="sxs-lookup"><span data-stu-id="d03c7-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d03c7-120">Versión</span><span class="sxs-lookup"><span data-stu-id="d03c7-120">Version</span></span><br/> | <span data-ttu-id="d03c7-121">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d03c7-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d03c7-122">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d03c7-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d03c7-123">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d03c7-123">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="d03c7-124">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="d03c7-124">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d03c7-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d03c7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d03c7-126">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d03c7-126">Properties</span></span>](properties.md)
</dt> </dl>

 

 




