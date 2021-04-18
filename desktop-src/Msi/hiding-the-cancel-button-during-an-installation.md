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
# <a name="hiding-the-cancel-button-during-an-installation"></a>Ocultar el botón Cancelar durante una instalación

Puede ocultar el botón **Cancelar** que se usa para cancelar una instalación mediante una opción de línea de comandos, la API de Windows Installer o una acción personalizada. El botón **Cancelar** se puede ocultar para parte o para toda la instalación, en función del método que use.

## <a name="hiding-the-cancel-button-from-the-command-line"></a>Ocultar el botón Cancelar desde la línea de comandos

El botón **Cancelar** se puede ocultar durante la instalación mediante la opción de línea de comandos (!). Esto solo se puede hacer para una instalación básica del nivel de interfaz de usuario (/QB). El botón **Cancelar** está oculto para toda la instalación. Para obtener más información, vea [Opciones de la línea de comandos](command-line-options.md) y niveles de la [interfaz de usuario](user-interface-levels.md). La siguiente línea de comandos oculta el botón **Cancelar** e instala Example.msi.

**msiexec/I example.msi/QB!**

## <a name="hiding-the-cancel-button-from-an-application-or-script"></a>Ocultar el botón Cancelar desde una aplicación o un script

Puede escribir una aplicación o un script para ocultar el botón **Cancelar** . Esto solo se puede hacer para una instalación básica de nivel de interfaz de usuario, de modo que el botón **Cancelar** esté oculto para toda la instalación.

Para ocultar el botón Cancelar de una aplicación, establezca INSTALLUILEVEL \_ HIDECANCEL al llamar a [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui). En el ejemplo siguiente se oculta el botón **Cancelar** y se instala Example.msi.


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



Para ocultar el botón **Cancelar** de la secuencia de comandos, agregue msiUILevelHideCancel a la propiedad [**elemento uilevel**](installer-uilevel.md) del [**objeto Installer**](installer-object.md). El siguiente ejemplo de VBScript oculta el botón **Cancelar** e instala Example.msi.


```VB
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.UILevel = msiUILevelBasic + msiUILevelHideCancel
Installer.InstallProduct "example.msi"
```



## <a name="hiding-the-cancel-button-for-parts-of-an-installation-using-a-custom-action"></a>Ocultar el botón Cancelar para las partes de una instalación mediante una acción personalizada

La instalación puede ocultar y mostrar el botón **Cancelar** durante partes de una instalación mediante el envío de un \_ mensaje de INSTALLMESSAGE COMMONDATA mediante una acción personalizada o scripts de dll. Para obtener más información, consulte [bibliotecas de vínculos dinámicos](dynamic-link-libraries.md), [scripts](scripts.md), [acciones personalizadas](custom-actions.md)y [envío de mensajes a Windows Installer mediante MsiProcessMessage](sending-messages-to-windows-installer-using-msiprocessmessage.md).

Una llamada a una acción personalizada debe proporcionar un registro. El campo 1 de este registro debe contener el valor 2 (dos) para especificar el botón **Cancelar** . El campo 2 debe contener el valor 0 o 1. Un valor de 0 en el campo 2 oculta el botón y un valor de 1 en el campo 2 Desoculta el botón. Tenga en cuenta que la asignación de un registro de tamaño 2 con [**MsiCreateRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msicreaterecord) proporciona los campos 0, 1 y 2.

La siguiente acción personalizada del archivo DLL de ejemplo oculta el botón **Cancelar** .


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



La acción personalizada de VBScript siguiente oculta el botón **Cancelar** .


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



 

 



