---
description: Puede ocultar el botón Cancelar que se usa para cancelar una instalación mediante una opción de línea de comandos, la API de Windows Installer o una acción personalizada. El botón Cancelar se puede ocultar para parte o para toda la instalación, en función del método que use.
ms.assetid: de2bb788-0d19-4818-8038-cae6000b38c4
title: Ocultar el botón Cancelar durante una instalación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e55658bc69fe81b83b13d6c6ee7da84db77ad466
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652826"
---
# <a name="hiding-the-cancel-button-during-an-installation"></a><span data-ttu-id="3c580-104">Ocultar el botón Cancelar durante una instalación</span><span class="sxs-lookup"><span data-stu-id="3c580-104">Hiding the Cancel Button During an Installation</span></span>

<span data-ttu-id="3c580-105">Puede ocultar el botón **Cancelar** que se usa para cancelar una instalación mediante una opción de línea de comandos, la API de Windows Installer o una acción personalizada.</span><span class="sxs-lookup"><span data-stu-id="3c580-105">You can hide the **Cancel** button that is used to cancel an installation by using a command-line option, the Windows Installer API, or a custom action.</span></span> <span data-ttu-id="3c580-106">El botón **Cancelar** se puede ocultar para parte o para toda la instalación, en función del método que use.</span><span class="sxs-lookup"><span data-stu-id="3c580-106">The **Cancel** button can be hidden for part or all of the installation depending on which method you use.</span></span>

## <a name="hiding-the-cancel-button-from-the-command-line"></a><span data-ttu-id="3c580-107">Ocultar el botón Cancelar desde la línea de comandos</span><span class="sxs-lookup"><span data-stu-id="3c580-107">Hiding the Cancel Button from the Command Line</span></span>

<span data-ttu-id="3c580-108">El botón **Cancelar** se puede ocultar durante la instalación mediante la opción de línea de comandos (!).</span><span class="sxs-lookup"><span data-stu-id="3c580-108">The **Cancel** button can be hidden during installation by using the (!) command-line option.</span></span> <span data-ttu-id="3c580-109">Esto solo se puede hacer para una instalación básica del nivel de interfaz de usuario (/QB).</span><span class="sxs-lookup"><span data-stu-id="3c580-109">This can only be done for a basic user interface level installation (/qb).</span></span> <span data-ttu-id="3c580-110">El botón **Cancelar** está oculto para toda la instalación.</span><span class="sxs-lookup"><span data-stu-id="3c580-110">The **Cancel** button is hidden for the entire installation.</span></span> <span data-ttu-id="3c580-111">Para obtener más información, vea [Opciones de la línea de comandos](command-line-options.md) y niveles de la [interfaz de usuario](user-interface-levels.md).</span><span class="sxs-lookup"><span data-stu-id="3c580-111">For more information, see [Command-Line Options](command-line-options.md) and [User Interface Levels](user-interface-levels.md).</span></span> <span data-ttu-id="3c580-112">La siguiente línea de comandos oculta el botón **Cancelar** e instala Example.msi.</span><span class="sxs-lookup"><span data-stu-id="3c580-112">The following command line hides the **Cancel** button and installs Example.msi.</span></span>

<span data-ttu-id="3c580-113">**msiexec/I example.msi/QB!**</span><span class="sxs-lookup"><span data-stu-id="3c580-113">**msiexec /I example.msi /qb!**</span></span>

## <a name="hiding-the-cancel-button-from-an-application-or-script"></a><span data-ttu-id="3c580-114">Ocultar el botón Cancelar desde una aplicación o un script</span><span class="sxs-lookup"><span data-stu-id="3c580-114">Hiding the Cancel Button from an Application or Script</span></span>

<span data-ttu-id="3c580-115">Puede escribir una aplicación o un script para ocultar el botón **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="3c580-115">You can write an application or script to hide the **Cancel** button.</span></span> <span data-ttu-id="3c580-116">Esto solo se puede hacer para una instalación básica de nivel de interfaz de usuario, de modo que el botón **Cancelar** esté oculto para toda la instalación.</span><span class="sxs-lookup"><span data-stu-id="3c580-116">This can only be done for a basic UI level installation so that the **Cancel** button is hidden for the entire installation.</span></span>

<span data-ttu-id="3c580-117">Para ocultar el botón Cancelar de una aplicación, establezca INSTALLUILEVEL \_ HIDECANCEL al llamar a [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui).</span><span class="sxs-lookup"><span data-stu-id="3c580-117">To hide the Cancel button from an application, set INSTALLUILEVEL\_HIDECANCEL when calling [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui).</span></span> <span data-ttu-id="3c580-118">En el ejemplo siguiente se oculta el botón **Cancelar** y se instala Example.msi.</span><span class="sxs-lookup"><span data-stu-id="3c580-118">The following example hides the **Cancel** button and installs Example.msi.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <Shellapi.h>
#include <msi.h>
#include <Msiquery.h>
#include <tchar.h>
#pragma comment(lib, "msi.lib")

int main()  
{

INSTALLUILEVEL uiPrevLevel = MsiSetInternalUI( INSTALLUILEVEL(INSTALLUILEVEL_BASIC | INSTALLUILEVEL_HIDECANCEL), 0); 
UINT uiStat = MsiInstallProduct(_T("example.msi"), NULL);

return 0;  
}
```



<span data-ttu-id="3c580-119">Para ocultar el botón **Cancelar** de la secuencia de comandos, agregue msiUILevelHideCancel a la propiedad [**elemento uilevel**](installer-uilevel.md) del [**objeto Installer**](installer-object.md).</span><span class="sxs-lookup"><span data-stu-id="3c580-119">To hide the **Cancel** button from script, add msiUILevelHideCancel to the [**UILevel**](installer-uilevel.md) property of the [**Installer Object**](installer-object.md).</span></span> <span data-ttu-id="3c580-120">El siguiente ejemplo de VBScript oculta el botón **Cancelar** e instala Example.msi.</span><span class="sxs-lookup"><span data-stu-id="3c580-120">The following VBScript sample hides the **Cancel** button and installs Example.msi.</span></span>


```VB
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.UILevel = msiUILevelBasic + msiUILevelHideCancel
Installer.InstallProduct "example.msi"
```



## <a name="hiding-the-cancel-button-for-parts-of-an-installation-using-a-custom-action"></a><span data-ttu-id="3c580-121">Ocultar el botón Cancelar para las partes de una instalación mediante una acción personalizada</span><span class="sxs-lookup"><span data-stu-id="3c580-121">Hiding the Cancel Button for Parts of an Installation Using a Custom Action</span></span>

<span data-ttu-id="3c580-122">La instalación puede ocultar y mostrar el botón **Cancelar** durante partes de una instalación mediante el envío de un \_ mensaje de INSTALLMESSAGE COMMONDATA mediante una acción personalizada o scripts de dll.</span><span class="sxs-lookup"><span data-stu-id="3c580-122">Your installation can hide and unhide the **Cancel** button during parts of an installation by sending an INSTALLMESSAGE\_COMMONDATA message using a DLL custom action or scripts.</span></span> <span data-ttu-id="3c580-123">Para obtener más información, consulte [bibliotecas de vínculos dinámicos](dynamic-link-libraries.md), [scripts](scripts.md), [acciones personalizadas](custom-actions.md)y [envío de mensajes a Windows Installer mediante MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).</span><span class="sxs-lookup"><span data-stu-id="3c580-123">For more information, see [Dynamic-Link Libraries](dynamic-link-libraries.md), [Scripts](scripts.md), [Custom Actions](custom-actions.md), and [Sending Messages to Windows Installer Using MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).</span></span>

<span data-ttu-id="3c580-124">Una llamada a una acción personalizada debe proporcionar un registro.</span><span class="sxs-lookup"><span data-stu-id="3c580-124">A call to a custom action must provide a record.</span></span> <span data-ttu-id="3c580-125">El campo 1 de este registro debe contener el valor 2 (dos) para especificar el botón **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="3c580-125">Field 1 of this record must contain the value 2 (two) to specify the **Cancel** button.</span></span> <span data-ttu-id="3c580-126">El campo 2 debe contener el valor 0 o 1.</span><span class="sxs-lookup"><span data-stu-id="3c580-126">Field 2 must contain either the value 0 or 1.</span></span> <span data-ttu-id="3c580-127">Un valor de 0 en el campo 2 oculta el botón y un valor de 1 en el campo 2 Desoculta el botón.</span><span class="sxs-lookup"><span data-stu-id="3c580-127">A value of 0 in Field 2 hides the button and a value of 1 in Field 2 unhides the button.</span></span> <span data-ttu-id="3c580-128">Tenga en cuenta que la asignación de un registro de tamaño 2 con [**MsiCreateRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord) proporciona los campos 0, 1 y 2.</span><span class="sxs-lookup"><span data-stu-id="3c580-128">Note that allocating a record of size 2 with [**MsiCreateRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord) provides fields 0, 1, and 2.</span></span>

<span data-ttu-id="3c580-129">La siguiente acción personalizada del archivo DLL de ejemplo oculta el botón **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="3c580-129">The following sample DLL custom action hides the **Cancel** button.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#include <Shellapi.h>
#include <msi.h>
#include <Msiquery.h>

UINT __stdcall HideCancelButton(MSIHANDLE hInstall)
{
    PMSIHANDLE hRecord = MsiCreateRecord(2);
    if ( !hRecord)
        return ERROR_INSTALL_FAILURE;

    if (ERROR_SUCCESS != MsiRecordSetInteger(hRecord, 1, 2)
     || ERROR_SUCCESS != MsiRecordSetInteger(hRecord, 2, 0))
        return ERROR_INSTALL_FAILURE;

    MsiProcessMessage(hInstall, INSTALLMESSAGE_COMMONDATA, hRecord);

    return ERROR_SUCCESS;
}
```



<span data-ttu-id="3c580-130">La acción personalizada de VBScript siguiente oculta el botón **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="3c580-130">The following VBScript Custom Action hides the **Cancel** button.</span></span>


```VB
Function HideCancelButton()

    Dim Record
    Set Record = Installer.CreateRecord(2)

    Record.IntegerData(1) = 2
    Record.IntegerData(2) = 0

    Session.Message msiMessageTypeCommonData, Record
 
    ' return success
    HideCancelButton = 1
    Exit Function

End Function
```



 

 



