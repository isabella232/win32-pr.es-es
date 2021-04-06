---
description: Antes de llamar a cualquiera de las siguientes funciones de base de datos desde un programa, como una acción personalizada o un proceso de automatización, el instalador debe ejecutar primero la acción CostInitialize, la acción FileCost y la acción CostFinalize.
ms.assetid: b9795825-41fa-474b-a0c5-06770aa99bc1
title: Llamar a funciones de base de datos desde programas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e2adeab5570bc6786439d5de509f03ab906a0c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909038"
---
# <a name="calling-database-functions-from-programs"></a><span data-ttu-id="b9ad7-103">Llamar a funciones de base de datos desde programas</span><span class="sxs-lookup"><span data-stu-id="b9ad7-103">Calling Database Functions from Programs</span></span>

<span data-ttu-id="b9ad7-104">Antes de llamar a cualquiera de las siguientes [funciones de base de datos](database-functions.md) desde un programa, como una acción personalizada o un proceso de automatización, el instalador debe ejecutar primero la acción [CostInitialize](costinitialize-action.md), la acción [FileCost](filecost-action.md)y la [acción CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="b9ad7-104">Before calling any of the following [Database Functions](database-functions.md) from a program, such as a custom action or an automation process, the installer must first run the [CostInitialize action](costinitialize-action.md), [FileCost action](filecost-action.md), and [CostFinalize action](costfinalize-action.md).</span></span>

<span data-ttu-id="b9ad7-105">A continuación se muestra una lista de las funciones de base de datos que se usan en Windows Installer:</span><span class="sxs-lookup"><span data-stu-id="b9ad7-105">The following is a list of database functions used in Windows Installer:</span></span>

-   [<span data-ttu-id="b9ad7-106">**MsiGetComponentState**</span><span class="sxs-lookup"><span data-stu-id="b9ad7-106">**MsiGetComponentState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)
-   [<span data-ttu-id="b9ad7-107">**MsiGetFeatureCost**</span><span class="sxs-lookup"><span data-stu-id="b9ad7-107">**MsiGetFeatureCost**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)
-   [<span data-ttu-id="b9ad7-108">**MsiGetFeatureState**</span><span class="sxs-lookup"><span data-stu-id="b9ad7-108">**MsiGetFeatureState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)
-   [<span data-ttu-id="b9ad7-109">**MsiGetFeatureValidStates**</span><span class="sxs-lookup"><span data-stu-id="b9ad7-109">**MsiGetFeatureValidStates**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa)
-   [<span data-ttu-id="b9ad7-110">**MsiGetSourcePath**</span><span class="sxs-lookup"><span data-stu-id="b9ad7-110">**MsiGetSourcePath**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetsourcepatha)
-   [<span data-ttu-id="b9ad7-111">**MsiGetTargetPath**</span><span class="sxs-lookup"><span data-stu-id="b9ad7-111">**MsiGetTargetPath**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha)
-   [<span data-ttu-id="b9ad7-112">**MsiSetComponentState**</span><span class="sxs-lookup"><span data-stu-id="b9ad7-112">**MsiSetComponentState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea)
-   [<span data-ttu-id="b9ad7-113">**MsiSetFeatureState**</span><span class="sxs-lookup"><span data-stu-id="b9ad7-113">**MsiSetFeatureState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeaturestatea)
-   [<span data-ttu-id="b9ad7-114">**MsiSetInstallLevel**</span><span class="sxs-lookup"><span data-stu-id="b9ad7-114">**MsiSetInstallLevel**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisetinstalllevel)
-   [<span data-ttu-id="b9ad7-115">**MsiSetTargetPath**</span><span class="sxs-lookup"><span data-stu-id="b9ad7-115">**MsiSetTargetPath**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisettargetpatha)
-   [<span data-ttu-id="b9ad7-116">**MsiVerifyDiskSpace**</span><span class="sxs-lookup"><span data-stu-id="b9ad7-116">**MsiVerifyDiskSpace**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msiverifydiskspace)

<span data-ttu-id="b9ad7-117">Antes de llamar a [**MsiSetFeatureAttributes**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeatureattributesa) desde un programa, el instalador debe ejecutar primero la acción CostInitialize.</span><span class="sxs-lookup"><span data-stu-id="b9ad7-117">Before calling [**MsiSetFeatureAttributes**](/windows/desktop/api/Msiquery/nf-msiquery-msisetfeatureattributesa) from a program, the installer must first run the CostInitialize action.</span></span> <span data-ttu-id="b9ad7-118">Después, el instalador ejecuta la acción CostFinalize después de **MsiSetFeatureAttributes**.</span><span class="sxs-lookup"><span data-stu-id="b9ad7-118">The installer then runs the CostFinalize action after **MsiSetFeatureAttributes**.</span></span>

<span data-ttu-id="b9ad7-119">En el ejemplo siguiente se muestra el orden en el que se debe llamar a las acciones de función al usar [**MsiGetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) en un programa.</span><span class="sxs-lookup"><span data-stu-id="b9ad7-119">The following example illustrates the order in which function actions must be called when using [**MsiGetTargetPath**](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha) in a program.</span></span>


```C++
#include <windows.h>
#include <Msiquery.h>
#include <tchar.h>
#pragma comment(lib, "msi.lib") 

int main()  
{ 

MSIHANDLE hInstall;
TCHAR *szBuf;
DWORD cch  = 0 ;
 
if(MsiOpenPackage(_T("PathToPackage...."), &hInstall) == ERROR_SUCCESS)
{
    if(MsiDoAction(hInstall, _T("CostInitialize"))==ERROR_SUCCESS  
        && MsiDoAction(hInstall, _T("FileCost"))==ERROR_SUCCESS  
        && MsiDoAction(hInstall, _T("CostFinalize"))==ERROR_SUCCESS)   
    { 
        if(MsiGetTargetPath(hInstall, _T("FolderName"), _T(""),&cch)==ERROR_MORE_DATA)
        { 
            cch++; // add 1 to include null terminator since MsiGetTargetPath does not include it on return 
            szBuf = (TCHAR *) malloc(cch*sizeof(TCHAR));
            if(szBuf)
            {
                if(MsiGetTargetPath(hInstall, _T("FolderName"), szBuf,&cch)==ERROR_SUCCESS)
                {
                    // Add code to use szBuf here
                }
                free(szBuf);
            }
        } 
    } 
    MsiCloseHandle(hInstall);
}

return 0;  
}
```



 

 



