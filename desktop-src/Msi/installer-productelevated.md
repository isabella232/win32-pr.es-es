---
description: La propiedad ProductElevated del objeto de instalador devuelve true si el producto está administrado o false si el producto no está administrado.
ms.assetid: 8126f5a0-751f-46c3-9014-208e9c2db34c
title: Instalador::P propiedad roductElevated
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductElevated
- Installer.get_ProductElevated
- Installer.ProductElevated
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 22591c20cbabfda2eb052e4746e87739b9681804
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653957"
---
# <a name="installerproductelevated-property"></a>Instalador::P propiedad roductElevated

La propiedad **ProductElevated** del objeto de [**instalador**](installer-object.md) devuelve true si el producto está administrado o false si el producto no está administrado.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Installer.ProductElevated
```



## <a name="property-value"></a>Valor de propiedad

El GUID completo del código del producto. Este parámetro es necesario.

## <a name="remarks"></a>Observaciones

La propiedad **ProductElevated** usa la función [**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda) . El valor devuelto de la propiedad no tiene en cuenta la directiva [AlwaysInstallElevated](alwaysinstallelevated.md) .

## <a name="examples"></a>Ejemplos

En el siguiente script de ejemplo se muestra el uso de la propiedad **ProductElevated** .


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

' 
' Install Orca tool per-machine
'
installer.InstallProduct "\\products\public\orca\orca.msi", "ALLUSERS=1"

'
' Verify Orca is managed
'

Dim bManaged
bManaged = installer.ProductElevated("{85F4CBCB-9BBC-4B50-A7D8-E1106771498D}")

If bManaged Then
    MsgBox "Success - Product Is Managed"
Else
    MsgBox "Failure - Product Is Not Managed"
End If
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer 4,5 en Windows Server 2003 y Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                           |
| IID<br/>     | IID \_ IInstaller se define como 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Instalador**](installer-object.md)
</dt> <dt>

[No se admite en Windows Installer 3,1 y versiones anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




