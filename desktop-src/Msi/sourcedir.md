---
description: La propiedad SourceDir es el directorio raíz que contiene el archivo. cab de origen o el árbol de archivos de origen del paquete de instalación. Este valor se usa para la resolución de directorios.
ms.assetid: 900b26e8-80dd-4e70-8d79-37f09a0c6e86
title: Propiedad SourceDir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a366e4afecdd16722a06ecfbec08552baab8f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681042"
---
# <a name="sourcedir-property"></a><span data-ttu-id="3519a-104">Propiedad SourceDir</span><span class="sxs-lookup"><span data-stu-id="3519a-104">SourceDir property</span></span>

<span data-ttu-id="3519a-105">La propiedad **SourceDir** es el directorio raíz que contiene el archivo. cab de origen o el árbol de archivos de origen del paquete de instalación.</span><span class="sxs-lookup"><span data-stu-id="3519a-105">The **SourceDir** property is the root directory that contains the source cabinet file or the source file tree of the installation package.</span></span> <span data-ttu-id="3519a-106">Este valor se usa para la resolución de directorios.</span><span class="sxs-lookup"><span data-stu-id="3519a-106">This value is used for directory resolution.</span></span>

## <a name="default-value"></a><span data-ttu-id="3519a-107">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="3519a-107">Default Value</span></span>

<span data-ttu-id="3519a-108">Directorio que contiene el paquete de instalación.</span><span class="sxs-lookup"><span data-stu-id="3519a-108">The directory that contains the installation package.</span></span>

## <a name="remarks"></a><span data-ttu-id="3519a-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3519a-109">Remarks</span></span>

<span data-ttu-id="3519a-110">Se debe llamar a la [acción ResolveSource](resolvesource-action.md) antes de usar la propiedad **SourceDir** en cualquier expresión o intentar recuperar el valor de **SourceDir** con [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya).</span><span class="sxs-lookup"><span data-stu-id="3519a-110">The [ResolveSource action](resolvesource-action.md) must be called before using the **SourceDir** property in any expression or attempting to retrieve the value of **SourceDir** with [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya).</span></span> <span data-ttu-id="3519a-111">La acción ResolveSource no debe ejecutarse mientras el origen no esté disponible, por ejemplo, al desinstalar una aplicación, ya que esto puede producir un mensaje imprevisto para los medios de origen.</span><span class="sxs-lookup"><span data-stu-id="3519a-111">The ResolveSource action should not be run while the source is unavailable, such as when uninstalling an application, because this can cause an unintended prompt for the source media.</span></span>

## <a name="requirements"></a><span data-ttu-id="3519a-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3519a-112">Requirements</span></span>



| <span data-ttu-id="3519a-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="3519a-113">Requirement</span></span> | <span data-ttu-id="3519a-114">Value</span><span class="sxs-lookup"><span data-stu-id="3519a-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3519a-115">Versión</span><span class="sxs-lookup"><span data-stu-id="3519a-115">Version</span></span><br/> | <span data-ttu-id="3519a-116">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3519a-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3519a-117">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3519a-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3519a-118">Windows Installer en Windows Server 2003 o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3519a-118">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="3519a-119">Consulte los [requisitos de Run-Time de Windows Installer](windows-installer-portal.md) para obtener información sobre la Service Pack mínima de Windows que requiere una versión Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="3519a-119">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3519a-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3519a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3519a-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3519a-121">Properties</span></span>](properties.md)
</dt> </dl>

 

 




