---
description: El método LastErrorRecord del objeto de instalador devuelve un objeto de registro que contiene los parámetros de error del error más reciente de la función que generó el registro de errores.
ms.assetid: 48fe46bc-6c10-4bd5-89bc-013e650a44e6
title: Instalador. LastErrorRecord (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.LastErrorRecord
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b368f30b04734b2d253a7d5f2aa64f0d61c930e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653326"
---
# <a name="installerlasterrorrecord-method"></a><span data-ttu-id="bab55-103">Instalador. LastErrorRecord (método)</span><span class="sxs-lookup"><span data-stu-id="bab55-103">Installer.LastErrorRecord method</span></span>

<span data-ttu-id="bab55-104">El método **LastErrorRecord** del objeto de [**instalador**](installer-object.md) devuelve un objeto de [**registro**](record-object.md) que contiene los parámetros de error del error más reciente de la función que generó el registro de errores.</span><span class="sxs-lookup"><span data-stu-id="bab55-104">The **LastErrorRecord** method of the [**Installer**](installer-object.md) object returns a [**Record**](record-object.md) object that contains error parameters for the most recent error from the function that produced the error record.</span></span>

## <a name="syntax"></a><span data-ttu-id="bab55-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bab55-105">Syntax</span></span>


```JScript
Installer.LastErrorRecord()
```



## <a name="parameters"></a><span data-ttu-id="bab55-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bab55-106">Parameters</span></span>

<span data-ttu-id="bab55-107">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="bab55-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bab55-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bab55-108">Return value</span></span>

<span data-ttu-id="bab55-109">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="bab55-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bab55-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bab55-110">Remarks</span></span>

<span data-ttu-id="bab55-111">El objeto de [**registro**](record-object.md) se restablece después de la ejecución de esta función de cualquier función que genera un registro de errores.</span><span class="sxs-lookup"><span data-stu-id="bab55-111">The [**Record**](record-object.md) object is reset after the execution of this function of any function that generates an error record.</span></span>

<span data-ttu-id="bab55-112">Solo las siguientes funciones designadas generan un registro de error:</span><span class="sxs-lookup"><span data-stu-id="bab55-112">Only the following designated functions generate an error record:</span></span>

-   [<span data-ttu-id="bab55-113">**Método OpenDatabase (objeto Installer)**</span><span class="sxs-lookup"><span data-stu-id="bab55-113">**OpenDatabase method (Installer Object)**</span></span>](installer-opendatabase.md)
-   [<span data-ttu-id="bab55-114">**Promete**</span><span class="sxs-lookup"><span data-stu-id="bab55-114">**Commit**</span></span>](database-commit.md)
-   [<span data-ttu-id="bab55-115">**AbrirVista**</span><span class="sxs-lookup"><span data-stu-id="bab55-115">**OpenView**</span></span>](database-openview.md)
-   [<span data-ttu-id="bab55-116">**Importar**</span><span class="sxs-lookup"><span data-stu-id="bab55-116">**Import**</span></span>](database-import.md)
-   [<span data-ttu-id="bab55-117">**Exportación**</span><span class="sxs-lookup"><span data-stu-id="bab55-117">**Export**</span></span>](database-export.md)
-   [<span data-ttu-id="bab55-118">**Sin**</span><span class="sxs-lookup"><span data-stu-id="bab55-118">**Merge**</span></span>](database-merge.md)
-   [<span data-ttu-id="bab55-119">**GenerateTransform**</span><span class="sxs-lookup"><span data-stu-id="bab55-119">**GenerateTransform**</span></span>](database-generatetransform.md)
-   [<span data-ttu-id="bab55-120">**ApplyTransform**</span><span class="sxs-lookup"><span data-stu-id="bab55-120">**ApplyTransform**</span></span>](database-applytransform.md)
-   [<span data-ttu-id="bab55-121">**Ejecut**</span><span class="sxs-lookup"><span data-stu-id="bab55-121">**Execute**</span></span>](view-execute.md)
-   [<span data-ttu-id="bab55-122">**Modificar**</span><span class="sxs-lookup"><span data-stu-id="bab55-122">**Modify**</span></span>](view-modify.md)
-   [<span data-ttu-id="bab55-123">**SetStream**</span><span class="sxs-lookup"><span data-stu-id="bab55-123">**SetStream**</span></span>](record-setstream.md)
-   [<span data-ttu-id="bab55-124">**SummaryInformation**</span><span class="sxs-lookup"><span data-stu-id="bab55-124">**SummaryInformation**</span></span>](database-summaryinformation.md)
-   [<span data-ttu-id="bab55-125">**SourcePath**</span><span class="sxs-lookup"><span data-stu-id="bab55-125">**SourcePath**</span></span>](session-sourcepath.md)
-   [<span data-ttu-id="bab55-126">**TargetPath**</span><span class="sxs-lookup"><span data-stu-id="bab55-126">**TargetPath**</span></span>](session-targetpath.md)
-   [<span data-ttu-id="bab55-127">**ComponentCurrentState**</span><span class="sxs-lookup"><span data-stu-id="bab55-127">**ComponentCurrentState**</span></span>](session-componentcurrentstate.md)
-   [<span data-ttu-id="bab55-128">**ComponentRequestState**</span><span class="sxs-lookup"><span data-stu-id="bab55-128">**ComponentRequestState**</span></span>](session-componentrequeststate.md)
-   [<span data-ttu-id="bab55-129">**FeatureCurrentState**</span><span class="sxs-lookup"><span data-stu-id="bab55-129">**FeatureCurrentState**</span></span>](session-featurecurrentstate.md)
-   [<span data-ttu-id="bab55-130">**FeatureRequestState**</span><span class="sxs-lookup"><span data-stu-id="bab55-130">**FeatureRequestState**</span></span>](session-featurerequeststate.md)
-   [<span data-ttu-id="bab55-131">**FeatureCost**</span><span class="sxs-lookup"><span data-stu-id="bab55-131">**FeatureCost**</span></span>](session-featurecost.md)
-   [<span data-ttu-id="bab55-132">**FeatureValidStates**</span><span class="sxs-lookup"><span data-stu-id="bab55-132">**FeatureValidStates**</span></span>](session-featurevalidstates.md)
-   [<span data-ttu-id="bab55-133">**SetInstallLevel**</span><span class="sxs-lookup"><span data-stu-id="bab55-133">**SetInstallLevel**</span></span>](session-setinstalllevel.md)

<span data-ttu-id="bab55-134">En el ejemplo siguiente de VBScript se usa una llamada a [**OpenDatabase**](installer-opendatabase.md) para mostrar cómo obtener información de error extendida de uno de los métodos o propiedades que admiten el método **LastErrorRecord** .</span><span class="sxs-lookup"><span data-stu-id="bab55-134">The following sample in VBScript uses a call to [**OpenDatabase**](installer-opendatabase.md) to show how to obtain extended error information from one of the methods or properties that support the **LastErrorRecord** method.</span></span> <span data-ttu-id="bab55-135">El ejemplo genera un mensaje de error cuando se produce un error en el método **OpenDatabase** .</span><span class="sxs-lookup"><span data-stu-id="bab55-135">The sample constructs an error message when the **OpenDatabase** method fails.</span></span> <span data-ttu-id="bab55-136">El objeto **Err** se usa para determinar si se encontró un error.</span><span class="sxs-lookup"><span data-stu-id="bab55-136">The **Err** object is used to determine whether an error was encountered.</span></span>


```VB
Const msiOpenDatabaseModeReadOnly     = 0

On Error Resume Next ' defer error handling

Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

' attempt to open the non-existent MSI database
Dim database
Set database = installer.OpenDatabase("c:\nonexistent.msi", msiOpenDatabaseModeReadOnly)

' test for error
If Err.Number <> 0 Then
    Dim message, errorRec
    message = Err.Source & " " & Hex(Err.Number) & ": " & Err.Description
    If Not installer Is Nothing Then
        ' try to obtain extended error info
        Set errorRec = installer.LastErrorRecord
        If Not errorRec Is Nothing Then message = message & vbNewLine & errorRec.FormatText
    End If

    MsgBox message

    ' PLACE ADDITIONAL SCRIPTING CODE HERE TO LOG AND/OR DISPLAY THE MESSAGE AND
    ' DETERMINE WHETHER TO CONTINUE PROCESSING ANYTHING ELSE
End If
```



## <a name="requirements"></a><span data-ttu-id="bab55-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bab55-137">Requirements</span></span>



| <span data-ttu-id="bab55-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="bab55-138">Requirement</span></span> | <span data-ttu-id="bab55-139">Value</span><span class="sxs-lookup"><span data-stu-id="bab55-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bab55-140">Versión</span><span class="sxs-lookup"><span data-stu-id="bab55-140">Version</span></span><br/> | <span data-ttu-id="bab55-141">Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bab55-141">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="bab55-142">Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bab55-142">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="bab55-143">Windows Installer en Windows Server 2003 o Windows XP</span><span class="sxs-lookup"><span data-stu-id="bab55-143">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="bab55-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bab55-144">DLL</span></span><br/>     | <dl> <span data-ttu-id="bab55-145"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bab55-145"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="bab55-146">IID</span><span class="sxs-lookup"><span data-stu-id="bab55-146">IID</span></span><br/>     | <span data-ttu-id="bab55-147">IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="bab55-147">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




