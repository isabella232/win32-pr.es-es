---
description: 'Windows Installer funciones que devuelven datos en un usuario proporcionado: no se debe llamar a la ubicación de memoria con NULL como valor del puntero.'
ms.assetid: f566c4a4-b90c-4d73-9d7f-f5b836630636
title: Pasar null a Windows Installer funciones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb09ceb3982695792614a3c226af9ab276aa3a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652524"
---
# <a name="passing-null-as-the-argument-of-windows-installer-functions"></a><span data-ttu-id="2e634-103">Pasar null como argumento de funciones de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="2e634-103">Passing null as the Argument of Windows Installer Functions</span></span>

<span data-ttu-id="2e634-104">Windows Installer funciones que devuelven datos en un usuario proporcionado: no se debe llamar a la ubicación de memoria con NULL como valor del puntero.</span><span class="sxs-lookup"><span data-stu-id="2e634-104">Windows Installer functions that return data in a user provided–memory location should not be called with null as the value for the pointer.</span></span> <span data-ttu-id="2e634-105">Estas funciones devuelven una cadena o devuelven datos como punteros enteros, pero devuelven valores incoherentes al pasar null como valor para el argumento de salida.</span><span class="sxs-lookup"><span data-stu-id="2e634-105">These functions return a string or return data as integer pointers, but return inconsistent values when passing null as the value for the output argument.</span></span>

<span data-ttu-id="2e634-106">No pase NULL como el valor del argumento Output para cualquiera de las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="2e634-106">Do not pass Null as the value of the output argument for any of the following functions:</span></span>

[<span data-ttu-id="2e634-107">**MsiGetProperty**</span><span class="sxs-lookup"><span data-stu-id="2e634-107">**MsiGetProperty**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya)

[<span data-ttu-id="2e634-108">**MsiRecordGetString**</span><span class="sxs-lookup"><span data-stu-id="2e634-108">**MsiRecordGetString**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msirecordgetstringa)

[<span data-ttu-id="2e634-109">**MsiFormatRecord**</span><span class="sxs-lookup"><span data-stu-id="2e634-109">**MsiFormatRecord**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda)

[<span data-ttu-id="2e634-110">**MsiGetSourcePath**</span><span class="sxs-lookup"><span data-stu-id="2e634-110">**MsiGetSourcePath**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetsourcepatha)

[<span data-ttu-id="2e634-111">**MsiGetTargetPath**</span><span class="sxs-lookup"><span data-stu-id="2e634-111">**MsiGetTargetPath**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigettargetpatha)

[<span data-ttu-id="2e634-112">**MsiGetFeatureState**</span><span class="sxs-lookup"><span data-stu-id="2e634-112">**MsiGetFeatureState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)

[<span data-ttu-id="2e634-113">**MsiViewGetError**</span><span class="sxs-lookup"><span data-stu-id="2e634-113">**MsiViewGetError**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msiviewgeterrora)

[<span data-ttu-id="2e634-114">**MsiSummaryInfoGetProperty**</span><span class="sxs-lookup"><span data-stu-id="2e634-114">**MsiSummaryInfoGetProperty**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya)

[<span data-ttu-id="2e634-115">**MsiEvaluateCondition**</span><span class="sxs-lookup"><span data-stu-id="2e634-115">**MsiEvaluateCondition**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msievaluateconditiona)

[<span data-ttu-id="2e634-116">**MsiGetFeatureCost**</span><span class="sxs-lookup"><span data-stu-id="2e634-116">**MsiGetFeatureCost**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)

[<span data-ttu-id="2e634-117">**MsiGetFeatureState**</span><span class="sxs-lookup"><span data-stu-id="2e634-117">**MsiGetFeatureState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea)

[<span data-ttu-id="2e634-118">**MsiGetComponentState**</span><span class="sxs-lookup"><span data-stu-id="2e634-118">**MsiGetComponentState**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea)

[<span data-ttu-id="2e634-119">**MsiGetFeatureCost**</span><span class="sxs-lookup"><span data-stu-id="2e634-119">**MsiGetFeatureCost**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturecosta)

[<span data-ttu-id="2e634-120">**MsiGetFeatureValidStates**</span><span class="sxs-lookup"><span data-stu-id="2e634-120">**MsiGetFeatureValidStates**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturevalidstatesa)

 

 



