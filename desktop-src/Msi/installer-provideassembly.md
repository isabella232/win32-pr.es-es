---
description: El método ProvideAssembly del objeto Installer devuelve la ruta de acceso instalada de un ensamblado.
ms.assetid: c99b1934-3834-478b-ab1d-7e7583dba779
title: Installer::P rovideAssembly (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProvideAssembly
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 45d5c2d6b64936b034d859caddf72ddaaf6fba77451d066205d7f394200311f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105215"
---
# <a name="installerprovideassembly-method"></a>Installer::P rovideAssembly (método)

El **método ProvideAssembly** del [**objeto Installer**](installer-object.md) devuelve la ruta de acceso instalada de un ensamblado.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = .ProvideAssembly(
  assembly,
  appContext,
  installMode,
  assemblyInfo
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ensamblaje* 
</dt> <dd>

Nombre de seguridad del ensamblado instalado que se va a consultar.

</dd> <dt>

*appContext* 
</dt> <dd>

Se establece en NULL para los ensamblados globales. Para los ensamblados privados, establezca *appContext* en la ruta de acceso completa del archivo de configuración de la aplicación o en la ruta de acceso completa del archivo ejecutable de la aplicación en la que el ensamblado se ha convertido en privado.

</dd> <dt>

*installMode* 
</dt> <dd>

Define el modo de instalación. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                                                                                                                                                                                              | Significado                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallModeDefault"></span><span id="msiinstallmodedefault"></span><span id="MSIINSTALLMODEDEFAULT"></span><dl> <dt>**msiInstallModeDefault**</dt> <dt>0</dt> </dl>                                                                                                | Proporcione el componente y realice las instalaciones necesarias para proporcionar el componente. <br/>                                                                                        |
| <span id="msiInstallModeExisting"></span><span id="msiinstallmodeexisting"></span><span id="MSIINSTALLMODEEXISTING"></span><dl> <dt>**msiInstallModeExisting**</dt> <dt>-1</dt> </dl>                                                                                           | Proporcione el componente solo si la característica existe. Esta opción comprobará que el ensamblado existe.<br/>                                                                            |
| <span id="msiInstallModeNoDetection"></span><span id="msiinstallmodenodetection"></span><span id="MSIINSTALLMODENODETECTION"></span><dl> <dt>**msiInstallModeNoDetection**</dt> <dt>-2</dt> </dl>                                                                               | Proporcione el componente solo si la característica existe. Esta opción no comprueba que el ensamblado exista.<br/>                                                                        |
| <span id="msiInstallModeNoSourceResolution"></span><span id="msiinstallmodenosourceresolution"></span><span id="MSIINSTALLMODENOSOURCERESOLUTION"></span><dl> <dt>**msiInstallModeNoSourceResolution**</dt> <dt>-3</dt> </dl>                                                   | Proporciona el ensamblado solo si el ensamblado está instalado localmente.<br/>                                                                                                                 |
| <span id="Combination_of_the_flags_used_by_ReinstallFeature"></span><span id="combination_of_the_flags_used_by_reinstallfeature"></span><span id="COMBINATION_OF_THE_FLAGS_USED_BY_REINSTALLFEATURE"></span><dl> <dt>**Combinación de las marcas usadas por [ **ReinstallFeature**](installer-reinstallfeature.md)**</dt> </dl> | Llama al [**método ReinstallFeature**](installer-reinstallfeature.md) para volver a instalar la característica con este parámetro para *ReinstallMode* y, a continuación, devuelve la ruta de acceso del ensamblado.<br/> |



 

</dd> <dt>

*assemblyInfo* 
</dt> <dd>

Información de ensamblado y tipo de ensamblado. Establezca en uno de los valores siguientes.



| Value                                                                                                                                                                                                                                                                                       | Significado                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <span id="msiProvideAssemblyNet"></span><span id="msiprovideassemblynet"></span><span id="MSIPROVIDEASSEMBLYNET"></span><dl> <dt>**msiProvideAssemblyNet**</dt> <dt>0</dt> </dl>         | Un ensamblado de .NET.<br/>               |
| <span id="msiProvideAssemblyWin32"></span><span id="msiprovideassemblywin32"></span><span id="MSIPROVIDEASSEMBLYWIN32"></span><dl> <dt>**msiProvideAssemblyWin32**</dt> <dt>1</dt> </dl> | Un ensamblado win32 en paralelo.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Ruta de acceso al ensamblado instalado.

## <a name="remarks"></a>Comentarios

El **método ProvideAssembly** usa la [**función MsiProvideAssembly.**](/windows/desktop/api/Msi/nf-msi-msiprovideassemblya)

## <a name="examples"></a>Ejemplos

El siguiente script de ejemplo muestra el uso del método ProvideAssembly.


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

'
' ProvideAssembly - .NET global
'   
MsgBox Installer.ProvideAssembly("System.Security,Version=""1.0.5000.0"",PublicKeyToken=""b03f5f7f11d50a3a"",Culture=""neutral"",FileVersion=""1.1.4322.573""", vbNullString, 0, 0)

'
' ProvideAssembly - .NET private
'   
MsgBox Installer.ProvideAssembly("Sample,Version=""1.0.0.0"",Culture=""neutral""", "C:\Program Files\Microsoft\Sample\Sample.exe", 0, 0)

'
' ProvideAssembly - win32 global
'
MsgBox Installer.ProvideAssembly("Microsoft.MSXML2,publicKeyToken=""6bd6b9abf345378f"",version=""4.1.0.0"",type=""win32"",processorArchitecture=""x86""", vbNullString , -2, 1)
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador 4.5 en Windows Server 2003 y Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                           |
| IID<br/>     | IID IInstaller se define como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Instalador**](installer-object.md)
</dt> <dt>

[No se admite en Windows Installer 3.1 y versiones anteriores](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




