---
Description: Las constantes KNOWNFOLDERID representan los GUID que identifican las carpetas estándar registradas con el sistema como carpetas conocidas.
ms.assetid: f2c08ade-3083-44e4-82b0-dde45f0e3094
title: KNOWNFOLDERID (Knownfolders. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 97748d074d6b0982708f51ea679f0629e8abfad6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "104987433"
---
# <a name="knownfolderid"></a><span data-ttu-id="9cfe8-103">KNOWNFOLDERID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-103">KNOWNFOLDERID</span></span>

<span data-ttu-id="9cfe8-104">Las constantes **KNOWNFOLDERID** representan los GUID que identifican las carpetas estándar registradas con el sistema como [carpetas conocidas](known-folders.md).</span><span class="sxs-lookup"><span data-stu-id="9cfe8-104">The **KNOWNFOLDERID** constants represent GUIDs that identify standard folders registered with the system as [Known Folders](known-folders.md).</span></span> <span data-ttu-id="9cfe8-105">Estas carpetas se instalan con Windows Vista y sistemas operativos posteriores, y un equipo solo tendrá las carpetas adecuadas para su instalación.</span><span class="sxs-lookup"><span data-stu-id="9cfe8-105">These folders are installed with Windows Vista and later operating systems, and a computer will have only folders appropriate to it installed.</span></span> <span data-ttu-id="9cfe8-106">Para obtener descripciones de estas carpetas, consulte [**CSIDL**](csidl.md).</span><span class="sxs-lookup"><span data-stu-id="9cfe8-106">For descriptions of these folders, see [**CSIDL**](csidl.md).</span></span>

## <a name="example"></a><span data-ttu-id="9cfe8-107">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="9cfe8-107">Example</span></span>

```c
HRESULT CExplorerBrowserHostDialog::_FillViewWithKnownFolders(IResultsFolder *prf)
{
    IKnownFolderManager *pManager;
    HRESULT hr = CoCreateInstance(CLSID_KnownFolderManager, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pManager));
    if (SUCCEEDED(hr))
    {
        UINT cCount;
        KNOWNFOLDERID *pkfid;

        hr = pManager->GetFolderIds(&pkfid, &cCount);
        if (SUCCEEDED(hr))
        {
            for (UINT i = 0; i < cCount; i++)
            {
                IKnownFolder *pKnownFolder;
                hr = pManager->GetFolder(pkfid[i], &pKnownFolder);
                if (SUCCEEDED(hr))
                {
                    IShellItem *psi;
                    hr = pKnownFolder->GetShellItem(0, IID_PPV_ARGS(&psi));
                    if (SUCCEEDED(hr))
                    {
                        hr = prf->AddItem(psi);
                        psi->Release();
                    }
                    pKnownFolder->Release();
                }
            }
            CoTaskMemFree(pkfid);
        }
        pManager->Release();
    }
    return hr;
}

```

<span data-ttu-id="9cfe8-108">Ejemplo de [ejemplos clásicos de Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winui/shell/appplatform/ExplorerBrowserCustomContents/ExplorerBrowserCustomContents.cpp) en github.</span><span class="sxs-lookup"><span data-stu-id="9cfe8-108">Example from [Windows classic samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winui/shell/appplatform/ExplorerBrowserCustomContents/ExplorerBrowserCustomContents.cpp) on GitHub.</span></span>

## <a name="constants"></a><span data-ttu-id="9cfe8-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="9cfe8-109">Constants</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="9cfe8-110">Constante</span><span class="sxs-lookup"><span data-stu-id="9cfe8-110">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="9cfe8-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="9cfe8-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_AccountPictures"></span><span id="folderid_accountpictures"></span><span id="FOLDERID_ACCOUNTPICTURES"></span><dl> <span data-ttu-id="9cfe8-112"><dt><strong>FOLDERID_AccountPictures</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-112"><dt><strong>FOLDERID_AccountPictures</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-113">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-113">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-114">{008ca0b1-55b4-4c56-b8a8-4de4b299d3be}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-114">{008ca0b1-55b4-4c56-b8a8-4de4b299d3be}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-115">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-115">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-116">Imágenes de la cuenta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-116">Account Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-117">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-117">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-118">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-118">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-119">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-119">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-120">%APPDATA%\Microsoft\Windows\AccountPictures</span><span class="sxs-lookup"><span data-stu-id="9cfe8-120">%APPDATA%\Microsoft\Windows\AccountPictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-121">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-121">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-122">Ninguno, valor introducido en Windows 8</span><span class="sxs-lookup"><span data-stu-id="9cfe8-122">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-123">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-123">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-124">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-124">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-125">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-125">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-126">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-126">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_AddNewPrograms"></span><span id="folderid_addnewprograms"></span><span id="FOLDERID_ADDNEWPROGRAMS"></span><dl> <span data-ttu-id="9cfe8-127"><dt><strong>FOLDERID_AddNewPrograms</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-127"><dt><strong>FOLDERID_AddNewPrograms</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-128">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-128">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-129">{de61d971-5ebc-4f02-a3a9-6c82895e5c04}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-129">{de61d971-5ebc-4f02-a3a9-6c82895e5c04}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-130">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-130">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-131">Obtener programas</span><span class="sxs-lookup"><span data-stu-id="9cfe8-131">Get Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-132">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-132">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-133">Virtualiza</span><span class="sxs-lookup"><span data-stu-id="9cfe8-133">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-134">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-134">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-135">No aplicable: carpeta virtual</span><span class="sxs-lookup"><span data-stu-id="9cfe8-135">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-136">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-136">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-137">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9cfe8-137">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-138">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-138">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-139">Agregar nuevos programas (encontrados en el elemento <strong>Agregar o quitar programas</strong> del panel de control)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-139">Add New Programs (found in the <strong>Add or Remove Programs</strong> item in the Control Panel)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-140">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-140">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-141">No aplicable: carpeta virtual</span><span class="sxs-lookup"><span data-stu-id="9cfe8-141">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_AdminTools"></span><span id="folderid_admintools"></span><span id="FOLDERID_ADMINTOOLS"></span><dl> <span data-ttu-id="9cfe8-142"><dt><strong>FOLDERID_AdminTools</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-142"><dt><strong>FOLDERID_AdminTools</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-143">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-143">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-144">{724EF170-A42D-4FEF-9F26-B60E846FBA4F}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-144">{724EF170-A42D-4FEF-9F26-B60E846FBA4F}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-145">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-145">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-146">Herramientas administrativas</span><span class="sxs-lookup"><span data-stu-id="9cfe8-146">Administrative Tools</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-147">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-147">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-148">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-148">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-149">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-149">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-150">%APPDATA%\Microsoft\Windows\Start Inicio\Programas\Herramientas Tools</span><span class="sxs-lookup"><span data-stu-id="9cfe8-150">%APPDATA%\Microsoft\Windows\Start Menu\Programs\Administrative Tools</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-151">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-151">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-152">CSIDL_ADMINTOOLS</span><span class="sxs-lookup"><span data-stu-id="9cfe8-152">CSIDL_ADMINTOOLS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-153">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-153">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-154">Herramientas administrativas</span><span class="sxs-lookup"><span data-stu-id="9cfe8-154">Administrative Tools</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-155">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-155">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-156">%USERPROFILE%\Start Inicio\Programas\Herramientas Tools</span><span class="sxs-lookup"><span data-stu-id="9cfe8-156">%USERPROFILE%\Start Menu\Programs\Administrative Tools</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_AppDataDesktop"></span><span id="folderid_appdatadesktop"></span><span id="FOLDERID_APPDATADESKTOP"></span><dl> <span data-ttu-id="9cfe8-157"><dt><strong>FOLDERID_AppDataDesktop</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-157"><dt><strong>FOLDERID_AppDataDesktop</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-158">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-158">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-159">{B2C5E279-7ADD-439F-B28C-C41FE1BBF672}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-159">{B2C5E279-7ADD-439F-B28C-C41FE1BBF672}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-160">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-160">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-161">AppDataDesktop</span><span class="sxs-lookup"><span data-stu-id="9cfe8-161">AppDataDesktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-162">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-162">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-163">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-163">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-164">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-164">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-165">%LOCALAPPDATA%\Desktop</span><span class="sxs-lookup"><span data-stu-id="9cfe8-165">%LOCALAPPDATA%\Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-166">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-166">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-167">Ninguno, valor introducido en Windows 10, versión 1709</span><span class="sxs-lookup"><span data-stu-id="9cfe8-167">None, value introduced in Windows 10, version 1709</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-168">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-168">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-169">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-169">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-170">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-170">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-171">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-171">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="9cfe8-172">Las aplicaciones .NET usan internamente este FOLDERID para habilitar la funcionalidad de aplicaciones multiplataforma.</span><span class="sxs-lookup"><span data-stu-id="9cfe8-172">This FOLDERID is used internally by .NET applications to enable cross-platform app functionality.</span></span> <span data-ttu-id="9cfe8-173">No está diseñado para utilizarse directamente desde una aplicación.</span><span class="sxs-lookup"><span data-stu-id="9cfe8-173">It is not intended to be used directly from an application.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_AppDataDocuments"></span><span id="folderid_appdatadocuments"></span><span id="FOLDERID_APPDATADOCUMENTS"></span><dl> <span data-ttu-id="9cfe8-174"><dt><strong>FOLDERID_AppDataDocuments</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-174"><dt><strong>FOLDERID_AppDataDocuments</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-175">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-175">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-176">{7BE16610-1F7F-44AC-BFF0-83E15F2FFCA1}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-176">{7BE16610-1F7F-44AC-BFF0-83E15F2FFCA1}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-177">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-177">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-178">AppDataDocuments</span><span class="sxs-lookup"><span data-stu-id="9cfe8-178">AppDataDocuments</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-179">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-179">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-180">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-180">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-181">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-181">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-182">%LOCALAPPDATA%\Documents</span><span class="sxs-lookup"><span data-stu-id="9cfe8-182">%LOCALAPPDATA%\Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-183">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-183">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-184">Ninguno, valor introducido en Windows 10, versión 1709</span><span class="sxs-lookup"><span data-stu-id="9cfe8-184">None, value introduced in Windows 10, version 1709</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-185">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-185">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-186">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-186">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-187">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-187">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-188">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-188">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="9cfe8-189">Las aplicaciones .NET usan internamente este FOLDERID para habilitar la funcionalidad de aplicaciones multiplataforma.</span><span class="sxs-lookup"><span data-stu-id="9cfe8-189">This FOLDERID is used internally by .NET applications to enable cross-platform app functionality.</span></span> <span data-ttu-id="9cfe8-190">No está diseñado para utilizarse directamente desde una aplicación.</span><span class="sxs-lookup"><span data-stu-id="9cfe8-190">It is not intended to be used directly from an application.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_AppDataFavorites"></span><span id="folderid_appdatafavorites"></span><span id="FOLDERID_APPDATAFAVORITES"></span><dl> <span data-ttu-id="9cfe8-191"><dt><strong>FOLDERID_AppDataFavorites</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-191"><dt><strong>FOLDERID_AppDataFavorites</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-192">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-192">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-193">{7CFBEFBC-DE1F-45AA-B843-A542AC536CC9}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-193">{7CFBEFBC-DE1F-45AA-B843-A542AC536CC9}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-194">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-194">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-195">AppDataFavorites</span><span class="sxs-lookup"><span data-stu-id="9cfe8-195">AppDataFavorites</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-196">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-196">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-197">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-197">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-198">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-198">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-199">%LOCALAPPDATA%\Favorites</span><span class="sxs-lookup"><span data-stu-id="9cfe8-199">%LOCALAPPDATA%\Favorites</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-200">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-200">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-201">Ninguno, valor introducido en Windows 10, versión 1709</span><span class="sxs-lookup"><span data-stu-id="9cfe8-201">None, value introduced in Windows 10, version 1709</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-202">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-202">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-203">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-203">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-204">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-204">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-205">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-205">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="9cfe8-206">Las aplicaciones .NET usan internamente este FOLDERID para habilitar la funcionalidad de aplicaciones multiplataforma.</span><span class="sxs-lookup"><span data-stu-id="9cfe8-206">This FOLDERID is used internally by .NET applications to enable cross-platform app functionality.</span></span> <span data-ttu-id="9cfe8-207">No está diseñado para utilizarse directamente desde una aplicación.</span><span class="sxs-lookup"><span data-stu-id="9cfe8-207">It is not intended to be used directly from an application.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_AppDataProgramData"></span><span id="folderid_appdataprogramdata"></span><span id="FOLDERID_APPDATAPROGRAMDATA"></span><dl> <span data-ttu-id="9cfe8-208"><dt><strong>FOLDERID_AppDataProgramData</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-208"><dt><strong>FOLDERID_AppDataProgramData</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-209">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-209">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-210">{559D40A3-A036-40FA-AF61-84CB430A4D34}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-210">{559D40A3-A036-40FA-AF61-84CB430A4D34}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-211">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-211">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-212">AppDataProgramData</span><span class="sxs-lookup"><span data-stu-id="9cfe8-212">AppDataProgramData</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-213">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-213">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-214">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-214">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-215">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-215">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-216">%LOCALAPPDATA%\ProgramData</span><span class="sxs-lookup"><span data-stu-id="9cfe8-216">%LOCALAPPDATA%\ProgramData</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-217">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-217">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-218">Ninguno, valor introducido en Windows 10, versión 1709</span><span class="sxs-lookup"><span data-stu-id="9cfe8-218">None, value introduced in Windows 10, version 1709</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-219">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-219">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-220">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-220">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-221">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-221">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-222">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-222">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="9cfe8-223">Las aplicaciones .NET usan internamente este FOLDERID para habilitar la funcionalidad de aplicaciones multiplataforma.</span><span class="sxs-lookup"><span data-stu-id="9cfe8-223">This FOLDERID is used internally by .NET applications to enable cross-platform app functionality.</span></span> <span data-ttu-id="9cfe8-224">No está diseñado para utilizarse directamente desde una aplicación.</span><span class="sxs-lookup"><span data-stu-id="9cfe8-224">It is not intended to be used directly from an application.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ApplicationShortcuts"></span><span id="folderid_applicationshortcuts"></span><span id="FOLDERID_APPLICATIONSHORTCUTS"></span><dl> <span data-ttu-id="9cfe8-225"><dt><strong>FOLDERID_ApplicationShortcuts</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-225"><dt><strong>FOLDERID_ApplicationShortcuts</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-226">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-226">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-227">{A3918781-E5F2-4890-B3D9-A7E54332328C}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-227">{A3918781-E5F2-4890-B3D9-A7E54332328C}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-228">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-228">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-229">Métodos abreviados de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="9cfe8-229">Application Shortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-230">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-230">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-231">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-231">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-232">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-232">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-233">Métodos abreviados de%LOCALAPPDATA%\Microsoft\Windows\Application</span><span class="sxs-lookup"><span data-stu-id="9cfe8-233">%LOCALAPPDATA%\Microsoft\Windows\Application Shortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-234">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-234">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-235">Ninguno, valor introducido en Windows 8</span><span class="sxs-lookup"><span data-stu-id="9cfe8-235">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-236">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-236">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-237">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-237">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-238">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-238">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-239">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-239">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_AppsFolder"></span><span id="folderid_appsfolder"></span><span id="FOLDERID_APPSFOLDER"></span><dl> <span data-ttu-id="9cfe8-240"><dt><strong>FOLDERID_AppsFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-240"><dt><strong>FOLDERID_AppsFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-241">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-241">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-242">{1e87508d-89c2-42f0-8a7e-645a0f50ca58}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-242">{1e87508d-89c2-42f0-8a7e-645a0f50ca58}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-243">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-243">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-244">APLICACIONES</span><span class="sxs-lookup"><span data-stu-id="9cfe8-244">Applications</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-245">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-245">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-246">Virtualiza</span><span class="sxs-lookup"><span data-stu-id="9cfe8-246">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-247">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-247">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-248">No aplicable: carpeta virtual</span><span class="sxs-lookup"><span data-stu-id="9cfe8-248">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-249">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-249">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-250">Ninguno, valor introducido en Windows 8</span><span class="sxs-lookup"><span data-stu-id="9cfe8-250">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-251">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-251">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-252">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-252">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-253">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-253">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-254">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-254">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_AppUpdates"></span><span id="folderid_appupdates"></span><span id="FOLDERID_APPUPDATES"></span><dl> <span data-ttu-id="9cfe8-255"><dt><strong>FOLDERID_AppUpdates</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-255"><dt><strong>FOLDERID_AppUpdates</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-256">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-256">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-257">{a305ce99-f527-492b-8b1a-7e76fa98d6e4}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-257">{a305ce99-f527-492b-8b1a-7e76fa98d6e4}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-258">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-258">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-259">Actualizaciones instaladas</span><span class="sxs-lookup"><span data-stu-id="9cfe8-259">Installed Updates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-260">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-260">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-261">Virtualiza</span><span class="sxs-lookup"><span data-stu-id="9cfe8-261">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-262">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-262">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-263">No aplicable: carpeta virtual</span><span class="sxs-lookup"><span data-stu-id="9cfe8-263">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-264">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-264">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-265">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9cfe8-265">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-266">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-266">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-267">Ninguno, valor introducido en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9cfe8-267">None, value introduced in Windows Vista.</span></span> <span data-ttu-id="9cfe8-268">En versiones anteriores de Windows, la información de esta página se incluía en <strong>Agregar o quitar programas</strong> si la casilla <strong>Mostrar actualizaciones</strong> estaba activada.</span><span class="sxs-lookup"><span data-stu-id="9cfe8-268">In earlier versions of Windows, the information on this page was included in <strong>Add or Remove Programs</strong> if the <strong>Show updates</strong> box was checked.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-269">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-269">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-270">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-270">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_CameraRoll"></span><span id="folderid_cameraroll"></span><span id="FOLDERID_CAMERAROLL"></span><dl> <span data-ttu-id="9cfe8-271"><dt><strong>FOLDERID_CameraRoll</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-271"><dt><strong>FOLDERID_CameraRoll</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-272">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-272">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-273">{AB5FB87B-7CE2-4F83-915D-550846C9537B}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-273">{AB5FB87B-7CE2-4F83-915D-550846C9537B}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-274">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-274">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-275">Rollo de cámara</span><span class="sxs-lookup"><span data-stu-id="9cfe8-275">Camera Roll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-276">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-276">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-277">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-277">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-278">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-278">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-279">%USERPROFILE%\Pictures\Camera roll</span><span class="sxs-lookup"><span data-stu-id="9cfe8-279">%USERPROFILE%\Pictures\Camera Roll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-280">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-280">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-281">Ninguno, valor introducido en Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9cfe8-281">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-282">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-282">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-283">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-283">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-284">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-284">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-285">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-285">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_CDBurning"></span><span id="folderid_cdburning"></span><span id="FOLDERID_CDBURNING"></span><dl> <span data-ttu-id="9cfe8-286"><dt><strong>FOLDERID_CDBurning</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-286"><dt><strong>FOLDERID_CDBurning</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-287">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-287">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-288">{9E52AB10-F80D-49DF-ACB8-4330F5687855}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-288">{9E52AB10-F80D-49DF-ACB8-4330F5687855}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-289">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-289">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-290">Carpeta de grabación temporal</span><span class="sxs-lookup"><span data-stu-id="9cfe8-290">Temporary Burn Folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-291">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-291">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-292">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-292">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-293">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-293">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-294">%LOCALAPPDATA%\Microsoft\Windows\Burn\Burn</span><span class="sxs-lookup"><span data-stu-id="9cfe8-294">%LOCALAPPDATA%\Microsoft\Windows\Burn\Burn</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-295">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-295">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-296">CSIDL_CDBURN_AREA</span><span class="sxs-lookup"><span data-stu-id="9cfe8-296">CSIDL_CDBURN_AREA</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-297">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-297">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-298">Grabación de CD</span><span class="sxs-lookup"><span data-stu-id="9cfe8-298">CD Burning</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-299">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-299">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-300">%USERPROFILE%\Local Settings\Application Data\Microsoft\CD Burning</span><span class="sxs-lookup"><span data-stu-id="9cfe8-300">%USERPROFILE%\Local Settings\Application Data\Microsoft\CD Burning</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ChangeRemovePrograms"></span><span id="folderid_changeremoveprograms"></span><span id="FOLDERID_CHANGEREMOVEPROGRAMS"></span><dl> <span data-ttu-id="9cfe8-301"><dt><strong>FOLDERID_ChangeRemovePrograms</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-301"><dt><strong>FOLDERID_ChangeRemovePrograms</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-302">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-302">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-303">{df7266ac-9274-4867-8d55-3bd661de872d}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-303">{df7266ac-9274-4867-8d55-3bd661de872d}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-304">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-304">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-305">Programas y características</span><span class="sxs-lookup"><span data-stu-id="9cfe8-305">Programs and Features</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-306">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-306">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-307">Virtualiza</span><span class="sxs-lookup"><span data-stu-id="9cfe8-307">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-308">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-308">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-309">No aplicable: carpeta virtual</span><span class="sxs-lookup"><span data-stu-id="9cfe8-309">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-310">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-310">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-311">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9cfe8-311">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-312">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-312">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-313">Agregar o quitar programas</span><span class="sxs-lookup"><span data-stu-id="9cfe8-313">Add or Remove Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-314">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-314">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-315">No aplicable: carpeta virtual</span><span class="sxs-lookup"><span data-stu-id="9cfe8-315">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_CommonAdminTools"></span><span id="folderid_commonadmintools"></span><span id="FOLDERID_COMMONADMINTOOLS"></span><dl> <span data-ttu-id="9cfe8-316"><dt><strong>FOLDERID_CommonAdminTools</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-316"><dt><strong>FOLDERID_CommonAdminTools</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-317">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-317">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-318">{D0384E7D-BAC3-4797-8F14-CBA229B392B5}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-318">{D0384E7D-BAC3-4797-8F14-CBA229B392B5}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-319">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-319">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-320">Herramientas administrativas</span><span class="sxs-lookup"><span data-stu-id="9cfe8-320">Administrative Tools</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-321">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-321">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-322">NORMAL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-322">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-323">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-323">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-324">%ALLUSERSPROFILE%\Microsoft\Windows\Start Inicio\Programas\Herramientas Tools</span><span class="sxs-lookup"><span data-stu-id="9cfe8-324">%ALLUSERSPROFILE%\Microsoft\Windows\Start Menu\Programs\Administrative Tools</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-325">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-325">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-326">CSIDL_COMMON_ADMINTOOLS</span><span class="sxs-lookup"><span data-stu-id="9cfe8-326">CSIDL_COMMON_ADMINTOOLS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-327">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-327">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-328">Herramientas administrativas</span><span class="sxs-lookup"><span data-stu-id="9cfe8-328">Administrative Tools</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-329">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-329">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-330">% ALLUSERSPROFILE administrativas herramientas</span><span class="sxs-lookup"><span data-stu-id="9cfe8-330">%ALLUSERSPROFILE%\Start Menu\Programs\Administrative Tools</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_CommonOEMLinks"></span><span id="folderid_commonoemlinks"></span><span id="FOLDERID_COMMONOEMLINKS"></span><dl> <span data-ttu-id="9cfe8-331"><dt><strong>FOLDERID_CommonOEMLinks</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-331"><dt><strong>FOLDERID_CommonOEMLinks</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-332">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-332">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-333">{C1BAE2D0-10DF-4334-BEDD-7AA20B227A9D}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-333">{C1BAE2D0-10DF-4334-BEDD-7AA20B227A9D}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-334">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-334">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-335">Vínculos de OEM</span><span class="sxs-lookup"><span data-stu-id="9cfe8-335">OEM Links</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-336">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-336">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-337">NORMAL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-337">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-338">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-338">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-339">Vínculos de%ALLUSERSPROFILE%\OEM</span><span class="sxs-lookup"><span data-stu-id="9cfe8-339">%ALLUSERSPROFILE%\OEM Links</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-340">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-340">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-341">CSIDL_COMMON_OEM_LINKS</span><span class="sxs-lookup"><span data-stu-id="9cfe8-341">CSIDL_COMMON_OEM_LINKS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-342">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-342">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-343">Vínculos de OEM</span><span class="sxs-lookup"><span data-stu-id="9cfe8-343">OEM Links</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-344">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-344">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-345">Vínculos de%ALLUSERSPROFILE%\OEM</span><span class="sxs-lookup"><span data-stu-id="9cfe8-345">%ALLUSERSPROFILE%\OEM Links</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_CommonPrograms"></span><span id="folderid_commonprograms"></span><span id="FOLDERID_COMMONPROGRAMS"></span><dl> <span data-ttu-id="9cfe8-346"><dt><strong>FOLDERID_CommonPrograms</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-346"><dt><strong>FOLDERID_CommonPrograms</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-347">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-347">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-348">{0139D44E-6AFE-49F2-8690-3DAFCAE6FFB8}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-348">{0139D44E-6AFE-49F2-8690-3DAFCAE6FFB8}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-349">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-349">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-350">Programas</span><span class="sxs-lookup"><span data-stu-id="9cfe8-350">Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-351">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-351">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-352">NORMAL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-352">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-353">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-353">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-354">%ALLUSERSPROFILE%\Microsoft\Windows\Start Menu\Programs</span><span class="sxs-lookup"><span data-stu-id="9cfe8-354">%ALLUSERSPROFILE%\Microsoft\Windows\Start Menu\Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-355">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-355">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-356">CSIDL_COMMON_PROGRAMS</span><span class="sxs-lookup"><span data-stu-id="9cfe8-356">CSIDL_COMMON_PROGRAMS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-357">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-357">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-358">Programas</span><span class="sxs-lookup"><span data-stu-id="9cfe8-358">Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-359">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-359">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-360">Inicio\programas</span><span class="sxs-lookup"><span data-stu-id="9cfe8-360">%ALLUSERSPROFILE%\Start Menu\Programs</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_CommonStartMenu"></span><span id="folderid_commonstartmenu"></span><span id="FOLDERID_COMMONSTARTMENU"></span><dl> <span data-ttu-id="9cfe8-361"><dt><strong>FOLDERID_CommonStartMenu</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-361"><dt><strong>FOLDERID_CommonStartMenu</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-362">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-362">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-363">{A4115719-D62E-491D-AA7C-E74B8BE3B067}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-363">{A4115719-D62E-491D-AA7C-E74B8BE3B067}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-364">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-364">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-365">Menú Inicio</span><span class="sxs-lookup"><span data-stu-id="9cfe8-365">Start Menu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-366">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-366">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-367">NORMAL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-367">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-368">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-368">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-369">Menú%ALLUSERSPROFILE%\Microsoft\Windows\Start</span><span class="sxs-lookup"><span data-stu-id="9cfe8-369">%ALLUSERSPROFILE%\Microsoft\Windows\Start Menu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-370">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-370">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-371">CSIDL_COMMON_STARTMENU</span><span class="sxs-lookup"><span data-stu-id="9cfe8-371">CSIDL_COMMON_STARTMENU</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-372">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-372">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-373">Menú Inicio</span><span class="sxs-lookup"><span data-stu-id="9cfe8-373">Start Menu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-374">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-374">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-375">Menú% ALLUSERSPROFILE</span><span class="sxs-lookup"><span data-stu-id="9cfe8-375">%ALLUSERSPROFILE%\Start Menu</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_CommonStartup"></span><span id="folderid_commonstartup"></span><span id="FOLDERID_COMMONSTARTUP"></span><dl> <span data-ttu-id="9cfe8-376"><dt><strong>FOLDERID_CommonStartup</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-376"><dt><strong>FOLDERID_CommonStartup</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-377">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-377">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-378">{82A5EA35-D9CD-47C5-9629-E15D2F714E6E}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-378">{82A5EA35-D9CD-47C5-9629-E15D2F714E6E}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-379">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-379">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-380">Inicio</span><span class="sxs-lookup"><span data-stu-id="9cfe8-380">Startup</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-381">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-381">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-382">NORMAL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-382">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-383">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-383">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-384">%ALLUSERSPROFILE%\Microsoft\Windows\Start Inicio\programas\inicio</span><span class="sxs-lookup"><span data-stu-id="9cfe8-384">%ALLUSERSPROFILE%\Microsoft\Windows\Start Menu\Programs\StartUp</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-385">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-385">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-386">CSIDL_COMMON_STARTUP, CSIDL_COMMON_ALTSTARTUP</span><span class="sxs-lookup"><span data-stu-id="9cfe8-386">CSIDL_COMMON_STARTUP, CSIDL_COMMON_ALTSTARTUP</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-387">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-387">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-388">Inicio</span><span class="sxs-lookup"><span data-stu-id="9cfe8-388">Startup</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-389">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-389">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-390">Inicio\programas\inicio</span><span class="sxs-lookup"><span data-stu-id="9cfe8-390">%ALLUSERSPROFILE%\Start Menu\Programs\StartUp</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_CommonTemplates"></span><span id="folderid_commontemplates"></span><span id="FOLDERID_COMMONTEMPLATES"></span><dl> <span data-ttu-id="9cfe8-391"><dt><strong>FOLDERID_CommonTemplates</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-391"><dt><strong>FOLDERID_CommonTemplates</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-392">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-392">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-393">{B94237E7-57AC-4347-9151-B08C6C32D1F7}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-393">{B94237E7-57AC-4347-9151-B08C6C32D1F7}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-394">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-394">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-395">Plantillas</span><span class="sxs-lookup"><span data-stu-id="9cfe8-395">Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-396">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-396">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-397">NORMAL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-397">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-398">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-398">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-399">%ALLUSERSPROFILE%\Microsoft\Windows\Templates</span><span class="sxs-lookup"><span data-stu-id="9cfe8-399">%ALLUSERSPROFILE%\Microsoft\Windows\Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-400">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-400">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-401">CSIDL_COMMON_TEMPLATES</span><span class="sxs-lookup"><span data-stu-id="9cfe8-401">CSIDL_COMMON_TEMPLATES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-402">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-402">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-403">Plantillas</span><span class="sxs-lookup"><span data-stu-id="9cfe8-403">Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-404">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-404">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-405">%ALLUSERSPROFILE%\Templates</span><span class="sxs-lookup"><span data-stu-id="9cfe8-405">%ALLUSERSPROFILE%\Templates</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ComputerFolder"></span><span id="folderid_computerfolder"></span><span id="FOLDERID_COMPUTERFOLDER"></span><dl> <span data-ttu-id="9cfe8-406"><dt><strong>FOLDERID_ComputerFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-406"><dt><strong>FOLDERID_ComputerFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-407">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-407">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-408">{0AC0837C-BBF8-452A-850D-79D08E667CA7}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-408">{0AC0837C-BBF8-452A-850D-79D08E667CA7}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-409">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-409">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-410">Computer</span><span class="sxs-lookup"><span data-stu-id="9cfe8-410">Computer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-411">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-411">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-412">Virtualiza</span><span class="sxs-lookup"><span data-stu-id="9cfe8-412">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-413">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-413">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-414">No aplicable: carpeta virtual</span><span class="sxs-lookup"><span data-stu-id="9cfe8-414">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-415">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-415">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-416">CSIDL_DRIVES</span><span class="sxs-lookup"><span data-stu-id="9cfe8-416">CSIDL_DRIVES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-417">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-417">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-418">Mi PC</span><span class="sxs-lookup"><span data-stu-id="9cfe8-418">My Computer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-419">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-419">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-420">No aplicable: carpeta virtual</span><span class="sxs-lookup"><span data-stu-id="9cfe8-420">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ConflictFolder"></span><span id="folderid_conflictfolder"></span><span id="FOLDERID_CONFLICTFOLDER"></span><dl> <span data-ttu-id="9cfe8-421"><dt><strong>FOLDERID_ConflictFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-421"><dt><strong>FOLDERID_ConflictFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-422">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-422">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-423">{4bfefb45-347d-4006-a5be-ac0cb0567192}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-423">{4bfefb45-347d-4006-a5be-ac0cb0567192}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-424">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-424">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-425">Conflictos</span><span class="sxs-lookup"><span data-stu-id="9cfe8-425">Conflicts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-426">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-426">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-427">Virtualiza</span><span class="sxs-lookup"><span data-stu-id="9cfe8-427">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-428">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-428">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-429">No aplicable: carpeta virtual</span><span class="sxs-lookup"><span data-stu-id="9cfe8-429">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-430">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-430">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-431">Ninguno, valor introducido en Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9cfe8-431">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-432">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-432">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-433">No es aplicable.</span><span class="sxs-lookup"><span data-stu-id="9cfe8-433">Not applicable.</span></span> <span data-ttu-id="9cfe8-434">Este <strong>KNOWNFOLDERID</strong> hace referencia al administrador de sincronización de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9cfe8-434">This <strong>KNOWNFOLDERID</strong> refers to the Windows Vista Synchronization Manager.</span></span> <span data-ttu-id="9cfe8-435">No es la carpeta a la que hace referencia el <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictfolder"><strong>ISyncMgrConflictFolder</strong></a>anterior.</span><span class="sxs-lookup"><span data-stu-id="9cfe8-435">It is not the folder referenced by the older <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictfolder"><strong>ISyncMgrConflictFolder</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-436">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-436">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-437">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-437">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ConnectionsFolder"></span><span id="folderid_connectionsfolder"></span><span id="FOLDERID_CONNECTIONSFOLDER"></span><dl> <span data-ttu-id="9cfe8-438"><dt><strong>FOLDERID_ConnectionsFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-438"><dt><strong>FOLDERID_ConnectionsFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-439">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-439">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-440">{6F0CD92B-2E97-45D1-88FF-B0D186B8DEDD}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-440">{6F0CD92B-2E97-45D1-88FF-B0D186B8DEDD}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-441">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-441">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-442">Conexiones de red</span><span class="sxs-lookup"><span data-stu-id="9cfe8-442">Network Connections</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-443">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-443">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-444">Virtualiza</span><span class="sxs-lookup"><span data-stu-id="9cfe8-444">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-445">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-445">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-446">No aplicable: carpeta virtual</span><span class="sxs-lookup"><span data-stu-id="9cfe8-446">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-447">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-447">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-448">CSIDL_CONNECTIONS</span><span class="sxs-lookup"><span data-stu-id="9cfe8-448">CSIDL_CONNECTIONS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-449">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-449">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-450">Conexiones de red</span><span class="sxs-lookup"><span data-stu-id="9cfe8-450">Network Connections</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-451">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-451">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-452">No aplicable: carpeta virtual</span><span class="sxs-lookup"><span data-stu-id="9cfe8-452">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Contacts"></span><span id="folderid_contacts"></span><span id="FOLDERID_CONTACTS"></span><dl> <span data-ttu-id="9cfe8-453"><dt><strong>FOLDERID_Contacts</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-453"><dt><strong>FOLDERID_Contacts</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-454">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-454">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-455">{56784854-C6CB-462b-8169-88E350ACB882}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-455">{56784854-C6CB-462b-8169-88E350ACB882}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-456">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-456">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-457">Contactos</span><span class="sxs-lookup"><span data-stu-id="9cfe8-457">Contacts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-458">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-458">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-459">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-459">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-460">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-460">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-461">%USERPROFILE%\Contacts</span><span class="sxs-lookup"><span data-stu-id="9cfe8-461">%USERPROFILE%\Contacts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-462">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-462">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-463">Ninguno, valor introducido en Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9cfe8-463">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-464">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-464">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-465">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-465">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-466">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-466">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-467">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-467">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ControlPanelFolder"></span><span id="folderid_controlpanelfolder"></span><span id="FOLDERID_CONTROLPANELFOLDER"></span><dl> <span data-ttu-id="9cfe8-468"><dt><strong>FOLDERID_ControlPanelFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-468"><dt><strong>FOLDERID_ControlPanelFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-469">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-469">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-470">{82A74AEB-AEB4-465C-A014-D097EE346D63}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-470">{82A74AEB-AEB4-465C-A014-D097EE346D63}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-471">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-471">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-472">Panel de control</span><span class="sxs-lookup"><span data-stu-id="9cfe8-472">Control Panel</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-473">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-473">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-474">Virtualiza</span><span class="sxs-lookup"><span data-stu-id="9cfe8-474">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-475">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-475">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-476">No aplicable: carpeta virtual</span><span class="sxs-lookup"><span data-stu-id="9cfe8-476">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-477">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-477">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-478">CSIDL_CONTROLS</span><span class="sxs-lookup"><span data-stu-id="9cfe8-478">CSIDL_CONTROLS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-479">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-479">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-480">Panel de control</span><span class="sxs-lookup"><span data-stu-id="9cfe8-480">Control Panel</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-481">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-481">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-482">No aplicable: carpeta virtual</span><span class="sxs-lookup"><span data-stu-id="9cfe8-482">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Cookies"></span><span id="folderid_cookies"></span><span id="FOLDERID_COOKIES"></span><dl> <span data-ttu-id="9cfe8-483"><dt><strong>FOLDERID_Cookies</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-483"><dt><strong>FOLDERID_Cookies</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-484">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-484">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-485">{2B0F765D-C0E9-4171-908E-08A611B84FF6}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-485">{2B0F765D-C0E9-4171-908E-08A611B84FF6}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-486">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-486">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-487">Cookies</span><span class="sxs-lookup"><span data-stu-id="9cfe8-487">Cookies</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-488">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-488">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-489">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-489">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-490">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-490">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-491">%APPDATA%\Microsoft\Windows\Cookies</span><span class="sxs-lookup"><span data-stu-id="9cfe8-491">%APPDATA%\Microsoft\Windows\Cookies</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-492">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-492">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-493">CSIDL_COOKIES</span><span class="sxs-lookup"><span data-stu-id="9cfe8-493">CSIDL_COOKIES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-494">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-494">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-495">Cookies</span><span class="sxs-lookup"><span data-stu-id="9cfe8-495">Cookies</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-496">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-496">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-497">%USERPROFILE%\Cookies</span><span class="sxs-lookup"><span data-stu-id="9cfe8-497">%USERPROFILE%\Cookies</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Desktop"></span><span id="folderid_desktop"></span><span id="FOLDERID_DESKTOP"></span><dl> <span data-ttu-id="9cfe8-498"><dt><strong>FOLDERID_Desktop</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-498"><dt><strong>FOLDERID_Desktop</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-499">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-499">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-500">{B4BFCC3A-DB2C-424C-B029-7FE99A87C641}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-500">{B4BFCC3A-DB2C-424C-B029-7FE99A87C641}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-501">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-501">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-502">Escritorio</span><span class="sxs-lookup"><span data-stu-id="9cfe8-502">Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-503">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-503">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-504">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-504">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-505">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-505">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-506">%USERPROFILE%\Desktop</span><span class="sxs-lookup"><span data-stu-id="9cfe8-506">%USERPROFILE%\Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-507">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-507">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-508">CSIDL_DESKTOP, CSIDL_DESKTOPDIRECTORY</span><span class="sxs-lookup"><span data-stu-id="9cfe8-508">CSIDL_DESKTOP, CSIDL_DESKTOPDIRECTORY</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-509">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-509">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-510">Escritorio</span><span class="sxs-lookup"><span data-stu-id="9cfe8-510">Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-511">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-511">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-512">%USERPROFILE%\Desktop</span><span class="sxs-lookup"><span data-stu-id="9cfe8-512">%USERPROFILE%\Desktop</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_DeviceMetadataStore"></span><span id="folderid_devicemetadatastore"></span><span id="FOLDERID_DEVICEMETADATASTORE"></span><dl> <span data-ttu-id="9cfe8-513"><dt><strong>FOLDERID_DeviceMetadataStore</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-513"><dt><strong>FOLDERID_DeviceMetadataStore</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-514">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-514">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-515">{5CE4A5E9-E4EB-479D-B89F-130C02886155}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-515">{5CE4A5E9-E4EB-479D-B89F-130C02886155}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-516">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-516">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-517">DeviceMetadataStore</span><span class="sxs-lookup"><span data-stu-id="9cfe8-517">DeviceMetadataStore</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-518">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-518">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-519">NORMAL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-519">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-520">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-520">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-521">%ALLUSERSPROFILE%\Microsoft\Windows\DeviceMetadataStore</span><span class="sxs-lookup"><span data-stu-id="9cfe8-521">%ALLUSERSPROFILE%\Microsoft\Windows\DeviceMetadataStore</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-522">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-522">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-523">Ninguno, valor introducido en Windows 7</span><span class="sxs-lookup"><span data-stu-id="9cfe8-523">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-524">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-524">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-525">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-525">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-526">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-526">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-527">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-527">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Documents"></span><span id="folderid_documents"></span><span id="FOLDERID_DOCUMENTS"></span><dl> <span data-ttu-id="9cfe8-528"><dt><strong>FOLDERID_Documents</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-528"><dt><strong>FOLDERID_Documents</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-529">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-529">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-530">{FDD39AD0-238F-46AF-ADB4-6C85480369C7}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-530">{FDD39AD0-238F-46AF-ADB4-6C85480369C7}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-531">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-531">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-532">Documentos</span><span class="sxs-lookup"><span data-stu-id="9cfe8-532">Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-533">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-533">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-534">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-534">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-535">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-535">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-536">%USERPROFILE%\Documents</span><span class="sxs-lookup"><span data-stu-id="9cfe8-536">%USERPROFILE%\Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-537">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-537">CSIDL Equivalents</span></span></td>
<td><span data-ttu-id="9cfe8-538">CSIDL_MYDOCUMENTS, CSIDL_PERSONAL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-538">CSIDL_MYDOCUMENTS, CSIDL_PERSONAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-539">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-539">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-540">Mis documentos</span><span class="sxs-lookup"><span data-stu-id="9cfe8-540">My Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-541">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-541">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-542">Documentos de%USERPROFILE%\My</span><span class="sxs-lookup"><span data-stu-id="9cfe8-542">%USERPROFILE%\My Documents</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_DocumentsLibrary"></span><span id="folderid_documentslibrary"></span><span id="FOLDERID_DOCUMENTSLIBRARY"></span><dl> <span data-ttu-id="9cfe8-543"><dt><strong>FOLDERID_DocumentsLibrary</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-543"><dt><strong>FOLDERID_DocumentsLibrary</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-544">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-544">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-545">{7B0DB17D-9CD2-4A93-9733-46CC89022E7C}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-545">{7B0DB17D-9CD2-4A93-9733-46CC89022E7C}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-546">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-546">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-547">Documentos</span><span class="sxs-lookup"><span data-stu-id="9cfe8-547">Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-548">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-548">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-549">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-549">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-550">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-550">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-551">%APPDATA%\Microsoft\Windows\Libraries\Documents.library-ms</span><span class="sxs-lookup"><span data-stu-id="9cfe8-551">%APPDATA%\Microsoft\Windows\Libraries\Documents.library-ms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-552">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-552">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-553">Ninguno, valor introducido en Windows 7</span><span class="sxs-lookup"><span data-stu-id="9cfe8-553">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-554">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-554">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-555">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-555">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-556">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-556">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-557">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-557">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Downloads"></span><span id="folderid_downloads"></span><span id="FOLDERID_DOWNLOADS"></span><dl> <span data-ttu-id="9cfe8-558"><dt><strong>FOLDERID_Downloads</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-558"><dt><strong>FOLDERID_Downloads</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-559">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-559">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-560">{374DE290-123F-4565-9164-39C4925E467B}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-560">{374DE290-123F-4565-9164-39C4925E467B}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-561">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-561">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-562">Descargas</span><span class="sxs-lookup"><span data-stu-id="9cfe8-562">Downloads</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-563">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-563">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-564">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-564">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-565">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-565">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-566">%USERPROFILE%\Downloads</span><span class="sxs-lookup"><span data-stu-id="9cfe8-566">%USERPROFILE%\Downloads</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-567">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-567">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-568">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9cfe8-568">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-569">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-569">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-570">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-570">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-571">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-571">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-572">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-572">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Favorites"></span><span id="folderid_favorites"></span><span id="FOLDERID_FAVORITES"></span><dl> <span data-ttu-id="9cfe8-573"><dt><strong>FOLDERID_Favorites</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-573"><dt><strong>FOLDERID_Favorites</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-574">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-574">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-575">{1777F761-68AD-4D8A-87BD-30B759FA33DD}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-575">{1777F761-68AD-4D8A-87BD-30B759FA33DD}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-576">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-576">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-577">Favoritos</span><span class="sxs-lookup"><span data-stu-id="9cfe8-577">Favorites</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-578">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-578">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-579">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-579">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-580">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-580">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-581">%USERPROFILE%\Favorites</span><span class="sxs-lookup"><span data-stu-id="9cfe8-581">%USERPROFILE%\Favorites</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-582">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-582">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-583">CSIDL_FAVORITES, CSIDL_COMMON_FAVORITES</span><span class="sxs-lookup"><span data-stu-id="9cfe8-583">CSIDL_FAVORITES, CSIDL_COMMON_FAVORITES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-584">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-584">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-585">Favoritos</span><span class="sxs-lookup"><span data-stu-id="9cfe8-585">Favorites</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-586">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-586">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-587">%USERPROFILE%\Favorites</span><span class="sxs-lookup"><span data-stu-id="9cfe8-587">%USERPROFILE%\Favorites</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Fonts"></span><span id="folderid_fonts"></span><span id="FOLDERID_FONTS"></span><dl> <span data-ttu-id="9cfe8-588"><dt><strong>FOLDERID_Fonts</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-588"><dt><strong>FOLDERID_Fonts</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-589">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-589">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-590">{FD228CB7-AE11-4AE3-864C-16F3910AB8FE}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-590">{FD228CB7-AE11-4AE3-864C-16F3910AB8FE}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-591">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-591">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-592">Fuentes</span><span class="sxs-lookup"><span data-stu-id="9cfe8-592">Fonts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-593">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-593">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-594">FIXED</span><span class="sxs-lookup"><span data-stu-id="9cfe8-594">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-595">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-595">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-596">%windir%\Fonts</span><span class="sxs-lookup"><span data-stu-id="9cfe8-596">%windir%\Fonts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-597">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-597">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-598">CSIDL_FONTS</span><span class="sxs-lookup"><span data-stu-id="9cfe8-598">CSIDL_FONTS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-599">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-599">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-600">Fuentes</span><span class="sxs-lookup"><span data-stu-id="9cfe8-600">Fonts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-601">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-601">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-602">%windir%\Fonts</span><span class="sxs-lookup"><span data-stu-id="9cfe8-602">%windir%\Fonts</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Games"></span><span id="folderid_games"></span><span id="FOLDERID_GAMES"></span><dl> <span data-ttu-id="9cfe8-603"><dt><strong>FOLDERID_Games</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-603"><dt><strong>FOLDERID_Games</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="9cfe8-604">Este FOLDERID está en desuso en Windows 10, versión 1803 y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="9cfe8-604">This FOLDERID is deprecated in Windows 10, version 1803 and later versions.</span></span> <span data-ttu-id="9cfe8-605">En estas versiones, devuelve <strong>0x80070057-E_INVALIDARG</strong>
</span><span class="sxs-lookup"><span data-stu-id="9cfe8-605">In these versions, it returns <strong>0x80070057 - E_INVALIDARG</strong>
</span></span></blockquote>
</div>
<div>
 
</div>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-606">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-606">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-607">{CAC52C1A-B53D-4edc-92D7-6B2E8AC19434}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-607">{CAC52C1A-B53D-4edc-92D7-6B2E8AC19434}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-608">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-608">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-609">Juegos</span><span class="sxs-lookup"><span data-stu-id="9cfe8-609">Games</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-610">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-610">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-611">Virtualiza</span><span class="sxs-lookup"><span data-stu-id="9cfe8-611">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-612">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-612">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-613">No aplicable: carpeta virtual</span><span class="sxs-lookup"><span data-stu-id="9cfe8-613">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-614">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-614">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-615">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9cfe8-615">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-616">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-616">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-617">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-617">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-618">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-618">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-619">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-619">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_GameTasks"></span><span id="folderid_gametasks"></span><span id="FOLDERID_GAMETASKS"></span><dl> <span data-ttu-id="9cfe8-620"><dt><strong>FOLDERID_GameTasks</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-620"><dt><strong>FOLDERID_GameTasks</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-621">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-621">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-622">{054FAE61-4DD8-4787-80B6-090220C4B700}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-622">{054FAE61-4DD8-4787-80B6-090220C4B700}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-623">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-623">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-624">GameExplorer</span><span class="sxs-lookup"><span data-stu-id="9cfe8-624">GameExplorer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-625">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-625">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-626">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-626">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-627">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-627">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-628">%LOCALAPPDATA%\Microsoft\Windows\GameExplorer</span><span class="sxs-lookup"><span data-stu-id="9cfe8-628">%LOCALAPPDATA%\Microsoft\Windows\GameExplorer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-629">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-629">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-630">Ninguno, valor introducido en Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9cfe8-630">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-631">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-631">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-632">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-632">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-633">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-633">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-634">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-634">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_History"></span><span id="folderid_history"></span><span id="FOLDERID_HISTORY"></span><dl> <span data-ttu-id="9cfe8-635"><dt><strong>FOLDERID_History</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-635"><dt><strong>FOLDERID_History</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-636">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-636">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-637">{D9DC8A3B-B784-432E-A781-5A1130A75963}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-637">{D9DC8A3B-B784-432E-A781-5A1130A75963}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-638">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-638">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-639">Historial</span><span class="sxs-lookup"><span data-stu-id="9cfe8-639">History</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-640">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-640">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-641">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-641">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-642">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-642">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-643">%LOCALAPPDATA%\Microsoft\Windows\History</span><span class="sxs-lookup"><span data-stu-id="9cfe8-643">%LOCALAPPDATA%\Microsoft\Windows\History</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-644">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-644">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-645">CSIDL_HISTORY</span><span class="sxs-lookup"><span data-stu-id="9cfe8-645">CSIDL_HISTORY</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-646">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-646">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-647">Historial</span><span class="sxs-lookup"><span data-stu-id="9cfe8-647">History</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-648">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-648">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-649">%USERPROFILE%\Local Settings\History</span><span class="sxs-lookup"><span data-stu-id="9cfe8-649">%USERPROFILE%\Local Settings\History</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_HomeGroup"></span><span id="folderid_homegroup"></span><span id="FOLDERID_HOMEGROUP"></span><dl> <span data-ttu-id="9cfe8-650"><dt><strong>FOLDERID_HomeGroup</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-650"><dt><strong>FOLDERID_HomeGroup</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-651">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-651">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-652">{52528A6B-B9E3-4ADD-B60D-588C2DBA842D}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-652">{52528A6B-B9E3-4ADD-B60D-588C2DBA842D}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-653">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-653">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-654">Grupo en el hogar</span><span class="sxs-lookup"><span data-stu-id="9cfe8-654">Homegroup</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-655">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-655">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-656">Virtualiza</span><span class="sxs-lookup"><span data-stu-id="9cfe8-656">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-657">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-657">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-658">No aplicable: carpeta virtual</span><span class="sxs-lookup"><span data-stu-id="9cfe8-658">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-659">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-659">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-660">Ninguno, valor introducido en Windows 7</span><span class="sxs-lookup"><span data-stu-id="9cfe8-660">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-661">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-661">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-662">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-662">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-663">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-663">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-664">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-664">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_HomeGroupCurrentUser"></span><span id="folderid_homegroupcurrentuser"></span><span id="FOLDERID_HOMEGROUPCURRENTUSER"></span><dl> <span data-ttu-id="9cfe8-665"><dt><strong>FOLDERID_HomeGroupCurrentUser</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-665"><dt><strong>FOLDERID_HomeGroupCurrentUser</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-666">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-666">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-667">{9B74B6A3-0DFD-4f11-9E78-5F7800F2E772}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-667">{9B74B6A3-0DFD-4f11-9E78-5F7800F2E772}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-668">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-668">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-669">El nombre de usuario (% USERNAME%)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-669">The user's username (%USERNAME%)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-670">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-670">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-671">Virtualiza</span><span class="sxs-lookup"><span data-stu-id="9cfe8-671">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-672">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-672">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-673">No aplicable: carpeta virtual</span><span class="sxs-lookup"><span data-stu-id="9cfe8-673">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-674">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-674">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-675">Ninguno, valor introducido en Windows 8</span><span class="sxs-lookup"><span data-stu-id="9cfe8-675">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-676">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-676">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-677">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-677">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-678">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-678">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-679">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-679">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ImplicitAppShortcuts"></span><span id="folderid_implicitappshortcuts"></span><span id="FOLDERID_IMPLICITAPPSHORTCUTS"></span><dl> <span data-ttu-id="9cfe8-680"><dt><strong>FOLDERID_ImplicitAppShortcuts</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-680"><dt><strong>FOLDERID_ImplicitAppShortcuts</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-681">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-681">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-682">{BCB5256F-79F6-4CEE-B725-DC34E402FD46}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-682">{BCB5256F-79F6-4CEE-B725-DC34E402FD46}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-683">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-683">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-684">ImplicitAppShortcuts</span><span class="sxs-lookup"><span data-stu-id="9cfe8-684">ImplicitAppShortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-685">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-685">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-686">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-686">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-687">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-687">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-688">%APPDATA%\Microsoft\Internet Explorer\Quick Launch\User Pinned\ImplicitAppShortcuts</span><span class="sxs-lookup"><span data-stu-id="9cfe8-688">%APPDATA%\Microsoft\Internet Explorer\Quick Launch\User Pinned\ImplicitAppShortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-689">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-689">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-690">Ninguno, valor introducido en Windows 7</span><span class="sxs-lookup"><span data-stu-id="9cfe8-690">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-691">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-691">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-692">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-692">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-693">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-693">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-694">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-694">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_InternetCache"></span><span id="folderid_internetcache"></span><span id="FOLDERID_INTERNETCACHE"></span><dl> <span data-ttu-id="9cfe8-695"><dt><strong>FOLDERID_InternetCache</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-695"><dt><strong>FOLDERID_InternetCache</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-696">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-696">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-697">{352481E8-33BE-4251-BA85-6007CAEDCF9D}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-697">{352481E8-33BE-4251-BA85-6007CAEDCF9D}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-698">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-698">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-699">Archivos temporales de Internet</span><span class="sxs-lookup"><span data-stu-id="9cfe8-699">Temporary Internet Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-700">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-700">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-701">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-701">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-702">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-702">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-703">%LOCALAPPDATA%\Microsoft\Windows\Temporary de archivos de Internet</span><span class="sxs-lookup"><span data-stu-id="9cfe8-703">%LOCALAPPDATA%\Microsoft\Windows\Temporary Internet Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-704">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-704">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-705">CSIDL_INTERNET_CACHE</span><span class="sxs-lookup"><span data-stu-id="9cfe8-705">CSIDL_INTERNET_CACHE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-706">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-706">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-707">Archivos temporales de Internet</span><span class="sxs-lookup"><span data-stu-id="9cfe8-707">Temporary Internet Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-708">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-708">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-709">% Userprofile archivos de Settings\Temporary de Internet</span><span class="sxs-lookup"><span data-stu-id="9cfe8-709">%USERPROFILE%\Local Settings\Temporary Internet Files</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_InternetFolder"></span><span id="folderid_internetfolder"></span><span id="FOLDERID_INTERNETFOLDER"></span><dl> <span data-ttu-id="9cfe8-710"><dt><strong>FOLDERID_InternetFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-710"><dt><strong>FOLDERID_InternetFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-711">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-711">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-712">{4D9F7874-4E0C-4904-967B-40B0D20C3E4B}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-712">{4D9F7874-4E0C-4904-967B-40B0D20C3E4B}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-713">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-713">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-714">Internet</span><span class="sxs-lookup"><span data-stu-id="9cfe8-714">The Internet</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-715">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-715">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-716">Virtualiza</span><span class="sxs-lookup"><span data-stu-id="9cfe8-716">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-717">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-717">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-718">No aplicable: carpeta virtual</span><span class="sxs-lookup"><span data-stu-id="9cfe8-718">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-719">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-719">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-720">CSIDL_INTERNET</span><span class="sxs-lookup"><span data-stu-id="9cfe8-720">CSIDL_INTERNET</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-721">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-721">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-722">Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="9cfe8-722">Internet Explorer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-723">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-723">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-724">No aplicable: carpeta virtual</span><span class="sxs-lookup"><span data-stu-id="9cfe8-724">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Libraries"></span><span id="folderid_libraries"></span><span id="FOLDERID_LIBRARIES"></span><dl> <span data-ttu-id="9cfe8-725"><dt><strong>FOLDERID_Libraries</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-725"><dt><strong>FOLDERID_Libraries</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-726">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-726">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-727">{1B3EA5DC-B587-4786-B4EF-BD1DC332AEAE}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-727">{1B3EA5DC-B587-4786-B4EF-BD1DC332AEAE}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-728">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-728">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-729">Bibliotecas</span><span class="sxs-lookup"><span data-stu-id="9cfe8-729">Libraries</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-730">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-730">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-731">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-731">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-732">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-732">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-733">%APPDATA%\Microsoft\Windows\Libraries</span><span class="sxs-lookup"><span data-stu-id="9cfe8-733">%APPDATA%\Microsoft\Windows\Libraries</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-734">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-734">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-735">Ninguno, valor introducido en Windows 7</span><span class="sxs-lookup"><span data-stu-id="9cfe8-735">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-736">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-736">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-737">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-737">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-738">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-738">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-739">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-739">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Links"></span><span id="folderid_links"></span><span id="FOLDERID_LINKS"></span><dl> <span data-ttu-id="9cfe8-740"><dt><strong>FOLDERID_Links</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-740"><dt><strong>FOLDERID_Links</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-741">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-741">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-742">{bfb9d5e0-c6a9-404c-b2b2-ae6db6af4968}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-742">{bfb9d5e0-c6a9-404c-b2b2-ae6db6af4968}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-743">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-743">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-744">Vínculos</span><span class="sxs-lookup"><span data-stu-id="9cfe8-744">Links</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-745">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-745">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-746">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-746">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-747">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-747">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-748">%USERPROFILE%\Links</span><span class="sxs-lookup"><span data-stu-id="9cfe8-748">%USERPROFILE%\Links</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-749">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-749">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-750">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9cfe8-750">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-751">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-751">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-752">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-752">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-753">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-753">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-754">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-754">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_LocalAppData"></span><span id="folderid_localappdata"></span><span id="FOLDERID_LOCALAPPDATA"></span><dl> <span data-ttu-id="9cfe8-755"><dt><strong>FOLDERID_LocalAppData</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-755"><dt><strong>FOLDERID_LocalAppData</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-756">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-756">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-757">{F1B32785-6FBA-4FCF-9D55-7B8E7F157091}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-757">{F1B32785-6FBA-4FCF-9D55-7B8E7F157091}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-758">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-758">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-759">Local</span><span class="sxs-lookup"><span data-stu-id="9cfe8-759">Local</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-760">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-760">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-761">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-761">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-762">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-762">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-763">% LOCALAPPDATA% (%USERPROFILE%\AppData\Local)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-763">%LOCALAPPDATA% (%USERPROFILE%\AppData\Local)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-764">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-764">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-765">CSIDL_LOCAL_APPDATA</span><span class="sxs-lookup"><span data-stu-id="9cfe8-765">CSIDL_LOCAL_APPDATA</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-766">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-766">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-767">Datos de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="9cfe8-767">Application Data</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-768">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-768">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-769">%USERPROFILE%\Local Settings\Application Data</span><span class="sxs-lookup"><span data-stu-id="9cfe8-769">%USERPROFILE%\Local Settings\Application Data</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_LocalAppDataLow"></span><span id="folderid_localappdatalow"></span><span id="FOLDERID_LOCALAPPDATALOW"></span><dl> <span data-ttu-id="9cfe8-770"><dt><strong>FOLDERID_LocalAppDataLow</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-770"><dt><strong>FOLDERID_LocalAppDataLow</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-771">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-771">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-772">{A520A1A4-1780-4FF6-BD18-167343C5AF16}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-772">{A520A1A4-1780-4FF6-BD18-167343C5AF16}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-773">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-773">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-774">LocalLow</span><span class="sxs-lookup"><span data-stu-id="9cfe8-774">LocalLow</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-775">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-775">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-776">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-776">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-777">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-777">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-778">%USERPROFILE%\AppData\LocalLow</span><span class="sxs-lookup"><span data-stu-id="9cfe8-778">%USERPROFILE%\AppData\LocalLow</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-779">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-779">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-780">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9cfe8-780">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-781">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-781">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-782">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-782">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-783">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-783">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-784">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-784">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_LocalizedResourcesDir"></span><span id="folderid_localizedresourcesdir"></span><span id="FOLDERID_LOCALIZEDRESOURCESDIR"></span><dl> <span data-ttu-id="9cfe8-785"><dt><strong>FOLDERID_LocalizedResourcesDir</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-785"><dt><strong>FOLDERID_LocalizedResourcesDir</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-786">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-786">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-787">{2A00375E-224C-49DE-B8D1-440DF7EF3DDC}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-787">{2A00375E-224C-49DE-B8D1-440DF7EF3DDC}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-788">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-788">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-789">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9cfe8-789">None</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-790">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-790">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-791">FIXED</span><span class="sxs-lookup"><span data-stu-id="9cfe8-791">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-792">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-792">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-793">%WINDIR%\resources\0409 (página de códigos)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-793">%windir%\resources\0409 (code page)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-794">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-794">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-795">CSIDL_RESOURCES_LOCALIZED</span><span class="sxs-lookup"><span data-stu-id="9cfe8-795">CSIDL_RESOURCES_LOCALIZED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-796">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-796">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-797">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9cfe8-797">None</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-798">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-798">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-799">%WINDIR%\resources\0409 (página de códigos)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-799">%windir%\resources\0409 (code page)</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Music"></span><span id="folderid_music"></span><span id="FOLDERID_MUSIC"></span><dl> <span data-ttu-id="9cfe8-800"><dt><strong>FOLDERID_Music</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-800"><dt><strong>FOLDERID_Music</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-801">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-801">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-802">{4BD8D571-6D19-48D3-BE97-422220080E43}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-802">{4BD8D571-6D19-48D3-BE97-422220080E43}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-803">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-803">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-804">Música</span><span class="sxs-lookup"><span data-stu-id="9cfe8-804">Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-805">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-805">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-806">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-806">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-807">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-807">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-808">%USERPROFILE%\Music</span><span class="sxs-lookup"><span data-stu-id="9cfe8-808">%USERPROFILE%\Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-809">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-809">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-810">CSIDL_MYMUSIC</span><span class="sxs-lookup"><span data-stu-id="9cfe8-810">CSIDL_MYMUSIC</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-811">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-811">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-812">Mi música</span><span class="sxs-lookup"><span data-stu-id="9cfe8-812">My Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-813">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-813">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-814">%USERPROFILE%\My Documentos\mis música</span><span class="sxs-lookup"><span data-stu-id="9cfe8-814">%USERPROFILE%\My Documents\My Music</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_MusicLibrary"></span><span id="folderid_musiclibrary"></span><span id="FOLDERID_MUSICLIBRARY"></span><dl> <span data-ttu-id="9cfe8-815"><dt><strong>FOLDERID_MusicLibrary</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-815"><dt><strong>FOLDERID_MusicLibrary</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-816">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-816">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-817">{2112AB0A-C86A-4FFE-A368-0DE96E47012E}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-817">{2112AB0A-C86A-4FFE-A368-0DE96E47012E}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-818">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-818">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-819">Música</span><span class="sxs-lookup"><span data-stu-id="9cfe8-819">Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-820">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-820">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-821">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-821">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-822">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-822">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-823">%APPDATA%\Microsoft\Windows\Libraries\Music.library-ms</span><span class="sxs-lookup"><span data-stu-id="9cfe8-823">%APPDATA%\Microsoft\Windows\Libraries\Music.library-ms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-824">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-824">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-825">Ninguno, valor introducido en Windows 7</span><span class="sxs-lookup"><span data-stu-id="9cfe8-825">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-826">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-826">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-827">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-827">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-828">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-828">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-829">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-829">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_NetHood"></span><span id="folderid_nethood"></span><span id="FOLDERID_NETHOOD"></span><dl> <span data-ttu-id="9cfe8-830"><dt><strong>FOLDERID_NetHood</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-830"><dt><strong>FOLDERID_NetHood</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-831">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-831">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-832">{C5ABBF53-E17F-4121-8900-86626FC2C973}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-832">{C5ABBF53-E17F-4121-8900-86626FC2C973}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-833">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-833">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-834">Métodos abreviados de red</span><span class="sxs-lookup"><span data-stu-id="9cfe8-834">Network Shortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-835">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-835">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-836">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-836">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-837">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-837">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-838">Métodos abreviados de%APPDATA%\Microsoft\Windows\Network</span><span class="sxs-lookup"><span data-stu-id="9cfe8-838">%APPDATA%\Microsoft\Windows\Network Shortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-839">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-839">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-840">CSIDL_NETHOOD</span><span class="sxs-lookup"><span data-stu-id="9cfe8-840">CSIDL_NETHOOD</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-841">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-841">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-842">NetHood</span><span class="sxs-lookup"><span data-stu-id="9cfe8-842">NetHood</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-843">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-843">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-844">%USERPROFILE%\NetHood</span><span class="sxs-lookup"><span data-stu-id="9cfe8-844">%USERPROFILE%\NetHood</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_NetworkFolder"></span><span id="folderid_networkfolder"></span><span id="FOLDERID_NETWORKFOLDER"></span><dl> <span data-ttu-id="9cfe8-845"><dt><strong>FOLDERID_NetworkFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-845"><dt><strong>FOLDERID_NetworkFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-846">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-846">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-847">{D20BEEC4-5CA8-4905-AE3B-BF251EA09B53}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-847">{D20BEEC4-5CA8-4905-AE3B-BF251EA09B53}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-848">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-848">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-849">Red</span><span class="sxs-lookup"><span data-stu-id="9cfe8-849">Network</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-850">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-850">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-851">Virtualiza</span><span class="sxs-lookup"><span data-stu-id="9cfe8-851">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-852">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-852">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-853">No aplicable: carpeta virtual</span><span class="sxs-lookup"><span data-stu-id="9cfe8-853">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-854">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-854">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-855">CSIDL_NETWORK, CSIDL_COMPUTERSNEARME</span><span class="sxs-lookup"><span data-stu-id="9cfe8-855">CSIDL_NETWORK, CSIDL_COMPUTERSNEARME</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-856">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-856">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-857">Mis sitios de red</span><span class="sxs-lookup"><span data-stu-id="9cfe8-857">My Network Places</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-858">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-858">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-859">No aplicable: carpeta virtual</span><span class="sxs-lookup"><span data-stu-id="9cfe8-859">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Objects3D"></span><span id="folderid_objects3d"></span><span id="FOLDERID_OBJECTS3D"></span><dl> <span data-ttu-id="9cfe8-860"><dt><strong>FOLDERID_Objects3D</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-860"><dt><strong>FOLDERID_Objects3D</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-861">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-861">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-862">{31C0DD25-9439-4F12-BF41-7FF4EDA38722}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-862">{31C0DD25-9439-4F12-BF41-7FF4EDA38722}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-863">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-863">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-864">Objetos 3D</span><span class="sxs-lookup"><span data-stu-id="9cfe8-864">3D Objects</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-865">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-865">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-866">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-866">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-867">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-867">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-868">Objetos%USERPROFILE%\3D</span><span class="sxs-lookup"><span data-stu-id="9cfe8-868">%USERPROFILE%\3D Objects</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-869">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-869">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-870">Ninguno, valor introducido en Windows 10, versión 1703</span><span class="sxs-lookup"><span data-stu-id="9cfe8-870">None, value introduced in Windows 10, version 1703</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-871">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-871">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-872">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-872">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-873">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-873">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-874">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-874">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_OriginalImages"></span><span id="folderid_originalimages"></span><span id="FOLDERID_ORIGINALIMAGES"></span><dl> <span data-ttu-id="9cfe8-875"><dt><strong>FOLDERID_OriginalImages</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-875"><dt><strong>FOLDERID_OriginalImages</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-876">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-876">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-877">{2C36C0AA-5812-4b87-BFD0-4CD0DFB19B39}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-877">{2C36C0AA-5812-4b87-BFD0-4CD0DFB19B39}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-878">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-878">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-879">Imágenes originales</span><span class="sxs-lookup"><span data-stu-id="9cfe8-879">Original Images</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-880">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-880">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-881">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-881">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-882">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-882">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-883">Imágenes de%LOCALAPPDATA%\Microsoft\Windows Photo Gallery\Original</span><span class="sxs-lookup"><span data-stu-id="9cfe8-883">%LOCALAPPDATA%\Microsoft\Windows Photo Gallery\Original Images</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-884">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-884">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-885">Ninguno, valor introducido en Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9cfe8-885">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-886">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-886">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-887">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-887">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-888">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-888">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-889">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-889">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PhotoAlbums"></span><span id="folderid_photoalbums"></span><span id="FOLDERID_PHOTOALBUMS"></span><dl> <span data-ttu-id="9cfe8-890"><dt><strong>FOLDERID_PhotoAlbums</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-890"><dt><strong>FOLDERID_PhotoAlbums</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-891">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-891">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-892">{69D2CF90-FC33-4FB7-9A0C-EBB0F0FCB43C}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-892">{69D2CF90-FC33-4FB7-9A0C-EBB0F0FCB43C}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-893">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-893">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-894">Presentaciones</span><span class="sxs-lookup"><span data-stu-id="9cfe8-894">Slide Shows</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-895">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-895">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-896">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-896">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-897">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-897">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-898">%USERPROFILE%\Pictures\Slide muestra</span><span class="sxs-lookup"><span data-stu-id="9cfe8-898">%USERPROFILE%\Pictures\Slide Shows</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-899">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-899">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-900">Ninguno, valor introducido en Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9cfe8-900">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-901">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-901">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-902">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-902">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-903">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-903">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-904">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-904">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PicturesLibrary"></span><span id="folderid_pictureslibrary"></span><span id="FOLDERID_PICTURESLIBRARY"></span><dl> <span data-ttu-id="9cfe8-905"><dt><strong>FOLDERID_PicturesLibrary</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-905"><dt><strong>FOLDERID_PicturesLibrary</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-906">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-906">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-907">{A990AE9F-A03B-4E80-94BC-9912D7504104}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-907">{A990AE9F-A03B-4E80-94BC-9912D7504104}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-908">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-908">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-909">Imágenes</span><span class="sxs-lookup"><span data-stu-id="9cfe8-909">Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-910">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-910">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-911">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-911">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-912">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-912">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-913">%APPDATA%\Microsoft\Windows\Libraries\Pictures.library-ms</span><span class="sxs-lookup"><span data-stu-id="9cfe8-913">%APPDATA%\Microsoft\Windows\Libraries\Pictures.library-ms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-914">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-914">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-915">Ninguno, valor introducido en Windows 7</span><span class="sxs-lookup"><span data-stu-id="9cfe8-915">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-916">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-916">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-917">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-917">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-918">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-918">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-919">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-919">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Pictures"></span><span id="folderid_pictures"></span><span id="FOLDERID_PICTURES"></span><dl> <span data-ttu-id="9cfe8-920"><dt><strong>FOLDERID_Pictures</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-920"><dt><strong>FOLDERID_Pictures</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-921">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-921">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-922">{33E28130-4E1E-4676-835A-98395C3BC3BB}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-922">{33E28130-4E1E-4676-835A-98395C3BC3BB}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-923">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-923">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-924">Imágenes</span><span class="sxs-lookup"><span data-stu-id="9cfe8-924">Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-925">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-925">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-926">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-926">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-927">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-927">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-928">%USERPROFILE%\Pictures</span><span class="sxs-lookup"><span data-stu-id="9cfe8-928">%USERPROFILE%\Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-929">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-929">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-930">CSIDL_MYPICTURES</span><span class="sxs-lookup"><span data-stu-id="9cfe8-930">CSIDL_MYPICTURES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-931">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-931">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-932">Mis imágenes</span><span class="sxs-lookup"><span data-stu-id="9cfe8-932">My Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-933">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-933">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-934">%USERPROFILE%\My Documentos\mis imágenes</span><span class="sxs-lookup"><span data-stu-id="9cfe8-934">%USERPROFILE%\My Documents\My Pictures</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Playlists"></span><span id="folderid_playlists"></span><span id="FOLDERID_PLAYLISTS"></span><dl> <span data-ttu-id="9cfe8-935"><dt><strong>FOLDERID_Playlists</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-935"><dt><strong>FOLDERID_Playlists</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-936">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-936">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-937">{DE92C1C7-837F-4F69-A3BB-86E631204A23}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-937">{DE92C1C7-837F-4F69-A3BB-86E631204A23}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-938">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-938">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-939">Reproducción</span><span class="sxs-lookup"><span data-stu-id="9cfe8-939">Playlists</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-940">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-940">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-941">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-941">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-942">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-942">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-943">%USERPROFILE%\Music\Playlists</span><span class="sxs-lookup"><span data-stu-id="9cfe8-943">%USERPROFILE%\Music\Playlists</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-944">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-944">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-945">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9cfe8-945">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-946">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-946">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-947">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-947">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-948">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-948">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-949">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-949">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PrintersFolder"></span><span id="folderid_printersfolder"></span><span id="FOLDERID_PRINTERSFOLDER"></span><dl> <span data-ttu-id="9cfe8-950"><dt><strong>FOLDERID_PrintersFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-950"><dt><strong>FOLDERID_PrintersFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-951">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-951">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-952">{76FC4E2D-D6AD-4519-A663-37BD56068185}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-952">{76FC4E2D-D6AD-4519-A663-37BD56068185}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-953">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-953">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-954">Impresoras</span><span class="sxs-lookup"><span data-stu-id="9cfe8-954">Printers</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-955">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-955">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-956">Virtualiza</span><span class="sxs-lookup"><span data-stu-id="9cfe8-956">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-957">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-957">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-958">No aplicable: carpeta virtual</span><span class="sxs-lookup"><span data-stu-id="9cfe8-958">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-959">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-959">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-960">CSIDL_PRINTERS</span><span class="sxs-lookup"><span data-stu-id="9cfe8-960">CSIDL_PRINTERS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-961">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-961">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-962">Impresoras y faxes</span><span class="sxs-lookup"><span data-stu-id="9cfe8-962">Printers and Faxes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-963">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-963">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-964">No aplicable: carpeta virtual</span><span class="sxs-lookup"><span data-stu-id="9cfe8-964">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PrintHood"></span><span id="folderid_printhood"></span><span id="FOLDERID_PRINTHOOD"></span><dl> <span data-ttu-id="9cfe8-965"><dt><strong>FOLDERID_PrintHood</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-965"><dt><strong>FOLDERID_PrintHood</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-966">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-966">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-967">{9274BD8D-CFD1-41C3-B35E-B13F55A758F4}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-967">{9274BD8D-CFD1-41C3-B35E-B13F55A758F4}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-968">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-968">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-969">Accesos directos de impresora</span><span class="sxs-lookup"><span data-stu-id="9cfe8-969">Printer Shortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-970">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-970">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-971">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-971">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-972">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-972">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-973">Métodos abreviados de%APPDATA%\Microsoft\Windows\Printer</span><span class="sxs-lookup"><span data-stu-id="9cfe8-973">%APPDATA%\Microsoft\Windows\Printer Shortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-974">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-974">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-975">CSIDL_PRINTHOOD</span><span class="sxs-lookup"><span data-stu-id="9cfe8-975">CSIDL_PRINTHOOD</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-976">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-976">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-977">PrintHood</span><span class="sxs-lookup"><span data-stu-id="9cfe8-977">PrintHood</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-978">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-978">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-979">%USERPROFILE%\PrintHood</span><span class="sxs-lookup"><span data-stu-id="9cfe8-979">%USERPROFILE%\PrintHood</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Profile"></span><span id="folderid_profile"></span><span id="FOLDERID_PROFILE"></span><dl> <span data-ttu-id="9cfe8-980"><dt><strong>FOLDERID_Profile</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-980"><dt><strong>FOLDERID_Profile</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-981">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-981">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-982">{5E6C858F-0E22-4760-9AFE-EA3317B67173}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-982">{5E6C858F-0E22-4760-9AFE-EA3317B67173}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-983">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-983">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-984">El nombre de usuario (% USERNAME%)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-984">The user's username (%USERNAME%)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-985">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-985">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-986">FIXED</span><span class="sxs-lookup"><span data-stu-id="9cfe8-986">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-987">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-987">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-988">% USERPROFILE% (%SystemDrive%\Users \% username%)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-988">%USERPROFILE% (%SystemDrive%\Users\%USERNAME%)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-989">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-989">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-990">CSIDL_PROFILE</span><span class="sxs-lookup"><span data-stu-id="9cfe8-990">CSIDL_PROFILE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-991">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-991">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-992">El nombre de usuario (% USERNAME%)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-992">The user's username (%USERNAME%)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-993">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-993">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-994">% USERPROFILE% (%SystemDrive%\Documents and Settings \% nombreDeUsuario%)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-994">%USERPROFILE% (%SystemDrive%\Documents and Settings\%USERNAME%)</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ProgramData"></span><span id="folderid_programdata"></span><span id="FOLDERID_PROGRAMDATA"></span><dl> <span data-ttu-id="9cfe8-995"><dt><strong>FOLDERID_ProgramData</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-995"><dt><strong>FOLDERID_ProgramData</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-996">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-996">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-997">{62AB5D82-FDC1-4DC3-A9DD-070D1D495D97}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-997">{62AB5D82-FDC1-4DC3-A9DD-070D1D495D97}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-998">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-998">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-999">ProgramData</span><span class="sxs-lookup"><span data-stu-id="9cfe8-999">ProgramData</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1000">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1000">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1001">FIXED</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1001">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1002">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1002">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1003">% ALLUSERSPROFILE% (% ProgramData%,%SystemDrive%\ProgramData)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1003">%ALLUSERSPROFILE% (%ProgramData%, %SystemDrive%\ProgramData)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1004">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1004">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1005">CSIDL_COMMON_APPDATA</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1005">CSIDL_COMMON_APPDATA</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1006">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1006">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1007">Datos de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1007">Application Data</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1008">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1008">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1009">Datos de%ALLUSERSPROFILE%\Application</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1009">%ALLUSERSPROFILE%\Application Data</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ProgramFiles"></span><span id="folderid_programfiles"></span><span id="FOLDERID_PROGRAMFILES"></span><dl> <span data-ttu-id="9cfe8-1010"><dt><strong>FOLDERID_ProgramFiles</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1010"><dt><strong>FOLDERID_ProgramFiles</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="9cfe8-1011">Vea Comentarios para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1011">See Remarks for more information.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1012">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1012">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1013">{905e63b6-c1bf-494e-b29c-65b732d3d21a}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1013">{905e63b6-c1bf-494e-b29c-65b732d3d21a}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1014">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1014">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1015">Archivos de programa</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1015">Program Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1016">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1016">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1017">FIXED</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1017">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1018">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1018">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1019">% ProgramFiles% (%SystemDrive%\Archivos de programa)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1019">%ProgramFiles% (%SystemDrive%\Program Files)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1020">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1020">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1021">CSIDL_PROGRAM_FILES</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1021">CSIDL_PROGRAM_FILES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1022">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1022">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1023">Archivos de programa</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1023">Program Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1024">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1024">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1025">% ProgramFiles% (%SystemDrive%\Archivos de programa)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1025">%ProgramFiles% (%SystemDrive%\Program Files)</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ProgramFilesX64"></span><span id="folderid_programfilesx64"></span><span id="FOLDERID_PROGRAMFILESX64"></span><dl> <span data-ttu-id="9cfe8-1026"><dt><strong>FOLDERID_ProgramFilesX64</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1026"><dt><strong>FOLDERID_ProgramFilesX64</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="9cfe8-1027">Este valor no se admite en los sistemas operativos de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1027">This value is not supported on 32-bit operating systems.</span></span> <span data-ttu-id="9cfe8-1028">Tampoco se admite para las aplicaciones de 32 bits que se ejecutan en sistemas operativos de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1028">It also is not supported for 32-bit applications running on 64-bit operating systems.</span></span> <span data-ttu-id="9cfe8-1029">Al intentar usar FOLDERID_ProgramFilesX64 en cualquiera de los casos, se produce un error.</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1029">Attempting to use FOLDERID_ProgramFilesX64 in either situation results in an error.</span></span> <span data-ttu-id="9cfe8-1030">Vea Comentarios para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1030">See Remarks for more information.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1031">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1031">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1032">{6D809377-6AF0-444b-8957-A3773F02200E}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1032">{6D809377-6AF0-444b-8957-A3773F02200E}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1033">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1033">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1034">Archivos de programa</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1034">Program Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1035">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1035">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1036">FIXED</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1036">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1037">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1037">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1038">% ProgramFiles% (%SystemDrive%\Archivos de programa)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1038">%ProgramFiles% (%SystemDrive%\Program Files)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1039">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1039">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1040">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1040">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1041">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1041">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1042">Archivos de programa</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1042">Program Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1043">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1043">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1044">% ProgramFiles% (%SystemDrive%\Archivos de programa)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1044">%ProgramFiles% (%SystemDrive%\Program Files)</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ProgramFilesX86"></span><span id="folderid_programfilesx86"></span><span id="FOLDERID_PROGRAMFILESX86"></span><dl> <span data-ttu-id="9cfe8-1045"><dt><strong>FOLDERID_ProgramFilesX86</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1045"><dt><strong>FOLDERID_ProgramFilesX86</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="9cfe8-1046">Vea Comentarios para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1046">See Remarks for more information.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1047">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1047">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1048">{7C5A40EF-A0FB-4BFC-874A-C0F2E0B9FA8E}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1048">{7C5A40EF-A0FB-4BFC-874A-C0F2E0B9FA8E}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1049">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1049">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1050">Archivos de programa</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1050">Program Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1051">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1051">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1052">FIXED</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1052">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1053">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1053">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1054">% ProgramFiles% (%SystemDrive%\Archivos de programa)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1054">%ProgramFiles% (%SystemDrive%\Program Files)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1055">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1055">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1056">CSIDL_PROGRAM_FILESX86</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1056">CSIDL_PROGRAM_FILESX86</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1057">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1057">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1058">Archivos de programa</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1058">Program Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1059">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1059">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1060">% ProgramFiles% (%SystemDrive%\Archivos de programa)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1060">%ProgramFiles% (%SystemDrive%\Program Files)</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ProgramFilesCommon"></span><span id="folderid_programfilescommon"></span><span id="FOLDERID_PROGRAMFILESCOMMON"></span><dl> <span data-ttu-id="9cfe8-1061"><dt><strong>FOLDERID_ProgramFilesCommon</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1061"><dt><strong>FOLDERID_ProgramFilesCommon</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="9cfe8-1062">Vea Comentarios para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1062">See Remarks for more information.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1063">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1063">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1064">{F7F1ED05-9F6D-47A2-AAAE-29D317C6F066}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1064">{F7F1ED05-9F6D-47A2-AAAE-29D317C6F066}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1065">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1065">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1066">Archivos comunes</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1066">Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1067">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1067">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1068">FIXED</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1068">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1069">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1069">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1070">Archivos de%ProgramFiles%\Archivos</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1070">%ProgramFiles%\Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1071">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1071">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1072">CSIDL_PROGRAM_FILES_COMMON</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1072">CSIDL_PROGRAM_FILES_COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1073">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1073">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1074">Archivos comunes</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1074">Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1075">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1075">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1076">Archivos de%ProgramFiles%\Archivos</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1076">%ProgramFiles%\Common Files</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ProgramFilesCommonX64"></span><span id="folderid_programfilescommonx64"></span><span id="FOLDERID_PROGRAMFILESCOMMONX64"></span><dl> <span data-ttu-id="9cfe8-1077"><dt><strong>FOLDERID_ProgramFilesCommonX64</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1077"><dt><strong>FOLDERID_ProgramFilesCommonX64</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="9cfe8-1078">Vea Comentarios para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1078">See Remarks for more information.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1079">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1079">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1080">{6365D5A7-0F0D-45E5-87F6-0DA56B6A4F7D}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1080">{6365D5A7-0F0D-45E5-87F6-0DA56B6A4F7D}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1081">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1081">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1082">Archivos comunes</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1082">Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1083">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1083">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1084">FIXED</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1084">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1085">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1085">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1086">Archivos de%ProgramFiles%\Archivos</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1086">%ProgramFiles%\Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1087">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1087">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1088">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1088">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1089">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1089">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1090">Archivos comunes</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1090">Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1091">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1091">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1092">Archivos de%ProgramFiles%\Archivos</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1092">%ProgramFiles%\Common Files</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ProgramFilesCommonX86"></span><span id="folderid_programfilescommonx86"></span><span id="FOLDERID_PROGRAMFILESCOMMONX86"></span><dl> <span data-ttu-id="9cfe8-1093"><dt><strong>FOLDERID_ProgramFilesCommonX86</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1093"><dt><strong>FOLDERID_ProgramFilesCommonX86</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="9cfe8-1094">Vea Comentarios para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1094">See Remarks for more information.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1095">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1095">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1096">{DE974D24-D9C6-4D3E-BF91-F4455120B917}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1096">{DE974D24-D9C6-4D3E-BF91-F4455120B917}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1097">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1097">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1098">Archivos comunes</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1098">Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1099">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1099">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1100">FIXED</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1100">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1101">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1101">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1102">Archivos de%ProgramFiles%\Archivos</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1102">%ProgramFiles%\Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1103">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1103">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1104">CSIDL_PROGRAM_FILES_COMMONX86</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1104">CSIDL_PROGRAM_FILES_COMMONX86</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1105">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1105">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1106">Archivos comunes</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1106">Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1107">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1107">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1108">Archivos de%ProgramFiles%\Archivos</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1108">%ProgramFiles%\Common Files</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Programs"></span><span id="folderid_programs"></span><span id="FOLDERID_PROGRAMS"></span><dl> <span data-ttu-id="9cfe8-1109"><dt><strong>FOLDERID_Programs</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1109"><dt><strong>FOLDERID_Programs</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1110">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1110">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1111">{A77F5D77-2E2B-44C3-A6A2-ABA601054A51}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1111">{A77F5D77-2E2B-44C3-A6A2-ABA601054A51}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1112">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1112">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1113">Programas</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1113">Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1114">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1114">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1115">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1115">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1116">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1116">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1117">Inicio\programas de%APPDATA%\Microsoft\Windows\Start</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1117">%APPDATA%\Microsoft\Windows\Start Menu\Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1118">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1118">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1119">CSIDL_PROGRAMS</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1119">CSIDL_PROGRAMS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1120">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1120">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1121">Programas</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1121">Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1122">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1122">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1123">Inicio\programas de%USERPROFILE%\Start</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1123">%USERPROFILE%\Start Menu\Programs</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Public"></span><span id="folderid_public"></span><span id="FOLDERID_PUBLIC"></span><dl> <span data-ttu-id="9cfe8-1124"><dt><strong>FOLDERID_Public</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1124"><dt><strong>FOLDERID_Public</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1125">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1125">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1126">{DFDF76A2-C82A-4D63-906A-5644AC457385}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1126">{DFDF76A2-C82A-4D63-906A-5644AC457385}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1127">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1127">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1128">Público</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1128">Public</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1129">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1129">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1130">FIXED</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1130">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1131">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1131">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1132">% De% público (%SystemDrive%\Users\Public)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1132">%PUBLIC% (%SystemDrive%\Users\Public)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1133">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1133">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1134">Ninguno, nuevo para Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1134">None, new for Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1135">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1135">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1136">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1136">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1137">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1137">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1138">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1138">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PublicDesktop"></span><span id="folderid_publicdesktop"></span><span id="FOLDERID_PUBLICDESKTOP"></span><dl> <span data-ttu-id="9cfe8-1139"><dt><strong>FOLDERID_PublicDesktop</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1139"><dt><strong>FOLDERID_PublicDesktop</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1140">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1140">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1141">{C4AA340D-F20F-4863-AFEF-F87EF2E6BA25}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1141">{C4AA340D-F20F-4863-AFEF-F87EF2E6BA25}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1142">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1142">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1143">Escritorio público</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1143">Public Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1144">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1144">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1145">NORMAL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1145">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1146">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1146">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1147">%PUBLIC%\Desktop</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1147">%PUBLIC%\Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1148">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1148">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1149">CSIDL_COMMON_DESKTOPDIRECTORY</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1149">CSIDL_COMMON_DESKTOPDIRECTORY</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1150">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1150">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1151">Escritorio</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1151">Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1152">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1152">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1153">%ALLUSERSPROFILE%\Desktop</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1153">%ALLUSERSPROFILE%\Desktop</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PublicDocuments"></span><span id="folderid_publicdocuments"></span><span id="FOLDERID_PUBLICDOCUMENTS"></span><dl> <span data-ttu-id="9cfe8-1154"><dt><strong>FOLDERID_PublicDocuments</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1154"><dt><strong>FOLDERID_PublicDocuments</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1155">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1155">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1156">{ED4824AF-DCE4-45A8-81E2-FC7965083634}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1156">{ED4824AF-DCE4-45A8-81E2-FC7965083634}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1157">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1157">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1158">Documentos públicos</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1158">Public Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1159">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1159">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1160">NORMAL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1160">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1161">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1161">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1162">%PUBLIC%\Documents</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1162">%PUBLIC%\Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1163">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1163">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1164">CSIDL_COMMON_DOCUMENTS</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1164">CSIDL_COMMON_DOCUMENTS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1165">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1165">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1166">Documentos compartidos</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1166">Shared Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1167">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1167">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1168">%ALLUSERSPROFILE%\Documents</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1168">%ALLUSERSPROFILE%\Documents</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PublicDownloads"></span><span id="folderid_publicdownloads"></span><span id="FOLDERID_PUBLICDOWNLOADS"></span><dl> <span data-ttu-id="9cfe8-1169"><dt><strong>FOLDERID_PublicDownloads</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1169"><dt><strong>FOLDERID_PublicDownloads</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1170">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1170">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1171">{3D644C9B-1FB8-4f30-9B45-F670235F79C0}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1171">{3D644C9B-1FB8-4f30-9B45-F670235F79C0}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1172">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1172">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1173">Descargas públicas</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1173">Public Downloads</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1174">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1174">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1175">NORMAL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1175">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1176">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1176">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1177">%PUBLIC%\Downloads</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1177">%PUBLIC%\Downloads</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1178">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1178">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1179">Ninguno, valor introducido en Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1179">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1180">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1180">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1181">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1181">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1182">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1182">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1183">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1183">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PublicGameTasks"></span><span id="folderid_publicgametasks"></span><span id="FOLDERID_PUBLICGAMETASKS"></span><dl> <span data-ttu-id="9cfe8-1184"><dt><strong>FOLDERID_PublicGameTasks</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1184"><dt><strong>FOLDERID_PublicGameTasks</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1185">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1185">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1186">{DEBF2536-E1A8-4c59-B6A2-414586476AEA}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1186">{DEBF2536-E1A8-4c59-B6A2-414586476AEA}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1187">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1187">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1188">GameExplorer</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1188">GameExplorer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1189">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1189">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1190">NORMAL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1190">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1191">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1191">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1192">%ALLUSERSPROFILE%\Microsoft\Windows\GameExplorer</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1192">%ALLUSERSPROFILE%\Microsoft\Windows\GameExplorer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1193">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1193">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1194">Ninguno, valor introducido en Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1194">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1195">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1195">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1196">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1196">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1197">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1197">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1198">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1198">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PublicLibraries"></span><span id="folderid_publiclibraries"></span><span id="FOLDERID_PUBLICLIBRARIES"></span><dl> <span data-ttu-id="9cfe8-1199"><dt><strong>FOLDERID_PublicLibraries</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1199"><dt><strong>FOLDERID_PublicLibraries</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1200">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1200">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1201">{48DAF80B-E6CF-4F4E-B800-0E69D84EE384}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1201">{48DAF80B-E6CF-4F4E-B800-0E69D84EE384}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1202">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1202">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1203">Bibliotecas</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1203">Libraries</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1204">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1204">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1205">NORMAL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1205">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1206">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1206">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1207">%ALLUSERSPROFILE%\Microsoft\Windows\Libraries</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1207">%ALLUSERSPROFILE%\Microsoft\Windows\Libraries</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1208">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1208">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1209">Ninguno, valor introducido en Windows 7</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1209">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1210">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1210">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1211">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1211">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1212">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1212">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1213">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1213">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PublicMusic"></span><span id="folderid_publicmusic"></span><span id="FOLDERID_PUBLICMUSIC"></span><dl> <span data-ttu-id="9cfe8-1214"><dt><strong>FOLDERID_PublicMusic</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1214"><dt><strong>FOLDERID_PublicMusic</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1215">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1215">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1216">{3214FAB5-9757-4298-BB61-92A9DEAA44FF}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1216">{3214FAB5-9757-4298-BB61-92A9DEAA44FF}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1217">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1217">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1218">Música pública</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1218">Public Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1219">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1219">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1220">NORMAL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1220">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1221">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1221">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1222">%PUBLIC%\Music</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1222">%PUBLIC%\Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1223">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1223">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1224">CSIDL_COMMON_MUSIC</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1224">CSIDL_COMMON_MUSIC</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1225">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1225">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1226">Música compartida</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1226">Shared Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1227">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1227">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1228">Música%ALLUSERSPROFILE%\Documents\My</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1228">%ALLUSERSPROFILE%\Documents\My Music</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PublicPictures"></span><span id="folderid_publicpictures"></span><span id="FOLDERID_PUBLICPICTURES"></span><dl> <span data-ttu-id="9cfe8-1229"><dt><strong>FOLDERID_PublicPictures</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1229"><dt><strong>FOLDERID_PublicPictures</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1230">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1230">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1231">{B6EBFB86-6907-413C-9AF7-4FC2ABF07CC5}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1231">{B6EBFB86-6907-413C-9AF7-4FC2ABF07CC5}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1232">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1232">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1233">Imágenes públicas</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1233">Public Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1234">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1234">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1235">NORMAL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1235">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1236">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1236">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1237">%PUBLIC%\Pictures</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1237">%PUBLIC%\Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1238">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1238">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1239">CSIDL_COMMON_PICTURES</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1239">CSIDL_COMMON_PICTURES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1240">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1240">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1241">Imágenes compartidas</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1241">Shared Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1242">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1242">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1243">Imágenes de%ALLUSERSPROFILE%\Documents\My</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1243">%ALLUSERSPROFILE%\Documents\My Pictures</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PublicRingtones"></span><span id="folderid_publicringtones"></span><span id="FOLDERID_PUBLICRINGTONES"></span><dl> <span data-ttu-id="9cfe8-1244"><dt><strong>FOLDERID_PublicRingtones</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1244"><dt><strong>FOLDERID_PublicRingtones</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1245">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1245">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1246">{E555AB60-153B-4D17-9F04-A5FE99FC15EC}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1246">{E555AB60-153B-4D17-9F04-A5FE99FC15EC}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1247">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1247">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1248">Tonos</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1248">Ringtones</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1249">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1249">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1250">NORMAL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1250">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1251">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1251">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1252">%ALLUSERSPROFILE%\Microsoft\Windows\Ringtones</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1252">%ALLUSERSPROFILE%\Microsoft\Windows\Ringtones</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1253">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1253">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1254">Ninguno, valor introducido en Windows 7</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1254">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1255">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1255">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1256">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1256">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1257">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1257">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1258">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1258">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PublicUserTiles"></span><span id="folderid_publicusertiles"></span><span id="FOLDERID_PUBLICUSERTILES"></span><dl> <span data-ttu-id="9cfe8-1259"><dt><strong>FOLDERID_PublicUserTiles</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1259"><dt><strong>FOLDERID_PublicUserTiles</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1260">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1260">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1261">{0482af6c-08f1-4c34-8c90-e17ec98b1e17}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1261">{0482af6c-08f1-4c34-8c90-e17ec98b1e17}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1262">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1262">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1263">Imágenes de cuentas públicas</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1263">Public Account Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1264">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1264">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1265">NORMAL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1265">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1266">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1266">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1267">%PUBLIC%\AccountPictures</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1267">%PUBLIC%\AccountPictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1268">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1268">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1269">Ninguno, valor introducido en Windows 8</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1269">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1270">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1270">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1271">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1271">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1272">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1272">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1273">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1273">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PublicVideos"></span><span id="folderid_publicvideos"></span><span id="FOLDERID_PUBLICVIDEOS"></span><dl> <span data-ttu-id="9cfe8-1274"><dt><strong>FOLDERID_PublicVideos</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1274"><dt><strong>FOLDERID_PublicVideos</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1275">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1275">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1276">{2400183A-6185-49FB-A2D8-4A392A602BA3}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1276">{2400183A-6185-49FB-A2D8-4A392A602BA3}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1277">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1277">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1278">Vídeos públicos</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1278">Public Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1279">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1279">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1280">NORMAL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1280">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1281">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1281">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1282">%PUBLIC%\Videos</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1282">%PUBLIC%\Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1283">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1283">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1284">CSIDL_COMMON_VIDEO</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1284">CSIDL_COMMON_VIDEO</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1285">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1285">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1286">Vídeo compartido</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1286">Shared Video</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1287">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1287">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1288">Vídeos de%ALLUSERSPROFILE%\Documents\My</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1288">%ALLUSERSPROFILE%\Documents\My Videos</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_QuickLaunch"></span><span id="folderid_quicklaunch"></span><span id="FOLDERID_QUICKLAUNCH"></span><dl> <span data-ttu-id="9cfe8-1289"><dt><strong>FOLDERID_QuickLaunch</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1289"><dt><strong>FOLDERID_QuickLaunch</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1290">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1290">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1291">{52a4f021-7b75-48a9-9f6b-4b87a210bc8f}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1291">{52a4f021-7b75-48a9-9f6b-4b87a210bc8f}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1292">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1292">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1293">Inicio rápido</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1293">Quick Launch</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1294">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1294">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1295">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1295">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1296">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1296">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1297">Inicio de%APPDATA%\Microsoft\Internet Explorer\Quick</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1297">%APPDATA%\Microsoft\Internet Explorer\Quick Launch</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1298">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1298">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1299">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1299">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1300">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1300">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1301">Inicio rápido</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1301">Quick Launch</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1302">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1302">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1303">Inicio de%APPDATA%\Microsoft\Internet Explorer\Quick</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1303">%APPDATA%\Microsoft\Internet Explorer\Quick Launch</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Recent"></span><span id="folderid_recent"></span><span id="FOLDERID_RECENT"></span><dl> <span data-ttu-id="9cfe8-1304"><dt><strong>FOLDERID_Recent</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1304"><dt><strong>FOLDERID_Recent</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1305">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1305">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1306">{AE50C081-EBD2-438A-8655-8A092E34987A}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1306">{AE50C081-EBD2-438A-8655-8A092E34987A}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1307">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1307">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1308">Elementos recientes</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1308">Recent Items</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1309">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1309">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1310">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1310">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1311">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1311">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1312">%APPDATA%\Microsoft\Windows\Recent</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1312">%APPDATA%\Microsoft\Windows\Recent</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1313">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1313">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1314">CSIDL_RECENT</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1314">CSIDL_RECENT</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1315">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1315">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1316">Mis documentos recientes</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1316">My Recent Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1317">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1317">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1318">%USERPROFILE%\Recent</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1318">%USERPROFILE%\Recent</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_RecordedTV"></span><span id="folderid_recordedtv"></span><span id="FOLDERID_RECORDEDTV"></span><dl> <span data-ttu-id="9cfe8-1319"><dt><strong>FOLDERID_RecordedTV</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1319"><dt><strong>FOLDERID_RecordedTV</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="9cfe8-1320">No se utiliza.</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1320">Not used.</span></span> <span data-ttu-id="9cfe8-1321">Este valor no está definido a partir de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1321">This value is undefined as of Windows 7.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_RecordedTVLibrary"></span><span id="folderid_recordedtvlibrary"></span><span id="FOLDERID_RECORDEDTVLIBRARY"></span><dl> <span data-ttu-id="9cfe8-1322"><dt><strong>FOLDERID_RecordedTVLibrary</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1322"><dt><strong>FOLDERID_RecordedTVLibrary</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1323">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1323">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1324">{1A6FDBA2-F42D-4358-A798-B74D745926C5}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1324">{1A6FDBA2-F42D-4358-A798-B74D745926C5}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1325">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1325">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1326">TV grabada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1326">Recorded TV</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1327">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1327">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1328">NORMAL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1328">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1329">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1329">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1330">%PUBLIC%\RecordedTV.library-ms</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1330">%PUBLIC%\RecordedTV.library-ms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1331">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1331">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1332">Ninguno, valor introducido en Windows 7</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1332">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1333">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1333">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1334">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1334">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1335">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1335">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1336">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1336">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_RecycleBinFolder"></span><span id="folderid_recyclebinfolder"></span><span id="FOLDERID_RECYCLEBINFOLDER"></span><dl> <span data-ttu-id="9cfe8-1337"><dt><strong>FOLDERID_RecycleBinFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1337"><dt><strong>FOLDERID_RecycleBinFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1338">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1338">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1339">{B7534046-3ECB-4C18-BE4E-64CD4CB7D6AC}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1339">{B7534046-3ECB-4C18-BE4E-64CD4CB7D6AC}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1340">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1340">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1341">Papelera de reciclaje</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1341">Recycle Bin</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1342">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1342">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1343">Virtualiza</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1343">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1344">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1344">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1345">No aplicable: carpeta virtual</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1345">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1346">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1346">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1347">CSIDL_BITBUCKET</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1347">CSIDL_BITBUCKET</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1348">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1348">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1349">Papelera de reciclaje</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1349">Recycle Bin</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1350">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1350">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1351">No aplicable: carpeta virtual</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1351">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ResourceDir"></span><span id="folderid_resourcedir"></span><span id="FOLDERID_RESOURCEDIR"></span><dl> <span data-ttu-id="9cfe8-1352"><dt><strong>FOLDERID_ResourceDir</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1352"><dt><strong>FOLDERID_ResourceDir</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1353">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1353">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1354">{8AD10C31-2ADB-4296-A8F7-E4701232C972}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1354">{8AD10C31-2ADB-4296-A8F7-E4701232C972}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1355">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1355">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1356">Recursos</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1356">Resources</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1357">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1357">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1358">FIXED</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1358">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1359">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1359">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1360">%windir%\Resources</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1360">%windir%\Resources</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1361">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1361">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1362">CSIDL_RESOURCES</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1362">CSIDL_RESOURCES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1363">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1363">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1364">Recursos</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1364">Resources</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1365">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1365">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1366">%windir%\Resources</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1366">%windir%\Resources</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Ringtones"></span><span id="folderid_ringtones"></span><span id="FOLDERID_RINGTONES"></span><dl> <span data-ttu-id="9cfe8-1367"><dt><strong>FOLDERID_Ringtones</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1367"><dt><strong>FOLDERID_Ringtones</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1368">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1368">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1369">{C870044B-F49E-4126-A9C3-B52A1FF411E8}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1369">{C870044B-F49E-4126-A9C3-B52A1FF411E8}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1370">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1370">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1371">Tonos</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1371">Ringtones</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1372">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1372">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1373">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1373">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1374">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1374">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1375">%LOCALAPPDATA%\Microsoft\Windows\Ringtones</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1375">%LOCALAPPDATA%\Microsoft\Windows\Ringtones</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1376">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1376">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1377">Ninguno, valor introducido en Windows 7</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1377">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1378">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1378">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1379">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1379">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1380">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1380">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1381">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1381">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_RoamingAppData"></span><span id="folderid_roamingappdata"></span><span id="FOLDERID_ROAMINGAPPDATA"></span><dl> <span data-ttu-id="9cfe8-1382"><dt><strong>FOLDERID_RoamingAppData</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1382"><dt><strong>FOLDERID_RoamingAppData</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1383">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1383">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1384">{3EB685DB-65F9-4CF6-A03A-E3EF65729F3D}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1384">{3EB685DB-65F9-4CF6-A03A-E3EF65729F3D}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1385">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1385">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1386">Movilidad</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1386">Roaming</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1387">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1387">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1388">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1388">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1389">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1389">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1390">% APPDATA% (%USERPROFILE%\AppData\Roaming)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1390">%APPDATA% (%USERPROFILE%\AppData\Roaming)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1391">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1391">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1392">CSIDL_APPDATA</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1392">CSIDL_APPDATA</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1393">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1393">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1394">Datos de aplicaciones</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1394">Application Data</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1395">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1395">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1396">% APPDATA% (datos de%USERPROFILE%\Application)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1396">%APPDATA% (%USERPROFILE%\Application Data)</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_RoamedTileImages"></span><span id="folderid_roamedtileimages"></span><span id="FOLDERID_ROAMEDTILEIMAGES"></span><dl> <span data-ttu-id="9cfe8-1397"><dt><strong>FOLDERID_RoamedTileImages</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1397"><dt><strong>FOLDERID_RoamedTileImages</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1398">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1398">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1399">{AAA8D5A5-F1D6-4259-BAA8-78E7EF60835E}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1399">{AAA8D5A5-F1D6-4259-BAA8-78E7EF60835E}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1400">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1400">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1401">RoamedTileImages</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1401">RoamedTileImages</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1402">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1402">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1403">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1403">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1404">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1404">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1405">%LOCALAPPDATA%\Microsoft\Windows\RoamedTileImages</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1405">%LOCALAPPDATA%\Microsoft\Windows\RoamedTileImages</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1406">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1406">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1407">Ninguno, valor introducido en Windows 8</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1407">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1408">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1408">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1409">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1409">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1410">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1410">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1411">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1411">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_RoamingTiles"></span><span id="folderid_roamingtiles"></span><span id="FOLDERID_ROAMINGTILES"></span><dl> <span data-ttu-id="9cfe8-1412"><dt><strong>FOLDERID_RoamingTiles</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1412"><dt><strong>FOLDERID_RoamingTiles</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1413">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1413">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1414">{00BCFC5A-ED94-4e48-96A1-3F6217F21990}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1414">{00BCFC5A-ED94-4e48-96A1-3F6217F21990}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1415">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1415">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1416">RoamingTiles</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1416">RoamingTiles</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1417">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1417">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1418">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1418">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1419">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1419">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1420">%LOCALAPPDATA%\Microsoft\Windows\RoamingTiles</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1420">%LOCALAPPDATA%\Microsoft\Windows\RoamingTiles</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1421">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1421">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1422">Ninguno, valor introducido en Windows 8</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1422">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1423">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1423">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1424">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1424">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1425">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1425">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1426">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1426">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SampleMusic"></span><span id="folderid_samplemusic"></span><span id="FOLDERID_SAMPLEMUSIC"></span><dl> <span data-ttu-id="9cfe8-1427"><dt><strong>FOLDERID_SampleMusic</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1427"><dt><strong>FOLDERID_SampleMusic</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1428">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1428">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1429">{B250C668-F57D-4EE1-A63C-290EE7D1AA1F}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1429">{B250C668-F57D-4EE1-A63C-290EE7D1AA1F}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1430">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1430">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1431">Música de ejemplo</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1431">Sample Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1432">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1432">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1433">NORMAL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1433">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1434">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1434">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1435">Música%PUBLIC%\Music\Sample</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1435">%PUBLIC%\Music\Sample Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1436">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1436">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1437">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1437">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1438">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1438">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1439">Música de ejemplo</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1439">Sample Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1440">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1440">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1441">%ALLUSERSPROFILE%\Documents\My Music\Sample Music</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1441">%ALLUSERSPROFILE%\Documents\My Music\Sample Music</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SamplePictures"></span><span id="folderid_samplepictures"></span><span id="FOLDERID_SAMPLEPICTURES"></span><dl> <span data-ttu-id="9cfe8-1442"><dt><strong>FOLDERID_SamplePictures</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1442"><dt><strong>FOLDERID_SamplePictures</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1443">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1443">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1444">{C4900540-2379-4C75-844B-64E6FAF8716B}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1444">{C4900540-2379-4C75-844B-64E6FAF8716B}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1445">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1445">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1446">Imágenes de ejemplo</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1446">Sample Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1447">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1447">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1448">NORMAL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1448">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1449">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1449">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1450">Imágenes de%PUBLIC%\Pictures\Sample</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1450">%PUBLIC%\Pictures\Sample Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1451">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1451">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1452">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1452">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1453">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1453">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1454">Imágenes de ejemplo</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1454">Sample Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1455">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1455">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1456">Imágenes de%ALLUSERSPROFILE%\Documents\My \ Sample Pictures</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1456">%ALLUSERSPROFILE%\Documents\My Pictures\Sample Pictures</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SamplePlaylists"></span><span id="folderid_sampleplaylists"></span><span id="FOLDERID_SAMPLEPLAYLISTS"></span><dl> <span data-ttu-id="9cfe8-1457"><dt><strong>FOLDERID_SamplePlaylists</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1457"><dt><strong>FOLDERID_SamplePlaylists</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1458">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1458">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1459">{15CA69B3-30EE-49C1-ACE1-6B5EC372AFB5}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1459">{15CA69B3-30EE-49C1-ACE1-6B5EC372AFB5}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1460">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1460">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1461">Listas de reproducción de ejemplo</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1461">Sample Playlists</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1462">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1462">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1463">NORMAL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1463">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1464">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1464">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1465">Listas de reproducción de%PUBLIC%\Music\Sample</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1465">%PUBLIC%\Music\Sample Playlists</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1466">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1466">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1467">Ninguno, valor introducido en Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1467">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1468">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1468">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1469">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1469">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1470">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1470">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1471">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1471">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SampleVideos"></span><span id="folderid_samplevideos"></span><span id="FOLDERID_SAMPLEVIDEOS"></span><dl> <span data-ttu-id="9cfe8-1472"><dt><strong>FOLDERID_SampleVideos</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1472"><dt><strong>FOLDERID_SampleVideos</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1473">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1473">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1474">{859EAD94-2E85-48AD-A71A-0969CB56A6CD}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1474">{859EAD94-2E85-48AD-A71A-0969CB56A6CD}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1475">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1475">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1476">Vídeos de ejemplo</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1476">Sample Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1477">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1477">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1478">NORMAL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1478">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1479">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1479">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1480">Vídeos de%PUBLIC%\Videos\Sample</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1480">%PUBLIC%\Videos\Sample Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1481">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1481">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1482">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1482">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1483">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1483">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1484">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1484">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1485">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1485">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1486">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1486">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SavedGames"></span><span id="folderid_savedgames"></span><span id="FOLDERID_SAVEDGAMES"></span><dl> <span data-ttu-id="9cfe8-1487"><dt><strong>FOLDERID_SavedGames</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1487"><dt><strong>FOLDERID_SavedGames</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1488">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1488">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1489">{4C5C32FF-BB9D-43b0-B5B4-2D72E54EAAA4}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1489">{4C5C32FF-BB9D-43b0-B5B4-2D72E54EAAA4}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1490">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1490">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1491">Juegos guardados</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1491">Saved Games</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1492">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1492">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1493">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1493">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1494">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1494">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1495">Juegos de%USERPROFILE%\Saved</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1495">%USERPROFILE%\Saved Games</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1496">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1496">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1497">Ninguno, valor introducido en Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1497">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1498">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1498">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1499">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1499">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1500">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1500">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1501">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1501">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SavedPictures"></span><span id="folderid_savedpictures"></span><span id="FOLDERID_SAVEDPICTURES"></span><dl> <span data-ttu-id="9cfe8-1502"><dt><strong>FOLDERID_SavedPictures</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1502"><dt><strong>FOLDERID_SavedPictures</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1503">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1503">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1504">{3B193882-D3AD-4eab-965A-69829D1FB59F}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1504">{3B193882-D3AD-4eab-965A-69829D1FB59F}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1505">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1505">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1506">Imágenes guardadas</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1506">Saved Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1507">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1507">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1508">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1508">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1509">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1509">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1510">Imágenes de%USERPROFILE%\Pictures\Saved</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1510">%USERPROFILE%\Pictures\Saved Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1511">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1511">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1512">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1512">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1513">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1513">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1514">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1514">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1515">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1515">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1516">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1516">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SavedPicturesLibrary"></span><span id="folderid_savedpictureslibrary"></span><span id="FOLDERID_SAVEDPICTURESLIBRARY"></span><dl> <span data-ttu-id="9cfe8-1517"><dt><strong>FOLDERID_SavedPicturesLibrary</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1517"><dt><strong>FOLDERID_SavedPicturesLibrary</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1518">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1518">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1519">{E25B5812-BE88-4bd9-94B0-29233477B6C3}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1519">{E25B5812-BE88-4bd9-94B0-29233477B6C3}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1520">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1520">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1521">Biblioteca de imágenes guardadas</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1521">Saved Pictures Library</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1522">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1522">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1523">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1523">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1524">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1524">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1525">%APPDATE%\Microsoft\Windows\Libraries\SavedPictures.library-ms</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1525">%APPDATE%\Microsoft\Windows\Libraries\SavedPictures.library-ms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1526">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1526">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1527">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1527">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1528">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1528">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1529">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1529">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1530">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1530">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1531">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1531">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SavedSearches"></span><span id="folderid_savedsearches"></span><span id="FOLDERID_SAVEDSEARCHES"></span><dl> <span data-ttu-id="9cfe8-1532"><dt><strong>FOLDERID_SavedSearches</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1532"><dt><strong>FOLDERID_SavedSearches</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1533">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1533">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1534">{7d1d3a04-debb-4115-95cf-2f29da2920da}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1534">{7d1d3a04-debb-4115-95cf-2f29da2920da}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1535">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1535">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1536">Búsquedas</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1536">Searches</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1537">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1537">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1538">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1538">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1539">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1539">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1540">%USERPROFILE%\Searches</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1540">%USERPROFILE%\Searches</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1541">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1541">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1542">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1542">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1543">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1543">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1544">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1544">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1545">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1545">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1546">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1546">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Screenshots"></span><span id="folderid_screenshots"></span><span id="FOLDERID_SCREENSHOTS"></span><dl> <span data-ttu-id="9cfe8-1547"><dt><strong>FOLDERID_Screenshots</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1547"><dt><strong>FOLDERID_Screenshots</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1548">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1548">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1549">{b7bede81-df94-4682-a7d8-57a52620b86f}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1549">{b7bede81-df94-4682-a7d8-57a52620b86f}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1550">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1550">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1551">Capturas de pantalla</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1551">Screenshots</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1552">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1552">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1553">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1553">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1554">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1554">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1555">%USERPROFILE%\Pictures\Screenshots</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1555">%USERPROFILE%\Pictures\Screenshots</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1556">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1556">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1557">Ninguno, valor introducido en Windows 8</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1557">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1558">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1558">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1559">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1559">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1560">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1560">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1561">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1561">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SEARCH_CSC"></span><span id="folderid_search_csc"></span><dl> <span data-ttu-id="9cfe8-1562"><dt><strong>FOLDERID_SEARCH_CSC</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1562"><dt><strong>FOLDERID_SEARCH_CSC</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1563">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1563">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1564">{ee32e446-31ca-4aba-814f-a5ebd2fd6d5e}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1564">{ee32e446-31ca-4aba-814f-a5ebd2fd6d5e}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1565">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1565">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1566">Archivos sin conexión</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1566">Offline Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1567">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1567">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1568">Virtualiza</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1568">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1569">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1569">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1570">No aplicable: carpeta virtual</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1570">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1571">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1571">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1572">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1572">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1573">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1573">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1574">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1574">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1575">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1575">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1576">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1576">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SearchHistory"></span><span id="folderid_searchhistory"></span><span id="FOLDERID_SEARCHHISTORY"></span><dl> <span data-ttu-id="9cfe8-1577"><dt><strong>FOLDERID_SearchHistory</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1577"><dt><strong>FOLDERID_SearchHistory</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1578">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1578">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1579">{0D4C3DB6-03A3-462F-A0E6-08924C41B5D4}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1579">{0D4C3DB6-03A3-462F-A0E6-08924C41B5D4}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1580">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1580">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1581">Historial</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1581">History</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1582">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1582">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1583">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1583">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1584">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1584">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1585">%LOCALAPPDATA%\Microsoft\Windows\ConnectedSearch\History</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1585">%LOCALAPPDATA%\Microsoft\Windows\ConnectedSearch\History</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1586">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1586">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1587">Ninguno, valor introducido en Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1587">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1588">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1588">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1589">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1589">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1590">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1590">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1591">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1591">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SearchHome"></span><span id="folderid_searchhome"></span><span id="FOLDERID_SEARCHHOME"></span><dl> <span data-ttu-id="9cfe8-1592"><dt><strong>FOLDERID_SearchHome</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1592"><dt><strong>FOLDERID_SearchHome</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1593">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1593">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1594">{190337d1-b8ca-4121-a639-6d472d16972a}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1594">{190337d1-b8ca-4121-a639-6d472d16972a}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1595">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1595">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1596">Resultados de la búsqueda</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1596">Search Results</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1597">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1597">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1598">Virtualiza</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1598">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1599">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1599">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1600">No aplicable: carpeta virtual</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1600">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1601">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1601">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1602">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1602">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1603">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1603">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1604">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1604">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1605">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1605">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1606">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1606">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SEARCH_MAPI"></span><span id="folderid_search_mapi"></span><dl> <span data-ttu-id="9cfe8-1607"><dt><strong>FOLDERID_SEARCH_MAPI</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1607"><dt><strong>FOLDERID_SEARCH_MAPI</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1608">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1608">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1609">{98ec0e18-2098-4d44-8644-66979315a281}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1609">{98ec0e18-2098-4d44-8644-66979315a281}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1610">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1610">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1611">Microsoft Office Outlook</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1611">Microsoft Office Outlook</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1612">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1612">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1613">Virtualiza</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1613">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1614">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1614">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1615">No aplicable: carpeta virtual</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1615">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1616">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1616">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1617">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1617">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1618">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1618">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1619">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1619">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1620">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1620">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1621">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1621">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SearchTemplates"></span><span id="folderid_searchtemplates"></span><span id="FOLDERID_SEARCHTEMPLATES"></span><dl> <span data-ttu-id="9cfe8-1622"><dt><strong>FOLDERID_SearchTemplates</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1622"><dt><strong>FOLDERID_SearchTemplates</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1623">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1623">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1624">{7E636BFE-DFA9-4D5E-B456-D7B39851D8A9}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1624">{7E636BFE-DFA9-4D5E-B456-D7B39851D8A9}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1625">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1625">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1626">Plantillas</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1626">Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1627">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1627">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1628">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1628">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1629">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1629">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1630">%LOCALAPPDATA%\Microsoft\Windows\ConnectedSearch\Templates</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1630">%LOCALAPPDATA%\Microsoft\Windows\ConnectedSearch\Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1631">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1631">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1632">Ninguno, valor introducido en Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1632">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1633">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1633">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1634">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1634">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1635">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1635">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1636">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1636">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SendTo"></span><span id="folderid_sendto"></span><span id="FOLDERID_SENDTO"></span><dl> <span data-ttu-id="9cfe8-1637"><dt><strong>FOLDERID_SendTo</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1637"><dt><strong>FOLDERID_SendTo</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1638">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1638">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1639">{8983036C-27C0-404B-8F08-102D10DCFD74}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1639">{8983036C-27C0-404B-8F08-102D10DCFD74}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1640">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1640">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1641">SendTo</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1641">SendTo</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1642">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1642">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1643">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1643">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1644">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1644">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1645">%APPDATA%\Microsoft\Windows\SendTo</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1645">%APPDATA%\Microsoft\Windows\SendTo</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1646">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1646">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1647">CSIDL_SENDTO</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1647">CSIDL_SENDTO</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1648">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1648">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1649">SendTo</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1649">SendTo</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1650">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1650">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1651">%USERPROFILE%\SendTo</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1651">%USERPROFILE%\SendTo</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SidebarDefaultParts"></span><span id="folderid_sidebardefaultparts"></span><span id="FOLDERID_SIDEBARDEFAULTPARTS"></span><dl> <span data-ttu-id="9cfe8-1652"><dt><strong>FOLDERID_SidebarDefaultParts</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1652"><dt><strong>FOLDERID_SidebarDefaultParts</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1653">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1653">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1654">{7B396E54-9EC5-4300-BE0A-2482EBAE1A26}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1654">{7B396E54-9EC5-4300-BE0A-2482EBAE1A26}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1655">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1655">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1656">Gadgets</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1656">Gadgets</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1657">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1657">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1658">NORMAL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1658">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1659">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1659">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1660">%ProgramFiles%\Windows Sidebar\Gadgets</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1660">%ProgramFiles%\Windows Sidebar\Gadgets</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1661">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1661">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1662">Ninguno, nuevo para Windows 7</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1662">None, new for Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1663">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1663">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1664">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1664">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1665">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1665">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1666">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1666">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SidebarParts"></span><span id="folderid_sidebarparts"></span><span id="FOLDERID_SIDEBARPARTS"></span><dl> <span data-ttu-id="9cfe8-1667"><dt><strong>FOLDERID_SidebarParts</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1667"><dt><strong>FOLDERID_SidebarParts</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1668">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1668">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1669">{A75D362E-50FC-4fb7-AC2C-A8BEAA314493}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1669">{A75D362E-50FC-4fb7-AC2C-A8BEAA314493}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1670">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1670">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1671">Gadgets</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1671">Gadgets</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1672">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1672">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1673">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1673">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1674">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1674">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1675">%LOCALAPPDATA%\Microsoft\Windows Sidebar\Gadgets</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1675">%LOCALAPPDATA%\Microsoft\Windows Sidebar\Gadgets</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1676">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1676">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1677">Ninguno, nuevo para Windows 7</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1677">None, new for Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1678">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1678">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1679">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1679">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1680">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1680">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1681">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1681">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SkyDrive"></span><span id="folderid_skydrive"></span><span id="FOLDERID_SKYDRIVE"></span><dl> <span data-ttu-id="9cfe8-1682"><dt><strong>FOLDERID_SkyDrive</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1682"><dt><strong>FOLDERID_SkyDrive</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1683">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1683">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1684">{A52BBA46-E9E1-435f-B3D9-28DAA648C0F6}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1684">{A52BBA46-E9E1-435f-B3D9-28DAA648C0F6}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1685">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1685">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1686">OneDrive</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1686">OneDrive</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1687">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1687">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1688">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1688">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1689">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1689">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1690">%USERPROFILE%\OneDrive</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1690">%USERPROFILE%\OneDrive</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1691">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1691">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1692">Ninguno, valor introducido en Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1692">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1693">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1693">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1694">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1694">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1695">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1695">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1696">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1696">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SkyDriveCameraRoll"></span><span id="folderid_skydrivecameraroll"></span><span id="FOLDERID_SKYDRIVECAMERAROLL"></span><dl> <span data-ttu-id="9cfe8-1697"><dt><strong>FOLDERID_SkyDriveCameraRoll</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1697"><dt><strong>FOLDERID_SkyDriveCameraRoll</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1698">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1698">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1699">{767E6811-49CB-4273-87C2-20F355E1085B}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1699">{767E6811-49CB-4273-87C2-20F355E1085B}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1700">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1700">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1701">Rollo de cámara</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1701">Camera Roll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1702">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1702">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1703">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1703">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1704">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1704">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1705">%USERPROFILE%\OneDrive\Pictures\Camera roll</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1705">%USERPROFILE%\OneDrive\Pictures\Camera Roll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1706">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1706">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1707">Ninguno, valor introducido en Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1707">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1708">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1708">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1709">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1709">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1710">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1710">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1711">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1711">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SkyDriveDocuments"></span><span id="folderid_skydrivedocuments"></span><span id="FOLDERID_SKYDRIVEDOCUMENTS"></span><dl> <span data-ttu-id="9cfe8-1712"><dt><strong>FOLDERID_SkyDriveDocuments</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1712"><dt><strong>FOLDERID_SkyDriveDocuments</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1713">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1713">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1714">{24D89E24-2F19-4534-9DDE-6A6671FBB8FE}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1714">{24D89E24-2F19-4534-9DDE-6A6671FBB8FE}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1715">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1715">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1716">Documentos</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1716">Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1717">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1717">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1718">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1718">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1719">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1719">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1720">%USERPROFILE%\OneDrive\Documents</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1720">%USERPROFILE%\OneDrive\Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1721">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1721">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1722">Ninguno, valor introducido en Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1722">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1723">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1723">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1724">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1724">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1725">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1725">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1726">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1726">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SkyDrivePictures"></span><span id="folderid_skydrivepictures"></span><span id="FOLDERID_SKYDRIVEPICTURES"></span><dl> <span data-ttu-id="9cfe8-1727"><dt><strong>FOLDERID_SkyDrivePictures</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1727"><dt><strong>FOLDERID_SkyDrivePictures</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1728">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1728">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1729">{339719B5-8C47-4894-94C2-D8F77ADD44A6}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1729">{339719B5-8C47-4894-94C2-D8F77ADD44A6}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1730">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1730">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1731">Imágenes</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1731">Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1732">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1732">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1733">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1733">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1734">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1734">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1735">%USERPROFILE%\OneDrive\Pictures</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1735">%USERPROFILE%\OneDrive\Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1736">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1736">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1737">Ninguno, valor introducido en Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1737">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1738">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1738">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1739">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1739">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1740">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1740">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1741">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1741">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_StartMenu"></span><span id="folderid_startmenu"></span><span id="FOLDERID_STARTMENU"></span><dl> <span data-ttu-id="9cfe8-1742"><dt><strong>FOLDERID_StartMenu</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1742"><dt><strong>FOLDERID_StartMenu</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1743">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1743">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1744">{625B53C3-AB48-4EC1-BA1F-A1EF4146FC19}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1744">{625B53C3-AB48-4EC1-BA1F-A1EF4146FC19}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1745">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1745">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1746">Menú Inicio</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1746">Start Menu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1747">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1747">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1748">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1748">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1749">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1749">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1750">Menú%APPDATA%\Microsoft\Windows\Start</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1750">%APPDATA%\Microsoft\Windows\Start Menu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1751">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1751">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1752">CSIDL_STARTMENU</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1752">CSIDL_STARTMENU</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1753">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1753">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1754">Menú Inicio</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1754">Start Menu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1755">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1755">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1756">Menú%USERPROFILE%\Start</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1756">%USERPROFILE%\Start Menu</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Startup"></span><span id="folderid_startup"></span><span id="FOLDERID_STARTUP"></span><dl> <span data-ttu-id="9cfe8-1757"><dt><strong>FOLDERID_Startup</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1757"><dt><strong>FOLDERID_Startup</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1758">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1758">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1759">{B97D20BB-F46A-4C97-BA10-5E3608430854}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1759">{B97D20BB-F46A-4C97-BA10-5E3608430854}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1760">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1760">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1761">Inicio</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1761">Startup</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1762">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1762">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1763">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1763">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1764">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1764">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1765">%APPDATA%\Microsoft\Windows\Start Inicio\programas\inicio</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1765">%APPDATA%\Microsoft\Windows\Start Menu\Programs\StartUp</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1766">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1766">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1767">CSIDL_STARTUP, CSIDL_ALTSTARTUP</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1767">CSIDL_STARTUP, CSIDL_ALTSTARTUP</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1768">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1768">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1769">Inicio</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1769">Startup</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1770">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1770">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1771">%USERPROFILE%\Start Inicio\programas\inicio</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1771">%USERPROFILE%\Start Menu\Programs\StartUp</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SyncManagerFolder"></span><span id="folderid_syncmanagerfolder"></span><span id="FOLDERID_SYNCMANAGERFOLDER"></span><dl> <span data-ttu-id="9cfe8-1772"><dt><strong>FOLDERID_SyncManagerFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1772"><dt><strong>FOLDERID_SyncManagerFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1773">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1773">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1774">{43668BF8-C14E-49B2-97C9-747784D784B7}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1774">{43668BF8-C14E-49B2-97C9-747784D784B7}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1775">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1775">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1776">Centro de sincronización</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1776">Sync Center</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1777">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1777">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1778">Virtualiza</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1778">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1779">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1779">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1780">No aplicable: carpeta virtual</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1780">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1781">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1781">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1782">Ninguno, valor introducido en Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1782">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1783">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1783">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1784">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1784">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1785">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1785">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1786">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1786">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SyncResultsFolder"></span><span id="folderid_syncresultsfolder"></span><span id="FOLDERID_SYNCRESULTSFOLDER"></span><dl> <span data-ttu-id="9cfe8-1787"><dt><strong>FOLDERID_SyncResultsFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1787"><dt><strong>FOLDERID_SyncResultsFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1788">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1788">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1789">{289a9a43-be44-4057-a41b-587a76d7e7f9}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1789">{289a9a43-be44-4057-a41b-587a76d7e7f9}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1790">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1790">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1791">Resultados de la sincronización</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1791">Sync Results</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1792">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1792">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1793">Virtualiza</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1793">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1794">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1794">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1795">No aplicable: carpeta virtual</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1795">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1796">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1796">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1797">Ninguno, valor introducido en Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1797">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1798">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1798">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1799">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1799">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1800">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1800">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1801">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1801">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SyncSetupFolder"></span><span id="folderid_syncsetupfolder"></span><span id="FOLDERID_SYNCSETUPFOLDER"></span><dl> <span data-ttu-id="9cfe8-1802"><dt><strong>FOLDERID_SyncSetupFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1802"><dt><strong>FOLDERID_SyncSetupFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1803">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1803">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1804">{0F214138-B1D3-4a90-BBA9-27CBC0C5389A}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1804">{0F214138-B1D3-4a90-BBA9-27CBC0C5389A}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1805">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1805">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1806">Configuración de sincronización</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1806">Sync Setup</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1807">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1807">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1808">Virtualiza</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1808">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1809">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1809">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1810">No aplicable: carpeta virtual</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1810">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1811">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1811">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1812">Ninguno, valor introducido en Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1812">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1813">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1813">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1814">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1814">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1815">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1815">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1816">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1816">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_System"></span><span id="folderid_system"></span><span id="FOLDERID_SYSTEM"></span><dl> <span data-ttu-id="9cfe8-1817"><dt><strong>FOLDERID_System</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1817"><dt><strong>FOLDERID_System</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1818">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1818">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1819">{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1819">{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1820">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1820">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1821">System32</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1821">System32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1822">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1822">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1823">FIXED</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1823">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1824">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1824">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1825">%windir%\system32</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1825">%windir%\system32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1826">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1826">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1827">CSIDL_SYSTEM</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1827">CSIDL_SYSTEM</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1828">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1828">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1829">system32</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1829">system32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1830">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1830">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1831">%windir%\system32</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1831">%windir%\system32</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SystemX86"></span><span id="folderid_systemx86"></span><span id="FOLDERID_SYSTEMX86"></span><dl> <span data-ttu-id="9cfe8-1832"><dt><strong>FOLDERID_SystemX86</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1832"><dt><strong>FOLDERID_SystemX86</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1833">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1833">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1834">{D65231B0-B2F1-4857-A4CE-A8E7C6EA7D27}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1834">{D65231B0-B2F1-4857-A4CE-A8E7C6EA7D27}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1835">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1835">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1836">System32</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1836">System32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1837">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1837">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1838">FIXED</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1838">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1839">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1839">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1840">%windir%\system32</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1840">%windir%\system32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1841">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1841">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1842">CSIDL_SYSTEMX86</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1842">CSIDL_SYSTEMX86</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1843">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1843">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1844">system32</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1844">system32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1845">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1845">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1846">%windir%\system32</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1846">%windir%\system32</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Templates"></span><span id="folderid_templates"></span><span id="FOLDERID_TEMPLATES"></span><dl> <span data-ttu-id="9cfe8-1847"><dt><strong>FOLDERID_Templates</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1847"><dt><strong>FOLDERID_Templates</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1848">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1848">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1849">{A63293E8-664E-48DB-A079-DF759E0509F7}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1849">{A63293E8-664E-48DB-A079-DF759E0509F7}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1850">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1850">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1851">Plantillas</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1851">Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1852">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1852">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1853">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1853">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1854">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1854">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1855">%APPDATA%\Microsoft\Windows\Templates</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1855">%APPDATA%\Microsoft\Windows\Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1856">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1856">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1857">CSIDL_TEMPLATES</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1857">CSIDL_TEMPLATES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1858">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1858">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1859">Plantillas</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1859">Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1860">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1860">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1861">%USERPROFILE%\Templates</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1861">%USERPROFILE%\Templates</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_TreeProperties"></span><span id="folderid_treeproperties"></span><span id="FOLDERID_TREEPROPERTIES"></span><dl> <span data-ttu-id="9cfe8-1862"><dt><strong>FOLDERID_TreeProperties</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1862"><dt><strong>FOLDERID_TreeProperties</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="9cfe8-1863">No se utiliza en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1863">Not used in Windows Vista.</span></span> <span data-ttu-id="9cfe8-1864">No se admite a partir de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1864">Unsupported as of Windows 7.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_UserPinned"></span><span id="folderid_userpinned"></span><span id="FOLDERID_USERPINNED"></span><dl> <span data-ttu-id="9cfe8-1865"><dt><strong>FOLDERID_UserPinned</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1865"><dt><strong>FOLDERID_UserPinned</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1866">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1866">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1867">{9E3995AB-1F9C-4F13-B827-48B24B6C7174}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1867">{9E3995AB-1F9C-4F13-B827-48B24B6C7174}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1868">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1868">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1869">Usuario anclado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1869">User Pinned</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1870">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1870">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1871">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1871">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1872">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1872">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1873">%APPDATA%\Microsoft\Internet Explorer\Quick Launch\User anclado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1873">%APPDATA%\Microsoft\Internet Explorer\Quick Launch\User Pinned</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1874">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1874">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1875">Ninguno, valor introducido en Windows 7</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1875">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1876">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1876">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1877">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1877">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1878">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1878">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1879">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1879">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_UserProfiles"></span><span id="folderid_userprofiles"></span><span id="FOLDERID_USERPROFILES"></span><dl> <span data-ttu-id="9cfe8-1880"><dt><strong>FOLDERID_UserProfiles</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1880"><dt><strong>FOLDERID_UserProfiles</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1881">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1881">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1882">{0762D272-C50A-4BB0-A382-697DCD729B80}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1882">{0762D272-C50A-4BB0-A382-697DCD729B80}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1883">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1883">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1884">Usuarios</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1884">Users</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1885">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1885">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1886">FIXED</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1886">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1887">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1887">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1888">%SystemDrive%\Users</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1888">%SystemDrive%\Users</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1889">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1889">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1890">Ninguno, nuevo para Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1890">None, new for Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1891">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1891">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1892">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1892">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1893">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1893">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1894">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1894">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_UserProgramFiles"></span><span id="folderid_userprogramfiles"></span><span id="FOLDERID_USERPROGRAMFILES"></span><dl> <span data-ttu-id="9cfe8-1895"><dt><strong>FOLDERID_UserProgramFiles</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1895"><dt><strong>FOLDERID_UserProgramFiles</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1896">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1896">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1897">{5CD7AEE2-2219-4A67-B85D-6C9CE15660CB}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1897">{5CD7AEE2-2219-4A67-B85D-6C9CE15660CB}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1898">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1898">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1899">Programas</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1899">Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1900">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1900">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1901">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1901">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1902">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1902">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1903">%LOCALAPPDATA%\Programs</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1903">%LOCALAPPDATA%\Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1904">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1904">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1905">Ninguno, valor introducido en Windows 7</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1905">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1906">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1906">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1907">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1907">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1908">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1908">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1909">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1909">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_UserProgramFilesCommon"></span><span id="folderid_userprogramfilescommon"></span><span id="FOLDERID_USERPROGRAMFILESCOMMON"></span><dl> <span data-ttu-id="9cfe8-1910"><dt><strong>FOLDERID_UserProgramFilesCommon</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1910"><dt><strong>FOLDERID_UserProgramFilesCommon</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1911">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1911">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1912">{BCBD3057-CA5C-4622-B42D-BC56DB0AE516}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1912">{BCBD3057-CA5C-4622-B42D-BC56DB0AE516}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1913">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1913">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1914">Programas</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1914">Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1915">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1915">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1916">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1916">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1917">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1917">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1918">%LOCALAPPDATA%\Programs\Common</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1918">%LOCALAPPDATA%\Programs\Common</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1919">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1919">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1920">Ninguno, valor introducido en Windows 7</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1920">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1921">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1921">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1922">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1922">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1923">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1923">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1924">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1924">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_UsersFiles"></span><span id="folderid_usersfiles"></span><span id="FOLDERID_USERSFILES"></span><dl> <span data-ttu-id="9cfe8-1925"><dt><strong>FOLDERID_UsersFiles</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1925"><dt><strong>FOLDERID_UsersFiles</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1926">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1926">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1927">{f3ce0f7c-4901-4acc-8648-d5d44b04ef8f}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1927">{f3ce0f7c-4901-4acc-8648-d5d44b04ef8f}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1928">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1928">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1929">Nombre completo del usuario (por ejemplo, Jean Philippe Bagel) que se especificó cuando se creó la cuenta de usuario.</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1929">The user's full name (for instance, Jean Philippe Bagel) entered when the user account was created.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1930">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1930">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1931">Virtualiza</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1931">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1932">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1932">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1933">No aplicable: carpeta virtual</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1933">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1934">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1934">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1935">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1935">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1936">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1936">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1937">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1937">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1938">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1938">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1939">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1939">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_UsersLibraries"></span><span id="folderid_userslibraries"></span><span id="FOLDERID_USERSLIBRARIES"></span><dl> <span data-ttu-id="9cfe8-1940"><dt><strong>FOLDERID_UsersLibraries</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1940"><dt><strong>FOLDERID_UsersLibraries</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1941">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1941">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1942">{A302545D-DEFF-464b-ABE8-61C8648D939B}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1942">{A302545D-DEFF-464b-ABE8-61C8648D939B}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1943">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1943">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1944">Bibliotecas</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1944">Libraries</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1945">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1945">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1946">Virtualiza</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1946">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1947">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1947">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1948">No aplicable: carpeta virtual</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1948">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1949">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1949">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1950">Ninguno, valor introducido en Windows 7</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1950">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1951">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1951">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1952">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1952">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1953">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1953">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1954">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1954">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Videos"></span><span id="folderid_videos"></span><span id="FOLDERID_VIDEOS"></span><dl> <span data-ttu-id="9cfe8-1955"><dt><strong>FOLDERID_Videos</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1955"><dt><strong>FOLDERID_Videos</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1956">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1956">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1957">{18989B1D-99B5-455B-841C-AB7C74E4DDFC}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1957">{18989B1D-99B5-455B-841C-AB7C74E4DDFC}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1958">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1958">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1959">Vídeos</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1959">Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1960">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1960">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1961">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1961">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1962">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1962">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1963">%USERPROFILE%\Videos</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1963">%USERPROFILE%\Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1964">CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1964">CSIDL</span></span></td>
<td><span data-ttu-id="9cfe8-1965">CSIDL_MYVIDEO</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1965">CSIDL_MYVIDEO</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1966">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1966">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1967">Mis vídeos</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1967">My Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1968">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1968">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1969">Vídeos de%USERPROFILE%\My Documentos\mis</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1969">%USERPROFILE%\My Documents\My Videos</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_VideosLibrary"></span><span id="folderid_videoslibrary"></span><span id="FOLDERID_VIDEOSLIBRARY"></span><dl> <span data-ttu-id="9cfe8-1970"><dt><strong>FOLDERID_VideosLibrary</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1970"><dt><strong>FOLDERID_VideosLibrary</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1971">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1971">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1972">{491E922F-5643-4AF4-A7EB-4E7A138D8174}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1972">{491E922F-5643-4AF4-A7EB-4E7A138D8174}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1973">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1973">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1974">Vídeos</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1974">Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1975">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1975">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1976">Perusuario</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1976">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1977">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1977">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1978">%APPDATA%\Microsoft\Windows\Libraries\Videos.library-ms</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1978">%APPDATA%\Microsoft\Windows\Libraries\Videos.library-ms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1979">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1979">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1980">Ninguno, valor introducido en Windows 7</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1980">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1981">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1981">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1982">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1982">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1983">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1983">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1984">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1984">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Windows"></span><span id="folderid_windows"></span><span id="FOLDERID_WINDOWS"></span><dl> <span data-ttu-id="9cfe8-1985"><dt><strong>FOLDERID_Windows</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="9cfe8-1985"><dt><strong>FOLDERID_Windows</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1986">GUID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1986">GUID</span></span></td>
<td><span data-ttu-id="9cfe8-1987">{F38BF404-1D43-42F2-9305-67DE0B28FC23}</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1987">{F38BF404-1D43-42F2-9305-67DE0B28FC23}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1988">Display Name (Nombre para mostrar)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1988">Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1989">Windows</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1989">Windows</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1990">Tipo de carpeta</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1990">Folder Type</span></span></td>
<td><span data-ttu-id="9cfe8-1991">FIXED</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1991">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1992">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1992">Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1993">DirWin</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1993">%windir%</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1994">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1994">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="9cfe8-1995">CSIDL_WINDOWS</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1995">CSIDL_WINDOWS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9cfe8-1996">Nombre para mostrar heredado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1996">Legacy Display Name</span></span></td>
<td><span data-ttu-id="9cfe8-1997">WINDOWS</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1997">WINDOWS</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9cfe8-1998">Ruta de acceso predeterminada heredada</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1998">Legacy Default Path</span></span></td>
<td><span data-ttu-id="9cfe8-1999">DirWin</span><span class="sxs-lookup"><span data-stu-id="9cfe8-1999">%windir%</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="9cfe8-2000">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2000">Remarks</span></span>

<span data-ttu-id="9cfe8-2001">La interpretación de ciertos valores de **KNOWNFOLDERID** depende de si la carpeta forma parte de una aplicación de 32 bits o de 64 bits y de si la aplicación se ejecuta en un sistema operativo de 32 bits o de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2001">The interpretation of certain **KNOWNFOLDERID** values depends on whether the folder is part of a 32-bit or 64-bit application and whether that application is running on a 32-bit or 64-bit operating system.</span></span> <span data-ttu-id="9cfe8-2002">Si la aplicación necesita distinguir entre, por ejemplo, **archivos de programa** y **archivos de programa (x86)**, debe usar la **KNOWNFOLDERID** adecuada para la situación.</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2002">If your application needs to distinguish between, for example, **Program Files** and **Program Files (x86)**, you must use the right **KNOWNFOLDERID** for the situation.</span></span>

<span data-ttu-id="9cfe8-2003">En las tablas siguientes se resume el uso de **KNOWNFOLDERID** en estos casos.</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2003">The following tables summarize the **KNOWNFOLDERID** use in those cases.</span></span>


<span data-ttu-id="9cfe8-2004">**FOLDERID \_ ProgramFiles**</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2004">**FOLDERID\_ProgramFiles**</span></span> 

| <span data-ttu-id="9cfe8-2005">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2005">Operating System</span></span> | <span data-ttu-id="9cfe8-2006">Application</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2006">Application</span></span> | <span data-ttu-id="9cfe8-2007">KNOWNFOLDERID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2007">KNOWNFOLDERID</span></span> | <span data-ttu-id="9cfe8-2008">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2008">Default Path</span></span> | <span data-ttu-id="9cfe8-2009">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2009">CSIDL Equivalent</span></span> |
|------------------|-------------|---------------|--------------|------------------|  
| <span data-ttu-id="9cfe8-2010">32 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2010">32 bit</span></span> | <span data-ttu-id="9cfe8-2011">32 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2011">32 bit</span></span> | <span data-ttu-id="9cfe8-2012">FOLDERID \_ ProgramFiles</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2012">FOLDERID\_ProgramFiles</span></span> | <span data-ttu-id="9cfe8-2013">% SystemDrive% \\ archivos de programa</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2013">%SystemDrive%\\Program Files</span></span> | <span data-ttu-id="9cfe8-2014">\_archivos de programa CSIDL \_</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2014">CSIDL\_PROGRAM\_FILES</span></span> |
| <span data-ttu-id="9cfe8-2015">32 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2015">32 bit</span></span> | <span data-ttu-id="9cfe8-2016">32 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2016">32 bit</span></span> | <span data-ttu-id="9cfe8-2017">FOLDERID \_ ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2017">FOLDERID\_ProgramFilesX86</span></span> | <span data-ttu-id="9cfe8-2018">% SystemDrive% \\ archivos de programa</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2018">%SystemDrive%\\Program Files</span></span> | <span data-ttu-id="9cfe8-2019">CSIDL \_ Program \_ FILESX86</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2019">CSIDL\_PROGRAM\_FILESX86</span></span> |
| <span data-ttu-id="9cfe8-2020">32 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2020">32 bit</span></span> | <span data-ttu-id="9cfe8-2021">32 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2021">32 bit</span></span> | <span data-ttu-id="9cfe8-2022">FOLDERID \_ ProgramFilesX64 (no se admite en sistemas operativos de 32 bits)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2022">FOLDERID\_ProgramFilesX64 (not supported under 32-bit operating systems)</span></span> | <span data-ttu-id="9cfe8-2023">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2023">Not applicable</span></span> | <span data-ttu-id="9cfe8-2024">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2024">Not applicable</span></span> |
| <span data-ttu-id="9cfe8-2025">64 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2025">64 bit</span></span> | <span data-ttu-id="9cfe8-2026">64 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2026">64 bit</span></span> | <span data-ttu-id="9cfe8-2027">FOLDERID \_ ProgramFiles</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2027">FOLDERID\_ProgramFiles</span></span> | <span data-ttu-id="9cfe8-2028">% SystemDrive% \\ archivos de programa</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2028">%SystemDrive%\\Program Files</span></span> | <span data-ttu-id="9cfe8-2029">\_archivos de programa CSIDL \_</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2029">CSIDL\_PROGRAM\_FILES</span></span> |
| <span data-ttu-id="9cfe8-2030">64 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2030">64 bit</span></span> | <span data-ttu-id="9cfe8-2031">64 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2031">64 bit</span></span> | <span data-ttu-id="9cfe8-2032">FOLDERID \_ ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2032">FOLDERID\_ProgramFilesX86</span></span> | <span data-ttu-id="9cfe8-2033">% SystemDrive% \\ archivos de programa (x86)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2033">%SystemDrive%\\Program Files (x86)</span></span> | <span data-ttu-id="9cfe8-2034">CSIDL \_ Program \_ FILESX86</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2034">CSIDL\_PROGRAM\_FILESX86</span></span> |
| <span data-ttu-id="9cfe8-2035">64 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2035">64 bit</span></span> | <span data-ttu-id="9cfe8-2036">64 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2036">64 bit</span></span> | <span data-ttu-id="9cfe8-2037">FOLDERID \_ ProgramFilesX64</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2037">FOLDERID\_ProgramFilesX64</span></span> | <span data-ttu-id="9cfe8-2038">% SystemDrive% \\ archivos de programa</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2038">%SystemDrive%\\Program Files</span></span> | <span data-ttu-id="9cfe8-2039">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2039">None</span></span> |
| <span data-ttu-id="9cfe8-2040">64 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2040">64 bit</span></span> | <span data-ttu-id="9cfe8-2041">32 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2041">32 bit</span></span> | <span data-ttu-id="9cfe8-2042">FOLDERID \_ ProgramFiles</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2042">FOLDERID\_ProgramFiles</span></span> | <span data-ttu-id="9cfe8-2043">% SystemDrive% \\ archivos de programa (x86)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2043">%SystemDrive%\\Program Files (x86)</span></span> | <span data-ttu-id="9cfe8-2044">\_archivos de programa CSIDL \_</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2044">CSIDL\_PROGRAM\_FILES</span></span> |
| <span data-ttu-id="9cfe8-2045">64 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2045">64 bit</span></span> | <span data-ttu-id="9cfe8-2046">32 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2046">32 bit</span></span> | <span data-ttu-id="9cfe8-2047">FOLDERID \_ ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2047">FOLDERID\_ProgramFilesX86</span></span> | <span data-ttu-id="9cfe8-2048">% SystemDrive% \\ archivos de programa (x86)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2048">%SystemDrive%\\Program Files (x86)</span></span> | <span data-ttu-id="9cfe8-2049">CSIDL \_ Program \_ FILESX86</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2049">CSIDL\_PROGRAM\_FILESX86</span></span> |
| <span data-ttu-id="9cfe8-2050">64 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2050">64 bit</span></span> | <span data-ttu-id="9cfe8-2051">32 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2051">32 bit</span></span> | <span data-ttu-id="9cfe8-2052">FOLDERID \_ ProgramFilesX64 (no se admite para aplicaciones de 32 bits)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2052">FOLDERID\_ProgramFilesX64 (not supported for 32-bit applications)</span></span> | <span data-ttu-id="9cfe8-2053">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2053">Not applicable</span></span> | <span data-ttu-id="9cfe8-2054">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2054">Not applicable</span></span> |


<span data-ttu-id="9cfe8-2055">**FOLDERID \_ ProgramFilesCommon**</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2055">**FOLDERID\_ProgramFilesCommon**</span></span>

| <span data-ttu-id="9cfe8-2056">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2056">Operating System</span></span> | <span data-ttu-id="9cfe8-2057">Application</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2057">Application</span></span> | <span data-ttu-id="9cfe8-2058">KNOWNFOLDERID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2058">KNOWNFOLDERID</span></span> | <span data-ttu-id="9cfe8-2059">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2059">Default Path</span></span> | <span data-ttu-id="9cfe8-2060">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2060">CSIDL Equivalent</span></span> |
|------------------|-------------|---------------|--------------|------------------|  
| <span data-ttu-id="9cfe8-2061">32 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2061">32 bit</span></span> | <span data-ttu-id="9cfe8-2062">32 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2062">32 bit</span></span> | <span data-ttu-id="9cfe8-2063">FOLDERID \_ ProgramFilesCommon</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2063">FOLDERID\_ProgramFilesCommon</span></span> | <span data-ttu-id="9cfe8-2064">% ProgramFiles% \\ archivos comunes</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2064">%ProgramFiles%\\Common Files</span></span> | <span data-ttu-id="9cfe8-2065">CSIDL \_ archivos de programa \_ \_ comunes</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2065">CSIDL\_PROGRAM\_FILES\_COMMON</span></span> |
| <span data-ttu-id="9cfe8-2066">32 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2066">32 bit</span></span> | <span data-ttu-id="9cfe8-2067">32 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2067">32 bit</span></span> | <span data-ttu-id="9cfe8-2068">FOLDERID \_ ProgramFilesCommonX86</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2068">FOLDERID\_ProgramFilesCommonX86</span></span> | <span data-ttu-id="9cfe8-2069">% ProgramFiles% \\ archivos comunes</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2069">%ProgramFiles%\\Common Files</span></span> | <span data-ttu-id="9cfe8-2070">CSIDL \_ archivos de programa \_ \_ COMMONX86</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2070">CSIDL\_PROGRAM\_FILES\_COMMONX86</span></span> |
| <span data-ttu-id="9cfe8-2071">32 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2071">32 bit</span></span> | <span data-ttu-id="9cfe8-2072">32 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2072">32 bit</span></span> | <span data-ttu-id="9cfe8-2073">FOLDERID \_ ProgramFilesCommonX64 (sin definir)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2073">FOLDERID\_ProgramFilesCommonX64 (undefined)</span></span> | <span data-ttu-id="9cfe8-2074">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2074">Not applicable</span></span> | <span data-ttu-id="9cfe8-2075">No aplicable</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2075">Not applicable</span></span> |
| <span data-ttu-id="9cfe8-2076">64 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2076">64 bit</span></span> | <span data-ttu-id="9cfe8-2077">64 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2077">64 bit</span></span> | <span data-ttu-id="9cfe8-2078">FOLDERID \_ ProgramFilesCommon</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2078">FOLDERID\_ProgramFilesCommon</span></span> | <span data-ttu-id="9cfe8-2079">% ProgramFiles% \\ archivos comunes</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2079">%ProgramFiles%\\Common Files</span></span> | <span data-ttu-id="9cfe8-2080">CSIDL \_ archivos de programa \_ \_ comunes</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2080">CSIDL\_PROGRAM\_FILES\_COMMON</span></span> |
| <span data-ttu-id="9cfe8-2081">64 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2081">64 bit</span></span> | <span data-ttu-id="9cfe8-2082">64 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2082">64 bit</span></span> | <span data-ttu-id="9cfe8-2083">FOLDERID \_ ProgramFilesCommonX86</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2083">FOLDERID\_ProgramFilesCommonX86</span></span> | <span data-ttu-id="9cfe8-2084">% Archivos de programa (x86)% \\ Common files</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2084">%ProgramFiles(x86)%\\Common Files</span></span> | <span data-ttu-id="9cfe8-2085">CSIDL \_ archivos de programa \_ \_ COMMONX86</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2085">CSIDL\_PROGRAM\_FILES\_COMMONX86</span></span> |
| <span data-ttu-id="9cfe8-2086">64 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2086">64 bit</span></span> | <span data-ttu-id="9cfe8-2087">64 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2087">64 bit</span></span> | <span data-ttu-id="9cfe8-2088">FOLDERID \_ ProgramFilesCommonX64</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2088">FOLDERID\_ProgramFilesCommonX64</span></span> | <span data-ttu-id="9cfe8-2089">% ProgramFiles% \\ archivos comunes</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2089">%ProgramFiles%\\Common Files</span></span> | <span data-ttu-id="9cfe8-2090">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2090">None</span></span> |
| <span data-ttu-id="9cfe8-2091">64 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2091">64 bit</span></span> | <span data-ttu-id="9cfe8-2092">32 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2092">32 bit</span></span> | <span data-ttu-id="9cfe8-2093">FOLDERID \_ ProgramFilesCommon</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2093">FOLDERID\_ProgramFilesCommon</span></span> | <span data-ttu-id="9cfe8-2094">% Archivos de programa (x86)% \\ Common files</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2094">%ProgramFiles(x86)%\\Common Files</span></span> | <span data-ttu-id="9cfe8-2095">CSIDL \_ archivos de programa \_ \_ comunes</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2095">CSIDL\_PROGRAM\_FILES\_COMMON</span></span> |
| <span data-ttu-id="9cfe8-2096">64 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2096">64 bit</span></span> | <span data-ttu-id="9cfe8-2097">32 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2097">32 bit</span></span> | <span data-ttu-id="9cfe8-2098">FOLDERID \_ ProgramFilesCommonX86</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2098">FOLDERID\_ProgramFilesCommonX86</span></span> | <span data-ttu-id="9cfe8-2099">% Archivos de programa (x86)% \\ Common files</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2099">%ProgramFiles(x86)%\\Common Files</span></span> | <span data-ttu-id="9cfe8-2100">CSIDL \_ archivos de programa \_ \_ COMMONX86</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2100">CSIDL\_PROGRAM\_FILES\_COMMONX86</span></span> |
| <span data-ttu-id="9cfe8-2101">64 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2101">64 bit</span></span> | <span data-ttu-id="9cfe8-2102">32 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2102">32 bit</span></span> | <span data-ttu-id="9cfe8-2103">FOLDERID \_ ProgramFilesCommonX64</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2103">FOLDERID\_ProgramFilesCommonX64</span></span> | <span data-ttu-id="9cfe8-2104">% ProgramFiles% \\ archivos comunes</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2104">%ProgramFiles%\\Common Files</span></span> | <span data-ttu-id="9cfe8-2105">Ninguno</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2105">None</span></span> |


<span data-ttu-id="9cfe8-2106">**\_Sistema FOLDERID**</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2106">**FOLDERID\_System**</span></span>

| <span data-ttu-id="9cfe8-2107">Sistema operativo</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2107">Operating System</span></span> | <span data-ttu-id="9cfe8-2108">Application</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2108">Application</span></span> | <span data-ttu-id="9cfe8-2109">KNOWNFOLDERID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2109">KNOWNFOLDERID</span></span> | <span data-ttu-id="9cfe8-2110">Valor predeterminado Path</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2110">Default Path</span></span> | <span data-ttu-id="9cfe8-2111">Equivalentes de CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2111">CSIDL Equivalent</span></span> |
|------------------|-------------|---------------|--------------|------------------|  
| <span data-ttu-id="9cfe8-2112">32 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2112">32 bit</span></span> | <span data-ttu-id="9cfe8-2113">32 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2113">32 bit</span></span> | <span data-ttu-id="9cfe8-2114">\_Sistema FOLDERID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2114">FOLDERID\_System</span></span> | <span data-ttu-id="9cfe8-2115">% WINDIR% \\ system32</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2115">%windir%\\system32</span></span> | <span data-ttu-id="9cfe8-2116">\_sistema CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2116">CSIDL\_SYSTEM</span></span> |
| <span data-ttu-id="9cfe8-2117">32 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2117">32 bit</span></span> | <span data-ttu-id="9cfe8-2118">32 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2118">32 bit</span></span> | <span data-ttu-id="9cfe8-2119">FOLDERID \_ SystemX86</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2119">FOLDERID\_SystemX86</span></span> | <span data-ttu-id="9cfe8-2120">% WINDIR% \\ system32</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2120">%windir%\\system32</span></span> | <span data-ttu-id="9cfe8-2121">CSIDL \_ SYSTEMX86</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2121">CSIDL\_SYSTEMX86</span></span> |
| <span data-ttu-id="9cfe8-2122">64 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2122">64 bit</span></span> | <span data-ttu-id="9cfe8-2123">64 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2123">64 bit</span></span> | <span data-ttu-id="9cfe8-2124">\_Sistema FOLDERID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2124">FOLDERID\_System</span></span> | <span data-ttu-id="9cfe8-2125">% WINDIR% \\ system32</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2125">%windir%\\system32</span></span> | <span data-ttu-id="9cfe8-2126">\_sistema CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2126">CSIDL\_SYSTEM</span></span> |
| <span data-ttu-id="9cfe8-2127">64 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2127">64 bit</span></span> | <span data-ttu-id="9cfe8-2128">64 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2128">64 bit</span></span> | <span data-ttu-id="9cfe8-2129">FOLDERID \_ SystemX86</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2129">FOLDERID\_SystemX86</span></span> | <span data-ttu-id="9cfe8-2130">% WINDIR% \\ SysWow64</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2130">%windir%\\syswow64</span></span> | <span data-ttu-id="9cfe8-2131">CSIDL \_ SYSTEMX86</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2131">CSIDL\_SYSTEMX86</span></span> |
| <span data-ttu-id="9cfe8-2132">64 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2132">64 bit</span></span> | <span data-ttu-id="9cfe8-2133">32 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2133">32 bit</span></span> | <span data-ttu-id="9cfe8-2134">\_Sistema FOLDERID</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2134">FOLDERID\_System</span></span> | <span data-ttu-id="9cfe8-2135">% WINDIR% \\ system32</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2135">%windir%\\system32</span></span> | <span data-ttu-id="9cfe8-2136">\_sistema CSIDL</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2136">CSIDL\_SYSTEM</span></span> |
| <span data-ttu-id="9cfe8-2137">64 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2137">64 bit</span></span> | <span data-ttu-id="9cfe8-2138">32 bits</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2138">32 bit</span></span> | <span data-ttu-id="9cfe8-2139">FOLDERID \_ SystemX86</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2139">FOLDERID\_SystemX86</span></span> | <span data-ttu-id="9cfe8-2140">% WINDIR% \\ SysWow64</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2140">%windir%\\syswow64</span></span> | <span data-ttu-id="9cfe8-2141">CSIDL \_ SYSTEMX86</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2141">CSIDL\_SYSTEMX86</span></span> |


<span data-ttu-id="9cfe8-2142">Hemos usado cadenas de entorno para proporcionar rutas de acceso genéricas en este tema.</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2142">We have used environment strings to provide generic paths throughout this topic.</span></span> <span data-ttu-id="9cfe8-2143">En las tablas siguientes se proporcionan ejemplos de las rutas de acceso que representan esas cadenas de entorno.</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2143">The following tables give examples of the paths those environment strings represent.</span></span> <span data-ttu-id="9cfe8-2144">En algunos casos, es posible que estas rutas de acceso no coincidan con las de un equipo determinado debido a las elecciones realizadas durante la instalación o la redirección de carpetas posterior.</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2144">In some cases, these paths might not match those on a particular computer because of choices made during installation or later folder redirection.</span></span> <span data-ttu-id="9cfe8-2145">Tenga en cuenta que algunas rutas de acceso han cambiado en Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2145">Note that some paths have changed for Windows Vista.</span></span>


<span data-ttu-id="9cfe8-2146">**Windows Vista y versiones posteriores**</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2146">**Windows Vista and later**</span></span>

| <span data-ttu-id="9cfe8-2147">Cadena de entorno</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2147">Environment String</span></span> | <span data-ttu-id="9cfe8-2148">Ruta de acceso de ejemplo</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2148">Example Path</span></span> |
|--------------------|--------------|
| <span data-ttu-id="9cfe8-2149">%ALLUSERSPROFILE%</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2149">%ALLUSERSPROFILE%</span></span> | <span data-ttu-id="9cfe8-2150">C: \\ ProgramData</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2150">C:\\ProgramData</span></span> |
| <span data-ttu-id="9cfe8-2151">%APPDATA%</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2151">%APPDATA%</span></span> | <span data-ttu-id="9cfe8-2152">C: \\ usuarios \\ *nombre de usuario* \\ AppData \\ roaming</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2152">C:\\Users\\*username*\\AppData\\Roaming</span></span> |
| <span data-ttu-id="9cfe8-2153">LOCALAPPDATA</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2153">%LOCALAPPDATA%</span></span> | <span data-ttu-id="9cfe8-2154">C: \\ usuarios \\ *nombre de usuario* \\ AppData \\ local</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2154">C:\\Users\\*username*\\AppData\\Local</span></span> |
| <span data-ttu-id="9cfe8-2155">%ProgramData%</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2155">%ProgramData%</span></span> | <span data-ttu-id="9cfe8-2156">C: \\ ProgramData</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2156">C:\\ProgramData</span></span> |
| <span data-ttu-id="9cfe8-2157">%ProgramFiles%</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2157">%ProgramFiles%</span></span> | <span data-ttu-id="9cfe8-2158">C: \\ archivos de programa</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2158">C:\\Program Files</span></span> |
| <span data-ttu-id="9cfe8-2159">%ProgramFiles(x86)%</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2159">%ProgramFiles(x86)%</span></span> | <span data-ttu-id="9cfe8-2160">C: \\ archivos de programa (x86)</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2160">C:\\Program Files (x86)</span></span> |
| <span data-ttu-id="9cfe8-2161">PÚBLICA</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2161">%PUBLIC%</span></span> | <span data-ttu-id="9cfe8-2162">C: \\ usuarios \\ públicos</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2162">C:\\Users\\Public</span></span> |
| <span data-ttu-id="9cfe8-2163">%SystemDrive%</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2163">%SystemDrive%</span></span> | <span data-ttu-id="9cfe8-2164">C.</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2164">C:</span></span> |
| <span data-ttu-id="9cfe8-2165">%USERPROFILE%</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2165">%USERPROFILE%</span></span> | <span data-ttu-id="9cfe8-2166">C: \\ usuarios \\ *nombre de usuario*</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2166">C:\\Users\\*username*</span></span> |
| <span data-ttu-id="9cfe8-2167">DirWin</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2167">%windir%</span></span> | <span data-ttu-id="9cfe8-2168">C: \\ Windows</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2168">C:\\Windows</span></span> |


<span data-ttu-id="9cfe8-2169">**Windows XP y versiones anteriores**</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2169">**Windows XP and earlier**</span></span>

| <span data-ttu-id="9cfe8-2170">Cadena de entorno</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2170">Environment String</span></span> | <span data-ttu-id="9cfe8-2171">Ruta de acceso de ejemplo</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2171">Example Path</span></span> |
|--------------------|--------------|
| <span data-ttu-id="9cfe8-2172">%ALLUSERSPROFILE%</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2172">%ALLUSERSPROFILE%</span></span> | <span data-ttu-id="9cfe8-2173">C: \\ Documents and Settings \\ All Users</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2173">C:\\Documents and Settings\\All Users</span></span> |
| <span data-ttu-id="9cfe8-2174">%APPDATA%</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2174">%APPDATA%</span></span> | <span data-ttu-id="9cfe8-2175">C: \\ Documents and Settings \\ *nombre de usuario* \\ datos de aplicación</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2175">C:\\Documents and Settings\\*username*\\Application Data</span></span> |
| <span data-ttu-id="9cfe8-2176">%ProgramFiles%</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2176">%ProgramFiles%</span></span> | <span data-ttu-id="9cfe8-2177">C: \\ archivos de programa</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2177">C:\\Program Files</span></span> |
| <span data-ttu-id="9cfe8-2178">%SystemDrive%</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2178">%SystemDrive%</span></span> | <span data-ttu-id="9cfe8-2179">C.</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2179">C:</span></span> |
| <span data-ttu-id="9cfe8-2180">%USERPROFILE%</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2180">%USERPROFILE%</span></span> | <span data-ttu-id="9cfe8-2181">C: \\ Documents and Settings \\ *nombre de usuario*</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2181">C:\\Documents and Settings\\*username*</span></span> |
| <span data-ttu-id="9cfe8-2182">DirWin</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2182">%windir%</span></span> | <span data-ttu-id="9cfe8-2183">C: \\ Windows</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2183">C:\\Windows</span></span> |


## <a name="requirements"></a><span data-ttu-id="9cfe8-2184">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2184">Requirements</span></span>


| <span data-ttu-id="9cfe8-2185">Requisito</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2185">Requirement</span></span> | <span data-ttu-id="9cfe8-2186">Value</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2186">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cfe8-2187">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2187">Header</span></span><br/> | <dl> <span data-ttu-id="9cfe8-2188"><dt>Knownfolders. h</dt></span><span class="sxs-lookup"><span data-stu-id="9cfe8-2188"><dt>Knownfolders.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cfe8-2189">Vea también</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cfe8-2190">**CSIDL**</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2190">**CSIDL**</span></span>](csidl.md)
</dt> <dt>

[<span data-ttu-id="9cfe8-2191">Carpetas conocidas</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2191">Known Folders</span></span>](known-folders.md)
</dt> <dt>

[<span data-ttu-id="9cfe8-2192">Trabajar con carpetas conocidas en aplicaciones</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2192">Working with Known Folders in Applications</span></span>](working-with-known-folders.md)
</dt> <dt>

[<span data-ttu-id="9cfe8-2193">Cómo extender carpetas conocidas con carpetas personalizadas</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2193">How to Extend Known Folders with Custom Folders</span></span>](how-to-extend-known-folders-with-custom-folders.md)
</dt> <dt>

<span data-ttu-id="9cfe8-2194">[Ejemplo de carpetas conocidas](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9cfe8-2194">[Known Folders Sample](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))</span></span>
</dt> </dl>

 

 
