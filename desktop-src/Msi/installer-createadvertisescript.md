---
description: El método CreateAdvertiseScript del objeto de instalador genera un script de anuncio.
ms.assetid: 32a331e5-d291-49cd-ab0e-7d0e4d72a95b
title: 'Installer:: CreateAdvertiseScript (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.CreateAdvertiseScript
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9ec4b18eee376e7bde4824a497ea14b503045f43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105654016"
---
# <a name="installercreateadvertisescript-method"></a>Installer:: CreateAdvertiseScript (método)

El método **CreateAdvertiseScript** del objeto de [**instalador**](installer-object.md) genera un script de anuncio.

## <a name="syntax"></a>Sintaxis


```JScript
.CreateAdvertiseScript(
  packagePath,
  scriptFilePath,
  transforms,
  language,
  platform,
  options
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*packagePath* 
</dt> <dd>

Ruta de acceso completa al paquete de Windows Installer (. msi) que se va a anunciar.

</dd> <dt>

*scriptFilePath* 
</dt> <dd>

Ruta de acceso completa al archivo de script que se va a crear con la información anunciada.

</dd> <dt>

*transforma* 
</dt> <dd>

Lista de transformaciones que se van a aplicar al producto. Las transformaciones en la lista están delimitadas por signos de punto y coma. Este parámetro es opcional.

</dd> <dt>

*language* 
</dt> <dd>

Idioma del paquete de instalación que se va a usar. Este parámetro es opcional.

</dd> <dt>

*platform* 
</dt> <dd>

Este parámetro especifica la plataforma en la que el instalador debe crear el script. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                                                                                                                       | Significado                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="msiAdvertiseCurrentPlatform"></span><span id="msiadvertisecurrentplatform"></span><span id="MSIADVERTISECURRENTPLATFORM"></span><dl> <dt>**msiAdvertiseCurrentPlatform**</dt> <dt>0</dt> </dl> | Crea un script para la plataforma actual.<br/>  |
| <span id="msiAdvertiseX86Platform"></span><span id="msiadvertisex86platform"></span><span id="MSIADVERTISEX86PLATFORM"></span><dl> <dt>**msiAdvertiseX86Platform**</dt> <dt>1</dt> </dl>                 | Crea un script para la plataforma x86.<br/>      |
| <span id="msiAdvertiseIA64Platform"></span><span id="msiadvertiseia64platform"></span><span id="MSIADVERTISEIA64PLATFORM"></span><dl> <dt>**msiAdvertiseIA64Platform**</dt> <dt>2</dt> </dl>             | Crea un script para sistemas basados en Itanium.<br/> |
| <span id="msiAdvertiseX64Platform"></span><span id="msiadvertisex64platform"></span><span id="MSIADVERTISEX64PLATFORM"></span><dl> <dt>**msiAdvertiseX64Platform**</dt> <dt>4</dt> </dl>                 | Crea un script para la plataforma x64.<br/>      |



 

</dd> <dt>

*options* 
</dt> <dd>

Opciones de anuncios. Este parámetro es opcional. Este parámetro puede ser uno de los valores siguientes. Este parámetro es opcional.



| Value                                                                                                                                                                                                                                                                                                   | Significado                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseDefault"></span><span id="msiadvertisedefault"></span><span id="MSIADVERTISEDEFAULT"></span><dl> <dt>**msiAdvertiseDefault**</dt> <dt>0</dt> </dl>                             | Anuncio estándar<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiAdvertiseSingleInstance"></span><span id="msiadvertisesingleinstance"></span><span id="MSIADVERTISESINGLEINSTANCE"></span><dl> <dt>**msiAdvertiseSingleInstance**</dt> <dt>1</dt> </dl> | Anuncia una nueva instancia del producto. Requiere que la primera transformación de la lista de transformación del parámetro *transformaciones* sea la transformación de instancia que cambia el código de producto. Para obtener más información, consulte [instalación de varias instancias de productos y revisiones](installing-multiple-instances-of-products-and-patches.md).<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El método [**AdvertiseProduct**](installer-advertiseproduct.md) usa la función [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa) .

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo se muestra el uso del método **CreateAdvertiseScript** .


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

'
' Create an advertise script for Orca
'

Installer.CreateAdvertiseScript "\\products\public\orca\orca.msi", "c:\scripts\orca.aas"
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

 

 




