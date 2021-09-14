---
description: La propiedad ProductElevated del objeto Installer devuelve True si el producto se administra o False si el producto no está administrado.
ms.assetid: 8126f5a0-751f-46c3-9014-208e9c2db34c
title: Installer::P roductElevated
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072120"
---
# <a name="installerproductelevated-property"></a>Installer::P roductElevated

La **propiedad ProductElevated del** objeto [**Installer**](installer-object.md) devuelve True si el producto se administra o False si el producto no está administrado.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
propVal = Installer.ProductElevated
```



## <a name="property-value"></a>Valor de propiedad

Guid del código de producto completo del producto. Este parámetro es obligatorio.

## <a name="remarks"></a>Observaciones

La **propiedad ProductElevated** usa la [**función MsiIsProductElevated.**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda) La devolución de la propiedad no tiene en cuenta la [directiva AlwaysInstallElevated.](alwaysinstallelevated.md)

## <a name="examples"></a>Ejemplos

El siguiente script de ejemplo muestra el uso de la **propiedad ProductElevated** .


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
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador 4.5 en Windows Server 2003 y Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                           |
| IID<br/>     | IInstaller de IID se define como \_ 000C1090-0000-0000-C000-00000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Instalador**](installer-object.md)
</dt> <dt>

[No se admite en Windows Installer 3.1 y versiones anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




