---
description: El método ReinstallFeature del objeto Installer reinstala las características o corrige los problemas con las características instaladas.
ms.assetid: cfe2aef4-7742-49cd-b7a3-7d484e1f85e3
title: Installer.ReinstallFeature (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ReinstallFeature
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: dfe4cb96ccac85fb5b94f3a2a8ec3dcca48f6fa4300a6bceb338b2ebbe01da22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946291"
---
# <a name="installerreinstallfeature-method"></a>Installer.ReinstallFeature (método)

El **método ReinstallFeature** del objeto [**Installer**](installer-object.md) reinstala las características o corrige los problemas con las características instaladas.

## <a name="syntax"></a>Sintaxis


```JScript
Installer.ReinstallFeature(
  Product,
  Feature,
  ReinstallMode
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Producto* 
</dt> <dd>

Especifica el código de producto del producto.

</dd> <dt>

*Característica* 
</dt> <dd>

Especifica la característica que se va a volver a instalar. La característica primaria o secundaria de la característica especificada no se vuelve a instalar. Para volver a instalar la característica primaria o secundaria, debe llamar al método **ReinstallFeature** para cada una por separado o usar el [**método ReinstallProduct.**](installer-reinstallproduct.md)

</dd> <dt>

*ReinstallMode* 
</dt> <dd>

Especifica el tipo de reinstalación. Este parámetro puede ser uno o varios de los valores siguientes.



| Valor                                                                                                                                                                                                                                                                    | Significado                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <span id="msiReinstallModeFileMissing"></span><span id="msireinstallmodefilemissing"></span><span id="MSIREINSTALLMODEFILEMISSING"></span><dl> <dt>**msiReinstallModeFileMissing**</dt> </dl>                     | Vuelve a instalar solo si falta el archivo.<br/>                                |
| <span id="msiReinstallModeFileOlderVersion"></span><span id="msireinstallmodefileolderversion"></span><span id="MSIREINSTALLMODEFILEOLDERVERSION"></span><dl> <dt>**msiReinstallModeFileOlderVersion**</dt> </dl> | Se vuelve a instalar si falta el archivo o si es una versión anterior.<br/>              |
| <span id="msiReinstallModeFileEqualVersion"></span><span id="msireinstallmodefileequalversion"></span><span id="MSIREINSTALLMODEFILEEQUALVERSION"></span><dl> <dt>**msiReinstallModeFileEqualVersion**</dt> </dl> | Se vuelve a instalar si falta el archivo o si es una versión igual o anterior.<br/>     |
| <span id="msiReinstallModeFileExact"></span><span id="msireinstallmodefileexact"></span><span id="MSIREINSTALLMODEFILEEXACT"></span><dl> <dt>**msiReinstallModeFileExact**</dt> </dl>                             | Se vuelve a instalar si falta el archivo o no es una versión exacta.<br/>          |
| <span id="msiReinstallModeFileVerify"></span><span id="msireinstallmodefileverify"></span><span id="MSIREINSTALLMODEFILEVERIFY"></span><dl> <dt>**msiReinstallModeFileVerify**</dt> </dl>                         | Comprueba la suma de los ejecutables y vuelve a instalarlos si faltan o están dañados.<br/> |
| <span id="msiReinstallModeFileReplace"></span><span id="msireinstallmodefilereplace"></span><span id="MSIREINSTALLMODEFILEREPLACE"></span><dl> <dt>**msiReinstallModeFileReplace**</dt> </dl>                     | Vuelve a instalar todos los archivos independientemente de la versión.<br/>                            |
| <span id="msiReinstallModeUserData"></span><span id="msireinstallmodeuserdata"></span><span id="MSIREINSTALLMODEUSERDATA"></span><dl> <dt>**msiReinstallModeUserData**</dt> </dl>                                 | Garantiza las entradas del Registro per=user necesarias.<br/>                            |
| <span id="msiReinstallModeMachineData"></span><span id="msireinstallmodemachinedata"></span><span id="MSIREINSTALLMODEMACHINEDATA"></span><dl> <dt>**msiReinstallModeMachineData**</dt> </dl>                     | Garantiza las entradas del Registro per=machine necesarias.<br/>                         |
| <span id="msiReinstallModeShortcut"></span><span id="msireinstallmodeshortcut"></span><span id="MSIREINSTALLMODESHORTCUT"></span><dl> <dt>**msiReinstallModeShortcut**</dt> </dl>                                 | Valida los accesos directos.<br/>                                                   |
| <span id="msiReinstallModePackage"></span><span id="msireinstallmodepackage"></span><span id="MSIREINSTALLMODEPACKAGE"></span><dl> <dt>**msiReinstallModePackage**</dt> </dl>                                     | Usa el origen de recache para instalar el paquete.<br/>                        |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IInstaller se define como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)
</dt> <dt>

[Funciones de instalación y configuración](installer-function-reference.md)
</dt> </dl>

 

 




