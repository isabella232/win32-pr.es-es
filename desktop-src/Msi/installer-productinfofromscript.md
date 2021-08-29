---
description: La propiedad ProductInfoFromScript del objeto Installer devuelve el valor del atributo especificado que se almacena en un script de anuncio.
ms.assetid: 92aa479b-2b4c-482c-a186-a290461bc6d8
title: Installer::P roductInfoFromScript
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
ms.openlocfilehash: 7b0319c83cc981f36bc4d744bb34e96a684adf8d203bdf4f4dc6ab8472033639
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129375"
---
# <a name="installerproductinfofromscript-property"></a>Installer::P roductInfoFromScript

La **propiedad ProductInfoFromScript** del objeto [**Installer**](installer-object.md) devuelve el valor del atributo especificado que se almacena en un script de anuncio.

Esta propiedad es de solo escritura.

## <a name="syntax"></a>Syntax


```JScript
Installer.ProductInfoFromScript = propVal 
```



## <a name="property-value"></a>Valor de propiedad

## <a name="error-codes"></a>Códigos de error

Valor de cadena o entero en función del atributo solicitado.

## <a name="remarks"></a>Comentarios

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
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador 4.5 en Windows Server 2003 y Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                           |
| IID<br/>     | IInstaller de IID se define como \_ 000C1090-0000-0000-C000-00000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Instalador**](installer-object.md)
</dt> <dt>

[No se admite en Windows Installer 3.1 y versiones anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




