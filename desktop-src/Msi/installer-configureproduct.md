---
description: El método ConfigureProduct del objeto Installer instala o desinstala un producto.
ms.assetid: 1215a03f-6c96-4416-881f-0071c1b3c5df
title: Método Installer.ConfigureProduct
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ConfigureProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 989855508215b2cd5d04bff7903628513314b9a5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127171698"
---
# <a name="installerconfigureproduct-method"></a>Método Installer.ConfigureProduct

El **método ConfigureProduct** del [**objeto Installer**](installer-object.md) instala o desinstala un producto.

## <a name="syntax"></a>Sintaxis


```JScript
Installer.ConfigureProduct(
  Product,
  InstallLevel,
  InstallState
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Producto* 
</dt> <dd>

Especifica el código de producto del producto.

</dd> <dt>

*InstallLevel* 
</dt> <dd>

Especifica la configuración de instalación predeterminada del producto. El parámetro InstallLevel se omite y todas las características se instalan si el parámetro InstallState está establecido en cualquier otro valor que no sea msiInstallStateDefault.

Este parámetro debe ser 0 (instalar mediante niveles de características de creación), 65535 (instalar todas las características) o un valor entre 0 y 65535 para instalar un subconjunto de características disponibles.

</dd> <dt>

*InstallState* 
</dt> <dd>

Especifica el estado de instalación de la característica. Este parámetro debe ser uno de los siguientes valores.



| Value                                                                                                                                                                                                                                        | Significado                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <span id="msiInstallStateAdvertised"></span><span id="msiinstallstateadvertised"></span><span id="MSIINSTALLSTATEADVERTISED"></span><dl> <dt>**msiInstallStateAdvertised**</dt> </dl> | La característica se anuncia<br/>                         |
| <span id="msiInstallStateLocal"></span><span id="msiinstallstatelocal"></span><span id="MSIINSTALLSTATELOCAL"></span><dl> <dt>**msiInstallStateLocal**</dt> </dl>                     | La característica se instala localmente.<br/>                 |
| <span id="msiInstallStateAbsent"></span><span id="msiinstallstateabsent"></span><span id="MSIINSTALLSTATEABSENT"></span><dl> <dt>**msiInstallStateAbsent**</dt> </dl>                 | La característica se desinstala.<br/>                       |
| <span id="msiInstallStateSource"></span><span id="msiinstallstatesource"></span><span id="MSIINSTALLSTATESOURCE"></span><dl> <dt>**msiInstallStateSource**</dt> </dl>                 | La característica se instala para ejecutarse desde el origen.<br/>      |
| <span id="msiInstallStateDefault"></span><span id="msiinstallstatedefault"></span><span id="MSIINSTALLSTATEDEFAULT"></span><dl> <dt>**msiInstallStateDefault**</dt> </dl>             | La característica se instala en su ubicación predeterminada.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El **método ConfigureProduct** muestra la interfaz de usuario mediante la configuración actual. La configuración de la interfaz de usuario se puede cambiar modificando la [**propiedad UILevel (objeto Installer)**](installer-uilevel.md) antes de llamar al **método ConfigureProduct.**

Si el *parámetro InstallState* se establece en cualquier otro valor que no sea msiInstallStateDefault, se omite el parámetro *InstallLevel* y se instalan todas las características del producto. Use el [**método ConfigureFeature**](installer-configurefeature.md) para controlar la instalación de características individuales cuando el parámetro *InstallState* no esté establecido en msiInstallStateDefault.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID IInstaller se define como \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**MsiConfigureProduct**](/windows/desktop/api/Msi/nf-msi-msiconfigureproducta)
</dt> <dt>

[Funciones de instalación y configuración](installer-function-reference.md)
</dt> </dl>

 

 




