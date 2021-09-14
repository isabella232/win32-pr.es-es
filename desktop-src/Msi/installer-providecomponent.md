---
description: El método ProvideComponent del objeto Installer devuelve la ruta de acceso completa del componente y realiza la instalación necesaria.
ms.assetid: 2bf09515-6f65-4712-89c1-01c43c1ce27c
title: Método Installer.ProvideComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProvideComponent
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e383c532d496ed217bdb7743b8171d732d61b2d0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072100"
---
# <a name="installerprovidecomponent-method"></a>Método Installer.ProvideComponent

El **método ProvideComponent** del objeto [**Installer**](installer-object.md) devuelve la ruta de acceso completa del componente y realiza la instalación necesaria. Si es necesario, **el método ProvideComponent** del [**objeto Installer**](installer-object.md) solicita el origen e incrementa el recuento de uso de la característica.

## <a name="syntax"></a>Sintaxis


```JScript
Installer.ProvideComponent(
  Product,
  Feature,
  Component,
  InstallMode
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

Especifica el identificador de característica de la característica que contiene el componente.

</dd> <dt>

*Componente* 
</dt> <dd>

Especifica el código del componente.

</dd> <dt>

*InstallMode* 
</dt> <dd>

Define el modo de instalación. Este parámetro puede ser uno de los valores que se muestran en la tabla siguiente.



| Nombre                                                                                                                                                                                                                                                                                                                                                               | Significado                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiInstallModeDefault"></span><span id="msiinstallmodedefault"></span><span id="MSIINSTALLMODEDEFAULT"></span><dl> <dt>**msiInstallModeDefault**</dt> <dt>0</dt> </dl>                                                                                | Proporciona la ruta de acceso del componente, realizando cualquier instalación, si es necesario.<br/>                                                                                                                                                  |
| <span id="msiInstallModeExisting"></span><span id="msiinstallmodeexisting"></span><span id="MSIINSTALLMODEEXISTING"></span><dl> <dt>**msiInstallModeExisting**</dt> <dt>–1</dt> </dl>                                                                           | Proporciona la ruta de acceso del componente solo si la característica existe; de lo contrario, devuelve una cadena vacía. Este modo comprueba la existencia del archivo de clave del componente.<br/>                                                                |
| <span id="msiInstallModeNoDetection"></span><span id="msiinstallmodenodetection"></span><span id="MSIINSTALLMODENODETECTION"></span><dl> <dt>**msiInstallModeNoDetection**</dt> <dt>–2</dt> </dl>                                                               | Proporciona la ruta de acceso del componente solo si la característica existe. De lo contrario, devuelve una cadena vacía. Este modo comprueba el registro del componente, pero no comprueba la existencia del archivo de clave del componente.<br/>                 |
| <span id="msiInstallModeNoSourceResolution"></span><span id="msiinstallmodenosourceresolution"></span><span id="MSIINSTALLMODENOSOURCERESOLUTION"></span><dl> <dt>**msiInstallModeNoSourceResolution**</dt> <dt>–3</dt> </dl>                                   | Proporciona la ruta de acceso del componente solo si la característica existe con un parámetro InstallState de *msiInstallStateLocal.* Esto comprueba el registro del componente, pero no comprueba la existencia del archivo de clave del componente.<br/> |
| <span id="combination_of_the_msiReinstallMode_flags"></span><span id="combination_of_the_msireinstallmode_flags"></span><span id="COMBINATION_OF_THE_MSIREINSTALLMODE_FLAGS"></span><dl> <dt>**combinación de las marcas msiReinstallMode**</dt><dt></dt> </dl> | Llama [**a ReinstallFeature**](installer-reinstallfeature.md) para volver a instalar la característica con este parámetro para el parámetro *ReinstallMode* y, a continuación, proporciona el componente .<br/>                                           |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El **método ProvideComponent** combina la funcionalidad de [**UseFeature,**](installer-usefeature.md) [**ConfigureFeature**](installer-configurefeature.md)y [**ComponentPath.**](installer-componentpath.md) El **método ProvideComponent** simplifica la secuencia de llamada, pero también incrementa el recuento de uso y se debe usar con precaución para evitar recuentos de uso inexactos. El **método ProvideComponent** también proporciona menos flexibilidad que una serie de llamadas individuales a los métodos y propiedades mencionados anteriormente.

Si la aplicación se está recuperando de una situación inesperada, es probable que la aplicación ya haya llamado a [**UseFeature**](installer-usefeature.md) y haya incrementado el recuento de uso. En este caso, la aplicación debe evitar incrementar el recuento de uso llamando al [**método ConfigureFeature**](installer-configurefeature.md) en lugar del **método ProvideComponent.**

La opción msiInstallModeExisting no se puede usar en combinación con marcas msiReinstallMode.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IInstaller de IID se define como \_ 000C1090-0000-0000-C000-00000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MsiProvideComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidecomponenta)
</dt> </dl>

 

 




