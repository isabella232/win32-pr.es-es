---
description: La propiedad ProductInfoFromScript del objeto Installer devuelve el valor del atributo especificado que se almacena en un script de anuncio.
ms.assetid: 92aa479b-2b4c-482c-a186-a290461bc6d8
title: Installer::P roductInfoFromScript, propiedad
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductInfoFromScript
- Installer.put_ProductInfoFromScript
- Installer.ProductInfoFromScript
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a4c8e29adb93f68228008770a95ad9fb9185e966
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072117"
---
# <a name="installerproductinfofromscript-property"></a>Installer::P roductInfoFromScript, propiedad

La **propiedad ProductInfoFromScript** del [**objeto Installer**](installer-object.md) devuelve el valor del atributo especificado que se almacena en un script de anuncio.

Esta propiedad es de solo escritura.

## <a name="syntax"></a>Sintaxis


```JScript
Installer.ProductInfoFromScript = propVal 
```



## <a name="property-value"></a>Valor de propiedad

## <a name="error-codes"></a>Códigos de error

Valor de cadena o entero en función del atributo solicitado.

## <a name="remarks"></a>Observaciones

La **propiedad ProductInfoFromScript** usa la [**función MsiGetProductInfoFromScript.**](/windows/desktop/api/Msi/nf-msi-msigetproductinfofromscripta)

## <a name="examples"></a>Ejemplos

El siguiente script de ejemplo muestra el uso de la **propiedad ProductInfoFromScript** .


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

' 
' Create an advertise script for Orca
'

installer.CreateAdvertiseScript "\\products\public\orca\orca.msi", "c:\scratch\orca.aas"

' 
' Output ProductName Information From Script
'

MsgBox  installer.ProductInfoFromScript("c:\scratch\orca.aas", 3)
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador 4.5 en Windows Server 2003 y Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                           |
| IID<br/>     | IID IInstaller se define como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Instalador**](installer-object.md)
</dt> <dt>

[No se admite en Windows Installer 3.1 y versiones anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




