---
description: Puede usar la Windows Installer para detectar los componentes o archivos que faltan y, a continuación, volver a instalar las características que contienen los componentes que faltan.
ms.assetid: b197c9d0-fcc2-4ca7-a870-e1af82343455
title: Instalación de un componente que falta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9bbfd38517e850a7f4e83c9c84075d92fea2290
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652583"
---
# <a name="installing-a-missing-component"></a><span data-ttu-id="ff55c-103">Instalación de un componente que falta</span><span class="sxs-lookup"><span data-stu-id="ff55c-103">Installing a Missing Component</span></span>

<span data-ttu-id="ff55c-104">Puede usar la Windows Installer para detectar los componentes o archivos que faltan y, a continuación, volver a instalar las características que contienen los componentes que faltan.</span><span class="sxs-lookup"><span data-stu-id="ff55c-104">You can use the Windows Installer to detect missing components or files, and then reinstall features that contain the missing components.</span></span> <span data-ttu-id="ff55c-105">Dado que el instalador instala las características de y no los componentes de, primero debe resolver el componente al que pertenece un archivo que falta y, a continuación, instalar la característica que contiene el componente.</span><span class="sxs-lookup"><span data-stu-id="ff55c-105">Because the Installer installs features and not components, it must first resolve to which component a missing file belongs, and then install the feature that contains the component.</span></span> <span data-ttu-id="ff55c-106">Si hay más de una característica vinculada al componente, el instalador instala la característica que requiere menos espacio en disco.</span><span class="sxs-lookup"><span data-stu-id="ff55c-106">If more than one feature is linked to the component, the Installer installs the feature that requires the least disk space.</span></span>

<span data-ttu-id="ff55c-107">Si llama a [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha), puede comprobar que el archivo de clave de un componente está presente.</span><span class="sxs-lookup"><span data-stu-id="ff55c-107">If you call [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha), you can verify that the key file of a component is present.</span></span> <span data-ttu-id="ff55c-108">Sin embargo, aún es posible que falten otros archivos que pertenecen al componente.</span><span class="sxs-lookup"><span data-stu-id="ff55c-108">However, it is still possible that other files belonging to the component are missing.</span></span> <span data-ttu-id="ff55c-109">En ese escenario, llame a [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea).</span><span class="sxs-lookup"><span data-stu-id="ff55c-109">In that scenario, call [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea).</span></span> <span data-ttu-id="ff55c-110">A continuación, el instalador se resuelve como el componente al que pertenece el archivo e instala la característica que está vinculada al componente que requiere menos espacio en disco.</span><span class="sxs-lookup"><span data-stu-id="ff55c-110">The Installer then resolves to which component the file belongs, and installs the feature that is linked to the component that requires the least disk space.</span></span>

<span data-ttu-id="ff55c-111">Si se produce un error inesperado en la función [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) , debe instalar los componentes que falten.</span><span class="sxs-lookup"><span data-stu-id="ff55c-111">If the [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) function unexpectedly fails, you must install any missing components.</span></span>

<span data-ttu-id="ff55c-112">En el procedimiento siguiente se muestra cómo instalar los componentes que faltan.</span><span class="sxs-lookup"><span data-stu-id="ff55c-112">The following procedure shows you how to install missing components.</span></span>

<span data-ttu-id="ff55c-113">**Para detectar e instalar un componente que falta**</span><span class="sxs-lookup"><span data-stu-id="ff55c-113">**To detect and install a missing component**</span></span>

1.  <span data-ttu-id="ff55c-114">Llame a [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) para comprobar que el archivo de clave de un componente está presente.</span><span class="sxs-lookup"><span data-stu-id="ff55c-114">Call [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) to verify that the key file of a component is present.</span></span> <span data-ttu-id="ff55c-115">Sin embargo, incluso si el archivo de clave del componente está presente, aún es posible que falten otros archivos que pertenecen al componente.</span><span class="sxs-lookup"><span data-stu-id="ff55c-115">However, even if the key file of the component is present, it is still possible that other files belonging to the component are missing.</span></span>
2.  <span data-ttu-id="ff55c-116">Llame a la función [**MsiInstallMissingComponent**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta) si se desconoce la característica asociada al componente.</span><span class="sxs-lookup"><span data-stu-id="ff55c-116">Call the [**MsiInstallMissingComponent**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingcomponenta) function if the feature associated with the component is unknown.</span></span>
3.  <span data-ttu-id="ff55c-117">Llame a la función [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) o [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta) si se conoce la característica asociada al componente.</span><span class="sxs-lookup"><span data-stu-id="ff55c-117">Call the [**MsiConfigureFeature**](/windows/desktop/api/Msi/nf-msi-msiconfigurefeaturea) or [**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta) function if the feature associated with the component is known.</span></span>
4.  <span data-ttu-id="ff55c-118">Llame a [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea) si una aplicación no puede abrir un archivo.</span><span class="sxs-lookup"><span data-stu-id="ff55c-118">Call [**MsiInstallMissingFile**](/windows/desktop/api/Msi/nf-msi-msiinstallmissingfilea) if an application is unable to open a file.</span></span>

 

 



